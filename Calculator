# CapitalAdvance-roi-calculator
Payoneer Capital Advance
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Capital Advance ROI 계산기 | Payoneer</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
            background: #f8f9fa;
            color: #1a1a1a;
            line-height: 1.6;
            padding: 20px;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .header {
            text-align: center;
            margin-bottom: 40px;
            padding: 30px 0;
        }
        
        .logo {
            color: #FF6200;
            font-size: 32px;
            font-weight: 700;
            margin-bottom: 10px;
        }
        
        h1 {
            font-size: 36px;
            color: #1a1a1a;
            margin-bottom: 10px;
            font-weight: 700;
        }
        
        .subtitle {
            font-size: 18px;
            color: #666;
        }
        
        .calculator-card {
            background: white;
            border-radius: 16px;
            box-shadow: 0 4px 20px rgba(0,0,0,0.08);
            overflow: hidden;
            margin-bottom: 30px;
        }
        
        .input-section {
            padding: 40px;
            background: white;
        }
        
        .section-title {
            font-size: 22px;
            font-weight: 700;
            color: #1a1a1a;
            margin-bottom: 25px;
            padding-left: 15px;
            border-left: 4px solid #FF6200;
        }
        
        .input-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 24px;
            margin-bottom: 30px;
        }
        
        .input-group label {
            display: block;
            font-weight: 600;
            margin-bottom: 8px;
            color: #374151;
            font-size: 14px;
        }
        
        .input-wrapper {
            position: relative;
        }
        
        .input-wrapper input {
            width: 100%;
            padding: 14px 16px 14px 40px;
            border: 2px solid #e5e7eb;
            border-radius: 10px;
            font-size: 16px;
            transition: all 0.3s;
        }
        
        .input-wrapper input:focus {
            outline: none;
            border-color: #FF6200;
            box-shadow: 0 0 0 4px rgba(255, 98, 0, 0.1);
        }
        
        .currency {
            position: absolute;
            left: 16px;
            top: 50%;
            transform: translateY(-50%);
            color: #9ca3af;
            font-weight: 600;
        }
        
        .plans {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 15px;
            margin-top: 15px;
        }
        
        .plan-card {
            border: 2px solid #e5e7eb;
            border-radius: 12px;
            padding: 20px;
            text-align: center;
            cursor: pointer;
            transition: all 0.3s;
            background: #fafafa;
        }
        
        .plan-card:hover {
            border-color: #FF6200;
            background: white;
        }
        
        .plan-card.selected {
            border-color: #FF6200;
            background: #fff5f0;
            box-shadow: 0 4px 12px rgba(255, 98, 0, 0.15);
        }
        
        .plan-name {
            color: #FF6200;
            font-weight: 700;
            font-size: 16px;
            margin-bottom: 5px;
        }
        
        .plan-period {
            color: #666;
            font-size: 13px;
            margin-bottom: 8px;
        }
        
        .plan-fee {
            font-size: 28px;
            font-weight: 700;
            color: #1a1a1a;
        }
        
        .plan-details {
            font-size: 12px;
            color: #666;
            margin-top: 8px;
        }
        
        .calculate-btn {
            width: 100%;
            padding: 16px;
            background: linear-gradient(135deg, #FF6200 0%, #FF8533 100%);
            color: white;
            border: none;
            border-radius: 10px;
            font-size: 18px;
            font-weight: 700;
            cursor: pointer;
            transition: all 0.3s;
            margin-top: 20px;
        }
        
        .calculate-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 20px rgba(255, 98, 0, 0.3);
        }
        
        .results {
            display: none;
            padding: 40px;
            background: #f8f9fa;
        }
        
        .results.show {
            display: block;
        }
        
        .comparison {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 24px;
            margin-bottom: 30px;
        }
        
        .scenario {
            background: white;
            border-radius: 12px;
            padding: 30px;
            position: relative;
            overflow: hidden;
        }
        
        .scenario::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
        }
        
        .before::before {
            background: #dc2626;
        }
        
        .after::before {
            background: #16a34a;
        }
        
        .scenario-label {
            font-size: 14px;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            margin-bottom: 8px;
        }
        
        .before .scenario-label {
            color: #dc2626;
        }
        
        .after .scenario-label {
            color: #16a34a;
        }
        
        .scenario-title {
            font-size: 24px;
            font-weight: 700;
            margin-bottom: 20px;
            color: #1a1a1a;
        }
        
        .metric {
            margin-bottom: 16px;
            padding-bottom: 16px;
            border-bottom: 1px solid #e5e7eb;
        }
        
        .metric:last-child {
            border-bottom: none;
            margin-bottom: 0;
        }
        
        .metric-label {
            font-size: 13px;
            color: #666;
            margin-bottom: 4px;
        }
        
        .metric-value {
            font-size: 26px;
            font-weight: 700;
            color: #1a1a1a;
        }
        
        .highlight-box {
            background: linear-gradient(135deg, #FF6200 0%, #FF8533 100%);
            color: white;
            border-radius: 12px;
            padding: 30px;
            text-align: center;
            margin-top: 30px;
        }
        
        .highlight-title {
            font-size: 18px;
            margin-bottom: 10px;
            opacity: 0.9;
        }
        
        .highlight-value {
            font-size: 42px;
            font-weight: 700;
            margin-bottom: 5px;
        }
        
        .highlight-subtitle {
            font-size: 14px;
            opacity: 0.9;
        }
        
        .key-insights {
            background: white;
            border-radius: 12px;
            padding: 30px;
            margin-top: 24px;
        }
        
        .insight-item {
            display: flex;
            align-items: start;
            margin-bottom: 16px;
            padding: 16px;
            background: #f8f9fa;
            border-radius: 8px;
        }
        
        .insight-item:last-child {
            margin-bottom: 0;
        }
        
        .insight-icon {
            width: 24px;
            height: 24px;
            background: #FF6200;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: 700;
            margin-right: 12px;
            flex-shrink: 0;
        }
        
        .insight-text {
            flex: 1;
            color: #374151;
            font-size: 15px;
            line-height: 1.6;
        }
        
        @media (max-width: 768px) {
            .comparison {
                grid-template-columns: 1fr;
            }
            
            .plans {
                grid-template-columns: 1fr;
            }
            
            h1 {
                font-size: 28px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <div class="logo">Payoneer</div>
            <h1>Capital Advance ROI 계산기</h1>
            <p class="subtitle">비즈니스 성장 기회를 수치로 확인해보세요</p>
        </div>
        
        <div class="calculator-card">
            <div class="input-section">
                <h2 class="section-title">비즈니스 정보 입력</h2>
                
                <div class="input-grid">
                    <div class="input-group">
                        <label>월 평균 매출</label>
                        <div class="input-wrapper">
                            <span class="currency">$</span>
                            <input type="number" id="monthlySales" value="50000" step="1000">
                        </div>
                    </div>
                    
                    <div class="input-group">
                        <label>현재 보유 재고 금액</label>
                        <div class="input-wrapper">
                            <span class="currency">$</span>
                            <input type="number" id="currentInventory" value="20000" step="1000">
                        </div>
                    </div>
                    
                    <div class="input-group">
                        <label>평균 이익률 (%)</label>
                        <div class="input-wrapper">
                            <span class="currency">%</span>
                            <input type="number" id="profitMargin" value="30" step="1">
                        </div>
                    </div>
                </div>
                
                <div class="input-grid">
                    <div class="input-group">
                        <label>예상 재고 소진 기간 (일)</label>
                        <div class="input-wrapper">
                            <span class="currency">일</span>
                            <input type="number" id="stockoutDays" value="15" step="1">
                        </div>
                    </div>
                    
                    <div class="input-group">
                        <label>재고 확보에 필요한 자금</label>
                        <div class="input-wrapper">
                            <span class="currency">$</span>
                            <input type="number" id="neededCapital" value="30000" step="1000">
                        </div>
                    </div>
                    
                    <div class="input-group">
                        <label>은행 대출 승인 기간 (일)</label>
                        <div class="input-wrapper">
                            <span class="currency">일</span>
                            <input type="number" id="bankLoanDays" value="30" step="1">
                        </div>
                    </div>
                </div>
                
                <div class="input-group">
                    <label class="section-title" style="font-size: 18px; margin-top: 20px;">Capital Advance 플랜 선택</label>
                    <div class="plans">
                        <div class="plan-card" data-plan="express">
                            <div class="plan-name">Express</div>
                            <div class="plan-period">1개월</div>
                            <div class="plan-fee">1.5%</div>
                            <div class="plan-details">상환비율: 50%</div>
                        </div>
                        <div class="plan-card selected" data-plan="grow">
                            <div class="plan-name">Grow</div>
                            <div class="plan-period">3개월</div>
                            <div class="plan-fee">4.5%</div>
                            <div class="plan-details">상환비율: 35%</div>
                        </div>
                        <div class="plan-card" data-plan="plus">
                            <div class="plan-name">Plus</div>
                            <div class="plan-period">6개월</div>
                            <div class="plan-fee">8.5%</div>
                            <div class="plan-details">상환비율: 25%</div>
                        </div>
                    </div>
                </div>
                
                <button class="calculate-btn" onclick="calculate()">ROI 계산하기</button>
            </div>
            
            <div class="results" id="results">
                <h2 class="section-title">비교 분석 결과</h2>
                
                <div class="comparison">
                    <div class="scenario before">
                        <div class="scenario-label">Without CA</div>
                        <h3 class="scenario-title">Capital Advance 미사용</h3>
                        
                        <div class="metric">
                            <div class="metric-label">재고 소진으로 인한 판매 불가 기간</div>
                            <div class="metric-value" id="beforeStockoutDays">-</div>
                        </div>
                        
                        <div class="metric">
                            <div class="metric-label">손실 매출액</div>
                            <div class="metric-value" id="beforeLostSales">-</div>
                        </div>
                        
                        <div class="metric">
                            <div class="metric-label">손실 이익</div>
                            <div class="metric-value" id="beforeLostProfit">-</div>
                        </div>
                        
                        <div class="metric">
                            <div class="metric-label">추가 비용</div>
                            <div class="metric-value">$0</div>
                        </div>
                        
                        <div class="metric">
                            <div class="metric-label" style="font-weight: 700; color: #1a1a1a;">최종 순손실</div>
                            <div class="metric-value" style="color: #dc2626;" id="beforeNetLoss">-</div>
                        </div>
                    </div>
                    
                    <div class="scenario after">
                        <div class="scenario-label">With CA</div>
                        <h3 class="scenario-title">Capital Advance 사용</h3>
                        
                        <div class="metric">
                            <div class="metric-label">재고 확보 기간 단축</div>
                            <div class="metric-value" id="afterSavedDays">-</div>
                        </div>
                        
                        <div class="metric">
                            <div class="metric-label">유지된 매출액</div>
                            <div class="metric-value" id="afterMaintainedSales">-</div>
                        </div>
                        
                        <div class="metric">
                            <div class="metric-label">발생 이익</div>
                            <div class="metric-value" id="afterProfit">-</div>
                        </div>
                        
                        <div class="metric">
                            <div class="metric-label">Capital Advance 수수료</div>
                            <div class="metric-value" id="afterFee">-</div>
                        </div>
                        
                        <div class="metric">
                            <div class="metric-label" style="font-weight: 700; color: #1a1a1a;">최종 순이익</div>
                            <div class="metric-value" style="color: #16a34a;" id="afterNetProfit">-</div>
                        </div>
                    </div>
                </div>
                
                <div class="highlight-box">
                    <div class="highlight-title">Capital Advance 사용 시 추가 이익</div>
                    <div class="highlight-value" id="totalBenefit">-</div>
                    <div class="highlight-subtitle">수수료 차감 후 순이익 증가</div>
                </div>
                
                <div class="key-insights">
                    <h3 class="section-title" style="font-size: 18px; margin-bottom: 20px;">핵심 인사이트</h3>
                    <div id="insights"></div>
                </div>
            </div>
        </div>
    </div>
    
    <script>
        // 플랜 선택
        const plans = document.querySelectorAll('.plan-card');
        let selectedPlan = 'grow';
        
        plans.forEach(plan => {
            plan.addEventListener('click', function() {
                plans.forEach(p => p.classList.remove('selected'));
                this.classList.add('selected');
                selectedPlan = this.dataset.plan;
            });
        });
        
        // 수수료 매핑
        const fees = {
            express: 1.5,
            grow: 4.5,
            plus: 8.5
        };
        
        const periods = {
            express: 1,
            grow: 3,
            plus: 6
        };
        
        function calculate() {
            // 입력값 가져오기
            const monthlySales = parseFloat(document.getElementById('monthlySales').value);
            const currentInventory = parseFloat(document.getElementById('currentInventory').value);
            const profitMargin = parseFloat(document.getElementById('profitMargin').value) / 100;
            const stockoutDays = parseFloat(document.getElementById('stockoutDays').value);
            const neededCapital = parseFloat(document.getElementById('neededCapital').value);
            const bankLoanDays = parseFloat(document.getElementById('bankLoanDays').value);
            
            // 일 평균 매출
            const dailySales = monthlySales / 30;
            
            // BEFORE: Capital Advance 미사용 (은행 대출 대기)
            const totalStockoutDays = stockoutDays + bankLoanDays;
            const lostSales = dailySales * totalStockoutDays;
            const lostProfit = lostSales * profitMargin;
            
            // AFTER: Capital Advance 사용 (즉시 확보)
            const savedDays = bankLoanDays;
            const maintainedSales = dailySales * savedDays;
            const earnedProfit = maintainedSales * profitMargin;
            const caFee = neededCapital * (fees[selectedPlan] / 100);
            const netProfit = earnedProfit - caFee;
            
            // 총 이익 차이
            const totalBenefit = netProfit + lostProfit;
            
            // 결과 표시
            document.getElementById('beforeStockoutDays').textContent = `${totalStockoutDays}일`;
            document.getElementById('beforeLostSales').textContent = `$${lostSales.toLocaleString('en-US', {minimumFractionDigits: 0, maximumFractionDigits: 0})}`;
            document.getElementById('beforeLostProfit').textContent = `$${lostProfit.toLocaleString('en-US', {minimumFractionDigits: 0, maximumFractionDigits: 0})}`;
            document.getElementById('beforeNetLoss').textContent = `-$${lostProfit.toLocaleString('en-US', {minimumFractionDigits: 0, maximumFractionDigits: 0})}`;
            
            document.getElementById('afterSavedDays').textContent = `${savedDays}일 단축`;
            document.getElementById('afterMaintainedSales').textContent = `$${maintainedSales.toLocaleString('en-US', {minimumFractionDigits: 0, maximumFractionDigits: 0})}`;
            document.getElementById('afterProfit').textContent = `$${earnedProfit.toLocaleString('en-US', {minimumFractionDigits: 0, maximumFractionDigits: 0})}`;
            document.getElementById('afterFee').textContent = `-$${caFee.toLocaleString('en-US', {minimumFractionDigits: 0, maximumFractionDigits: 0})}`;
            document.getElementById('afterNetProfit').textContent = `+$${netProfit.toLocaleString('en-US', {minimumFractionDigits: 0, maximumFractionDigits: 0})}`;
            
            document.getElementById('totalBenefit').textContent = `$${totalBenefit.toLocaleString('en-US', {minimumFractionDigits: 0, maximumFractionDigits: 0})}`;
            
            // ROI 계산
            const roi = ((totalBenefit / caFee) * 100).toFixed(0);
            
            // 인사이트 생성
            const insightsHTML = `
                <div class="insight-item">
                    <div class="insight-icon">✓</div>
                    <div class="insight-text">
                        <strong>재고 공백 방지:</strong> ${savedDays}일간의 판매 기회를 지키고, $${maintainedSales.toLocaleString('en-US', {maximumFractionDigits: 0})}의 매출을 확보합니다.
                    </div>
                </div>
                <div class="insight-item">
                    <div class="insight-icon">✓</div>
                    <div class="insight-text">
                        <strong>비용 대비 효과:</strong> $${caFee.toLocaleString('en-US', {maximumFractionDigits: 0})}의 수수료로 $${totalBenefit.toLocaleString('en-US', {maximumFractionDigits: 0})}의 이익을 창출합니다. (ROI: ${roi}%)
                    </div>
                </div>
                <div class="insight-item">
                    <div class="insight-icon">✓</div>
                    <div class="insight-text">
                        <strong>경쟁력 유지:</strong> 재고 부족으로 인한 랭킹 하락과 고객 이탈을 방지합니다.
                    </div>
                </div>
                <div class="insight-item">
                    <div class="insight-icon">✓</div>
                    <div class="insight-text">
                        <strong>빠른 실행:</strong> 은행 대출보다 ${bankLoanDays}일 빠르게 자금을 확보하여 시장 기회를 선점합니다.
                    </div>
                </div>
            `;
            
            document.getElementById('insights').innerHTML = insightsHTML;
            
            // 결과 섹션 표시
            document.getElementById('results').classList.add('show');
            document.getElementById('results').scrollIntoView({ behavior: 'smooth', block: 'start' });
        }
    </script>
</body>
</html>
