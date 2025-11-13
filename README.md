<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Get free Instagram, TikTok, and Facebook followers instantly. 100% safe and secure.">
    <title>Free Followers Generator - Instagram, TikTok & Facebook</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Helvetica Neue', sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            padding: 15px;
            color: #333;
            overflow-x: hidden;
        }

        .container {
            max-width: 480px;
            margin: 0 auto;
            padding: 10px 0;
        }

        .header {
            text-align: center;
            margin-bottom: 25px;
            color: white;
            animation: fadeInDown 0.8s ease;
        }

        .header h1 {
            font-size: 26px;
            font-weight: 700;
            margin-bottom: 8px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.2);
        }

        .header p {
            font-size: 15px;
            opacity: 0.95;
        }

        .card {
            background: white;
            border-radius: 20px;
            padding: 25px 20px;
            box-shadow: 0 20px 60px rgba(0,0,0,0.3);
            margin-bottom: 18px;
            animation: fadeInUp 0.8s ease;
        }

        .badge {
            background: linear-gradient(135deg, #ffd700 0%, #ffed4e 100%);
            color: #333;
            padding: 8px 16px;
            border-radius: 20px;
            font-size: 13px;
            font-weight: 700;
            display: inline-block;
            margin-bottom: 20px;
            box-shadow: 0 4px 10px rgba(255, 215, 0, 0.3);
        }

        .social-platforms {
            display: flex;
            justify-content: space-around;
            margin-bottom: 25px;
            gap: 12px;
        }

        .platform {
            text-align: center;
            cursor: pointer;
            transition: all 0.3s ease;
            flex: 1;
            padding: 10px;
            border-radius: 15px;
        }

        .platform:hover {
            transform: translateY(-5px);
            background: #f8f9fa;
        }

        .platform-icon {
            width: 65px;
            height: 65px;
            border-radius: 15px;
            margin-bottom: 8px;
            border: 3px solid transparent;
            transition: all 0.3s ease;
            object-fit: cover;
        }

        .platform.active .platform-icon {
            border-color: #667eea;
            box-shadow: 0 5px 15px rgba(102, 126, 234, 0.4);
        }

        .platform-name {
            font-size: 13px;
            font-weight: 600;
            color: #666;
        }

        .platform.active .platform-name {
            color: #667eea;
        }

        .form-section {
            margin-bottom: 22px;
        }

        label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            color: #333;
            font-size: 14px;
        }

        input[type="text"] {
            width: 100%;
            padding: 14px;
            border: 2px solid #e0e0e0;
            border-radius: 12px;
            font-size: 16px;
            transition: all 0.3s ease;
            outline: none;
        }

        input[type="text"]:focus {
            border-color: #667eea;
            box-shadow: 0 0 0 3px rgba(102, 126, 234, 0.1);
        }

        .followers-selector {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 10px;
            margin-top: 10px;
        }

        .follower-option {
            padding: 14px;
            border: 2px solid #e0e0e0;
            border-radius: 12px;
            text-align: center;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: 700;
            background: white;
            font-size: 15px;
        }

        .follower-option:hover {
            border-color: #667eea;
            transform: translateY(-2px);
        }

        .follower-option.selected {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            border-color: #667eea;
            box-shadow: 0 4px 12px rgba(102, 126, 234, 0.3);
        }

        .submit-btn {
            width: 100%;
            padding: 16px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            border: none;
            border-radius: 12px;
            font-size: 17px;
            font-weight: 700;
            cursor: pointer;
            transition: all 0.3s ease;
            margin-top: 20px;
            box-shadow: 0 6px 20px rgba(102, 126, 234, 0.4);
        }

        .submit-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 30px rgba(102, 126, 234, 0.5);
        }

        .submit-btn:active {
            transform: translateY(0);
        }

        .info-notice {
            background: linear-gradient(135deg, #e8f5e9 0%, #c8e6c9 100%);
            border-left: 4px solid #4caf50;
            border-radius: 10px;
            padding: 14px;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .info-notice-icon {
            font-size: 22px;
            flex-shrink: 0;
        }

        .info-notice p {
            margin: 0;
            color: #2e7d32;
            font-size: 13px;
            font-weight: 600;
            line-height: 1.4;
        }

        .features {
            display: grid;
            gap: 12px;
        }

        .feature {
            display: flex;
            align-items: center;
            gap: 12px;
            padding: 14px;
            background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
            border-radius: 12px;
            transition: transform 0.3s ease;
        }

        .feature:hover {
            transform: translateX(5px);
        }

        .feature-icon {
            width: 40px;
            height: 40px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: bold;
            flex-shrink: 0;
            font-size: 18px;
        }

        .feature-text {
            font-size: 14px;
            color: #333;
            font-weight: 600;
        }

        .stats-section {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 12px;
            margin-bottom: 20px;
        }

        .stat-box {
            text-align: center;
            padding: 15px 10px;
            background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
            border-radius: 12px;
        }

        .stat-number {
            font-size: 22px;
            font-weight: 700;
            color: #667eea;
            margin-bottom: 5px;
        }

        .stat-label {
            font-size: 11px;
            color: #666;
            font-weight: 600;
        }

        .footer {
            text-align: center;
            color: white;
            font-size: 13px;
            margin-top: 25px;
            opacity: 0.9;
        }

        @keyframes fadeInDown {
            from {
                opacity: 0;
                transform: translateY(-20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @media (max-width: 400px) {
            .header h1 {
                font-size: 22px;
            }
            
            .platform-icon {
                width: 55px;
                height: 55px;
            }
            
            .follower-option {
                font-size: 13px;
                padding: 12px 8px;
            }

            .stat-number {
                font-size: 18px;
            }
        }

        /* Loading animation */
        .loading {
            pointer-events: none;
            opacity: 0.7;
        }

        .loading::after {
            content: '';
            position: absolute;
            width: 20px;
            height: 20px;
            top: 50%;
            left: 50%;
            margin-left: -10px;
            margin-top: -10px;
            border: 3px solid #fff;
            border-radius: 50%;
            border-top-color: transparent;
            animation: spin 0.6s linear infinite;
        }

        @keyframes spin {
            to { transform: rotate(360deg); }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>🚀 Free Followers Generator</h1>
            <p>Boost Your Social Media Instantly!</p>
        </div>

        <div class="card">
            <center><span class="badge">✨ 100% FREE & SAFE</span></center>
            
            <div class="info-notice">
                <div class="info-notice-icon">📧</div>
                <p>Enter your details below. Email will be collected on the next secure page.</p>
            </div>

            <div class="social-platforms">
                <div class="platform active" data-platform="instagram">
                    <img src="https://static.vecteezy.com/system/resources/previews/042/387/654/non_2x/instagram-button-icon-set-instagram-screen-social-media-and-social-network-interface-template-stories-user-button-symbol-sign-logo-stories-liked-editorial-free-png.png" alt="Instagram" class="platform-icon">
                    <div class="platform-name">Instagram</div>
                </div>
                <div class="platform" data-platform="tiktok">
                    <img src="https://static.vecteezy.com/system/resources/previews/018/910/788/non_2x/tiktok-logo-tiktok-symbol-tiktok-icon-free-free-vector.jpg" alt="TikTok" class="platform-icon">
                    <div class="platform-name">TikTok</div>
                </div>
                <div class="platform" data-platform="facebook">
                    <img src="https://img.freepik.com/premium-vector/vector-facebook-social-media-icon-illustration_534308-21672.jpg?semt=ais_incoming&w=740&q=80" alt="Facebook" class="platform-icon">
                    <div class="platform-name">Facebook</div>
                </div>
            </div>

            <div class="form-section">
                <label for="username">📱 Your Username</label>
                <input type="text" id="username" placeholder="@yourusername" required>
            </div>

            <div class="form-section">
                <label>🎯 Select Followers Amount</label>
                <div class="followers-selector">
                    <div class="follower-option selected" data-value="1000">1K</div>
                    <div class="follower-option" data-value="5000">5K</div>
                    <div class="follower-option" data-value="10000">10K</div>
                </div>
            </div>

            <button id="continueBtn" class="submit-btn">🎁 Get Free Followers Now</button>
        </div>

        <div class="card">
            <div class="stats-section">
                <div class="stat-box">
                    <div class="stat-number">50K+</div>
                    <div class="stat-label">Happy Users</div>
                </div>
                <div class="stat-box">
                    <div class="stat-number">1M+</div>
                    <div class="stat-label">Followers Sent</div>
                </div>
                <div class="stat-box">
                    <div class="stat-number">24/7</div>
                    <div class="stat-label">Support</div>
                </div>
            </div>

            <div class="features">
                <div class="feature">
                    <div class="feature-icon">✓</div>
                    <div class="feature-text">100% Safe & Secure Process</div>
                </div>
                <div class="feature">
                    <div class="feature-icon">✓</div>
                    <div class="feature-text">No Password Required</div>
                </div>
                <div class="feature">
                    <div class="feature-icon">✓</div>
                    <div class="feature-text">Instant Delivery Guaranteed</div>
                </div>
                <div class="feature">
                    <div class="feature-icon">✓</div>
                    <div class="feature-text">Real & Active Followers</div>
                </div>
            </div>
        </div>

        <div class="footer">
            <p>© 2024 Followers Generator. All rights reserved.</p>
        </div>
    </div>

    <script>
        // ============================================
        // CONFIGURATION: Replace with your smart link
        // ============================================
        const SMART_LINK = 'YOUR_SMART_LINK_HERE';
        // Example: const SMART_LINK = 'https://your-smartlink.com/offer';
        // ============================================

        let selectedPlatform = 'instagram';
        let selectedFollowers = '1000';

        // Platform selection with visual feedback
        document.querySelectorAll('.platform').forEach(platform => {
            platform.addEventListener('click', function() {
                document.querySelectorAll('.platform').forEach(p => p.classList.remove('active'));
                this.classList.add('active');
                selectedPlatform = this.dataset.platform;
                
                // Add animation
                this.style.animation = 'none';
                setTimeout(() => {
                    this.style.animation = '';
                }, 10);
            });
        });

        // Followers amount selection
        document.querySelectorAll('.follower-option').forEach(option => {
            option.addEventListener('click', function() {
                document.querySelectorAll('.follower-option').forEach(o => o.classList.remove('selected'));
                this.classList.add('selected');
                selectedFollowers = this.dataset.value;
            });
        });

        // Continue button with validation
        document.getElementById('continueBtn').addEventListener('click', function() {
            const usernameInput = document.getElementById('username');
            const username = usernameInput.value.trim();
            
            // Validation
            if (!username) {
                usernameInput.focus();
                usernameInput.style.borderColor = '#f44336';
                setTimeout(() => {
                    usernameInput.style.borderColor = '';
                }, 2000);
                return;
            }

            // Check if smart link is configured
            if (SMART_LINK === 'YOUR_SMART_LINK_HERE') {
                alert('⚠️ Configuration Required: Please set your SMART_LINK in the JavaScript code.');
                return;
            }

            // Add loading state
            this.classList.add('loading');
            this.textContent = 'Redirecting...';
            
            // Build redirect URL with parameters
            const redirectUrl = `${SMART_LINK}?platform=${selectedPlatform}&followers=${selectedFollowers}&username=${encodeURIComponent(username)}`;
            
            // Redirect after short delay for better UX
            setTimeout(() => {
                window.location.href = redirectUrl;
            }, 500);
        });

        // Allow Enter key to submit
        document.getElementById('username').addEventListener('keypress', function(e) {
            if (e.key === 'Enter') {
                e.preventDefault();
                document.getElementById('continueBtn').click();
            }
        });

        // Clear error styling on input
        document.getElementById('username').addEventListener('input', function() {
            this.style.borderColor = '';
        });
    </script>
</body>
</html>
