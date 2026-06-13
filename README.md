# Tigerke5615M.github.io
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Super AI - Build Your Own AI Platform | Better Than Claude & GPT-4</title>
    <meta name="description" content="Open-source AI platform. Build, train, and deploy custom AI models. RAG, web search, voice, mobile apps, and more.">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&family=JetBrains+Mono:wght@400;500;600&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* ========================================
           ALL CSS IN ONE PLACE
           ======================================== */
        :root {
            --primary: #6366f1;
            --primary-dark: #4f46e5;
            --primary-light: #818cf8;
            --secondary: #ec4899;
            --accent: #14b8a6;
            --success: #10b981;
            --warning: #f59e0b;
            --error: #ef4444;
            --bg-primary: #ffffff;
            --bg-secondary: #f9fafb;
            --bg-tertiary: #f3f4f6;
            --bg-dark: #0f172a;
            --bg-darker: #020617;
            --text-primary: #0f172a;
            --text-secondary: #475569;
            --text-tertiary: #94a3b8;
            --text-light: #cbd5e1;
            --gradient-primary: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            --gradient-secondary: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
            --gradient-ai: linear-gradient(135deg, #667eea 0%, #764ba2 50%, #f093fb 100%);
            --shadow-sm: 0 1px 2px 0 rgba(0, 0, 0, 0.05);
            --shadow-md: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
            --shadow-lg: 0 10px 15px -3px rgba(0, 0, 0, 0.1);
            --shadow-xl: 0 20px 25px -5px rgba(0, 0, 0, 0.1);
            --shadow-2xl: 0 25px 50px -12px rgba(0, 0, 0, 0.25);
            --shadow-glow: 0 0 50px rgba(99, 102, 241, 0.5);
            --transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }
        html { scroll-behavior: smooth; }
        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
            line-height: 1.6;
            color: var(--text-primary);
            background: var(--bg-primary);
            overflow-x: hidden;
            -webkit-font-smoothing: antialiased;
        }
        .container { max-width: 1280px; margin: 0 auto; padding: 0 24px; }
        h1, h2, h3, h4, h5, h6 { font-weight: 800; line-height: 1.2; letter-spacing: -0.02em; }
        
        .gradient-text {
            background: var(--gradient-ai);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            background-size: 200% 200%;
            animation: gradient-shift 3s ease infinite;
        }
        @keyframes gradient-shift {
            0%, 100% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
        }
        ::-webkit-scrollbar { width: 10px; }
        ::-webkit-scrollbar-track { background: var(--bg-secondary); }
        ::-webkit-scrollbar-thumb { background: var(--gradient-primary); border-radius: 10px; }

        /* NAVIGATION */
        .navbar {
            position: fixed; top: 0; left: 0; right: 0;
            background: rgba(255, 255, 255, 0.8);
            backdrop-filter: blur(20px);
            -webkit-backdrop-filter: blur(20px);
            border-bottom: 1px solid rgba(0, 0, 0, 0.05);
            z-index: 1000;
            transition: var(--transition);
        }
        .navbar.scrolled { background: rgba(255, 255, 255, 0.95); box-shadow: var(--shadow-md); }
        .navbar .container {
            display: flex; align-items: center; justify-content: space-between; height: 80px;
        }
        .nav-brand { display: flex; align-items: center; gap: 8px; font-size: 24px; font-weight: 800; cursor: pointer; }
        .logo-icon { font-size: 32px; animation: float 3s ease-in-out infinite; }
        @keyframes float { 0%, 100% { transform: translateY(0); } 50% { transform: translateY(-5px); } }
        .nav-menu { display: flex; list-style: none; gap: 40px; }
        .nav-menu a {
            color: var(--text-secondary); text-decoration: none; font-weight: 500;
            font-size: 15px; transition: var(--transition); position: relative;
        }
        .nav-menu a:hover { color: var(--text-primary); }
        .nav-menu a::after {
            content: ''; position: absolute; bottom: -5px; left: 0; width: 0; height: 2px;
            background: var(--gradient-primary); transition: width 0.3s;
        }
        .nav-menu a:hover::after { width: 100%; }
        .nav-actions { display: flex; gap: 12px; align-items: center; }
        .nav-toggle { display: none; background: none; border: none; font-size: 24px; cursor: pointer; }

        /* BUTTONS */
        .btn {
            display: inline-flex; align-items: center; justify-content: center; gap: 8px;
            padding: 12px 24px; border-radius: 12px; font-weight: 600; font-size: 15px;
            text-decoration: none; border: none; cursor: pointer; transition: var(--transition);
            position: relative; overflow: hidden;
        }
        .btn-large { padding: 16px 32px; font-size: 16px; }
        .btn-block { width: 100%; }
        .btn-primary { background: var(--gradient-primary); color: white; box-shadow: 0 4px 14px rgba(99, 102, 241, 0.4); }
        .btn-primary:hover { transform: translateY(-2px); box-shadow: 0 8px 20px rgba(99, 102, 241, 0.5); }
        .btn-secondary { background: var(--bg-tertiary); color: var(--text-primary); }
        .btn-secondary:hover { background: var(--text-primary); color: white; transform: translateY(-2px); }
        .btn-ghost { background: transparent; color: var(--text-primary); }
        .btn-ghost:hover { background: var(--bg-tertiary); }
        .btn::before {
            content: ''; position: absolute; top: 0; left: -100%; width: 100%; height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.2), transparent);
            transition: left 0.5s;
        }
        .btn:hover::before { left: 100%; }

        /* HERO */
        .hero { position: relative; padding: 160px 0 80px; overflow: hidden; background: var(--bg-secondary); }
        .hero-bg { position: absolute; inset: 0; z-index: 0; }
        .grid-pattern {
            position: absolute; inset: 0;
            background-image: linear-gradient(rgba(99, 102, 241, 0.1) 1px, transparent 1px),
                              linear-gradient(90deg, rgba(99, 102, 241, 0.1) 1px, transparent 1px);
            background-size: 50px 50px;
            mask-image: radial-gradient(ellipse at center, black 30%, transparent 70%);
            -webkit-mask-image: radial-gradient(ellipse at center, black 30%, transparent 70%);
        }
        .gradient-orb {
            position: absolute; border-radius: 50%; filter: blur(80px); opacity: 0.5;
            animation: orb-float 20s ease-in-out infinite;
        }
        .orb-1 { width: 400px; height: 400px; background: #667eea; top: 10%; left: 10%; }
        .orb-2 { width: 300px; height: 300px; background: #f093fb; top: 50%; right: 10%; animation-delay: 5s; }
        .orb-3 { width: 350px; height: 350px; background: #4facfe; bottom: 10%; left: 40%; animation-delay: 10s; }
        @keyframes orb-float {
            0%, 100% { transform: translate(0, 0) scale(1); }
            33% { transform: translate(50px, -50px) scale(1.1); }
            66% { transform: translate(-50px, 50px) scale(0.9); }
        }
        .hero .container {
            position: relative; z-index: 1; display: grid; grid-template-columns: 1fr 1fr;
            gap: 60px; align-items: center;
        }
        .hero-content { animation: slide-up 1s ease-out; }
        @keyframes slide-up { from { opacity: 0; transform: translateY(30px); } to { opacity: 1; transform: translateY(0); } }
        .hero-badge {
            display: inline-flex; align-items: center; gap: 8px; padding: 8px 16px;
            background: white; border: 1px solid var(--bg-tertiary); border-radius: 100px;
            font-size: 14px; font-weight: 500; margin-bottom: 24px; box-shadow: var(--shadow-sm);
        }
        .pulse-dot {
            width: 8px; height: 8px; background: var(--success); border-radius: 50%;
            animation: pulse 2s ease-in-out infinite;
        }
        @keyframes pulse { 0%, 100% { opacity: 1; transform: scale(1); } 50% { opacity: 0.5; transform: scale(1.5); } }
        .hero-title { font-size: clamp(40px, 6vw, 72px); line-height: 1.1; margin-bottom: 24px; }
        .hero-subtitle { font-size: 20px; color: var(--text-secondary); margin-bottom: 40px; max-width: 600px; }
        .hero-actions { display: flex; gap: 16px; margin-bottom: 60px; flex-wrap: wrap; }
        .hero-stats {
            display: grid; grid-template-columns: repeat(4, 1fr); gap: 32px; padding-top: 40px;
            border-top: 1px solid rgba(0, 0, 0, 0.1);
        }
        .stat-value {
            font-size: 36px; font-weight: 800;
            background: var(--gradient-primary);
            -webkit-background-clip: text; -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        .stat-label { font-size: 14px; color: var(--text-tertiary); margin-top: 4px; }
        .hero-visual { position: relative; animation: slide-up 1s ease-out 0.3s backwards; }
        .code-window {
            background: #1e1e1e; border-radius: 16px; overflow: hidden;
            box-shadow: var(--shadow-2xl);
            transform: perspective(1000px) rotateY(-5deg) rotateX(5deg);
            transition: var(--transition);
        }
        .code-window:hover { transform: perspective(1000px) rotateY(0) rotateX(0); }
        .code-header {
            background: #2d2d2d; padding: 12px 16px; display: flex; align-items: center; gap: 12px;
        }
        .code-dots { display: flex; gap: 6px; }
        .dot { width: 12px; height: 12px; border-radius: 50%; }
        .dot.red { background: #ff5f57; } .dot.yellow { background: #febc2e; } .dot.green { background: #28c840; }
        .code-title { color: #999; font-size: 13px; margin-left: auto; }
        .code-content {
            padding: 24px; color: #d4d4d4; font-family: 'JetBrains Mono', monospace;
            font-size: 14px; line-height: 1.6; overflow-x: auto;
        }
        .code-content .comment { color: #6a9955; }
        .code-content .keyword { color: #c586c0; }
        .code-content .string { color: #ce9178; }
        .code-content .function { color: #dcdcaa; }
        .floating-card {
            position: absolute; background: white; padding: 12px 20px; border-radius: 12px;
            box-shadow: var(--shadow-lg); display: flex; align-items: center; gap: 8px;
            font-size: 14px; font-weight: 600; animation: float-card 3s ease-in-out infinite;
        }
        .floating-card i { color: var(--primary); }
        .card-1 { top: 10%; left: -20px; }
        .card-2 { top: 50%; right: -20px; animation-delay: 1s; }
        .card-3 { bottom: 10%; left: 20%; animation-delay: 2s; }
        @keyframes float-card { 0%, 100% { transform: translateY(0); } 50% { transform: translateY(-10px); } }

        /* TRUSTED */
        .trusted { padding: 60px 0; background: white; border-top: 1px solid var(--bg-tertiary); border-bottom: 1px solid var(--bg-tertiary); }
        .trusted-label { text-align: center; color: var(--text-tertiary); font-size: 14px; margin-bottom: 32px; text-transform: uppercase; letter-spacing: 0.1em; }
        .trusted-logos { display: flex; justify-content: space-around; align-items: center; flex-wrap: wrap; gap: 40px; }
        .logo-item { font-size: 24px; font-weight: 700; color: var(--text-tertiary); opacity: 0.6; transition: var(--transition); }
        .logo-item:hover { opacity: 1; color: var(--text-primary); }

        /* SECTIONS */
        section { padding: 120px 0; }
        .section-header { text-align: center; max-width: 800px; margin: 0 auto 80px; }
        .section-badge {
            display: inline-block; padding: 6px 16px; background: var(--bg-tertiary);
            color: var(--primary); border-radius: 100px; font-size: 12px; font-weight: 700;
            letter-spacing: 0.1em; margin-bottom: 16px;
        }
        .section-title { font-size: clamp(32px, 5vw, 56px); margin-bottom: 16px; }
        .section-subtitle { font-size: 20px; color: var(--text-secondary); }

        /* FEATURES */
        .features { background: var(--bg-secondary); }
        .features-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 24px; }
        .feature-card {
            background: white; padding: 40px 32px; border-radius: 20px;
            border: 1px solid var(--bg-tertiary); transition: var(--transition);
            cursor: pointer; position: relative; overflow: hidden;
        }
        .feature-card::before {
            content: ''; position: absolute; top: 0; left: 0; right: 0; height: 4px;
            background: var(--gradient-primary); transform: scaleX(0);
            transform-origin: left; transition: transform 0.3s;
        }
        .feature-card:hover { transform: translateY(-5px); box-shadow: var(--shadow-xl); border-color: var(--primary-light); }
        .feature-card:hover::before { transform: scaleX(1); }
        .feature-icon {
            width: 56px; height: 56px; border-radius: 14px; background: var(--gradient-primary);
            display: flex; align-items: center; justify-content: center;
            color: white; font-size: 24px; margin-bottom: 24px; transition: var(--transition);
        }
        .feature-card:hover .feature-icon { transform: scale(1.1) rotate(5deg); }
        .feature-card h3 { font-size: 20px; margin-bottom: 12px; }
        .feature-card p { color: var(--text-secondary); line-height: 1.6; }

        /* DEMO */
        .demo { background: var(--bg-dark); color: white; }
        .demo .section-title { color: white; }
        .demo .section-subtitle { color: var(--text-light); }
        .demo-container { max-width: 900px; margin: 0 auto; }
        .demo-window { background: #1a1a1a; border-radius: 20px; overflow: hidden; box-shadow: var(--shadow-2xl); }
        .demo-header { background: #2d2d2d; padding: 16px 20px; display: flex; align-items: center; gap: 12px; }
        .demo-title { color: #999; font-size: 14px; margin-left: auto; }
        .demo-body { height: 400px; overflow-y: auto; padding: 24px; display: flex; flex-direction: column; gap: 16px; }
        .message { display: flex; gap: 12px; animation: message-in 0.3s ease-out; }
        @keyframes message-in { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }
        .message-avatar {
            width: 40px; height: 40px; border-radius: 50%; background: var(--gradient-primary);
            display: flex; align-items: center; justify-content: center; font-size: 20px; flex-shrink: 0;
        }
        .message-content { background: #2d2d2d; padding: 12px 16px; border-radius: 12px; color: white; max-width: 70%; line-height: 1.5; white-space: pre-wrap; }
        .user-message { flex-direction: row-reverse; }
        .user-message .message-avatar { background: var(--gradient-secondary); }
        .user-message .message-content { background: var(--primary); }
        .demo-input { background: #2d2d2d; padding: 16px; display: flex; gap: 12px; border-top: 1px solid #1a1a1a; }
        .demo-input input { flex: 1; background: #1a1a1a; border: none; color: white; padding: 12px 16px; border-radius: 12px; font-size: 15px; outline: none; }
        .demo-input input::placeholder { color: #666; }
        .demo-input button {
            width: 48px; height: 48px; background: var(--gradient-primary); color: white;
            border: none; border-radius: 12px; cursor: pointer; transition: var(--transition);
        }
        .demo-input button:hover { transform: scale(1.05); }

        /* HOW IT WORKS */
        .how-it-works { background: white; }
        .steps { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 40px; }
        .step { text-align: center; position: relative; }
        .step-number {
            width: 80px; height: 80px; border-radius: 50%; background: var(--gradient-primary);
            color: white; font-size: 32px; font-weight: 800; display: flex; align-items: center;
            justify-content: center; margin: 0 auto 24px; box-shadow: var(--shadow-glow);
            animation: pulse-glow 2s ease-in-out infinite;
        }
        @keyframes pulse-glow { 0%, 100% { box-shadow: 0 0 50px rgba(99, 102, 241, 0.5); } 50% { box-shadow: 0 0 80px rgba(99, 102, 241, 0.8); } }
        .step h3 { font-size: 24px; margin-bottom: 12px; }
        .step p { color: var(--text-secondary); margin-bottom: 20px; }
        .step-code { background: #1e1e1e; color: #ce9178; padding: 12px 20px; border-radius: 8px; font-family: 'JetBrains Mono', monospace; display: inline-block; }

        /* COMPARISON */
        .comparison { background: var(--bg-secondary); }
        .comparison-table { background: white; border-radius: 20px; overflow: hidden; box-shadow: var(--shadow-lg); }
        .comparison-row { display: grid; grid-template-columns: 2fr 1fr 1fr 1fr 1fr; padding: 20px; border-bottom: 1px solid var(--bg-tertiary); align-items: center; }
        .comparison-row.header { background: var(--bg-dark); color: white; font-weight: 700; }
        .comparison-row.header .highlight { background: var(--gradient-primary); padding: 8px 12px; border-radius: 8px; }
        .comparison-row:last-child { border-bottom: none; }
        .check { color: var(--success); font-size: 20px; }
        .cross { color: var(--error); font-size: 20px; }
        .partial { color: var(--warning); font-size: 20px; }

        /* PRICING */
        .pricing { background: var(--bg-secondary); }
        .pricing-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 24px; max-width: 1100px; margin: 0 auto; }
        .pricing-card { background: white; padding: 40px 32px; border-radius: 20px; border: 2px solid var(--bg-tertiary); transition: var(--transition); position: relative; }
        .pricing-card:hover { transform: translateY(-5px); border-color: var(--primary); box-shadow: var(--shadow-xl); }
        .pricing-card.popular { border-color: var(--primary); background: linear-gradient(180deg, white 0%, #f0f4ff 100%); transform: scale(1.05); }
        .popular-badge { position: absolute; top: -12px; left: 50%; transform: translateX(-50%); background: var(--gradient-primary); color: white; padding: 6px 16px; border-radius: 100px; font-size: 12px; font-weight: 700; letter-spacing: 0.05em; }
        .pricing-card h3 { font-size: 24px; margin-bottom: 16px; }
        .price { display: flex; align-items: baseline; margin-bottom: 32px; }
        .price-currency { font-size: 24px; font-weight: 600; color: var(--text-secondary); }
        .price-amount { font-size: 56px; font-weight: 800; background: var(--gradient-primary); -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text; }
        .price-period { color: var(--text-tertiary); font-size: 16px; margin-left: 8px; }
        .pricing-features { list-style: none; margin-bottom: 32px; }
        .pricing-features li { padding: 8px 0; color: var(--text-secondary); display: flex; align-items: center; gap: 12px; }
        .pricing-features i { color: var(--success); font-size: 14px; }

        /* TESTIMONIALS */
        .testimonials { background: white; }
        .testimonials-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 24px; }
        .testimonial-card { background: var(--bg-secondary); padding: 32px; border-radius: 20px; transition: var(--transition); border: 1px solid transparent; }
        .testimonial-card:hover { background: white; border-color: var(--bg-tertiary); box-shadow: var(--shadow-lg); transform: translateY(-3px); }
        .testimonial-rating { color: #fbbf24; margin-bottom: 16px; }
        .testimonial-text { color: var(--text-primary); font-size: 16px; line-height: 1.6; margin-bottom: 24px; font-style: italic; }
        .testimonial-author { display: flex; align-items: center; gap: 12px; }
        .author-avatar { width: 48px; height: 48px; border-radius: 50%; background: var(--gradient-primary); color: white; display: flex; align-items: center; justify-content: center; font-weight: 700; }
        .author-name { font-weight: 600; }
        .author-role { font-size: 14px; color: var(--text-tertiary); }

        /* USE CASES */
        .use-cases { background: var(--bg-secondary); }
        .use-cases-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 24px; }
        .use-case { background: white; padding: 32px; border-radius: 20px; text-align: center; transition: var(--transition); }
        .use-case:hover { transform: translateY(-5px); box-shadow: var(--shadow-xl); }
        .use-case-icon { width: 80px; height: 80px; margin: 0 auto 20px; border-radius: 20px; background: var(--gradient-primary); display: flex; align-items: center; justify-content: center; color: white; font-size: 36px; }
        .use-case h3 { margin-bottom: 12px; font-size: 20px; }
        .use-case p { color: var(--text-secondary); }

        /* INTEGRATIONS */
        .integrations { background: white; }
        .integrations-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(140px, 1fr)); gap: 20px; }
        .integration-card { background: var(--bg-secondary); padding: 24px; border-radius: 16px; text-align: center; transition: var(--transition); cursor: pointer; }
        .integration-card:hover { background: var(--gradient-primary); color: white; transform: translateY(-3px); }
        .integration-card:hover .integration-name { color: white; }
        .integration-icon { font-size: 32px; margin-bottom: 12px; }
        .integration-name { font-size: 14px; font-weight: 600; color: var(--text-secondary); transition: var(--transition); }

        /* FAQ */
        .faq { background: var(--bg-secondary); }
        .faq-list { max-width: 800px; margin: 0 auto; }
        .faq-item { background: white; margin-bottom: 16px; border-radius: 16px; overflow: hidden; box-shadow: var(--shadow-sm); transition: var(--transition); }
        .faq-item:hover { box-shadow: var(--shadow-md); }
        .faq-question { padding: 24px; cursor: pointer; display: flex; justify-content: space-between; align-items: center; font-weight: 600; font-size: 18px; }
        .faq-question i { transition: transform 0.3s; color: var(--primary); }
        .faq-item.active .faq-question i { transform: rotate(180deg); }
        .faq-answer { max-height: 0; overflow: hidden; transition: max-height 0.3s ease, padding 0.3s ease; padding: 0 24px; color: var(--text-secondary); }
        .faq-item.active .faq-answer { max-height: 500px; padding: 0 24px 24px; }

        /* STATS BANNER */
        .stats-banner { background: var(--gradient-ai); color: white; padding: 60px 0; }
        .stats-banner-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 40px; text-align: center; }
        .stats-banner-stat .number { font-size: 48px; font-weight: 800; }
        .stats-banner-stat .label { font-size: 16px; opacity: 0.9; margin-top: 8px; }

        /* CTA */
        .cta { background: var(--bg-darker); color: white; text-align: center; position: relative; overflow: hidden; }
        .cta::before { content: ''; position: absolute; inset: 0; background: var(--gradient-ai); opacity: 0.3; animation: gradient-shift 10s ease infinite; background-size: 200% 200%; }
        .cta-content { position: relative; z-index: 1; }
        .cta h2 { font-size: clamp(32px, 5vw, 64px); margin-bottom: 16px; color: white; }
        .cta p { font-size: 20px; color: var(--text-light); margin-bottom: 40px; }
        .cta-actions { display: flex; gap: 16px; justify-content: center; flex-wrap: wrap; }

        /* NEWSLETTER */
        .newsletter { background: white; }
        .newsletter-container { max-width: 600px; margin: 0 auto; text-align: center; }
        .newsletter-form { display: flex; gap: 12px; margin-top: 32px; }
        .newsletter-input { flex: 1; padding: 16px 20px; border: 2px solid var(--bg-tertiary); border-radius: 12px; font-size: 16px; outline: none; transition: var(--transition); }
        .newsletter-input:focus { border-color: var(--primary); }

        /* FOOTER */
        .footer { background: var(--bg-darker); color: var(--text-light); padding: 80px 0 32px; }
        .footer-grid { display: grid; grid-template-columns: 2fr 1fr 1fr 1fr; gap: 60px; margin-bottom: 60px; }
        .footer-brand { display: flex; align-items: center; gap: 8px; font-size: 24px; font-weight: 800; margin-bottom: 16px; }
        .footer-col p { margin-bottom: 20px; color: var(--text-tertiary); max-width: 300px; }
        .social-links { display: flex; gap: 12px; }
        .social-links a { width: 40px; height: 40px; border-radius: 10px; background: rgba(255, 255, 255, 0.1); color: white; display: flex; align-items: center; justify-content: center; transition: var(--transition); text-decoration: none; }
        .social-links a:hover { background: var(--gradient-primary); transform: translateY(-3px); }
        .footer-col h4 { color: white; font-size: 16px; margin-bottom: 20px; }
        .footer-col ul { list-style: none; }
        .footer-col li { margin-bottom: 12px; }
        .footer-col a { color: var(--text-tertiary); text-decoration: none; transition: var(--transition); }
        .footer-col a:hover { color: white; }
        .footer-bottom { padding-top: 32px; border-top: 1px solid rgba(255, 255, 255, 0.1); text-align: center; color: var(--text-tertiary); font-size: 14px; }

        /* MODAL */
        .modal { display: none; position: fixed; inset: 0; background: rgba(0,0,0,0.7); z-index: 2000; align-items: center; justify-content: center; padding: 20px; }
        .modal.active { display: flex; }
        .modal-content { background: white; border-radius: 20px; padding: 40px; max-width: 500px; width: 100%; position: relative; animation: modal-in 0.3s ease-out; }
        @keyframes modal-in { from { opacity: 0; transform: scale(0.9); } to { opacity: 1; transform: scale(1); } }
        .modal-close { position: absolute; top: 20px; right: 20px; background: none; border: none; font-size: 24px; cursor: pointer; color: var(--text-tertiary); }
        .modal h2 { margin-bottom: 16px; }
        .modal p { color: var(--text-secondary); margin-bottom: 24px; }
        .modal-form { display: flex; flex-direction: column; gap: 12px; }
        .modal-form input, .modal-form textarea { padding: 12px 16px; border: 2px solid var(--bg-tertiary); border-radius: 10px; font-size: 15px; outline: none; font-family: inherit; }
        .modal-form input:focus, .modal-form textarea:focus { border-color: var(--primary); }
        .modal-form textarea { min-height: 100px; resize: vertical; }

        /* THEME TOGGLE */
        .theme-toggle { position: fixed; bottom: 30px; right: 30px; width: 50px; height: 50px; border-radius: 50%; background: var(--gradient-primary); color: white; border: none; cursor: pointer; font-size: 20px; box-shadow: var(--shadow-lg); z-index: 999; transition: var(--transition); }
        .theme-toggle:hover { transform: scale(1.1) rotate(15deg); }

        /* BACK TO TOP */
        .back-to-top { position: fixed; bottom: 30px; left: 30px; width: 50px; height: 50px; border-radius: 50%; background: var(--text-primary); color: white; border: none; cursor: pointer; font-size: 20px; box-shadow: var(--shadow-lg); z-index: 999; transition: var(--transition); opacity: 0; pointer-events: none; }
        .back-to-top.visible { opacity: 1; pointer-events: all; }
        .back-to-top:hover { transform: translateY(-3px); background: var(--gradient-primary); }

        /* DARK MODE */
        body.dark-mode { background: var(--bg-darker); color: white; }
        body.dark-mode .navbar { background: rgba(15, 23, 42, 0.9); }
        body.dark-mode .feature-card, body.dark-mode .pricing-card, body.dark-mode .testimonial-card, body.dark-mode .use-case, body.dark-mode .faq-item { background: var(--bg-dark); color: white; }
        body.dark-mode .section-subtitle, body.dark-mode .feature-card p, body.dark-mode .testimonial-text, body.dark-mode .faq-answer { color: var(--text-light); }
        body.dark-mode .hero, body.dark-mode .features, body.dark-mode .pricing, body.dark-mode .use-cases, body.dark-mode .integrations, body.dark-mode .faq, body.dark-mode .testimonials, body.dark-mode .newsletter, body.dark-mode .comparison, body.dark-mode .trusted, body.dark-mode .how-it-works { background: var(--bg-darker); }
        body.dark-mode .trusted, body.dark-mode .newsletter, body.dark-mode .testimonials, body.dark-mode .how-it-works, body.dark-mode .integrations { background: var(--bg-dark); }

        /* RESPONSIVE */
        @media (max-width: 1024px) {
            .hero .container { grid-template-columns: 1fr; text-align: center; }
            .hero-subtitle { margin-left: auto; margin-right: auto; }
            .hero-actions { justify-content: center; }
            .hero-stats { max-width: 600px; margin: 0 auto; }
            .footer-grid { grid-template-columns: 1fr 1fr; }
            .comparison-row { grid-template-columns: 2fr 1fr 1fr 1fr 1fr; font-size: 14px; }
        }
        @media (max-width: 768px) {
            .nav-menu, .nav-actions { display: none; }
            .nav-toggle { display: block; }
            .nav-menu.active { display: flex; position: absolute; top: 80px; left: 0; right: 0; background: white; flex-direction: column; padding: 20px; box-shadow: var(--shadow-md); }
            .hero { padding: 120px 0 60px; }
            .hero-stats { grid-template-columns: repeat(2, 1fr); }
            .section-header { margin-bottom: 60px; }
            .pricing-card.popular { transform: none; }
            .footer-grid { grid-template-columns: 1fr; gap: 40px; }
            .newsletter-form { flex-direction: column; }
            .comparison-row { grid-template-columns: 1fr; text-align: center; }
            .comparison-row > * { padding: 8px 0; }
            .comparison-row.header { display: none; }
        }
    </style>
</head>
<body>
    <!-- NAVIGATION -->
    <nav class="navbar" id="navbar">
        <div class="container">
            <div class="nav-brand" onclick="scrollToTop()">
                <span class="logo-icon">🧠</span>
                <span class="logo-text">Super<span class="gradient-text">AI</span></span>
            </div>
            <ul class="nav-menu" id="navMenu">
                <li><a href="#features">Features</a></li>
                <li><a href="#demo">Demo</a></li>
                <li><a href="#use-cases">Use Cases</a></li>
                <li><a href="#pricing">Pricing</a></li>
                <li><a href="#faq">FAQ</a></li>
                <li><a href="#" onclick="openModal('contactModal')">Contact</a></li>
            </ul>
            <div class="nav-actions">
                <a href="#" class="btn btn-ghost" onclick="openModal('loginModal')">Sign In</a>
                <a href="#" class="btn btn-primary" onclick="openModal('signupModal')">Get Started</a>
            </div>
            <button class="nav-toggle" id="navToggle" onclick="toggleMenu()">
                <i class="fas fa-bars"></i>
            </button>
        </div>
    </nav>

    <!-- HERO -->
    <section class="hero">
        <div class="hero-bg">
            <div class="grid-pattern"></div>
            <div class="gradient-orb orb-1"></div>
            <div class="gradient-orb orb-2"></div>
            <div class="gradient-orb orb-3"></div>
        </div>
        <div class="container">
            <div class="hero-content">
                <div class="hero-badge">
                    <span class="pulse-dot"></span>
                    <span>v2.0 Now Live — GPT-4 Class Performance</span>
                </div>
                <h1 class="hero-title">Build Your Own<br><span class="gradient-text">Super AI</span><br>In Minutes</h1>
                <p class="hero-subtitle">The complete open-source platform to build, train, and deploy custom AI models. Better than Claude, GPT-4, and Gemini — for free.</p>
                <div class="hero-actions">
                    <a href="#" class="btn btn-primary btn-large" onclick="openModal('signupModal')">
                        <i class="fas fa-rocket"></i> Start Building Free
                    </a>
                    <a href="#demo" class="btn btn-secondary btn-large">
                        <i class="fas fa-play"></i> Try Live Demo
                    </a>
                </div>
                <div class="hero-stats">
                    <div class="stat">
                        <div class="stat-value" data-target="50000">0</div>
                        <div class="stat-label">Developers</div>
                    </div>
                    <div class="stat">
                        <div class="stat-value" data-target="10000">0</div>
                        <div class="stat-label">Models Trained</div>
                    </div>
                    <div class="stat">
                        <div class="stat-value" data-target="99">0</div>
                        <div class="stat-label">% Uptime</div>
                    </div>
                    <div class="stat">
                        <div class="stat-value" data-target="20">0</div>
                        <div class="stat-label">Languages</div>
                    </div>
                </div>
            </div>
            <div class="hero-visual">
                <div class="code-window">
                    <div class="code-header">
                        <div class="code-dots">
                            <span class="dot red"></span><span class="dot yellow"></span><span class="dot green"></span>
                        </div>
                        <div class="code-title">main.py — super-ai</div>
                    </div>
                    <pre class="code-content"><code><span class="comment"># Build your AI in 3 lines</span>
<span class="keyword">from</span> super_ai <span class="keyword">import</span> SuperAI

ai = <span class="function">SuperAI</span>(<span class="string">"my-model"</span>)
response = ai.<span class="function">chat</span>(<span class="string">"Hello!"</span>)
<span class="keyword">print</span>(response)
<span class="comment"># 🧠 "Hi! How can I help you today?"</span>

<span class="comment"># Add knowledge base</span>
ai.<span class="function">add_knowledge</span>(<span class="string">"my_docs.pdf"</span>)

<span class="comment"># Enable web search</span>
ai.<span class="function">enable_web</span>()</code></pre>
                </div>
                <div class="floating-card card-1"><i class="fas fa-brain"></i> Training Complete</div>
                <div class="floating-card card-2"><i class="fas fa-check-circle"></i> 99.9% Accuracy</div>
                <div class="floating-card card-3"><i class="fas fa-bolt"></i> 3x Faster</div>
            </div>
        </div>
    </section>

    <!-- TRUSTED BY -->
    <section class="trusted">
        <div class="container">
            <p class="trusted-label">Trusted by 50,000+ developers and companies</p>
            <div class="trusted-logos">
                <div class="logo-item">Google</div>
                <div class="logo-item">Microsoft</div>
                <div class="logo-item">Meta</div>
                <div class="logo-item">Apple</div>
                <div class="logo-item">Amazon</div>
                <div class="logo-item">Netflix</div>
                <div class="logo-item">Tesla</div>
            </div>
        </div>
    </section>

    <!-- FEATURES -->
    <section class="features" id="features">
        <div class="container">
            <div class="section-header">
                <span class="section-badge">⚡ FEATURES</span>
                <h2 class="section-title">Everything you need to build <span class="gradient-text">production AI</span></h2>
                <p class="section-subtitle">A complete platform with all the tools, integrations, and infrastructure you need.</p>
            </div>
            <div class="features-grid">
                <div class="feature-card"><div class="feature-icon"><i class="fas fa-robot"></i></div><h3>Custom Model Training</h3><p>Train from scratch or fine-tune. Support for Llama, Mistral, Qwen, DeepSeek, and more.</p></div>
                <div class="feature-card"><div class="feature-icon"><i class="fas fa-database"></i></div><h3>RAG & Vector Search</h3><p>Add your own knowledge base. ChromaDB, FAISS, Pinecone, Weaviate support out of the box.</p></div>
                <div class="feature-card"><div class="feature-icon"><i class="fas fa-globe"></i></div><h3>Web Search Integration</h3><p>Real-time web search built-in. Your AI always has the latest information from the internet.</p></div>
                <div class="feature-card"><div class="feature-icon"><i class="fas fa-tools"></i></div><h3>Agent System</h3><p>Autonomous agents that execute code, browse the web, and use tools for complex tasks.</p></div>
                <div class="feature-card"><div class="feature-icon"><i class="fas fa-mobile-alt"></i></div><h3>Mobile Apps (iOS/Android)</h3><p>React Native apps included. Plus web UI, CLI, and REST API for everything.</p></div>
                <div class="feature-card"><div class="feature-icon"><i class="fas fa-language"></i></div><h3>20+ Languages</h3><p>Multi-language support. Chat in any language, get responses in any language.</p></div>
                <div class="feature-card"><div class="feature-icon"><i class="fas fa-microphone"></i></div><h3>Voice I/O (STT + TTS)</h3><p>Speech-to-text with Whisper. Text-to-speech with Edge TTS. Build voice assistants easily.</p></div>
                <div class="feature-card"><div class="feature-icon"><i class="fas fa-chart-line"></i></div><h3>Analytics Dashboard</h3><p>Real-time metrics, performance monitoring, and usage tracking with beautiful charts.</p></div>
                <div class="feature-card"><div class="feature-icon"><i class="fas fa-plug"></i></div><h3>Plugin System</h3><p>Extensible architecture. Add custom tools, integrations, and capabilities in minutes.</p></div>
                <div class="feature-card"><div class="feature-icon"><i class="fas fa-bell"></i></div><h3>Webhooks & Notifications</h3><p>Slack, Discord, Email, SMS, and custom webhook integrations with retry logic.</p></div>
                <div class="feature-card"><div class="feature-icon"><i class="fas fa-code-branch"></i></div><h3>Model Versioning (Git-like)</h3><p>Version control for models. Track, compare, rollback, and branch your AI models.</p></div>
                <div class="feature-card"><div class="feature-icon"><i class="fas fa-store"></i></div><h3>Model Marketplace</h3><p>Share and discover pre-trained models. One-click install from community.</p></div>
                <div class="feature-card"><div class="feature-icon"><i class="fas fa-search"></i></div><h3>Advanced Search & Filters</h3><p>Full-text search with faceting, filters, sorting, and fuzzy matching.</p></div>
                <div class="feature-card"><div class="feature-icon"><i class="fas fa-paint-brush"></i></div><h3>Custom Themes</h3><p>7+ built-in themes. Dark/light mode. Fully customizable. White-label ready.</p></div>
                <div class="feature-card"><div class="feature-icon"><i class="fas fa-shield-alt"></i></div><h3>Authentication & Security</h3><p>API keys, JWT tokens, rate limiting, role-based access control. Enterprise security.</p></div>
                <div class="feature-card"><div class="feature-icon"><i class="fab fa-docker"></i></div><h3>Docker & Cloud Deploy</h3><p>One-click deploy to AWS, GCP, Azure. Docker Compose included. Auto-scaling.</p></div>
                <div class="feature-card"><div class="feature-icon"><i class="fas fa-memory"></i></div><h3>Memory & Caching</h3><p>Redis-backed conversation memory. Smart caching for 10x faster responses.</p></div>
                <div class="feature-card"><div class="feature-icon"><i class="fas fa-file-code"></i></div><h3>Markdown & Code Render</h3><p>Syntax highlighting, math equations, tables, task lists, and footnotes support.</p></div>
            </div>
        </div>
    </section>

    <!-- COMPARISON TABLE -->
    <section class="comparison">
        <div class="container">
            <div class="section-header">
                <span class="section-badge">⚖️ COMPARISON</span>
                <h2 class="section-title">How Super AI <span class="gradient-text">compares</span></h2>
                <p class="section-subtitle">See why developers are switching from paid services.</p>
            </div>
            <div class="comparison-table">
                <div class="comparison-row header">
                    <div>Feature</div>
                    <div class="highlight">Super AI</div>
                    <div>Claude Pro</div>
                    <div>GPT-4</div>
                    <div>Gemini Pro</div>
                </div>
                <div class="comparison-row">
                    <div><strong>Price</strong></div>
                    <div><strong style="color: var(--success);">Free</strong></div>
                    <div>$20/mo</div>
                    <div>$20/mo</div>
                    <div>$20/mo</div>
                </div>
                <div class="comparison-row">
                    <div>Custom Training</div>
                    <div><i class="fas fa-check check"></i></div>
                    <div><i class="fas fa-times cross"></i></div>
                    <div><i class="fas fa-check check"></i> (paid)</div>
                    <div><i class="fas fa-times cross"></i></div>
                </div>
                <div class="comparison-row">
                    <div>Self-Hosted</div>
                    <div><i class="fas fa-check check"></i></div>
                    <div><i class="fas fa-times cross"></i></div>
                    <div><i class="fas fa-times cross"></i></div>
                    <div><i class="fas fa-times cross"></i></div>
                </div>
                <div class="comparison-row">
                    <div>RAG Built-in</div>
                    <div><i class="fas fa-check check"></i></div>
                    <div><i class="fas fa-check check"></i></div>
                    <div><i class="fas fa-check check"></i></div>
                    <div><i class="fas fa-check check"></i></div>
                </div>
                <div class="comparison-row">
                    <div>Web Search</div>
                    <div><i class="fas fa-check check"></i></div>
                    <div><i class="fas fa-check check"></i></div>
                    <div><i class="fas fa-check check"></i></div>
                    <div><i class="fas fa-check check"></i></div>
                </div>
                <div class="comparison-row">
                    <div>Voice I/O</div>
                    <div><i class="fas fa-check check"></i></div>
                    <div><i class="fas fa-times cross"></i></div>
                    <div><i class="fas fa-check check"></i></div>
                    <div><i class="fas fa-check check"></i></div>
                </div>
                <div class="comparison-row">
                    <div>Agent System</div>
                    <div><i class="fas fa-check check"></i></div>
                    <div><i class="fas fa-check check"></i></div>
                    <div><i class="fas fa-check check"></i></div>
                    <div><i class="fas fa-check check"></i></div>
                </div>
                <div class="comparison-row">
                    <div>Plugin System</div>
                    <div><i class="fas fa-check check"></i></div>
                    <div><i class="fas fa-times cross"></i></div>
                    <div><i class="fas fa-check check"></i></div>
                    <div><i class="fas fa-check check"></i></div>
                </div>
                <div class="comparison-row">
                    <div>Mobile Apps</div>
                    <div><i class="fas fa-check check"></i></div>
                    <div><i class="fas fa-check check"></i></div>
                    <div><i class="fas fa-check check"></i></div>
                    <div><i class="fas fa-check check"></i></div>
                </div>
                <div class="comparison-row">
                    <div>Open Source</div>
                    <div><i class="fas fa-check check"></i></div>
                    <div><i class="fas fa-times cross"></i></div>
                    <div><i class="fas fa-times cross"></i></div>
                    <div><i class="fas fa-times cross"></i></div>
                </div>
                <div class="comparison-row">
                    <div>Model Ownership</div>
                    <div><i class="fas fa-check check"></i></div>
                    <div><i class="fas fa-times cross"></i></div>
                    <div><i class="fas fa-times cross"></i></div>
                    <div><i class="fas fa-times cross"></i></div>
                </div>
            </div>
        </div>
    </section>

    <!-- DEMO -->
    <section class="demo" id="demo">
        <div class="container">
            <div class="section-header">
                <span class="section-badge">🎮 LIVE DEMO</span>
                <h2 class="section-title">See Super AI in <span class="gradient-text">action</span></h2>
                <p class="section-subtitle">Try it yourself. No signup required.</p>
            </div>
            <div class="demo-container">
                <div class="demo-window">
                    <div class="demo-header">
                        <div class="code-dots">
                            <span class="dot red"></span><span class="dot yellow"></span><span class="dot green"></span>
                        </div>
                        <div class="demo-title">super-ai.chat</div>
                    </div>
                    <div class="demo-body" id="demoBody">
                        <div class="message ai-message">
                            <div class="message-avatar">🧠</div>
                            <div class="message-content">Hi! I'm Super AI. I can help with coding, research, writing, math, and more. What would you like to do? 🚀</div>
                        </div>
                    </div>
                    <div class="demo-input">
                        <input type="text" id="demoInput" placeholder="Type your message...">
                        <button id="demoSend"><i class="fas fa-paper-plane"></i></button>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- HOW IT WORKS -->
    <section class="how-it-works">
        <div class="container">
            <div class="section-header">
                <span class="section-badge">🚀 GETTING STARTED</span>
                <h2 class="section-title">Up and running in <span class="gradient-text">3 simple steps</span></h2>
                <p class="section-subtitle">From zero to production AI in under 5 minutes.</p>
            </div>
            <div class="steps">
                <div class="step">
                    <div class="step-number">1</div>
                    <h3>Install</h3>
                    <p>One command to install. Works on Windows, Mac, and Linux. No dependencies hell.</p>
                    <div class="step-code"><code>$ pip install super-ai</code></div>
                </div>
                <div class="step">
                    <div class="step-number">2</div>
                    <h3>Configure</h3>
                    <p>Add your data, choose your model, customize behavior. Or use our pre-trained models.</p>
                    <div class="step-code"><code>$ super-ai init</code></div>
                </div>
                <div class="step">
                    <div class="step-number">3</div>
                    <h3>Deploy</h3>
                    <p>Run locally, or deploy to cloud with one click. Auto-scaling and monitoring included.</p>
                    <div class="step-code"><code>$ super-ai deploy</code></div>
                </div>
            </div>
        </div>
    </section>

    <!-- USE CASES -->
    <section class="use-cases" id="use-cases">
        <div class="container">
            <div class="section-header">
                <span class="section-badge">💼 USE CASES</span>
                <h2 class="section-title">Built for <span class="gradient-text">every industry</span></h2>
                <p class="section-subtitle">From startups to Fortune 500, see what you can build.</p>
            </div>
            <div class="use-cases-grid">
                <div class="use-case"><div class="use-case-icon">💻</div><h3>Developer Tools</h3><p>Code generation, debugging, refactoring, and documentation. Like having a senior dev on call 24/7.</p></div>
                <div class="use-case"><div class="use-case-icon">📚</div><h3>Research & Education</h3><p>Analyze papers, summarize research, generate educational content. Your personal research assistant.</p></div>
                <div class="use-case"><div class="use-case-icon">🏥</div><h3>Healthcare</h3><p>Medical Q&A, patient triage, clinical documentation. HIPAA-compliant deployment available.</p></div>
                <div class="use-case"><div class="use-case-icon">⚖️</div><h3>Legal</h3><p>Contract analysis, legal research, document review. Trained on legal corpora for accuracy.</p></div>
                <div class="use-case"><div class="use-case-icon">💰</div><h3>Finance</h3><p>Financial analysis, report generation, market research. Real-time data integration.</p></div>
                <div class="use-case"><div class="use-case-icon">🎨</div><h3>Creative</h3><p>Content creation, copywriting, brainstorming, image generation. Your creative partner.</p></div>
                <div class="use-case"><div class="use-case-icon">🛒</div><h3>E-commerce</h3><p>Customer support, product recommendations, inventory management. 24/7 shopping assistant.</p></div>
                <div class="use-case"><div class="use-case-icon">🏭</div><h3>Manufacturing</h3><p>Quality control, predictive maintenance, process optimization. Industry 4.0 ready.</p></div>
            </div>
        </div>
    </section>

    <!-- STATS BANNER -->
    <section class="stats-banner">
        <div class="container">
            <div class="stats-banner-grid">
                <div class="stats-banner-stat"><div class="number">50K+</div><div class="label">Active Developers</div></div>
                <div class="stats-banner-stat"><div class="number">10M+</div><div class="label">API Calls/Day</div></div>
                <div class="stats-banner-stat"><div class="number">99.9%</div><div class="label">Uptime</div></div>
                <div class="stats-banner-stat"><div class="number">150+</div><div class="label">Countries</div></div>
            </div>
        </div>
    </section>

    <!-- INTEGRATIONS -->
    <section class="integrations">
        <div class="container">
            <div class="section-header">
                <span class="section-badge">🔌 INTEGRATIONS</span>
                <h2 class="section-title">Works with your <span class="gradient-text">favorite tools</span></h2>
                <p class="section-subtitle">Connect to anything. Integrate everywhere.</p>
            </div>
            <div class="integrations-grid">
                <div class="integration-card"><div class="integration-icon">💬</div><div class="integration-name">Slack</div></div>
                <div class="integration-card"><div class="integration-icon">🎮</div><div class="integration-name">Discord</div></div>
                <div class="integration-card"><div class="integration-icon">📧</div><div class="integration-name">Email</div></div>
                <div class="integration-card"><div class="integration-icon">📱</div><div class="integration-name">WhatsApp</div></div>
                <div class="integration-card"><div class="integration-icon">🐙</div><div class="integration-name">GitHub</div></div>
                <div class="integration-card"><div class="integration-icon">📝</div><div class="integration-name">Notion</div></div>
                <div class="integration-card"><div class="integration-icon">📊</div><div class="integration-name">Google Drive</div></div>
                <div class="integration-card"><div class="integration-icon">📅</div><div class="integration-name">Calendar</div></div>
                <div class="integration-card"><div class="integration-icon">🗄️</div><div class="integration-name">PostgreSQL</div></div>
                <div class="integration-card"><div class="integration-icon">🔥</div><div class="integration-name">Firebase</div></div>
                <div class="integration-card"><div class="integration-icon">⚡</div><div class="integration-name">Zapier</div></div>
                <div class="integration-card"><div class="integration-icon">🔗</div><div class="integration-name">Webhooks</div></div>
            </div>
        </div>
    </section>

    <!-- PRICING -->
    <section class="pricing" id="pricing">
        <div class="container">
            <div class="section-header">
                <span class="section-badge">💎 PRICING</span>
                <h2 class="section-title">Simple, <span class="gradient-text">transparent</span> pricing</h2>
                <p class="section-subtitle">Start free, scale as you grow. No hidden fees.</p>
            </div>
            <div class="pricing-grid">
                <div class="pricing-card">
                    <h3>🆓 Free</h3>
                    <div class="price"><span class="price-currency">$</span><span class="price-amount">0</span><span class="price-period">/month</span></div>
                    <ul class="pricing-features">
                        <li><i class="fas fa-check"></i> Local development</li>
                        <li><i class="fas fa-check"></i> All core features</li>
                        <li><i class="fas fa-check"></i> Community support</li>
                        <li><i class="fas fa-check"></i> 1 model</li>
                        <li><i class="fas fa-check"></i> 1,000 API calls/month</li>
                        <li><i class="fas fa-check"></i> 1GB storage</li>
                    </ul>
                    <a href="#" class="btn btn-secondary btn-block" onclick="openModal('signupModal')">Get Started</a>
                </div>
                <div class="pricing-card popular">
                    <div class="popular-badge">⭐ MOST POPULAR</div>
                    <h3>🚀 Pro</h3>
                    <div class="price"><span class="price-currency">$</span><span class="price-amount">49</span><span class="price-period">/month</span></div>
                    <ul class="pricing-features">
                        <li><i class="fas fa-check"></i> Everything in Free</li>
                        <li><i class="fas fa-check"></i> Cloud deployment</li>
                        <li><i class="fas fa-check"></i> 10 models</li>
                        <li><i class="fas fa-check"></i> 100,000 API calls/month</li>
                        <li><i class="fas fa-check"></i> 100GB storage</li>
                        <li><i class="fas fa-check"></i> Priority support</li>
                        <li><i class="fas fa-check"></i> Custom plugins</li>
                        <li><i class="fas fa-check"></i> Team collaboration</li>
                    </ul>
                    <a href="#" class="btn btn-primary btn-block" onclick="openModal('signupModal')">Start Free Trial</a>
                </div>
                <div class="pricing-card">
                    <h3>🏢 Enterprise</h3>
                    <div class="price"><span class="price-currency">$</span><span class="price-amount">499</span><span class="price-period">/month</span></div>
                    <ul class="pricing-features">
                        <li><i class="fas fa-check"></i> Everything in Pro</li>
                        <li><i class="fas fa-check"></i> Unlimited models</li>
                        <li><i class="fas fa-check"></i> Unlimited API calls</li>
                        <li><i class="fas fa-check"></i> Unlimited storage</li>
                        <li><i class="fas fa-check"></i> Dedicated support</li>
                        <li><i class="fas fa-check"></i> SLA guarantee (99.99%)</li>
                        <li><i class="fas fa-check"></i> On-premise option</li>
                        <li><i class="fas fa-check"></i> Custom training</li>
                        <li><i class="fas fa-check"></i> White label</li>
                    </ul>
                    <a href="#" class="btn btn-secondary btn-block" onclick="openModal('contactModal')">Contact Sales</a>
                </div>
            </div>
        </div>
    </section>

    <!-- TESTIMONIALS -->
    <section class="testimonials">
        <div class="container">
            <div class="section-header">
                <span class="section-badge">⭐ TESTIMONIALS</span>
                <h2 class="section-title">Loved by <span class="gradient-text">developers</span> worldwide</h2>
                <p class="section-subtitle">Don't just take our word for it.</p>
            </div>
            <div class="testimonials-grid">
                <div class="testimonial-card">
                    <div class="testimonial-rating"><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i></div>
                    <p class="testimonial-text">"Super AI replaced our $5k/month OpenAI bill. We trained a custom model that's actually better for our use case. ROI in 2 weeks."</p>
                    <div class="testimonial-author"><div class="author-avatar">SJ</div><div class="author-info"><div class="author-name">Sarah Johnson</div><div class="author-role">CTO at TechStartup</div></div></div>
                </div>
                <div class="testimonial-card">
                    <div class="testimonial-rating"><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i></div>
                    <p class="testimonial-text">"The RAG system is incredible. We added our entire 10,000-page knowledge base in minutes. Game changer for our support team."</p>
                    <div class="testimonial-author"><div class="author-avatar">MK</div><div class="author-info"><div class="author-name">Michael Kim</div><div class="author-role">Lead Engineer at BigCorp</div></div></div>
                </div>
                <div class="testimonial-card">
                    <div class="testimonial-rating"><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i></div>
                    <p class="testimonial-text">"I've tried every AI platform. Super AI is the first that lets me actually OWN my models. 10/10 would recommend."</p>
                    <div class="testimonial-author"><div class="author-avatar">AL</div><div class="author-info"><div class="author-name">Alex Lee</div><div class="author-role">Indie Developer</div></div></div>
                </div>
                <div class="testimonial-card">
                    <div class="testimonial-rating"><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i></div>
                    <p class="testimonial-text">"The mobile app is beautiful and fast. Our field engineers use it daily. The voice features are mind-blowing."</p>
                    <div class="testimonial-author"><div class="author-avatar">RP</div><div class="author-info"><div class="author-name">Rachel Patel</div><div class="author-role">Product Manager</div></div></div>
                </div>
                <div class="testimonial-card">
                    <div class="testimonial-rating"><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i></div>
                    <p class="testimonial-text">"Setup took 10 minutes. We had a production AI serving 1M users within a day. The plugin system saved us weeks of work."</p>
                    <div class="testimonial-author"><div class="author-avatar">DW</div><div class="author-info"><div class="author-name">David Wang</div><div class="author-role">DevOps Lead</div></div></div>
                </div>
                <div class="testimonial-card">
                    <div class="testimonial-rating"><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i></div>
                    <p class="testimonial-text">"Best open-source AI project I've seen. The documentation is excellent and the community is super helpful."</p>
                    <div class="testimonial-author"><div class="author-avatar">EM</div><div class="author-info"><div class="author-name">Emma Martinez</div><div class="author-role">ML Engineer</div></div></div>
                </div>
            </div>
        </div>
    </section>

    <!-- FAQ -->
    <section class="faq" id="faq">
        <div class="container">
            <div class="section-header">
                <span class="section-badge">❓ FAQ</span>
                <h2 class="section-title">Frequently asked <span class="gradient-text">questions</span></h2>
                <p class="section-subtitle">Everything you need to know.</p>
            </div>
            <div class="faq-list">
                <div class="faq-item">
                    <div class="faq-question" onclick="toggleFaq(this)">Is Super AI really free? <i class="fas fa-chevron-down"></i></div>
                    <div class="faq-answer">Yes! The core platform is 100% free and open-source under MIT license. You only pay if you want cloud hosting, premium support, or enterprise features. Run it locally forever, no strings attached.</div>
                </div>
                <div class="faq-item">
                    <div class="faq-question" onclick="toggleFaq(this)">How is it different from ChatGPT/Claude? <i class="fas fa-chevron-down"></i></div>
                    <div class="faq-answer">Super AI is open-source, self-hostable, and fully customizable. You own your models, your data, and your infrastructure. No vendor lock-in, no usage limits, no surprise bills. You can also fine-tune on your own data.</div>
                </div>
                <div class="faq-item">
                    <div class="faq-question" onclick="toggleFaq(this)">Do I need a GPU? <i class="fas fa-chevron-down"></i></div>
                    <div class="faq-answer">For training large models, yes — a GPU is recommended (NVIDIA with 16GB+ VRAM). But for inference, you can run smaller models on CPU. We also offer cloud GPU rentals starting at $0.40/hour.</div>
                </div>
                <div class="faq-item">
                    <div class="faq-question" onclick="toggleFaq(this)">Can I use my own data? <i class="fas fa-chevron-down"></i></div>
                    <div class="faq-answer">Absolutely! That's the whole point. Upload PDFs, docs, websites, or any text. The RAG system indexes everything and your AI can answer questions using your private knowledge base.</div>
                </div>
                <div class="faq-item">
                    <div class="faq-question" onclick="toggleFaq(this)">Is it production-ready? <i class="fas fa-chevron-down"></i></div>
                    <div class="faq-answer">Yes. Companies serving millions of users run on Super AI. It includes auto-scaling, load balancing, monitoring, error handling, and all the production features you need. 99.9% uptime SLA available on Enterprise.</div>
                </div>
                <div class="faq-item">
                    <div class="faq-question" onclick="toggleFaq(this)">What models are supported? <i class="fas fa-chevron-down"></i></div>
                    <div class="faq-answer">All major open-source models: Llama 3.1, Mistral, Mixtral, Qwen 2.5, DeepSeek, Phi, Gemma, and more. You can also import models from Hugging Face, or train your own from scratch.</div>
                </div>
                <div class="faq-item">
                    <div class="faq-question" onclick="toggleFaq(this)">How does pricing work? <i class="fas fa-chevron-down"></i></div>
                    <div class="faq-answer">Free tier: unlimited local use, 1,000 API calls/month on cloud. Pro ($49/mo): 100K calls, 10 models, priority support. Enterprise ($499/mo): unlimited everything, SLA, custom training, on-premise option.</div>
                </div>
                <div class="faq-item">
                    <div class="faq-question" onclick="toggleFaq(this)">Can I deploy on my own servers? <i class="fas fa-chevron-down"></i></div>
                    <div class="faq-answer">Yes! Self-host on any infrastructure — AWS, GCP, Azure, on-premise, or even a Raspberry Pi for small models. Docker, Kubernetes, and bare-metal deployments all supported.</div>
                </div>
            </div>
        </div>
    </section>

    <!-- NEWSLETTER -->
    <section class="newsletter">
        <div class="container">
            <div class="newsletter-container">
                <div class="section-header" style="margin-bottom: 20px;">
                    <span class="section-badge">📬 STAY UPDATED</span>
                    <h2 class="section-title">Get the <span class="gradient-text">latest updates</span></h2>
                    <p class="section-subtitle">Join 10,000+ developers getting weekly AI tips, tutorials, and product updates.</p>
                </div>
                <form class="newsletter-form" onsubmit="subscribeNewsletter(event)">
                    <input type="email" class="newsletter-input" placeholder="Enter your email" required>
                    <button type="submit" class="btn btn-primary">Subscribe</button>
                </form>
                <p style="margin-top: 16px; font-size: 14px; color: var(--text-tertiary);">🔒 No spam. Unsubscribe anytime.</p>
            </div>
        </div>
    </section>

    <!-- CTA -->
    <section class="cta">
        <div class="container">
            <div class="cta-content">
                <h2>Ready to build your <span class="gradient-text">Super AI</span>?</h2>
                <p>Join 50,000+ developers building the future of AI. Start free in 60 seconds.</p>
                <div class="cta-actions">
                    <a href="#" class="btn btn-primary btn-large" onclick="openModal('signupModal')">
                        <i class="fas fa-rocket"></i> Get Started Free
                    </a>
                    <a href="https://github.com" class="btn btn-ghost btn-large" style="color: white; border: 2px solid white;">
                        <i class="fab fa-github"></i> Star on GitHub
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- FOOTER -->
    <footer class="footer">
        <div class="container">
            <div class="footer-grid">
                <div class="footer-col">
                    <div class="footer-brand"><span class="logo-icon">🧠</span><span>Super<span class="gradient-text">AI</span></span></div>
                    <p>The complete open-source AI platform. Build, train, and deploy custom AI models. Made with ❤️ by developers, for developers.</p>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-github"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-discord"></i></a>
                        <a href="#"><i class="fab fa-youtube"></i></a>
                        <a href="#"><i class="fab fa-linkedin"></i></a>
                    </div>
                </div>
                <div class="footer-col">
                    <h4>Product</h4>
                    <ul>
                        <li><a href="#features">Features</a></li>
                        <li><a href="#pricing">Pricing</a></li>
                        <li><a href="#">Documentation</a></li>
                        <li><a href="#">API Reference</a></li>
                        <li><a href="#">Changelog</a></li>
                        <li><a href="#">Roadmap</a></li>
                    </ul>
                </div>
                <div class="footer-col">
                    <h4>Resources</h4>
                    <ul>
                        <li><a href="#">Tutorials</a></li>
                        <li><a href="#">Blog</a></li>
                        <li><a href="#">Community</a></li>
                        <li><a href="#">Discord</a></li>
                        <li><a href="#">GitHub</a></li>
                        <li><a href="#">Status</a></li>
                    </ul>
                </div>
                <div class="footer-col">
                    <h4>Company</h4>
                    <ul>
                        <li><a href="#">About</a></li>
                        <li><a href="#">Careers</a></li>
                        <li><a href="#">Privacy</a></li>
                        <li><a href="#">Terms</a></li>
                        <li><a href="#">Security</a></li>
                        <li><a href="#" onclick="openModal('contactModal')">Contact</a></li>
                    </ul>
                </div>
            </div>
            <div class="footer-bottom">
                <p>&copy; 2024 Super AI. All rights reserved. Released under MIT License. Built with ❤️ and ☕</p>
            </div>
        </div>
    </footer>

    <!-- FLOATING BUTTONS -->
    <button class="theme-toggle" onclick="toggleTheme()" title="Toggle dark mode">🌓</button>
    <button class="back-to-top" id="backToTop" onclick="scrollToTop()" title="Back to top"><i class="fas fa-arrow-up"></i></button>

    <!-- MODALS -->
    <div class="modal" id="signupModal">
        <div class="modal-content">
            <button class="modal-close" onclick="closeModal('signupModal')">×</button>
            <h2>🚀 Get Started Free</h2>
            <p>Create your account and start building AI in 60 seconds.</p>
            <form class="modal-form" onsubmit="handleSignup(event)">
                <input type="text" placeholder="Full Name" required>
                <input type="email" placeholder="Email Address" required>
                <input type="password" placeholder="Password (min 8 chars)" required minlength="8">
                <button type="submit" class="btn btn-primary btn-block">Create Account</button>
            </form>
            <p style="text-align: center; margin-top: 20px; font-size: 14px;">Already have an account? <a href="#" onclick="closeModal('signupModal'); openModal('loginModal');" style="color: var(--primary);">Sign in</a></p>
        </div>
    </div>

    <div class="modal" id="loginModal">
        <div class="modal-content">
            <button class="modal-close" onclick="closeModal('loginModal')">×</button>
            <h2>👋 Welcome Back</h2>
            <p>Sign in to your Super AI account.</p>
            <form class="modal-form" onsubmit="handleLogin(event)">
                <input type="email" placeholder="Email Address" required>
                <input type="password" placeholder="Password" required>
                <button type="submit" class="btn btn-primary btn-block">Sign In</button>
            </form>
            <p style="text-align: center; margin-top: 20px; font-size: 14px;">Don't have an account? <a href="#" onclick="closeModal('loginModal'); openModal('signupModal');" style="color: var(--primary);">Sign up</a></p>
        </div>
    </div>

    <div class="modal" id="contactModal">
        <div class="modal-content">
            <button class="modal-close" onclick="closeModal('contactModal')">×</button>
            <h2>💬 Get in Touch</h2>
            <p>Have questions? We'd love to hear from you.</p>
            <form class="modal-form" onsubmit="handleContact(event)">
                <input type="text" placeholder="Your Name" required>
                <input type="email" placeholder="Email Address" required>
                <textarea placeholder="Your Message" required></textarea>
                <button type="submit" class="btn btn-primary btn-block">Send Message</button>
            </form>
        </div>
    </div>

    <script>
        // ========================================
        // ALL JAVASCRIPT IN ONE PLACE
        // ========================================
        
        // NAVIGATION
        const navbar = document.getElementById('navbar');
        window.addEventListener('scroll', () => {
            navbar.classList.toggle('scrolled', window.scrollY > 50);
            const btn = document.getElementById('backToTop');
            btn.classList.toggle('visible', window.scrollY > 500);
        });

        function toggleMenu() {
            document.getElementById('navMenu').classList.toggle('active');
        }

        function scrollToTop() {
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        // SMOOTH SCROLL
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                const href = this.getAttribute('href');
                if (href === '#' || href.startsWith('http')) return;
                e.preventDefault();
                const target = document.querySelector(href);
                if (target) {
                    target.scrollIntoView({ behavior: 'smooth', block: 'start' });
                    document.getElementById('navMenu').classList.remove('active');
                }
            });
        });

        // COUNTER ANIMATION
        function animateCounter(el, target) {
            const duration = 2000;
            const start = performance.now();
            const update = (t) => {
                const p = Math.min((t - start) / duration, 1);
                const current = Math.floor(p * target);
                el.textContent = current.toLocaleString() + (target === 99 ? '%' : '+');
                if (p < 1) requestAnimationFrame(update);
            };
            requestAnimationFrame(update);
        }

        const statsObserver = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    document.querySelectorAll('.stat-value').forEach(stat => {
                        const target = parseInt(stat.getAttribute('data-target'));
                        animateCounter(stat, target);
                    });
                    statsObserver.unobserve(entry.target);
                }
            });
        }, { threshold: 0.5 });
        const statsEl = document.querySelector('.hero-stats');
        if (statsEl) statsObserver.observe(statsEl);

        // DEMO CHAT
        const demoResponses = {
            "hi": "Hello! 👋 How can I help you today?",
            "hello": "Hi there! What would you like to know?",
            "what can you do": "I can help with:\n• 💻 Code generation & debugging\n• 📚 Research & analysis\n• ✍️ Writing & editing\n• 🧮 Math & calculations\n• 🌐 Language translation\n• 🎨 Creative tasks\nWhat interests you?",
            "who made you": "I was built using Super AI - an open-source platform! 🚀 You can build your own version too, completely free!",
            "help": "Sure! Try asking me:\n• 'Write a Python function to sort a list'\n• 'Explain quantum computing'\n• 'Translate hello to Spanish'\n• 'Calculate 15% of 200'\nOr just chat! 😊",
            "pricing": "Super AI is FREE for local use! 🎉\n\n• Free: $0/month\n• Pro: $49/month (cloud hosting)\n• Enterprise: $499/month (custom)\n\nNo credit card required to start!",
            "features": "Super AI has 50+ features! 🌟\n\nTop ones:\n• Custom model training\n• RAG & vector search\n• Web search integration\n• Agent system\n• Mobile apps\n• Voice I/O\n• 20+ languages\n• And much more!",
            "code": "Here's a Python function to reverse a string:\n\n```python\ndef reverse_string(s):\n    return s[::-1]\n\n# Usage\nprint(reverse_string('hello'))\n# Output: 'olleh'\n```\n\nWant more code examples? 💻",
            "default": "That's a great question! 🤔 In the full version, I'd give you a detailed answer. Try the live demo on our GitHub to see the complete experience! 🚀"
        };

        const demoBody = document.getElementById('demoBody');
        const demoInput = document.getElementById('demoInput');
        const demoSend = document.getElementById('demoSend');

        function addMessage(text, isUser = false) {
            const msg = document.createElement('div');
            msg.className = `message ${isUser ? 'user-message' : 'ai-message'}`;
            const formattedText = text.replace(/```(\w*)\n([\s\S]*?)\n```/g, '<pre style="background:#1a1a1a;padding:12px;border-radius:8px;margin:8px 0;overflow-x:auto;"><code>$2</code></pre>').replace(/\n/g, '<br>');
            msg.innerHTML = `<div class="message-avatar">${isUser ? '👤' : '🧠'}</div><div class="message-content">${formattedText}</div>`;
            demoBody.appendChild(msg);
            demoBody.scrollTop = demoBody.scrollHeight;
        }

        function getResponse(msg) {
            const key = msg.toLowerCase().trim();
            for (const k in demoResponses) {
                if (key.includes(k)) return demoResponses[k];
            }
            return demoResponses.default;
        }

        function sendDemo() {
            const text = demoInput.value.trim();
            if (!text) return;
            addMessage(text, true);
            demoInput.value = '';
            setTimeout(() => addMessage(getResponse(text), false), 800);
        }

        demoSend.addEventListener('click', sendDemo);
        demoInput.addEventListener('keypress', (e) => { if (e.key === 'Enter') sendDemo(); });

        // PARALLAX
        document.addEventListener('mousemove', (e) => {
            const x = (e.clientX / window.innerWidth - 0.5) * 20;
            const y = (e.clientY / window.innerHeight - 0.5) * 20;
            document.querySelectorAll('.gradient-orb').forEach((orb, i) => {
                orb.style.transform = `translate(${x * (i+1) * 0.3}px, ${y * (i+1) * 0.3}px)`;
            });
        });

        // FAQ TOGGLE
        function toggleFaq(el) {
            const item = el.parentElement;
            document.querySelectorAll('.faq-item').forEach(i => {
                if (i !== item) i.classList.remove('active');
            });
            item.classList.toggle('active');
        }

        // MODALS
        function openModal(id) {
            document.getElementById(id).classList.add('active');
            document.body.style.overflow = 'hidden';
        }
        function closeModal(id) {
            document.getElementById(id).classList.remove('active');
            document.body.style.overflow = '';
        }
        document.querySelectorAll('.modal').forEach(modal => {
            modal.addEventListener('click', (e) => {
                if (e.target === modal) closeModal(modal.id);
            });
        });
        document.addEventListener('keydown', (e) => {
            if (e.key === 'Escape') document.querySelectorAll('.modal.active').forEach(m => closeModal(m.id));
        });

        // THEME TOGGLE
        function toggleTheme() {
            document.body.classList.toggle('dark-mode');
            localStorage.setItem('theme', document.body.classList.contains('dark-mode') ? 'dark' : 'light');
        }
        if (localStorage.getItem('theme') === 'dark') {
            document.body.classList.add('dark-mode');
        }

        // FORM HANDLERS
        function handleSignup(e) {
            e.preventDefault();
            alert('🎉 Welcome aboard! Check your email to verify your account.');
            closeModal('signupModal');
            e.target.reset();
        }
        function handleLogin(e) {
            e.preventDefault();
            alert('✅ Signed in successfully! Redirecting...');
            closeModal('loginModal');
            e.target.reset();
        }
        function handleContact(e) {
            e.preventDefault();
            alert('📧 Message sent! We\'ll get back to you within 24 hours.');
            closeModal('contactModal');
            e.target.reset();
        }
        function subscribeNewsletter(e) {
            e.preventDefault();
            alert('📬 Subscribed! Check your inbox for a welcome email.');
            e.target.reset();
        }

        // ANIMATIONS
        const animObserver = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, { threshold: 0.1 });

        document.querySelectorAll('.feature-card, .use-case, .testimonial-card, .pricing-card, .integration-card, .faq-item, .step').forEach((el, i) => {
            el.style.opacity = '0';
            el.style.transform = 'translateY(30px)';
            el.style.transition = `opacity 0.6s ease ${i * 0.05}s, transform 0.6s ease ${i * 0.05}s`;
            animObserver.observe(el);
        });

        console.log('🧠 Super AI website loaded! All features integrated.');
    </script>
</body>
</html>
