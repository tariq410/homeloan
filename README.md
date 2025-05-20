<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ultimate Loan Calculator Suite | EMI Breakdown & Analysis</title>
    <meta name="description" content="Professional loan calculators with monthly EMI breakdowns for Home, Car, Bike, and Personal loans. Compare interest types and calculate moratorium impacts.">
    <meta name="keywords" content="EMI calculator, loan calculator, amortization schedule, home loan, car loan, bike loan, financial planning">
    <link rel="canonical" href="https://www.yourdomain.com/loan-calculators">
    
    <!-- Google AdSense -->
    <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-XXXXXXXXXXXXXXXX" crossorigin="anonymous"></script>

    <style>
        :root {
            --primary: #2c3e50;
            --secondary: #3498db;
            --accent: #e74c3c;
            --light: #ecf0f1;
            --dark: #2c3e50;
            --success: #27ae60;
            --danger: #c0392b;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', system-ui, sans-serif;
        }

        body {
            background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
            color: var(--dark);
            line-height: 1.6;
        }

        .container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 2rem 1rem;
        }

        .calculator-tabs {
            display: flex;
            gap: 1rem;
            overflow-x: auto;
            padding: 1rem 0;
            margin-bottom: 2rem;
        }

        .tab-btn {
            background: var(--light);
            border: none;
            padding: 1rem 2rem;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s;
            white-space: nowrap;
            font-weight: 600;
        }

        .tab-btn.active {
            background: var(--secondary);
            color: white;
            box-shadow: 0 4px 15px rgba(52, 152, 219, 0.3);
        }

        .calculator-card {
            background: white;
            border-radius: 1.5rem;
            padding: 2.5rem;
            margin: 2rem 0;
            box-shadow: 0 10px 40px rgba(0,0,0,0.08);
        }

        .calculator-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            margin-top: 2rem;
        }

        .input-group {
            margin-bottom: 1.8rem;
            position: relative;
        }

        .input-label {
            display: block;
            margin-bottom: 0.8rem;
            font-weight: 600;
            color: var(--dark);
            font-size: 1.05rem;
        }

        .input-field {
            width: 100%;
            padding: 1.2rem;
            border: 2px solid #e0e0e0;
            border-radius: 0.8rem;
            font-size: 1.1rem;
            transition: all 0.3s;
            background: #f8f9fa;
        }

        .input-field:focus {
            border-color: var(--secondary);
            background: white;
            box-shadow: 0 0 0 3px rgba(52, 152, 219, 0.1);
            outline: none;
        }

        .range-slider {
            width: 100%;
            margin-top: 1rem;
            -webkit-appearance: none;
            height: 6px;
            border-radius: 3px;
            background: #e0e0e0;
        }

        .range-slider::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 20px;
            height: 20px;
            background: var(--secondary);
            border-radius: 50%;
            cursor: pointer;
            transition: transform 0.2s;
        }

        .range-slider::-webkit-slider-thumb:hover {
            transform: scale(1.2);
        }

        .result-section {
            margin-top: 3rem;
            padding: 2rem;
            background: var(--light);
            border-radius: 1rem;
        }

        .amortization-table {
            overflow-x: auto;
            margin-top: 2rem;
            border-radius: 0.8rem;
            box-shadow: 0 2px 15px rgba(0,0,0,0.05);
        }

        table {
            width: 100%;
            border-collapse: collapse;
            background: white;
            min-width: 600px;
        }

        th, td {
            padding: 1.2rem;
            text-align: center;
            border-bottom: 1px solid #eee;
        }

        th {
            background: var(--primary);
            color: white;
            font-weight: 600;
        }

        tr:hover {
            background-color: #f8f9fa;
        }

        .chart-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin: 2rem 0;
        }

        .pie-chart {
            width: 200px;
            height: 200px;
            border-radius: 50%;
            margin: 0 auto;
            background: conic-gradient(
                var(--success) 0% var(--principal-percent),
                var(--danger) var(--principal-percent) 100%
            );
            transition: all 0.5s ease;
        }

        .ad-section {
            margin: 3rem 0;
            text-align: center;
            padding: 2rem;
            background: white;
            border-radius: 1rem;
            box-shadow: 0 5px 20px rgba(0,0,0,0.05);
        }

        @media (max-width: 768px) {
            .container {
                padding: 1rem;
            }

            .calculator-grid {
                grid-template-columns: 1fr;
            }

            .calculator-card {
                padding: 1.5rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header Ad -->
        <div class="ad-section">
            <ins class="adsbygoogle" style="display:block" data-ad-client="ca-pub-XXXXXXXXXXXXXXXX" data-ad-slot="1234567890" data-ad-format="auto" data-full-width-responsive="true"></ins>
        </div>

        <h1 style="text-align: center; margin-bottom: 1.5rem; color: var(--primary);">Ultimate Loan Calculator Suite</h1>
        
        <div class="calculator-tabs">
            <button class="tab-btn active" data-tab="home">Home Loan</button>
            <button class="tab-btn" data-tab="car">Car Loan</button>
            <button class="tab-btn" data-tab="bike">Two Wheeler</button>
            <button class="tab-btn" data-tab="compare">Rate Compare</button>
            <button class="tab-btn" data-tab="moratorium">Moratorium</button>
        </div>

        <!-- Home Loan Calculator -->
        <div class="calculator-card active-tab" id="home">
            <h2>🏠 Home Loan Calculator</h2>
            <div class="calculator-grid">
                <div>
                    <div class="input-group">
                        <label class="input-label">Loan Amount (₹)</label>
                        <input type="number" id="home-amount" class="input-field" value="5000000" step="100000">
                        <input type="range" class="range-slider" min="1000000" max="50000000" step="100000">
                    </div>
                    <div class="input-group">
                        <label class="input-label">Interest Rate (%)</label>
                        <input type="number" id="home-rate" class="input-field" value="8.4" step="0.1">
                        <input type="range" class="range-slider" min="6" max="15" step="0.1">
                    </div>
                    <div class="input-group">
                        <label class="input-label">Tenure (Years)</label>
                        <input type="number" id="home-tenure" class="input-field" value="20" min="5" max="30">
                        <input type="range" class="range-slider" min="5" max="30" step="1">
                    </div>
                </div>
                <div class="result-section">
                    <h3>Monthly EMI: ₹<span id="home-emi">0</span></h3>
                    <div class="chart-container">
                        <div class="pie-chart" style="--principal-percent: 50%"></div>
                        <div>
                            <p>Total Interest: ₹<span id="home-interest">0</span></p>
                            <p>Total Payment: ₹<span id="home-total">0</span></p>
                            <p>Loan Period: <span id="home-period">0</span> months</p>
                        </div>
                    </div>
                </div>
            </div>
            <div class="amortization-table">
                <table>
                    <thead>
                        <tr>
                            <th>Month</th>
                            <th>Principal</th>
                            <th>Interest</th>
                            <th>Balance</th>
                        </tr>
                    </thead>
                    <tbody id="home-schedule"></tbody>
                </table>
            </div>
        </div>

        <!-- Car Loan Calculator -->
        <div class="calculator-card" id="car" style="display:none;">
            <!-- Similar structure with car-specific ranges -->
        </div>

        <!-- Two Wheeler Loan Calculator -->
        <div class="calculator-card" id="bike" style="display:none;">
            <!-- Bike loan structure -->
        </div>

        <!-- Rate Comparison Calculator -->
        <div class="calculator-card" id="compare" style="display:none;">
            <!-- Comparison calculator -->
        </div>

        <!-- Moratorium Calculator -->
        <div class="calculator-card" id="moratorium" style="display:none;">
            <!-- Moratorium structure -->
        </div>

        <!-- Mid Content Ad -->
        <div class="ad-section">
            <ins class="adsbygoogle" style="display:block" data-ad-format="fluid" data-ad-layout-key="-gw-3+1f-3d+2z" data-ad-client="ca-pub-XXXXXXXXXXXXXXXX" data-ad-slot="0987654321"></ins>
        </div>
    </div>

    <script>
        // Core Calculation Engine
        function calculateEMI(principal, rate, years, type = 'reducing') {
            const monthlyRate = rate / 1200;
            const months = years * 12;
            
            if(type === 'reducing') {
                const emi = principal * monthlyRate * Math.pow(1 + monthlyRate, months) / 
                          (Math.pow(1 + monthlyRate, months) - 1);
                return {
                    emi: emi,
                    schedule: generateSchedule(principal, monthlyRate, emi, months)
                };
            }
            
            // Flat rate calculation
            const totalInterest = principal * (rate/100) * years;
            const emi = (principal + totalInterest) / months;
            return {
                emi: emi,
                schedule: generateFlatSchedule(principal, totalInterest, months)
            };
        }

        function generateSchedule(P, r, emi, months) {
            let balance = P;
            const schedule = [];
            
            for(let month = 1; month <= months; month++) {
                const interest = balance * r;
                const principal = emi - interest;
                balance -= principal;
                
                schedule.push({
                    month: month,
                    principal: Math.max(principal, 0),
                    interest: interest,
                    balance: Math.max(balance, 0)
                });
            }
            return schedule;
        }

        // Update UI Functions
        function updateHomeLoan() {
            const amount = parseFloat(document.getElementById('home-amount').value);
            const rate = parseFloat(document.getElementById('home-rate').value);
            const tenure = parseFloat(document.getElementById('home-tenure').value);
            
            const { emi, schedule } = calculateEMI(amount, rate, tenure);
            const totalInterest = schedule.reduce((sum, m) => sum + m.interest, 0);
            
            // Update Results
            document.getElementById('home-emi').textContent = emi.toFixed(2);
            document.getElementById('home-interest').textContent = totalInterest.toFixed(2);
            document.getElementById('home-total').textContent = (amount + totalInterest).toFixed(2);
            document.getElementById('home-period').textContent = tenure * 12;
            
            // Update Chart
            const principalPercent = (amount / (amount + totalInterest) * 100).toFixed(1);
            document.querySelector('#home .pie-chart').style.setProperty('--principal-percent', `${principalPercent}%`);
            
            // Update Amortization Table
            const tbody = document.getElementById('home-schedule');
            tbody.innerHTML = schedule.map(m => `
                <tr>
                    <td>${m.month}</td>
                    <td style="color: var(--success);">₹${m.principal.toFixed(2)}</td>
                    <td style="color: var(--danger);">₹${m.interest.toFixed(2)}</td>
                    <td>₹${m.balance.toFixed(2)}</td>
                </tr>
            `).join('');
        }

        // Event Listeners
        document.querySelectorAll('.tab-btn').forEach(btn => {
            btn.addEventListener('click', () => {
                document.querySelectorAll('.calculator-card').forEach(c => c.style.display = 'none');
                document.querySelectorAll('.tab-btn').forEach(t => t.classList.remove('active'));
                btn.classList.add('active');
                document.getElementById(btn.dataset.tab).style.display = 'block';
            });
        });

        document.querySelectorAll('input').forEach(input => {
            input.addEventListener('input', () => {
                if(input.closest('#home')) updateHomeLoan();
                // Add other calculator update functions
            });
        });

        // Initialize Ads
        (adsbygoogle = window.adsbygoogle || []).push({});

        // Initial Calculation
        updateHomeLoan();
    </script>

    <!-- Structured Data -->
    <script type="application/ld+json">
    {
        "@context": "https://schema.org",
        "@type": "WebApplication",
        "name": "Ultimate Loan Calculator Suite",
        "description": "Comprehensive loan calculators with detailed amortization schedules and interest breakdowns",
        "applicationCategory": "FinancialApplication",
        "operatingSystem": "All",
        "offers": {
            "@type": "Offer",
            "price": "0",
            "priceCurrency": "USD"
        }
    }
    </script>
</body>
</html>
