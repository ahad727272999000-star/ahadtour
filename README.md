<!DOCTYPE html>
<html lang="bn">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AHAD TOUR - গেমিং প্ল্যাটফর্ম</title>
    
    <!-- ফেভিকন (ব্রাউজার আইকন) -->
    <link rel="icon" type="image/png" href="logo.png">
    
    <link href="https://fonts.googleapis.com/css2?family=Hind+Siliguri:wght@400;500;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        /* টাইলস ব্যাকগ্রাউন্ড */
        body {
            background-image: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" width="100" height="100"><rect width="100" height="100" fill="%230f172a"/><circle cx="20" cy="20" r="4" fill="%232563eb" opacity="0.3"/><circle cx="80" cy="40" r="3" fill="%2310b981" opacity="0.3"/><circle cx="40" cy="80" r="5" fill="%23a855f7" opacity="0.3"/><circle cx="70" cy="70" r="2" fill="%23f97316" opacity="0.3"/><path d="M10 90 L20 80 L30 90" stroke="%233b82f6" stroke-width="1" fill="none" opacity="0.2"/><path d="M90 10 L80 20 L90 30" stroke="%23f87171" stroke-width="1" fill="none" opacity="0.2"/></svg>');
            background-repeat: repeat;
            background-size: 100px 100px;
        }
        
        :root {
            --bg-color: #050b1a;
            --card-bg: rgba(255, 255, 255, 0.05);
            --primary-blue: #2563eb;
            --glow-blue: #3b82f6;
            --text-white: #ffffff;
            --text-gray: #cbd5e1;
            --card-1-color: #3b82f6;
            --card-2-color: #10b981;
            --card-3-color: #a855f7;
            --card-4-color: #f97316;
            --red-accent: #f87171;
            --yellow-accent: #fbbf24;
            --whatsapp-color: #25D366;
            --facebook-color: #1877f2;
            --telegram-color: #0088cc;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Hind Siliguri', sans-serif;
        }

        body {
            background: linear-gradient(180deg, #0f172a 0%, #020617 100%);
            color: var(--text-white);
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 20px;
        }

        /* লোগো সেকশন */
        .header {
            text-align: center;
            margin-top: 40px;
            margin-bottom: 30px;
        }

        .logo-box {
            width: 120px;
            height: 120px;
            background: linear-gradient(135deg, #1e293b, #0f172a);
            border-radius: 25px;
            margin: 0 auto 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 0 30px rgba(59, 130, 246, 0.5);
            border: 2px solid rgba(255, 255, 255, 0.1);
            overflow: hidden;
        }

        .logo-box img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .subtitle-sm {
            color: var(--text-gray);
            font-size: 14px;
            margin-bottom: 5px;
        }

        .main-title {
            font-size: 24px;
            font-weight: 700;
            margin-bottom: 15px;
            background: linear-gradient(to right, #60a5fa, #ffffff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .tagline {
            color: var(--text-gray);
            font-size: 14px;
            display: flex;
            gap: 10px;
            justify-content: center;
            align-items: center;
        }

        /* ডাউনলোড বাটন */
        .download-btn {
            background: linear-gradient(90deg, #2563eb, #1d4ed8);
            color: white;
            border: none;
            padding: 15px 30px;
            border-radius: 12px;
            font-size: 16px;
            font-weight: 600;
            width: 100%;
            max-width: 350px;
            margin: 30px 0;
            cursor: pointer;
            box-shadow: 0 4px 20px rgba(37, 99, 235, 0.4);
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            transition: transform 0.2s;
            text-decoration: none;
        }

        .download-btn:active {
            transform: scale(0.98);
        }

        /* গ্রিড লেআউট */
        .stats-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 15px;
            width: 100%;
            max-width: 380px;
        }

        /* কার্ড ডিজাইন */
        .card {
            background: linear-gradient(180deg, rgba(255,255,255,0.05) 0%, rgba(255,255,255,0.02) 100%);
            border-radius: 20px;
            padding: 20px 15px;
            text-align: center;
            position: relative;
            overflow: hidden;
            border: 1px solid rgba(255, 255, 255, 0.05);
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            min-height: 140px;
        }

        .icon-bg {
            width: 50px;
            height: 50px;
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 20px;
            margin-bottom: 15px;
            position: relative;
        }

        .card h3 {
            font-size: 18px;
            font-weight: 700;
            margin-bottom: 5px;
        }

        .card p {
            font-size: 12px;
            color: var(--text-gray);
            font-weight: 500;
        }

        .card-1 .icon-bg { background: rgba(59, 130, 246, 0.2); color: var(--card-1-color); }
        .card-1::before { content:''; position: absolute; top: 10px; right: 10px; width: 6px; height: 6px; background: var(--card-1-color); border-radius: 50%; box-shadow: 0 0 10px var(--card-1-color); }

        .card-2 .icon-bg { background: rgba(16, 185, 129, 0.2); color: var(--card-2-color); }
        .card-2::before { content:''; position: absolute; top: 10px; right: 10px; width: 6px; height: 6px; background: var(--card-2-color); border-radius: 50%; box-shadow: 0 0 10px var(--card-2-color); }

        .card-3 .icon-bg { background: rgba(168, 85, 247, 0.2); color: var(--card-3-color); }
        .card-3::before { content:''; position: absolute; top: 10px; right: 10px; width: 6px; height: 6px; background: var(--card-3-color); border-radius: 50%; box-shadow: 0 0 10px var(--card-3-color); }

        .card-4 .icon-bg { background: rgba(249, 115, 22, 0.2); color: var(--card-4-color); }
        .card-4::before { content:''; position: absolute; top: 10px; right: 10px; width: 6px; height: 6px; background: var(--card-4-color); border-radius: 50%; box-shadow: 0 0 10px var(--card-4-color); }

        .features-section { 
            width: 100%; 
            max-width: 400px; 
            padding: 0 0 50px; 
        }

        .features-header { 
            text-align: center; 
            margin-top: 30px;
            margin-bottom: 30px; 
        }
        .features-header h2 { 
            font-size: 24px; 
            font-weight: 700; 
            margin-bottom: 10px; 
            line-height: 1.3; 
        }
        .features-header p { 
            color: var(--text-gray); 
            font-size: 14px; 
            font-weight: 500; 
        }

        .feature-card {
            background: linear-gradient(180deg, rgba(255,255,255,0.05) 0%, rgba(255,255,255,0.02) 100%);
            border-radius: 16px;
            padding: 30px 20px;
            margin-bottom: 20px;
            border: 1px solid rgba(255, 255, 255, 0.05);
            text-align: left;
            position: relative;
        }

        .feature-card .icon-large {
            width: 65px; 
            height: 65px; 
            border-radius: 16px;
            display: flex; 
            align-items: center; 
            justify-content: center;
            font-size: 30px; 
            margin-bottom: 15px; 
            box-shadow: 0 4px 15px rgba(0,0,0,0.2);
        }

        .feature-card h3 { 
            font-size: 19px; 
            font-weight: 700; 
            margin-bottom: 4px; 
        }
        .feature-card p { 
            color: var(--text-gray); 
            font-size: 14px; 
        }

        .card-deposit .icon-large { background: rgba(248, 113, 113, 0.15); color: var(--red-accent); }
        .card-deposit::before { content:''; position: absolute; top: 12px; right: 12px; width: 6px; height: 6px; background: var(--red-accent); border-radius: 50%; box-shadow: 0 0 8px var(--red-accent); }

        .card-withdraw .icon-large { background: rgba(16, 185, 129, 0.15); color: var(--card-2-color); }
        .card-withdraw::before { content:''; position: absolute; top: 12px; right: 12px; width: 6px; height: 6px; background: var(--card-2-color); border-radius: 50%; box-shadow: 0 0 8px var(--card-2-color); }

        .card-secure .icon-large { background: rgba(59, 130, 246, 0.15); color: var(--card-1-color); }
        .card-secure::before { content:''; position: absolute; top: 12px; right: 12px; width: 6px; height: 6px; background: var(--card-1-color); border-radius: 50%; box-shadow: 0 0 8px var(--card-1-color); }

        .card-rewards .icon-large { background: rgba(251, 191, 36, 0.15); color: var(--yellow-accent); }
        .card-rewards::before { content:''; position: absolute; top: 12px; right: 12px; width: 6px; height: 6px; background: var(--yellow-accent); border-radius: 50%; box-shadow: 0 0 8px var(--yellow-accent); }

        .final-cta-text { 
            font-size: 18px; 
            font-weight: 500; 
            margin-bottom: 20px; 
            text-align: center; 
        }
        .final-cta-btn {
            background: linear-gradient(180deg, #3b82f6 0%, #1d4ed8 100%); 
            padding: 18px 0;
            border-radius: 14px; 
            text-decoration: none; 
            color: white; 
            font-size: 17px; 
            font-weight: 600;
            border-top: 1px solid rgba(255,255,255,0.3); 
            border-bottom: 2px solid rgba(0,0,0,0.3);
            box-shadow: 0 10px 30px -5px rgba(37, 99, 235, 0.6);
            width: 100%; 
            max-width: 380px; 
            display: flex; 
            align-items: center; 
            justify-content: center; 
            gap: 12px;
            transition: transform 0.2s;
        }

        .community-section {
            width: 100%;
            max-width: 400px;
            padding: 60px 20px 40px;
            text-align: center;
        }

        .community-section h2 {
            font-size: 26px;
            font-weight: 700;
            margin-bottom: 30px;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 25px;
            margin-bottom: 50px;
            flex-wrap: wrap;
        }

        .social-link {
            text-decoration: none;
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 8px;
        }

        .social-link i {
            font-size: 30px;
            width: 60px;
            height: 60px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: transform 0.2s;
            box-shadow: 0 4px 15px rgba(0,0,0,0.3);
        }

        .social-link span {
            font-size: 12px;
            color: var(--text-gray);
        }

        .social-link:hover i {
            transform: scale(1.1);
        }

        .whatsapp-icon {
            background: rgba(37, 211, 102, 0.15);
            color: var(--whatsapp-color);
            border: 1px solid rgba(37, 211, 102, 0.3);
        }

        .facebook-icon {
            background: rgba(24, 119, 242, 0.15);
            color: var(--facebook-color);
            border: 1px solid rgba(24, 119, 242, 0.3);
        }

        .telegram-icon {
            background: rgba(0, 136, 204, 0.15);
            color: var(--telegram-color);
            border: 1px solid rgba(0, 136, 204, 0.3);
        }

        .footer-logo-info {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 15px;
            margin-bottom: 25px;
        }

        .footer-logo-box {
            width: 70px;
            height: 70px;
            border-radius: 15px;
            background: linear-gradient(135deg, #1e293b, #0f172a);
            box-shadow: 0 0 20px rgba(59, 130, 246, 0.5);
            border: 2px solid rgba(255, 255, 255, 0.1);
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
        }
        .footer-logo-box img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .app-name {
            font-size: 24px;
            font-weight: 700;
            background: linear-gradient(to right, #60a5fa, #ffffff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .footer-contact {
            margin: 30px 0 20px;
            padding: 20px;
            background: rgba(255, 255, 255, 0.03);
            border-radius: 16px;
            border: 1px solid rgba(255, 255, 255, 0.05);
        }

        .contact-item {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            margin-bottom: 15px;
            color: var(--text-gray);
        }

        .contact-item i {
            color: var(--glow-blue);
            width: 20px;
        }

        .contact-item a {
            color: var(--text-white);
            text-decoration: none;
            transition: color 0.2s;
        }

        .contact-item a:hover {
            color: var(--glow-blue);
        }

        .copyright-text {
            font-size: 13px;
            color: var(--text-gray);
            font-weight: 400;
            margin-top: 20px;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }
        .copyright-text a {
            color: var(--glow-blue);
            text-decoration: none;
            font-weight: 500;
        }

        .developer-badge {
            display: inline-block;
            background: rgba(59, 130, 246, 0.1);
            padding: 5px 15px;
            border-radius: 20px;
            font-size: 12px;
            border: 1px solid rgba(59, 130, 246, 0.3);
            margin-bottom: 15px;
        }
    </style>
</head>
<body>

    <header class="header">
        <!-- হেডারে লোগো -->
        <div class="logo-box">
            <img src="https://i.ibb.co/N613QM73/IMG-20260829-072031-886.jpg" alt="AHAD TOUR LOGO">
        </div>
        <p class="subtitle-sm">বাংলাদেশের</p>
        <h1 class="main-title">#১ গেমিং প্ল্যাটফর্ম</h1>
        <div class="tagline">
            <span>খেলুন</span> • <span>জিতুন</span> • <span>উপভোগ করুন</span>
        </div>
        
        <!-- এখানে তোর অ্যাপের ডাউনলোড লিংক বসাবি -->
        <a href="ahad" class="download-btn" target="_blank">
            <i class="fa-solid fa-download"></i>
            অ্যাপ ডাউনলোড করুন
        </a>
    </header>

    <div class="stats-grid">
        <div class="card card-1">
            <div class="icon-bg">
                <i class="fa-solid fa-download"></i>
            </div>
            <h3>৩০হাজার+</h3>
            <p>Downloads</p>
        </div>

        <div class="card card-2">
            <div class="icon-bg">
                <i class="fa-solid fa-users"></i>
            </div>
            <h3>১০হাজার+</h3>
            <p>Regular Players</p>
        </div>

        <div class="card card-3">
            <div class="icon-bg">
                <i class="fa-regular fa-star"></i>
            </div>
            <h3>24/7</h3>
            <p>Support</p>
        </div>

        <div class="card card-4">
            <div class="icon-bg">
                <i class="fa-solid fa-trophy"></i>
            </div>
            <h3>6+</h3>
            <p>Games & Modes</p>
        </div>
    </div>

    <section class="features-section">
        <div class="features-header">
            <h2>কেন আমাদের প্ল্যাটফর্ম বেছে নিবেন?</h2>
            <p>বাংলাদেশের সবচেয়ে বিশ্বস্ত এবং নিরাপদ গেমিং প্ল্যাটফর্ম</p>
        </div>
        
        <div class="feature-card card-deposit">
            <div class="icon-large">
                <i class="fa-regular fa-credit-card"></i>
            </div>
            <h3>Instant Deposits</h3>
            <p>Deposit money instantly and start playing</p>
        </div>
        
        <div class="feature-card card-withdraw">
            <div class="icon-large">
                <i class="fa-solid fa-wallet"></i>
            </div>
            <h3>Instant Withdrawal</h3>
            <p>Withdraw your winnings immediately without any delay</p>
        </div>
        
        <div class="feature-card card-secure">
            <div class="icon-large">
                <i class="fa-solid fa-shield-halved"></i>
            </div>
            <h3>Secure and Safe</h3>
            <p>Your money is safe with us</p>
        </div>
        
        <div class="feature-card card-rewards">
            <div class="icon-large">
                <i class="fa-solid fa-medal"></i>
            </div>
            <h3>Best Rewards</h3>
            <p>Get the best rewards for your performance</p>
        </div>

        <p class="final-cta-text">Download now and start playing!</p>
        
        <!-- এখানে তোর অ্যাপের ডাউনলোড লিংক বসাবি -->
        <a href="https://upload.app/api/download?sha256=951c121c6f7db851fb7a315a2979483ac1d22522d3fedc40382050b19cc626a5&download_id=upload_29bb9349-cf75-4a52-a384-3cffa661fdfa&token=74d15eb702d542b13e4da77bfd5d58056a94113f" class="final-cta-btn" target="_blank">
            <i class="fa-solid fa-download"></i>
            Download App
        </a>
    </section>

    <section class="community-section">
        <h2>Our Community</h2>

        <div class="social-links">
            <!-- এখানে তোর ওয়াটসঅ্যাপ গ্রুপের লিংক বসাবি -->
            <a href="https://t.me/AhAD_TeAM1" class="social-link" target="_blank">
                <i class="fab fa-whatsapp whatsapp-icon"></i>
                <span>WhatsApp</span>
            </a>
            <!-- এখানে তোর ফেসবুক গ্রুপ/পেজের লিংক বসাবি -->
            <a href="https://t.me/AhAD_TeAM1" class="social-link" target="_blank">
                <i class="fab fa-facebook-f facebook-icon"></i>
                <span>Facebook</span>
            </a>
            <!-- এখানে তোর টেলিগ্রাম গ্রুপের লিংক বসাবি -->
            <a href="https://t.me/AhAD_TeAM1" class="social-link" target="_blank">
                <i class="fab fa-telegram-plane telegram-icon"></i>
                <span>Telegram</span>
            </a>
        </div>

        <div class="footer-logo-info">
            <!-- ফুটারে লোগো -->
            <div class="footer-logo-box">
                <img src="https://i.ibb.co/N613QM73/IMG-20260829-072031-886.jpg" alt="LOGOAHAD">
            </div>
            <span class="app-name">AHAD TOUR</span>
        </div>

        <div class="footer-contact">
            <div class="developer-badge">
                <i class="fa-solid fa-code"></i> Official App
            </div>
            <div class="contact-item">
                <i class="fa-solid fa-envelope"></i>
                <!-- এখানে তোর ইমেইল বসাবি -->
                <a href="mailto:support@ahad.fun">support@iasantour.fun</a>
            </div>
            <div class="contact-item">
                <i class="fa-solid fa-phone"></i>
     
