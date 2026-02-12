# Codnb-
New giveaway project investment plan earning
<!DOCTYPE html>
<html lang="ur" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>VIP Investment Hub - Premium Platform</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        :root {
            --gold: #FFD700;
            --dark-gold: #B8860B;
            --dark: #0a0a0a;
            --card: #1a1a1a;
            --success: #00C853;
            --danger: #FF1744;
            --primary: #667eea;
        }

        body {
            background: var(--dark);
            color: white;
            min-height: 100vh;
        }

        /* Loader */
        #loader {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: var(--dark);
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 99999;
            flex-direction: column;
        }

        .spinner {
            width: 80px;
            height: 80px;
            border: 5px solid var(--gold);
            border-top-color: transparent;
            border-radius: 50%;
            animation: spin 1s linear infinite;
        }

        @keyframes spin {
            to { transform: rotate(360deg); }
        }

        /* Header */
        .header {
            background: linear-gradient(135deg, #1a1a2e 0%, #16213e 100%);
            padding: 1rem;
            border-bottom: 3px solid var(--gold);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .logo {
            text-align: center;
            font-size: 1.8rem;
            font-weight: bold;
            color: var(--gold);
            margin-bottom: 1rem;
        }

        .balance-cards {
            display: flex;
            justify-content: center;
            gap: 1rem;
            flex-wrap: wrap;
        }

        .balance-card {
            background: rgba(255, 215, 0, 0.1);
            border: 2px solid var(--gold);
            padding: 1rem 2rem;
            border-radius: 15px;
            text-align: center;
            min-width: 150px;
        }

        .balance-label {
            font-size: 0.9rem;
            color: #aaa;
            margin-bottom: 0.5rem;
        }

        .balance-amount {
            font-size: 1.8rem;
            font-weight: bold;
            color: var(--gold);
        }

        /* Navigation */
        .nav-container {
            background: rgba(0,0,0,0.8);
            padding: 1rem;
            display: flex;
            justify-content: center;
            gap: 0.5rem;
            flex-wrap: wrap;
            border-bottom: 1px solid #333;
        }

        .nav-btn {
            padding: 12px 20px;
            background: transparent;
            border: 2px solid var(--gold);
            color: var(--gold);
            border-radius: 25px;
            cursor: pointer;
            transition: all 0.3s;
            font-weight: 600;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .nav-btn:hover, .nav-btn.active {
            background: var(--gold);
            color: black;
            transform: translateY(-2px);
        }

        /* Sections */
        .section {
            display: none;
            padding: 2rem 1rem;
            max-width: 1200px;
            margin: 0 auto;
            animation: fadeIn 0.5s;
        }

        .section.active {
            display: block;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .section-title {
            text-align: center;
            font-size: 2rem;
            color: var(--gold);
            margin-bottom: 0.5rem;
        }

        .section-subtitle {
            text-align: center;
            color: #aaa;
            margin-bottom: 2rem;
        }

        /* VIP Plans */
        .plans-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 1.5rem;
        }

        .plan-card {
            background: linear-gradient(145deg, #1a1a1a 0%, #2d2d2d 100%);
            border: 2px solid transparent;
            border-radius: 20px;
            padding: 2rem;
            text-align: center;
            position: relative;
            transition: all 0.3s;
            overflow: hidden;
        }

        .plan-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(90deg, var(--gold), orange);
        }

        .plan-card:hover {
            transform: translateY(-10px);
            border-color: var(--gold);
            box-shadow: 0 20px 40px rgba(255, 215, 0, 0.2);
        }

        .plan-badge {
            background: linear-gradient(45deg, var(--gold), orange);
            color: black;
            padding: 5px 20px;
            border-radius: 20px;
            font-weight: bold;
            display: inline-block;
            margin-bottom: 1rem;
        }

        .plan-price {
            font-size: 2.5rem;
            color: var(--gold);
            font-weight: bold;
            margin: 1rem 0;
        }

        .plan-detail {
            margin: 0.5rem 0;
            color: #ccc;
        }

        .plan-profit {
            color: var(--success);
            font-size: 1.2rem;
            font-weight: bold;
            margin: 1rem 0;
        }

        .btn-invest {
            width: 100%;
            padding: 1rem;
            background: linear-gradient(45deg, var(--gold), orange);
            border: none;
            border-radius: 10px;
            color: black;
            font-weight: bold;
            font-size: 1.1rem;
            cursor: pointer;
            margin-top: 1rem;
            transition: all 0.3s;
        }

        .btn-invest:hover {
            transform: scale(1.05);
            box-shadow: 0 10px 30px rgba(255, 215, 0, 0.4);
        }

        .btn-invest:disabled {
            background: #444;
            cursor: not-allowed;
            transform: none;
        }

        /* Forms */
        .form-container {
            max-width: 500px;
            margin: 0 auto;
            background: linear-gradient(145deg, #1a1a1a 0%, #2d2d2d 100%);
            padding: 2rem;
            border-radius: 20px;
            border: 2px solid var(--gold);
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            color: var(--gold);
            font-weight: 600;
        }

        .form-group input, .form-group select {
            width: 100%;
            padding: 1rem;
            border: 1px solid #444;
            background: #0a0a0a;
            color: white;
            border-radius: 10px;
            font-size: 1rem;
        }

        .form-group input:focus {
            outline: none;
            border-color: var(--gold);
        }

        .deposit-info {
            background: rgba(0, 200, 83, 0.1);
            border: 2px dashed var(--success);
            padding: 1.5rem;
            border-radius: 15px;
            text-align: center;
            margin-bottom: 2rem;
        }

        .deposit-number {
            font-size: 2rem;
            color: var(--success);
            font-weight: bold;
            letter-spacing: 2px;
            margin: 1rem 0;
        }

        .copy-btn {
            background: var(--success);
            color: white;
            border: none;
            padding: 10px 30px;
            border-radius: 25px;
            cursor: pointer;
            font-weight: bold;
        }

        /* Tables */
        .table-container {
            overflow-x: auto;
            background: linear-gradient(145deg, #1a1a1a 0%, #2d2d2d 100%);
            border-radius: 15px;
            padding: 1rem;
        }

        table {
            width: 100%;
            border-collapse: collapse;
        }

        th, td {
            padding: 1rem;
            text-align: left;
            border-bottom: 1px solid #333;
        }

        th {
            color: var(--gold);
            font-weight: 600;
        }

        .status-pending { color: orange; }
        .status-approved { color: var(--success); }
        .status-rejected { color: var(--danger); }

        /* Admin Panel */
        .admin-login {
            max-width: 400px;
            margin: 2rem auto;
            background: linear-gradient(145deg, #1a1a1a 0%, #2d2d2d 100%);
            padding: 2rem;
            border-radius: 20px;
            border: 2px solid var(--danger);
        }

        .admin-dashboard {
            display: none;
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1rem;
            margin-bottom: 2rem;
        }

        .stat-box {
            background: linear-gradient(145deg, #1a1a1a 0%, #2d2d2d 100%);
            padding: 1.5rem;
            border-radius: 15px;
            border-left: 4px solid var(--gold);
        }

        .stat-value {
            font-size: 2rem;
            color: var(--gold);
            font-weight: bold;
        }

        .action-btn {
            padding: 5px 15px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            margin: 0 5px;
            font-weight: 600;
        }

        .btn-approve {
            background: var(--success);
            color: white;
        }

        .btn-reject {
            background: var(--danger);
            color: white;
        }

        /* Modal */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.9);
            z-index: 10000;
            justify-content: center;
            align-items: center;
        }

        .modal-content {
            background: linear-gradient(145deg, #1a1a1a 0%, #2d2d2d 100%);
            padding: 2rem;
            border-radius: 20px;
            border: 2px solid var(--gold);
            max-width: 500px;
            width: 90%;
            position: relative;
        }

        .close-btn {
            position: absolute;
            top: 15px;
            left: 15px;
            font-size: 1.5rem;
            cursor: pointer;
            color: var(--danger);
        }

        /* Toast Notification */
        .toast {
            position: fixed;
            top: 20px;
            right: 20px;
            background: linear-gradient(45deg, var(--success), #00E676);
            color: white;
            padding: 1rem 2rem;
            border-radius: 10px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
            z-index: 10001;
            display: none;
            animation: slideIn 0.3s;
        }

        @keyframes slideIn {
            from { transform: translateX(100%); }
            to { transform: translateX(0); }
        }

        /* Responsive */
        @media (max-width: 768px) {
            .plans-grid {
                grid-template-columns: 1fr;
            }
            .balance-cards {
                flex-direction: column;
                align-items: center;
            }
            .nav-btn {
                padding: 10px 15px;
                font-size: 0.9rem;
            }
        }
    </style>
</head>
<body>

    <!-- Loader -->
    <div id="loader">
        <div class="spinner"></div>
        <h2 style="color: var(--gold); margin-top: 1rem;">VIP Investment Hub</h2>
        <p>Loading Secure Environment...</p>
    </div>

    <!-- Toast -->
    <div id="toast" class="toast"></div>

    <!-- Header -->
    <div class="header">
        <div class="logo">
            <i class="fas fa-crown"></i> VIP Investment Hub
        </div>
        <div class="balance-cards">
            <div class="balance-card">
                <div class="balance-label">موجودہ بیلنس</div>
                <div class="balance-amount">Rs <span id="currentBalance">0</span></div>
            </div>
            <div class="balance-card">
                <div class="balance-label">کل منافع</div>
                <div class="balance-amount" style="color: var(--success);">Rs <span id="totalProfit">0</span></div>
            </div>
            <div class="balance-card">
                <div class="balance-label">سرمایہ کاری</div>
                <div class="balance-amount" style="color: var(--primary);">Rs <span id="totalInvested">0</span></div>
            </div>
        </div>
    </div>

    <!-- Navigation -->
    <div class="nav-container">
        <button class="nav-btn active" onclick="showSection('home')">
            <i class="fas fa-home"></i> Home
        </button>
        <button class="nav-btn" onclick="showSection('plans')">
            <i class="fas fa-crown"></i> VIP Plans
        </button>
        <button class="nav-btn" onclick="showSection('deposit')">
            <i class="fas fa-wallet"></i> Deposit
        </button>
        <button class="nav-btn" onclick="showSection('withdraw')">
            <i class="fas fa-money-bill-wave"></i> Withdraw
        </button>
        <button class="nav-btn" onclick="showSection('myplans')">
            <i class="fas fa-chart-pie"></i> My Plans
        </button>
        <button class="nav-btn" onclick="showSection('history')">
            <i class="fas fa-history"></i> History
        </button>
        <button class="nav-btn" onclick="showSection('admin')">
            <i class="fas fa-lock"></i> Admin
        </button>
    </div>

    <!-- Home Section -->
    <div id="home" class="section active">
        <h1 class="section-title">Welcome to VIP Investment Hub</h1>
        <p class="section-subtitle">پیشہ ورانہ انویسٹمنٹ پلیٹ فارم - محفوظ اور قابل اعتماد</p>
        
        <div style="text-align: center; padding: 3rem 1rem;">
            <i class="fas fa-shield-alt" style="font-size: 4rem; color: var(--success); margin-bottom: 1rem;"></i>
            <h2 style="color: var(--gold); margin-bottom: 1rem;">256-bit SSL Security</h2>
            <p style="color: #aaa; max-width: 600px; margin: 0 auto 2rem;">
                Your investments are secured with bank-level encryption. 
                Start with as low as Rs 100 and earn 10% daily profit.
            </p>
            <button class="btn-invest" onclick="showSection('plans')" style="max-width: 300px;">
                View VIP Plans <i class="fas fa-arrow-right"></i>
            </button>
        </div>

        <div class="plans-grid" style="margin-top: 3rem;">
            <div class="plan-card">
                <i class="fas fa-rocket" style="font-size: 3rem; color: var(--gold); margin-bottom: 1rem;"></i>
                <h3>Quick Returns</h3>
                <p style="color: #aaa;">10% daily profit for 10 days</p>
            </div>
            <div class="plan-card">
                <i class="fas fa-lock" style="font-size: 3rem; color: var(--success); margin-bottom: 1rem;"></i>
                <h3>Secure Platform</h3>
                <p style="color: #aaa;">256-bit SSL encryption</p>
            </div>
            <div class="plan-card">
                <i class="fas fa-headset" style="font-size: 3rem; color: var(--primary); margin-bottom: 1rem;"></i>
                <h3>24/7 Support</h3>
                <p style="color: #aaa;">Always here to help you</p>
            </div>
        </div>
    </div>

    <!-- VIP Plans Section -->
    <div id="plans" class="section">
        <h2 class="section-title"><i class="fas fa-crown"></i> VIP Investment Plans</h2>
        <p class="section-subtitle">10 Days Plan - 10% Daily Profit - Double Your Investment</p>
        
        <div class="plans-grid" id="plansContainer">
            <!-- Plans generated by JS -->
        </div>
    </div>

    <!-- Deposit Section -->
    <div id="deposit" class="section">
        <h2 class="section-title"><i class="fas fa-wallet"></i> Deposit Funds</h2>
        <p class="section-subtitle">Minimum Deposit: Rs 100 | Maximum: Rs 10,000</p>
        
        <div class="form-container">
            <div class="deposit-info">
                <i class="fas fa-mobile-alt" style="font-size: 2rem; color: var(--success); margin-bottom: 0.5rem;"></i>
                <h3 style="margin-bottom: 0.5rem;">Send Money To:</h3>
                <div class="deposit-number">0325-1518865</div>
                <p style="color: #aaa; font-size: 0.9rem;">JazzCash / EasyPaisa</p>
                <button class="copy-btn" onclick="copyNumber()">
                    <i class="fas fa-copy"></i> Copy Number
                </button>
            </div>

            <form id="depositForm" onsubmit="submitDeposit(event)">
                <div class="form-group">
                    <label>Your Full Name</label>
                    <input type="text" id="depName" required placeholder="Enter your name">
                </div>
                <div class="form-group">
                    <label>Amount (Rs)</label>
                    <input type="number" id="depAmount" min="100" max="10000" required placeholder="100 - 10000">
                </div>
                <div class="form-group">
                    <label>Transaction ID (TID)</label>
                    <input type="text" id="depTid" required placeholder="Enter JazzCash/EasyPaisa TID">
                </div>
                <div class="form-group">
                    <label>Screenshot (Optional)</label>
                    <input type="file" id="depScreenshot" accept="image/*">
                </div>
                <button type="submit" class="btn-invest">
                    <i class="fas fa-paper-plane"></i> Submit Deposit Request
                </button>
            </form>
        </div>
    </div>

    <!-- Withdraw Section -->
    <div id="withdraw" class="section">
        <h2 class="section-title"><i class="fas fa-money-bill-wave"></i> Withdraw Funds</h2>
        <p class="section-subtitle">Minimum Withdrawal: Rs 500</p>
        
        <div class="form-container">
            <form id="withdrawForm" onsubmit="submitWithdraw(event)">
                <div class="form-group">
                    <label>Amount (Rs)</label>
                    <input type="number" id="witAmount" min="500" required placeholder="Enter amount">
                </div>
                <div class="form-group">
                    <label>Payment Method</label>
                    <select id="witMethod" required>
                        <option value="">Select Method</option>
                        <option value="jazzcash">JazzCash</option>
                        <option value="easypaisa">EasyPaisa</option>
                        <option value="bank">Bank Transfer</option>
                    </select>
                </div>
                <div class="form-group">
                    <label>Account Number / IBAN</label>
                    <input type="text" id="witAccount" required placeholder="03XX-XXXXXXX or IBAN">
                </div>
                <div class="form-group">
                    <label>Account Title</label>
                    <input type="text" id="witTitle" required placeholder="Account holder name">
                </div>
                <button type="submit" class="btn-invest" style="background: linear-gradient(45deg, var(--success), #00E676);">
                    <i class="fas fa-paper-plane"></i> Request Withdrawal
                </button>
            </form>
        </div>
    </div>

    <!-- My Plans Section -->
    <div id="myplans" class="section">
        <h2 class="section-title"><i class="fas fa-chart-pie"></i> My Active Plans</h2>
        <div id="activePlansContainer" class="plans-grid">
            <!-- Active plans displayed here -->
        </div>
    </div>

    <!-- History Section -->
    <div id="history" class="section">
        <h2 class="section-title"><i class="fas fa-history"></i> Transaction History</h2>
        <div class="table-container">
            <table>
                <thead>
                    <tr>
                        <th>Date</th>
                        <th>Type</th>
                        <th>Amount</th>
                        <th>Details</th>
                        <th>Status</th>
                    </tr>
                </thead>
                <tbody id="historyTableBody">
                    <!-- History rows -->
                </tbody>
            </table>
        </div>
    </div>

    <!-- Admin Section -->
    <div id="admin" class="section">
        <div class="admin-login" id="adminLogin">
            <h2 style="text-align: center; color: var(--danger); margin-bottom: 2rem;">
                <i class="fas fa-lock"></i> Admin Login
            </h2>
            <form onsubmit="adminLogin(event)">
                <div class="form-group">
                    <label>Username</label>
                    <input type="text" id="adminUser" required placeholder="Enter username">
                </div>
                <div class="form-group">
                    <label>Password</label>
                    <input type="password" id="adminPass" required placeholder="Enter password">
                </div>
                <button type="submit" class="btn-invest" style="background: linear-gradient(45deg, var(--danger), #FF5252);">
                    <i class="fas fa-sign-in-alt"></i> Login
                </button>
            </form>
        </div>

        <div class="admin-dashboard" id="adminDashboard">
            <h2 class="section-title" style="color: var(--danger);">
                <i class="fas fa-user-shield"></i> Admin Dashboard
            </h2>
            
            <div class="stats-grid">
                <div class="stat-box">
                    <div class="stat-value" id="statUsers">0</div>
                    <div>Total Users</div>
                </div>
                <div class="stat-box">
                    <div class="stat-value" id="statDeposits">0</div>
                    <div>Pending Deposits</div>
                </div>
                <div class="stat-box">
                    <div class="stat-value" id="statWithdrawals">0</div>
                    <div>Pending Withdrawals</div>
                </div>
                <div class="stat-box">
                    <div class="stat-value" id="statInvestments">0</div>
                    <div>Active Investments</div>
                </div>
            </div>

            <h3 style="color: var(--gold); margin: 2rem 0 1rem;">Pending Deposits</h3>
            <div class="table-container">
                <table>
                    <thead>
                        <tr>
                            <th>User</th>
                            <th>Amount</th>
                            <th>TID</th>
                            <th>Date</th>
                            <th>Action</th>
                        </tr>
                    </thead>
                    <tbody id="adminDepositsTable"></tbody>
                </table>
            </div>

            <h3 style="color: var(--gold); margin: 2rem 0 1rem;">Pending Withdrawals</h3>
            <div class="table-container">
                <table>
                    <thead>
                        <tr>
                            <th>User</th>
                            <th>Amount</th>
                            <th>Method</th>
                            <th>Account</th>
                            <th>Action</th>
                        </tr>
                    </thead>
                    <tbody id="adminWithdrawalsTable"></tbody>
                </table>
            </div>

            <button onclick="adminLogout()" class="btn-invest" style="margin-top: 2rem; background: #444;">
                <i class="fas fa-sign-out-alt"></i> Logout
            </button>
        </div>
    </div>

    <!-- Investment Modal -->
    <div id="investModal" class="modal">
        <div class="modal-content">
            <span class="close-btn" onclick="closeModal()">&times;</span>
            <h2 style="color: var(--gold); margin-bottom: 1.5rem; text-align: center;">
                Confirm Investment
            </h2>
            <div id="modalContent"></div>
            <button class="btn-invest" onclick="confirmInvestment()" style="margin-top: 1.5rem;">
                <i class="fas fa-check"></i> Confirm Investment
            </button>
        </div>
    </div>

    <script>
        // Data Management
        const DB = {
            get: (key) => JSON.parse(localStorage.getItem(key) || 'null'),
            set: (key, value) => localStorage.setItem(key, JSON.stringify(value)),
            init: () => {
                if (!DB.get('vip_user')) {
                    DB.set('vip_user', {
                        balance: 0,
                        totalProfit: 0,
                        totalInvested: 0,
                        activePlans: [],
                        history: []
                    });
                }
                if (!DB.get('pending_deposits')) DB.set('pending_deposits', []);
                if (!DB.get('pending_withdrawals')) DB.set('pending_withdrawals', []);
                if (!DB.get('all_users')) DB.set('all_users', []);
            }
        };

        // VIP Plans Configuration
        const PLANS = [
            { id: 1, name: 'VIP 1', price: 100, dailyProfit: 10, totalProfit: 100, days: 10 },
            { id: 2, name: 'VIP 2', price: 500, dailyProfit: 50, totalProfit: 500, days: 10 },
            { id: 3, name: 'VIP 3', price: 1000, dailyProfit: 100, totalProfit: 1000, days: 10 },
            { id: 4, name: 'VIP 4', price: 2000, dailyProfit: 200, totalProfit: 2000, days: 10 },
            { id: 5, name: 'VIP 5', price: 3000, dailyProfit: 300, totalProfit: 3000, days: 10 },
            { id: 6, name: 'VIP 6', price: 5000, dailyProfit: 500, totalProfit: 5000, days: 10 },
            { id: 7, name: 'VIP 7', price: 8000, dailyProfit: 800, totalProfit: 8000, days: 10 },
            { id: 8, name: 'VIP 8', price: 10000, dailyProfit: 1000, totalProfit: 10000, days: 10 }
        ];

        let selectedPlan = null;
        let currentUser = null;

        // Initialize
        window.onload = function() {
            DB.init();
            currentUser = DB.get('vip_user');
            
            setTimeout(() => {
                document.getElementById('loader').style.display = 'none';
            }, 1500);
            
            renderPlans();
            updateDashboard();
            renderHistory();
            renderActivePlans();
            startProfitTimer();
        };

        // Navigation
        function showSection(sectionId) {
            document.querySelectorAll('.section').forEach(s => s.classList.remove('active'));
            document.querySelectorAll('.nav-btn').forEach(b => b.classList.remove('active'));
            
            document.getElementById(sectionId).classList.add('active');
            event.target.classList.add('active');
            
            if (sectionId === 'admin' && sessionStorage.getItem('admin_logged') === 'true') {
                showAdminDashboard();
            }
        }

        // Render VIP Plans
        function renderPlans() {
            const container = document.getElementById('plansContainer');
            container.innerHTML = PLANS.map(plan => `
                <div class="plan-card">
                    <div class="plan-badge">${plan.name}</div>
                    <div class="plan-price">Rs ${plan.price.toLocaleString()}</div>
                    <div class="plan-detail">
                        <i class="fas fa-calendar-alt"></i> ${plan.days} Days Plan
                    </div>
                    <div class="plan-profit">
                        <i class="fas fa-coins"></i> Daily: Rs ${plan.dailyProfit}
                    </div>
                    <div class="plan-profit" style="color: var(--gold);">
                        Total Return: Rs ${plan.price + plan.totalProfit}
                    </div>
                    <div class="plan-detail" style="font-size: 0.9rem; color: #666;">
                        Profit: ${plan.totalProfit} (${(plan.totalProfit/plan.price*100).toFixed(0)}%)
                    </div>
                    <button class="btn-invest" onclick="openInvestModal(${plan.id})">
                        <i class="fas fa-crown"></i> Invest Now
                    </button>
                </div>
            `).join('');
        }

        // Investment Modal
        function openInvestModal(planId) {
            selectedPlan = PLANS.find(p => p.id === planId);
            
            if (currentUser.balance < selectedPlan.price) {
                showToast('Insufficient balance! Please deposit first.', 'error');
                showSection('deposit');
                document.querySelector('[onclick="showSection(\'deposit\')"]').click();
                return;
            }
            
            document.getElementById('modalContent').innerHTML = `
                <div style="text-align: center; line-height: 2;">
                    <p><strong style="color: var(--gold);">Plan:</strong> ${selectedPlan.name}</p>
                    <p><strong style="color: var(--gold);">Investment:</strong> Rs ${selectedPlan.price.toLocaleString()}</p>
                    <p><strong style="color: var(--gold);">Daily Profit:</strong> Rs ${selectedPlan.dailyProfit}</p>
                    <p><strong style="color: var(--gold);">Duration:</strong> ${selectedPlan.days} Days</p>
                    <hr style="border-color: #333; margin: 1rem 0;">
                    <p><strong style="color: var(--success);">Total Return:</strong> Rs ${(selectedPlan.price + selectedPlan.totalProfit).toLocaleString()}</p>
                </div>
            `;
            document.getElementById('investModal').style.display = 'flex';
        }

        function closeModal() {
            document.getElementById('investModal').style.display = 'none';
            selectedPlan = null;
        }

        function confirmInvestment() {
            if (!selectedPlan) return;
            
            currentUser.balance -= selectedPlan.price;
            currentUser.totalInvested += selectedPlan.price;
            
            const plan = {
                ...selectedPlan,
                startDate: new Date().toISOString(),
                lastProfitDate: new Date().toISOString(),
                daysCompleted: 0,
                totalEarned: 0
            };
            
            currentUser.activePlans.push(plan);
            addToHistory('Investment', selectedPlan.price, `Purchased ${selectedPlan.name}`, 'completed');
            
            DB.set('vip_user', currentUser);
            updateDashboard();
            renderActivePlans();
            closeModal();
            showToast('Investment successful!');
        }

        // Profit Calculation System
        function startProfitTimer() {
            setInterval(() => {
                let updated = false;
                const now = new Date();
                
                currentUser.activePlans.forEach((plan, index) => {
                    if (plan.daysCompleted >= plan.days) return;
                    
                    const lastProfit = new Date(plan.lastProfitDate);
                    const hoursDiff = (now - lastProfit) / (1000 * 60 * 60);
                    
                    if (hoursDiff >= 24) {
                        currentUser.balance += plan.dailyProfit;
                        currentUser.totalProfit += plan.dailyProfit;
                        plan.totalEarned += plan.dailyProfit;
                        plan.daysCompleted++;
                        plan.lastProfitDate = now.toISOString();
                        updated = true;
                        
                        addToHistory('Daily Profit', plan.dailyProfit, `From ${plan.name} - Day ${plan.daysCompleted}`, 'completed');
                        
                        if (plan.daysCompleted >= plan.days) {
                            addToHistory('Plan Completed', plan.price + plan.totalProfit, `${plan.name} completed successfully`, 'completed');
                        }
                    }
                });
                
                if (updated) {
                    DB.set('vip_user', currentUser);
                    updateDashboard();
                    renderActivePlans();
                }
            }, 60000); // Check every minute
        }

        // Deposit Functions
        function copyNumber() {
            navigator.clipboard.writeText('03251518865');
            showToast('Number copied: 0325-1518865');
        }

        function submitDeposit(e) {
            e.preventDefault();
            
            const deposit = {
                id: Date.now(),
                userId: 'user_' + Math.random().toString(36).substr(2, 9),
                name: document.getElementById('depName').value,
                amount: parseInt(document.getElementById('depAmount').value),
                tid: document.getElementById('depTid').value,
                date: new Date().toLocaleString(),
                status: 'pending'
            };
            
            let deposits = DB.get('pending_deposits') || [];
            deposits.push(deposit);
            DB.set('pending_deposits', deposits);
            
            showToast('Deposit request submitted! Waiting for admin approval.');
            e.target.reset();
        }

        // Withdrawal Functions
        function submitWithdraw(e) {
            e.preventDefault();
            
            const amount = parseInt(document.getElementById('witAmount').value);
            
            if (amount > currentUser.balance) {
                showToast('Insufficient balance!', 'error');
                return;
            }
            
            const withdrawal = {
                id: Date.now(),
                amount: amount,
                method: document.getElementById('witMethod').value,
                account: document.getElementById('witAccount').value,
                title: document.getElementById('witTitle').value,
                date: new Date().toLocaleString(),
                status: 'pending'
            };
            
            let withdrawals = DB.get('pending_withdrawals') || [];
            withdrawals.push(withdrawal);
            DB.set('pending_withdrawals', withdrawals);
            
            currentUser.balance -= amount;
            DB.set('vip_user', currentUser);
            updateDashboard();
            
            addToHistory('Withdrawal Request', amount, `To ${withdrawal.account}`, 'pending');
            showToast('Withdrawal request submitted!');
            e.target.reset();
        }

        // History Management
        function addToHistory(type, amount, details, status) {
            currentUser.history.unshift({
                date: new Date().toLocaleString(),
                type: type,
                amount: amount,
                details: details,
                status: status
            });
            DB.set('vip_user', currentUser);
            renderHistory();
        }

        function renderHistory() {
            const tbody = document.getElementById('historyTableBody');
            if (!currentUser.history.length) {
                tbody.innerHTML = '<tr><td colspan="5" style="text-align: center; color: #666;">No transactions yet</td></tr>';
                return;
            }
            
            tbody.innerHTML = currentUser.history.map(h => `
                <tr>
                    <td>${h.date}</td>
                    <td>${h.type}</td>
                    <td style="color: ${h.type.includes('Profit') || h.type.includes('Deposit') ? 'var(--success)' : 'white'}">
                        Rs ${h.amount.toLocaleString()}
                    </td>
                    <td>${h.details}</td>
                    <td class="status-${h.status}">${h.status.toUpperCase()}</td>
                </tr>
            `).join('');
        }

        // Active Plans
        function renderActivePlans() {
            const container = document.getElementById('activePlansContainer');
            if (!currentUser.activePlans.length) {
                container.innerHTML = '<p style="text-align: center; color: #666; grid-column: 1/-1;">No active plans</p>';
                return;
            }
            
            container.innerHTML = currentUser.activePlans.map(plan => `
                <div class="plan-card" style="${plan.daysCompleted >= plan.days ? 'border-color: var(--success);' : ''}">
                    <div class="plan-badge" style="${plan.daysCompleted >= plan.days ? 'background: var(--success);' : ''}">
                        ${plan.daysCompleted >= plan.days ? 'Completed' : plan.name}
                    </div>
                    <div class="plan-price">Rs ${plan.price.toLocaleString()}</div>
                    <div class="plan-detail">Progress: ${plan.daysCompleted}/${plan.days} Days</div>
                    <div class="plan-profit">Earned: Rs ${plan.totalEarned}</div>
                    <div style="background: #0a0a0a; height: 10px; border-radius: 5px; margin: 1rem 0; overflow: hidden;">
                        <div style="width: ${(plan.daysCompleted/plan.days*100)}%; height: 100%; background: linear-gradient(90deg, var(--gold), orange); transition: width 0.3s;"></div>
                    </div>
                    <div class="plan-detail" style="color: ${plan.daysCompleted >= plan.days ? 'var(--success)' : 'var(--gold)'};">
                        ${plan.daysCompleted >= plan.days ? 'Plan Completed!' : 'Running...'}
                    </div>
                </div>
            `).join('');
        }

        // Dashboard Update
        function updateDashboard() {
            document.getElementById('currentBalance').textContent = currentUser.balance.toLocaleString();
            document.getElementById('totalProfit').textContent = currentUser.totalProfit.toLocaleString();
            document.getElementById('totalInvested').textContent = currentUser.totalInvested.toLocaleString();
        }

        // Admin Functions
        function adminLogin(e) {
            e.preventDefault();
            const user = document.getElementById('adminUser').value;
            const pass = document.getElementById('adminPass').value;
            
            if (user === 'admin' && pass === 'admin123') {
                sessionStorage.setItem('admin_logged', 'true');
                showAdminDashboard();
            } else {
                showToast('Invalid credentials!', 'error');
            }
        }

        function showAdminDashboard() {
            document.getElementById('adminLogin').style.display = 'none';
            document.getElementById('adminDashboard').style.display = 'block';
            renderAdminData();
        }

        function adminLogout() {
            sessionStorage.removeItem('admin_logged');
            document.getElementById('adminLogin').style.display = 'block';
            document.getElementById('adminDashboard').style.display = 'none';
        }

        function renderAdminData() {
            const deposits = DB.get('pending_deposits') || [];
            const withdrawals = DB.get('pending_withdrawals') || [];
            
            document.getElementById('statDeposits').textContent = deposits.length;
            document.getElementById('statWithdrawals').textContent = withdrawals.length;
            document.getElementById('statInvestments').textContent = currentUser.activePlans.length;
            document.getElementById('statUsers').textContent = '1'; // Simplified for demo
            
            // Deposits Table
            document.getElementById('adminDepositsTable').innerHTML = deposits.map(d => `
                <tr>
                    <td>${d.name}</td>
                    <td>Rs ${d.amount.toLocaleString()}</td>
                    <td>${d.tid}</td>
                    <td>${d.date}</td>
                    <td>
                        <button class="action-btn btn-approve" onclick="approveDeposit(${d.id})">Approve</button>
                        <button class="action-btn btn-reject" onclick="rejectDeposit(${d.id})">Reject</button>
                    </td>
                </tr>
            `).join('') || '<tr><td colspan="5" style="text-align: center;">No pending deposits</td></tr>';
            
            // Withdrawals Table
            document.getElementById('adminWithdrawalsTable').innerHTML = withdrawals.map(w => `
                <tr>
                    <td>${w.title}</td>
                    <td>Rs ${w.amount.toLocaleString()}</td>
                    <td>${w.method}</td>
                    <td>${w.account}</td>
                    <td>
                        <button class="action-btn btn-approve" onclick="approveWithdrawal(${w.id})">Approve</button>
                        <button class="action-btn btn-reject" onclick="rejectWithdrawal(${w.id})">Reject</button>
                    </td>
                </tr>
            `).join('') || '<tr><td colspan="5" style="text-align: center;">No pending withdrawals</td></tr>';
        }

        function approveDeposit(id) {
            let deposits = DB.get('pending_deposits') || [];
            const deposit = deposits.find(d => d.id === id);
            if (deposit) {
                currentUser.balance += deposit.amount;
                DB.set('vip_user', currentUser);
                addToHistory('Deposit', deposit.amount, 'Approved by admin', 'completed');
                
                deposits = deposits.filter(d => d.id !== id);
                DB.set('pending_deposits', deposits);
                
                updateDashboard();
                renderAdminData();
                showToast('Deposit approved!');
            }
        }

        function rejectDeposit(id) {
            let deposits = DB.get('pending_deposits') || [];
            deposits = deposits.filter(d => d.id !== id);
            DB.set('pending_deposits', deposits);
            renderAdminData();
            showToast('Deposit rejected');
        }

        function approveWithdrawal(id) {
            let withdrawals = DB.get('pending_withdrawals') || [];
            const withdrawal = withdrawals.find(w => w.id === id);
            if (withdrawal) {
                addToHistory('Withdrawal', withdrawal.amount, 'Approved and sent', 'completed');
                
                withdrawals = withdrawals.filter(w => w.id !== id);
                DB.set('pending_withdrawals', withdrawals);
                
                renderAdminData();
                showToast('Withdrawal approved!');
            }
        }

        function rejectWithdrawal(id) {
            let withdrawals = DB.get('pending_withdrawals') || [];
            const withdrawal = withdrawals.find(w => w.id === id);
            if (withdrawal) {
                currentUser.balance += withdrawal.amount;
                DB.set('vip_user', currentUser);
                updateDashboard();
            }
            withdrawals = withdrawals.filter(w => w.id !== id);
            DB.set('pending_withdrawals', withdrawals);
            renderAdminData();
            showToast('Withdrawal rejected');
        }

        // Toast Notification
        function showToast(message, type = 'success') {
            const toast = document.getElementById('toast');
            toast.textContent = message;
            toast.style.background = type === 'error' 
                ? 'linear-gradient(45deg, #FF1744, #FF5252)' 
                : 'linear-gradient(45deg, #00C853, #00E676)';
            toast.style.display = 'block';
            
            setTimeout(() => {
                toast.style.display = 'none';
            }, 3000);
        }

        // Close modal on outside click
        window.onclick = function(event) {
            const modal = document.getElementById('investModal');
            if (event.target === modal) {
                closeModal();
            }
        }
    </script>
</body>
</html>
