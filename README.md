
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Free Followers Generator - Instagram, TikTok & Facebook</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            padding: 20px;
            color: #333;
        }

        .container {
            max-width: 500px;
            margin: 0 auto;
            padding: 20px 0;
        }

        .header {
            text-align: center;
            margin-bottom: 30px;
            color: white;
        }

        .header h1 {
            font-size: 28px;
            font-weight: 700;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.2);
        }

        .header p {
            font-size: 16px;
            opacity: 0.95;
        }

        .card {
            background: white;
            border-radius: 20px;
            padding: 30px 25px;
            box-shadow: 0 20px 60px rgba(0,0,0,0.3);
            margin-bottom: 20px;
        }

        .social-platforms {
            display: flex;
            justify-content: space-around;
            margin-bottom: 30px;
            gap: 15px;
        }

        .platform {
            text-align: center;
            cursor: pointer;
            transition: transform 0.3s ease;
            flex: 1;
        }

        .platform:hover {
            transform: translateY(-5px);
        }

        .platform-icon {
            width: 70px;
            height: 70px;
            border-radius: 15px;
            margin-bottom: 10px;
            border: 3px solid transparent;
            transition: all 0.3s ease;
            object-fit: cover;
        }

        .platform.active .platform-icon {
            border-color: #667eea;
            box-shadow: 0 5px 15px rgba(102, 126, 234, 0.4);
        }

        .platform-name {
            font-size: 14px;
            font-weight: 600;
            color: #666;
        }

        .platform.active .platform-name {
            color: #667eea;
        }

        .form-section {
            margin-bottom: 25px;
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
            padding: 15px;
            border: 2px solid #e0e0e0;
            border-radius: 10px;
            font-size: 16px;
            transition: border-color 0.3s ease;
            outline: none;
        }

        input[type="text"]:focus {
            border-color: #667eea;
        }

        .followers-selector {
            display: flex;
            gap: 10px;
            margin-top: 10px;
        }

        .follower-option {
            flex: 1;
            padding: 12px;
            border: 2px solid #e0e0e0;
            border-radius: 10px;
            text-align: center;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: 600;
            background: white;
        }

        .follower-option:hover {
            border-color: #667eea;
        }

        .follower-option.selected {
            background: #667eea;
            color: white;
            border-color: #667eea;
        }

        .submit-btn {
            width: 100%;
            padding: 18px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            border: none;
            border-radius: 10px;
            font-size: 18px;
            font-weight: 700;
            cursor: pointer;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            margin-top: 20px;
        }

        .submit-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 25px rgba(102, 126, 234, 0.4);
        }

        .submit-btn:active {
            transform: translateY(0);
        }

        .submit-btn:disabled {
            opacity: 0.6;
            cursor: not-allowed;
            transform: none;
        }

        .features {
            display: grid;
            gap: 15px;
            margin-top: 20px;
        }

        .feature {
            display: flex;
            align-items: center;
            gap: 12px;
            padding: 15px;
            background: #f8f9fa;
            border-radius: 10px;
        }

        .feature-icon {
            width: 24px;
            height: 24px;
            background: #667eea;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: bold;
            flex-shrink: 0;
            font-size: 14px;
        }

        .feature-text {
            font-size: 14px;
            color: #666;
        }

        .info-box {
            background: #e7f3ff;
            border: 2px solid #2196F3;
            border-radius: 10px;
            padding: 15px;
            margin-bottom: 20px;
            text-align: center;
        }

        .info-box p {
            margin: 0;
            color: #0d47a1;
            font-size: 14px;
            font-weight: 600;
        }

        .loading {
            display: none;
            text-align: center;
            margin-top: 15px;
        }

        .loading.active {
            display: block;
        }

        .spinner {
            border: 3px solid #f3f3f3;
            border-top: 3px solid #667eea;
            border-radius: 50%;
            width: 40px;
            height: 40px;
            animation: spin 1s linear infinite;
            margin: 0 auto 10px;
        }

        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        .loading-text {
            color: #667eea;
            font-weight: 600;
        }

        @media (max-width: 480px) {
            .header h1 {
                font-size: 24px;
            }
            
            .card {
                padding: 25px 20px;
            }
            
            .platform-icon {
                width: 60px;
                height: 60px;
            }
            
            .follower-option {
                font-size: 14px;
                padding: 10px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>🚀 Free Followers Generator</h1>
            <p>Boost your social media presence instantly!</p>
        </div>

        <div class="card">
            <div class="info-box">
                <p>📧 Complete verification on the next page to receive followers</p>
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
                <label for="username">Your Username</label>
                <input type="text" id="username" placeholder="Enter your username" required>
            </div>

            <div class="form-section">
                <label>Select Followers Amount</label>
                <div class="followers-selector">
                    <div class="follower-option selected" data-value="1000">1K</div>
                    <div class="follower-option" data-value="5000">5K</div>
                    <div class="follower-option" data-value="10000">10K</div>
                </div>
            </div>

            <button id="continueBtn" class="submit-btn">Continue to Get Followers →</button>

            <div id="loading" class="loading">
                <div class="spinner"></div>
                <p class="loading-text">Processing your request...</p>
            </div>
        </div>

        <div class="card">
            <div class="features">
                <div class="feature">
                    <div class="feature-icon">✓</div>
                    <div class="feature-text">100% Safe & Secure</div>
                </div>
                <div class="feature">
                    <div class="feature-icon">✓</div>
                    <div class="feature-text">No Password Required</div>
                </div>
                <div class="feature">
                    <div class="feature-icon">✓</div>
                    <div class="feature-text">Instant Delivery</div>
                </div>
                <div class="feature">
                    <div class="feature-icon">✓</div>
                    <div class="feature-text">24/7 Support Available</div>
                </div>
            </div>
        </div>
    </div>

    <script>
        const SMART_LINK = 'https://singingfiles.com/show.php?l=0&u=2467326&id=72846';

        let selectedPlatform = 'instagram';
        let selectedFollowers = '1000';

        // Platform selection
        document.querySelectorAll('.platform').forEach(platform => {
            platform.addEventListener('click', function() {
                document.querySelectorAll('.platform').forEach(p => p.classList.remove('active'));
                this.classList.add('active');
                selectedPlatform = this.dataset.platform;
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

        // Continue button click
        document.getElementById('continueBtn').addEventListener('click', function() {
            const username = document.getElementById('username').value.trim();
            const btn = document.getElementById('continueBtn');
            const loading = document.getElementById('loading');
            
            if (!username) {
                alert('Please enter your username');
                document.getElementById('username').focus();
                return;
            }
            
            // Show loading state
            btn.disabled = true;
            btn.textContent = 'Please wait...';
            loading.classList.add('active');
            
            // Redirect to smart link after a brief delay
            setTimeout(() => {
                window.location.href = SMART_LINK;
            }, 1500);
        });

        // Allow Enter key to submit
        document.getElementById('username').addEventListener('keypress', function(e) {
            if (e.key === 'Enter') {
                document.getElementById('continueBtn').click();
            }
        });
    </script>
</body>
</html>
