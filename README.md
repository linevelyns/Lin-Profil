[index2.html](https://github.com/user-attachments/files/33204091/index2.html)
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lin Lin - Ultimate Ice Portfolio & Career Goals Edition</title>

    <!-- FontAwesome 6 Pro/Free Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    <!-- Google Fonts: Plus Jakarta Sans -->
    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;600;700;800&display=swap">

    <style>
        :root {
            --ice-primary: #38bdf8;
            --ice-glow: #7dd3fc;
            --ice-light: #a5f3fc;
            --ice-dark: #0284c7;
            --bg-deep: #030a16;
            --glass-bg: rgba(6, 25, 48, 0.55);
            --glass-border: rgba(165, 243, 252, 0.25);
            --glass-glow: rgba(56, 189, 248, 0.4);
            --text-main: #f0f9ff;
            --text-muted: #bae6fd;
        }

        * { 
            margin: 0; 
            padding: 0; 
            box-sizing: border-box; 
        } 
         
        html {
            scroll-behavior: smooth;
        }

        /* Custom Frost Scrollbar */
        ::-webkit-scrollbar {
            width: 10px;
        }
        ::-webkit-scrollbar-track {
            background: #020712;
        }
        ::-webkit-scrollbar-thumb {
            background: linear-gradient(180deg, var(--ice-light), var(--ice-primary), var(--ice-dark));
            border-radius: 5px;
            box-shadow: 0 0 10px var(--ice-primary);
        }

        /* Scroll Progress Bar Neon */
        .progress-bar {
            position: fixed;
            top: 0;
            left: 0;
            height: 4px;
            background: linear-gradient(90deg, #38bdf8, #a5f3fc, #38bdf8, #0284c7);
            background-size: 200% 100%;
            animation: gradientMove 3s linear infinite;
            width: 0%;
            z-index: 10001;
            box-shadow: 0 0 12px var(--ice-primary), 0 0 20px var(--ice-light);
            transition: width 0.1s ease-out;
        }

        @keyframes gradientMove {
            0% { background-position: 0% 50%; }
            100% { background-position: 200% 50%; }
        }

        body { 
            font-family: 'Plus Jakarta Sans', "Segoe UI", sans-serif; 
            background-color: var(--bg-deep);
            background-image: 
                radial-gradient(circle at 15% 20%, rgba(56, 189, 248, 0.25), transparent 40%), 
                radial-gradient(circle at 85% 25%, rgba(165, 243, 252, 0.2), transparent 35%), 
                radial-gradient(circle at 50% 80%, rgba(2, 132, 199, 0.2), transparent 45%); 
            background-attachment: fixed;
            min-height: 100vh; 
            color: var(--text-main); 
            line-height: 1.6; 
            overflow-x: hidden; 
            position: relative;
        } 

        /* Ambient Cursor Light Orb */
        .cursor-light-orb {
            position: fixed;
            width: 350px;
            height: 350px;
            border-radius: 50%;
            background: radial-gradient(circle, rgba(56, 189, 248, 0.22), rgba(165, 243, 252, 0.08), transparent 70%);
            pointer-events: none;
            z-index: 1;
            transform: translate(-50%, -50%);
            transition: width 0.3s ease, height 0.3s ease;
        }

        /* Animated Aurora Borealis Background */
        .aurora-bg {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 0;
            opacity: 0.45;
            background: linear-gradient(125deg, rgba(3, 10, 22, 0) 0%, rgba(56, 189, 248, 0.15) 30%, rgba(165, 243, 252, 0.1) 60%, rgba(2, 132, 199, 0) 100%);
            background-size: 400% 400%;
            animation: auroraMove 15s ease infinite;
        }

        @keyframes auroraMove {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        /* Canvas Salju Jatuh Interactive Background */
        #snowCanvas {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 1;
        }

        /* Frost Freeze Canvas Overlay */
        #freezeCanvas {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 9995;
            pointer-events: none;
            opacity: 0;
            transition: opacity 0.5s ease;
        }

        #freezeCanvas.active {
            pointer-events: auto;
            opacity: 1;
            cursor: crosshair;
        }

        header { 
            background: rgba(3, 13, 29, 0.7);
            backdrop-filter: blur(18px);
            -webkit-backdrop-filter: blur(18px);
            position: sticky; 
            top: 0; 
            z-index: 1000; 
            box-shadow: 0 4px 30px rgba(0, 0, 0, 0.5), 0 1px 0 rgba(165, 243, 252, 0.2); 
            border-bottom: 1px solid rgba(165, 243, 252, 0.2); 
        } 
         
        .navbar { 
            max-width: 1200px; 
            margin: auto; 
            display: flex; 
            justify-content: space-between; 
            align-items: center; 
            padding: 16px 24px; 
        } 
         
        .logo { 
            color: var(--ice-light); 
            font-size: 22px; 
            font-weight: 800; 
            letter-spacing: 1px; 
            text-shadow: 0 0 12px var(--ice-primary); 
            display: flex;
            align-items: center;
            gap: 10px;
            text-decoration: none;
        } 

        .logo i {
            color: var(--ice-primary);
            filter: drop-shadow(0 0 8px var(--ice-primary));
            animation: iceSpin 8s linear infinite;
        }

        @keyframes iceSpin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
         
        .nav-menu { 
            list-style: none; 
            display: flex; 
            gap: 28px; 
        } 
         
        .nav-menu a { 
            color: var(--text-main); 
            text-decoration: none; 
            font-weight: 600; 
            font-size: 15px;
            position: relative; 
            padding: 6px 0;
            transition: color 0.35s ease; 
        } 
         
        .nav-menu a::after { 
            content: ""; 
            position: absolute; 
            width: 0; 
            height: 3px; 
            left: 50%; 
            bottom: -2px; 
            transform: translateX(-50%); 
            background: linear-gradient(90deg, var(--ice-light), var(--ice-primary)); 
            border-radius: 10px; 
            box-shadow: 0 0 10px var(--ice-primary);
            transition: width 0.35s cubic-bezier(0.4, 0, 0.2, 1); 
        } 
         
        .nav-menu a:hover,
        .nav-menu a.active { 
            color: var(--ice-light); 
            text-shadow: 0 0 10px var(--ice-primary); 
        } 
         
        .nav-menu a:hover::after,
        .nav-menu a.active::after { 
            width: 100%; 
        } 

        .hero { 
            max-width: 1200px; 
            min-height: 88vh; 
            margin: auto; 
            padding: 60px 24px; 
            display: flex; 
            justify-content: space-between; 
            align-items: center; 
            gap: 50px; 
            position: relative;
            z-index: 2;
        } 
         
        .hero-text { 
            flex: 1.2; 
        } 
         
        .sapaan { 
            display: inline-flex;
            align-items: center;
            gap: 8px;
            background: rgba(56, 189, 248, 0.15);
            border: 1px solid rgba(165, 243, 252, 0.3);
            padding: 6px 16px;
            border-radius: 20px;
            color: var(--ice-light); 
            font-size: 14px; 
            font-weight: 700; 
            letter-spacing: 1px;
            margin-bottom: 16px; 
            box-shadow: 0 0 15px rgba(56, 189, 248, 0.2);
            backdrop-filter: blur(8px);
        } 
         
        .hero h1 { 
            color: #ffffff; 
            font-size: 56px; 
            font-weight: 800;
            line-height: 1.1;
            margin: 10px 0 16px 0; 
            text-shadow: 0 0 20px rgba(56, 189, 248, 0.6), 0 0 40px rgba(2, 132, 199, 0.4); 
            background: linear-gradient(180deg, #ffffff, var(--ice-light));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        } 
         
        .hero h2 { 
            color: var(--ice-glow); 
            margin-bottom: 22px; 
            font-size: 26px; 
            font-weight: 700;
            min-height: 40px;
            border-right: 3px solid var(--ice-primary);
            display: inline-block;
            white-space: nowrap;
            overflow: hidden;
            animation: cursorBlink 0.75s infinite;
        } 

        @keyframes cursorBlink {
            0%, 100% { border-color: transparent; }
            50% { border-color: var(--ice-primary); }
        }
         
        .hero p { 
            margin-bottom: 32px; 
            color: var(--text-muted); 
            font-size: 17px;
            max-width: 600px; 
            line-height: 1.7;
        } 

        .action-buttons {
            display: flex;
            gap: 16px;
            flex-wrap: wrap;
        }

        /* Tombol Es Kristal & Shimmering Effect */
        .tombol, .magnetic-btn { 
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            background: linear-gradient(135deg, rgba(56, 189, 248, 0.9), rgba(2, 132, 199, 0.95)); 
            color: white; 
            padding: 14px 28px; 
            border-radius: 30px; 
            text-decoration: none; 
            font-weight: 700; 
            font-size: 15px;
            position: relative; 
            overflow: hidden; 
            border: 1px solid rgba(224, 242, 254, 0.6);
            transition: transform 0.2s cubic-bezier(0.2, 0.8, 0.2, 1), box-shadow 0.35s ease, border-color 0.35s ease; 
            box-shadow: 0 8px 25px rgba(56, 189, 248, 0.4), inset 0 0 15px rgba(255, 255, 255, 0.4); 
            backdrop-filter: blur(8px);
            cursor: pointer;
            will-change: transform;
        } 
        
        .tombol.secondary {
            background: rgba(6, 25, 48, 0.75);
            border-color: rgba(165, 243, 252, 0.4);
            color: var(--ice-light);
            box-shadow: 0 8px 20px rgba(3, 10, 22, 0.5);
        }

        .tombol::before, .magnetic-btn::before {
            content: "";
            position: absolute;
            top: 0;
            left: -100%;
            width: 60%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.8), transparent);
            transform: skewX(-20deg);
            transition: left 0.6s ease;
        }

        .tombol:hover::before, .magnetic-btn:hover::before {
            left: 140%;
        }

        .tombol:hover, .magnetic-btn:hover { 
            box-shadow: 0 12px 35px rgba(56, 189, 248, 0.7), inset 0 0 25px rgba(255, 255, 255, 0.7); 
            border-color: #ffffff;
            color: #ffffff;
        } 
         
        .hero-image { 
            flex: 0.9; 
            text-align: center; 
            position: relative; 
        } 

        /* Frame Es Glossy di Sekitar Foto */
        .hero-image-wrapper {
            position: relative;
            display: inline-block;
            cursor: pointer;
            transition: transform 0.3s cubic-bezier(0.2, 0.8, 0.2, 1);
            will-change: transform;
        }

        .hero-image-wrapper::before {
            content: "";
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 320px;
            height: 320px;
            border-radius: 50%;
            background: radial-gradient(circle, rgba(165, 243, 252, 0.4), rgba(56, 189, 248, 0.15), transparent 70%);
            filter: blur(16px);
            z-index: 0;
            animation: iceGlow 4s ease-in-out infinite alternate;
        }

        @keyframes iceGlow {
            0% { transform: translate(-50%, -50%) scale(0.95); opacity: 0.6; }
            100% { transform: translate(-50%, -50%) scale(1.1); opacity: 1; }
        }
         
        .hero-image img { 
            width: 290px; 
            height: 290px; 
            object-fit: cover; 
            border-radius: 50%; 
            position: relative;
            z-index: 1;
            border: 6px solid rgba(224, 242, 254, 0.85); 
            box-shadow: 0 0 35px rgba(56, 189, 248, 0.6), inset 0 0 20px rgba(255, 255, 255, 0.6); 
            animation: profileFloat 5s ease-in-out infinite; 
            transition: transform 0.4s ease; 
        } 
         
        @keyframes profileFloat { 
            0%, 100% { transform: translateY(0); } 
            50% { transform: translateY(-12px); } 
        } 

        /* Scroll Reveal Effect Class */
        .reveal {
            opacity: 0;
            transform: translateY(40px);
            transition: all 0.8s cubic-bezier(0.16, 1, 0.3, 1);
        }

        .reveal.active {
            opacity: 1;
            transform: translateY(0);
        }

        .section-container { 
            max-width: 1200px;
            margin: auto;
            padding: 80px 24px; 
            position: relative;
            z-index: 2;
        } 

        .tentang-bg {
            background: rgba(3, 13, 29, 0.45); 
            border-top: 1px solid var(--glass-border); 
            border-bottom: 1px solid var(--glass-border); 
        }
         
        .judul { 
            text-align: center; 
            color: var(--ice-light); 
            font-size: 38px; 
            font-weight: 800;
            margin-bottom: 12px; 
            text-shadow: 0 0 15px var(--ice-primary); 
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 12px;
        } 

        .sub-judul {
            text-align: center;
            color: var(--text-muted);
            margin-bottom: 40px;
            font-size: 16px;
        }

        /* TAB SYSTEM STYLING */
        .tabs-nav {
            display: flex;
            justify-content: center;
            gap: 12px;
            margin-bottom: 40px;
            flex-wrap: wrap;
        }

        .tab-btn {
            background: rgba(6, 25, 48, 0.6);
            border: 1px solid rgba(165, 243, 252, 0.25);
            color: var(--text-muted);
            padding: 12px 24px;
            border-radius: 30px;
            font-weight: 700;
            font-size: 15px;
            cursor: pointer;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            gap: 10px;
            backdrop-filter: blur(10px);
        }

        .tab-btn i {
            color: var(--ice-primary);
        }

        .tab-btn:hover {
            border-color: var(--ice-light);
            color: var(--ice-light);
        }

        .tab-btn.active {
            background: linear-gradient(135deg, rgba(56, 189, 248, 0.8), rgba(2, 132, 199, 0.9));
            color: #ffffff;
            border-color: #ffffff;
            box-shadow: 0 6px 20px rgba(56, 189, 248, 0.4);
        }

        .tab-btn.active i {
            color: #ffffff;
        }

        .tab-content {
            display: none;
            animation: fadeIn 0.5s ease-in-out;
        }

        .tab-content.active {
            display: block;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(15px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* Card Frosted Glassmorphism with Spotlight Effect */
        .tentang-container { 
            display: grid; 
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr)); 
            gap: 28px; 
        } 
         
        .card { 
            background: linear-gradient(135deg, rgba(12, 42, 77, 0.55), rgba(6, 25, 48, 0.65)); 
            padding: 32px; 
            border-radius: 24px; 
            border: 1px solid var(--glass-border); 
            backdrop-filter: blur(16px); 
            -webkit-backdrop-filter: blur(16px);
            transition: transform 0.25s ease-out, box-shadow 0.35s ease, border-color 0.35s ease; 
            transform-style: preserve-3d;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.4), inset 0 0 15px rgba(165, 243, 252, 0.08);
            position: relative;
            overflow: hidden;
            will-change: transform;
        } 

        .card-spotlight {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            background: radial-gradient(circle at var(--mouse-x, 50%) var(--mouse-y, 50%), rgba(165, 243, 252, 0.22), transparent 60%);
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .card:hover .card-spotlight {
            opacity: 1;
        }

        .card:hover {
            border-color: rgba(165, 243, 252, 0.8);
            box-shadow: 0 18px 40px rgba(56, 189, 248, 0.35), inset 0 0 20px rgba(255, 255, 255, 0.2);
        }
         
        .card h3 { 
            color: var(--ice-glow); 
            margin-bottom: 18px; 
            font-size: 22px; 
            font-weight: 700;
            display: flex;
            align-items: center;
            gap: 12px;
        } 

        .card h3 i {
            color: var(--ice-light);
            background: rgba(56, 189, 248, 0.2);
            padding: 10px;
            border-radius: 12px;
            font-size: 18px;
            border: 1px solid rgba(165, 243, 252, 0.3);
        }

        .card p, .card ul {
            color: var(--text-muted);
            line-height: 1.7;
        }

        .card ul {
            padding-left: 20px;
            margin-top: 10px;
        }

        .card ul li {
            margin-bottom: 8px;
        }

        /* SKILL PROGRESS BARS */
        .skill-item {
            margin-bottom: 20px;
        }

        .skill-info {
            display: flex;
            justify-content: space-between;
            margin-bottom: 8px;
            font-weight: 600;
            color: var(--text-main);
        }

        .skill-info span i {
            margin-right: 8px;
            color: var(--ice-primary);
        }

        .progress-bar-bg {
            height: 10px;
            background: rgba(2, 13, 29, 0.8);
            border-radius: 10px;
            overflow: hidden;
            border: 1px solid rgba(165, 243, 252, 0.2);
            position: relative;
        }

        .progress-bar-fill {
            height: 100%;
            background: linear-gradient(90deg, #0284c7, #38bdf8, #a5f3fc);
            border-radius: 10px;
            width: 0%;
            transition: width 1.5s cubic-bezier(0.1, 0.5, 0.1, 1);
            box-shadow: 0 0 12px var(--ice-primary);
        }

        /* FROST ICE TABLE STYLING */
        .table-responsive {
            width: 100%;
            overflow-x: auto;
            border-radius: 20px;
            border: 1px solid var(--glass-border);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
            backdrop-filter: blur(16px);
            background: linear-gradient(135deg, rgba(12, 42, 77, 0.4), rgba(6, 25, 48, 0.6));
        }

        .ice-table {
            width: 100%;
            border-collapse: collapse;
            text-align: left;
            color: var(--text-main);
        }

        .ice-table th {
            background: linear-gradient(90deg, rgba(2, 132, 199, 0.6), rgba(56, 189, 248, 0.5));
            padding: 18px 20px;
            font-size: 15px;
            font-weight: 800;
            color: #ffffff;
            text-transform: uppercase;
            letter-spacing: 1px;
            border-bottom: 2px solid rgba(165, 243, 252, 0.4);
            text-shadow: 0 0 8px rgba(0, 0, 0, 0.5);
        }

        .ice-table td {
            padding: 16px 20px;
            border-bottom: 1px solid rgba(165, 243, 252, 0.12);
            font-size: 15px;
            vertical-align: middle;
            transition: background 0.3s ease;
        }

        .ice-table tbody tr {
            transition: all 0.3s ease;
        }

        .ice-table tbody tr:hover {
            background: rgba(56, 189, 248, 0.15);
            box-shadow: inset 0 0 15px rgba(165, 243, 252, 0.2);
        }

        /* Badge Pills */
        .badge {
            display: inline-flex;
            align-items: center;
            gap: 6px;
            padding: 6px 14px;
            border-radius: 20px;
            font-size: 13px;
            font-weight: 700;
            letter-spacing: 0.5px;
        }

        .badge-advanced {
            background: rgba(56, 189, 248, 0.2);
            color: #a5f3fc;
            border: 1px solid rgba(165, 243, 252, 0.5);
            box-shadow: 0 0 10px rgba(56, 189, 248, 0.3);
        }

        .badge-intermediate {
            background: rgba(2, 132, 199, 0.25);
            color: #7dd3fc;
            border: 1px solid rgba(125, 211, 252, 0.4);
        }

        .kontak-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
            gap: 24px;
            margin-top: 30px;
        }

        .kontak-card {
            background: linear-gradient(135deg, rgba(12, 42, 77, 0.5), rgba(6, 25, 48, 0.65));
            padding: 28px;
            border-radius: 20px;
            border: 1px solid var(--glass-border);
            text-align: center;
            backdrop-filter: blur(14px);
            transition: all 0.35s ease;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.3);
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            position: relative;
            overflow: hidden;
            will-change: transform;
        }

        .kontak-card:hover {
            border-color: var(--ice-light);
            box-shadow: 0 15px 35px rgba(56, 189, 248, 0.35);
        }

        .kontak-icon {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            background: linear-gradient(135deg, rgba(56, 189, 248, 0.3), rgba(2, 132, 199, 0.4));
            border: 1px solid rgba(165, 243, 252, 0.5);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 24px;
            color: var(--ice-light);
            margin-bottom: 16px;
            box-shadow: 0 0 15px rgba(56, 189, 248, 0.3);
        }

        .kontak-card h4 {
            color: var(--text-main);
            font-size: 18px;
            margin-bottom: 8px;
        }

        .kontak-card p, .kontak-card a {
            color: var(--text-muted);
            font-size: 15px;
            text-decoration: none;
            word-break: break-all;
            transition: color 0.3s ease;
        }

        .kontak-card a:hover {
            color: var(--ice-light);
            text-shadow: 0 0 8px var(--ice-primary);
        }

        footer { 
            background: #010610; 
            color: var(--text-muted); 
            text-align: center; 
            padding: 32px 20px; 
            border-top: 1px solid rgba(165, 243, 252, 0.15); 
            position: relative;
            z-index: 2;
            font-size: 14px;
        } 

        /* FLOATING SOCIAL & MUSIC BUTTONS */
        .floating-socials {
            position: fixed;
            right: 25px;
            bottom: 25px;
            display: flex;
            align-items: center;
            gap: 12px;
            z-index: 9999;
        }

        .social-btn, .music-player {
            width: 52px;
            height: 52px;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 50%;
            color: white;
            text-decoration: none;
            backdrop-filter: blur(14px);
            transition: transform 0.2s cubic-bezier(0.2, 0.8, 0.2, 1), box-shadow 0.3s ease, border-color 0.3s ease;
            border: 1px solid rgba(224, 242, 254, 0.4);
            cursor: pointer;
            font-size: 20px;
            position: relative;
            will-change: transform;
        }

        .social-btn.tiktok {
            background: linear-gradient(135deg, rgba(0, 0, 0, 0.85), rgba(254, 44, 85, 0.85));
            box-shadow: 0 0 15px rgba(254, 44, 85, 0.4);
        }

        .social-btn.roblox {
            background: linear-gradient(135deg, rgba(0, 0, 0, 0.85), rgba(0, 162, 255, 0.85));
            box-shadow: 0 0 15px rgba(0, 162, 255, 0.4);
        }

        .music-player {
            background: linear-gradient(135deg, rgba(56, 189, 248, 0.85), rgba(2, 132, 199, 0.85));
            box-shadow: 0 0 20px rgba(56, 189, 248, 0.6);
        }

        .social-btn:hover, .music-player:hover {
            border-color: #ffffff;
            box-shadow: 0 10px 25px rgba(56, 189, 248, 0.8);
        }

        /* Audio Visualizer Pulse Effect */
        .music-player.playing::before {
            content: "";
            position: absolute;
            width: 100%;
            height: 100%;
            border-radius: 50%;
            border: 2px solid var(--ice-light);
            animation: pulseWave 1.5s infinite ease-out;
        }

        @keyframes pulseWave {
            0% { transform: scale(1); opacity: 0.8; }
            100% { transform: scale(1.6); opacity: 0; }
        }

        /* Ripple Effect saat Layar Diklik */
        .click-ripple {
            position: fixed;
            border-radius: 50%;
            border: 2px solid var(--ice-light);
            box-shadow: 0 0 20px var(--ice-primary), inset 0 0 10px var(--ice-primary);
            pointer-events: none;
            z-index: 99999;
            transform: translate(-50%, -50%) scale(0);
            animation: rippleAnim 0.6s ease-out forwards;
        }

        @keyframes rippleAnim {
            0% { width: 0px; height: 0px; opacity: 1; transform: translate(-50%, -50%) scale(0); }
            100% { width: 140px; height: 140px; opacity: 0; transform: translate(-50%, -50%) scale(1); }
        }

        /* Partikel Ledakan Kristal Es */
        .ice-shard {
            position: fixed;
            pointer-events: none;
            z-index: 99999;
            border-radius: 2px;
            background: radial-gradient(circle, #a5f3fc, #38bdf8);
            box-shadow: 0 0 8px #38bdf8;
            animation: shardFly 0.6s ease-out forwards;
        }

        @keyframes shardFly {
            0% { opacity: 1; transform: translate(0, 0) scale(1) rotate(0deg); }
            100% { opacity: 0; transform: translate(var(--dx), var(--dy)) scale(0) rotate(360deg); }
        }

        @media screen and (max-width: 900px) { 
            .hero { flex-direction: column-reverse; text-align: center; padding-top: 40px; } 
            .hero h1 { font-size: 42px; } 
            .hero h2 { font-size: 22px; } 
            .hero p { margin-left: auto; margin-right: auto; }
            .action-buttons { justify-content: center; }
            .hero-image img { width: 230px; height: 230px; }
            .hero-image-wrapper::before { width: 250px; height: 250px; }
            .navbar { flex-direction: column; gap: 15px; }
            .nav-menu { gap: 18px; flex-wrap: wrap; justify-content: center; }
        } 
    </style>
</head>

<body>

    <!-- Dynamic Cursor Ambient Light Orb -->
    <div class="cursor-light-orb" id="cursorOrb"></div>

    <!-- Scroll Progress Bar -->
    <div class="progress-bar" id="progressBar"></div>

    <!-- Animated Aurora Background -->
    <div class="aurora-bg"></div>

    <!-- Canvas Animasi Es/Salju Jatuh Interaktif -->
    <canvas id="snowCanvas"></canvas>

    <!-- Canvas Freeze Overlay Interaktif -->
    <canvas id="freezeCanvas"></canvas>

    <header>
        <nav class="navbar">
            <a href="#beranda" class="logo">
                <i class="fa-regular fa-snowflake"></i> LIN LIN
            </a>
            <ul class="nav-menu">
                <li><a href="#beranda" class="active"><i class="fa-solid fa-house"></i> Beranda</a></li>
                <li><a href="#tentang"><i class="fa-solid fa-user"></i> Tentang Saya</a></li>
                <li><a href="#citacita"><i class="fa-solid fa-rocket"></i> Cita-Cita</a></li>
                <li><a href="#target"><i class="fa-solid fa-bullseye"></i> Target Masa Depan</a></li>
                <li><a href="#keahlian"><i class="fa-solid fa-code"></i> Keahlian</a></li>
                <li><a href="#kontak"><i class="fa-solid fa-envelope"></i> Kontak</a></li>
            </ul>
        </nav>
    </header>

    <section id="beranda" class="hero">
        <div class="hero-text" data-speed="0.12">
            <div class="sapaan">
                <i class="fa-solid fa-wand-magic-sparkles"></i> Selamat Datang di Portofolio Saya
            </div>
            <h1>Lin Lin</h1>
            <h2></h2>
            <p>Siswa jurusan Pengembangan Perangkat Lunak dan Gim (PPLG) yang berdedikasi menciptakan pengalaman web modern, futuristik, dan interaktif berestetika kristal es.</p>
            
            <div class="action-buttons">
                <a href="#tentang" class="tombol magnetic-element">
                    <span>Jelajahi Profil</span> <i class="fa-solid fa-arrow-down"></i>
                </a>
                <button class="tombol secondary magnetic-element" id="freezeToggleBtn">
                    <i class="fa-solid fa-icicles"></i> <span>Bekukan Layar</span>
                </button>
            </div>
        </div>

        <div class="hero-image" data-speed="-0.08">
            <div class="hero-image-wrapper magnetic-element" id="heroImageWrapper">
                <img src="https://media3.giphy.com/media/v1.Y2lkPTc5MGI3NjExb2s4aWN4YW1xYzIwZzAxMTE4cncydmpiNmQ5N24xMjNnajJ4YXMxciZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/eSPEwBxWml5O8OZQAD/giphy.gif" alt="Foto Profil Lin Lin">
            </div>
        </div>
    </section>

    <div class="tentang-bg">
        <section id="tentang" class="section-container reveal">
            <h2 class="judul"><i class="fa-regular fa-snowflake"></i> Informasi Profil Interaktif</h2>
            <p class="sub-judul">Klik tab di bawah untuk melihat rincian informasi profil saya</p>

            <!-- TAB NAVIGATION -->
            <div class="tabs-nav">
                <button class="tab-btn active magnetic-element" data-tab="tab-ringkasan">
                    <i class="fa-solid fa-address-card"></i> Ringkasan Diri
                </button>
                <button class="tab-btn magnetic-element" data-tab="tab-keahlian">
                    <i class="fa-solid fa-table-list"></i> Tabel Keahlian
                </button>
                <button class="tab-btn magnetic-element" data-tab="tab-hobi">
                    <i class="fa-solid fa-gamepad"></i> Hobi & Minat
                </button>
            </div>

            <!-- TAB CONTENT 1: RINGKASAN DIRI -->
            <div id="tab-ringkasan" class="tab-content active">
                <div class="tentang-container">
                    <div class="card">
                        <div class="card-spotlight"></div>
                        <h3><i class="fa-solid fa-user-graduate"></i> Perkenalan</h3>
                        <p>Halo! Nama saya <strong>Lin Lin</strong>. Saya adalah seorang siswa jurusan <strong>Pengembangan Perangkat Lunak dan Gim (PPLG)</strong> di <strong>SMK Negeri 2 Magelang</strong>.</p>
                        <br>
                        <p>Saya sangat antusias mempelajari pemrograman web frontend, eksperimen desain UI/UX, serta pemanfaatan teknologi AI untuk pengembangan aplikasi modern.</p>
                    </div>

                    <div class="card">
                        <div class="card-spotlight"></div>
                        <h3><i class="fa-solid fa-bullseye"></i> Visi & Misi</h3>
                        <p><strong>Visi:</strong> Menjadi pengembang perangkat lunak profesional yang mampu menciptakan solusi digital yang estetis dan berkinerja tinggi.</p>
                        <br>
                        <p><strong>Misi:</strong> Terus mengasah pemahaman algoritma, memperdalam teknologi web modern, dan menguasai pembuatan game interaktif.</p>
                    </div>

                    <div class="card">
                        <div class="card-spotlight"></div>
                        <h3><i class="fa-solid fa-building-columns"></i> Pendidikan</h3>
                        <p><strong>Institusi:</strong> SMK Negeri 2 Magelang</p>
                        <p><strong>Jurusan:</strong> Pengembangan Perangkat Lunak dan Gim (PPLG)</p>
                        <p><strong>Status:</strong> Siswa Aktif</p>
                        <p><strong>Tahun:</strong> 2026 - Sekarang</p>
                    </div>
                </div>
            </div>

            <!-- TAB CONTENT 2: TABEL KEAHLIAN (INTERACTIVE FROST TABLE) -->
            <div id="tab-keahlian" class="tab-content">
                <div class="table-responsive">
                    <table class="ice-table">
                        <thead>
                            <tr>
                                <th>Teknologi / Skill</th>
                                <th>Kategori</th>
                                <th>Tingkat Penguasaan</th>
                                <th>Status Skill</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr>
                                <td><i class="fa-brands fa-html5" style="color: #e34f26; margin-right: 8px;"></i> HTML5</td>
                                <td>Frontend Web</td>
                                <td>75% (Baik)</td>
                                <td><span class="badge badge-advanced"><i class="fa-solid fa-circle-check"></i> Menguasai</span></td>
                            </tr>
                            <tr>
                                <td><i class="fa-brands fa-css3-alt" style="color: #1572b6; margin-right: 8px;"></i> CSS3 & Glassmorphism</td>
                                <td>Styling & UI Design</td>
                                <td>60% (Menengah)</td>
                                <td><span class="badge badge-intermediate"><i class="fa-solid fa-spinner"></i> Aktif Belajar</span></td>
                            </tr>
                            <tr>
                                <td><i class="fa-brands fa-js" style="color: #f7df1e; margin-right: 8px;"></i> JavaScript Interaktif & Canvas</td>
                                <td>Programming</td>
                                <td>55% (Menengah)</td>
                                <td><span class="badge badge-intermediate"><i class="fa-solid fa-spinner"></i> Aktif Belajar</span></td>
                            </tr>
                            <tr>
                                <td><i class="fa-solid fa-robot" style="color: #a5f3fc; margin-right: 8px;"></i> Prompt Engineering & Web UI/UX</td>
                                <td>Productivity & Design</td>
                                <td>95% (Sangat Baik)</td>
                                <td><span class="badge badge-advanced"><i class="fa-solid fa-circle-check"></i> Menguasai</span></td>
                            </tr>
                        </tbody>
                    </table>
                </div>
            </div>

            <!-- TAB CONTENT 3: HOBI & MINAT -->
            <div id="tab-hobi" class="tab-content">
                <div class="tentang-container">
                    <div class="card">
                        <div class="card-spotlight"></div>
                        <h3><i class="fa-solid fa-laptop-code"></i> Belajar Teknologi Web</h3>
                        <p>Eksplorasi sintaks baru, animasi CSS3, manipulasi HTML Canvas, dan arsitektur web modern.</p>
                    </div>

                    <div class="card">
                        <div class="card-spotlight"></div>
                        <h3><i class="fa-solid fa-gamepad"></i> Bermain Game</h3>
                        <p>Menikmati game platformer, simulasi, dan dunia Roblox untuk mengamati mekanisme game dan level design.</p>
                    </div>

                    <div class="card">
                        <div class="card-spotlight"></div>
                        <h3><i class="fa-solid fa-headphones"></i> Mendengarkan Musik</h3>
                        <p>Mendengarkan musik favorit sambil menulis kode program untuk menjaga kestabilan fokus dan kreativitas.</p>
                    </div>
                </div>
            </div>
        </section>
    </div>

    <!-- SECTION CITA-CITA -->
    <section id="citacita" class="section-container reveal">
        <h2 class="judul"><i class="fa-solid fa-star"></i> Cita-Cita Impian</h2>
        <p class="sub-judul">Impian karir dan keahlian profesional yang ingin dicapai Lin Lin</p>

        <div class="tentang-container">
            <div class="card">
                <div class="card-spotlight"></div>
                <h3><i class="fa-solid fa-laptop-code"></i> Senior Full-Stack Web Developer</h3>
                <p><strong>Penjelasan:</strong> Pengembang web ahli yang menguasai pembuatan tampilan depan (Frontend) yang menarik sekaligus logika sistem belakang (Backend) yang cepat dan aman untuk membangun aplikasi web berskala besar.</p>
            </div>

            <div class="card">
                <div class="card-spotlight"></div>
                <h3><i class="fa-solid fa-gamepad"></i> Indie Game Developer</h3>
                <p><strong>Penjelasan:</strong> Pembuat game mandiri yang merancang serta merilis game buatan sendiri, mulai dari ide cerita, karakter, hingga alur permainan yang seru dan kreatif.</p>
            </div>

            <div class="card">
                <div class="card-spotlight"></div>
                <h3><i class="fa-solid fa-wand-magic-sparkles"></i> Specialist UI/UX & AI Integrator</h3>
                <p><strong>Penjelasan:</strong> Ahli desain tampilan aplikasi yang mudah digunakan oleh pengguna, serta mampu memanfaatkan kecerdasan buatan (AI) untuk membuat aplikasi menjadi lebih pintar dan otomatis.</p>
            </div>
        </div>
    </section>

    <!-- SECTION TARGET MASA DEPAM -->
    <div class="tentang-bg">
        <section id="target" class="section-container reveal">
            <h2 class="judul"><i class="fa-solid fa-graduation-cap"></i> Target Masa Depan</h2>
            <p class="sub-judul">Langkah nyata pendidikan lanjutan untuk mendukung cita-cita</p>

            <div style="max-width: 800px; margin: auto;" class="card">
                <div class="card-spotlight"></div>
                <h3><i class="fa-solid fa-university"></i> Melanjutkan Pendidikan di ITB</h3>
                <p style="font-size: 16px; line-height: 1.8;">
                    Setelah menyelesaikan pendidikan di SMK Negeri 2 Magelang, target utama Lin Lin adalah melanjutkan studi ke <strong>ITB (Institut Teknologi Bandung)</strong> secara langsung pada program studi berfokus pada teknologi informasi dan komputer untuk memperdalam ilmu rekayasa perangkat lunak serta membangun fondasi karir profesional.
                </p>
            </div>
        </section>
    </div>

    <section id="keahlian" class="section-container reveal">
        <h2 class="judul"><i class="fa-solid fa-chart-line"></i> Progres Keahlian Utama</h2>
        <p class="sub-judul">Persentase penguasaan teknologi yang dipelajari</p>

        <div style="max-width: 800px; margin: auto;" class="card">
            <div class="card-spotlight"></div>
            <div class="skill-item">
                <div class="skill-info">
                    <span><i class="fa-brands fa-html5"></i> HTML5 (Semantik & Struktur Web)</span>
                    <span>75%</span>
                </div>
                <div class="progress-bar-bg">
                    <div class="progress-bar-fill" data-progress="75%"></div>
                </div>
            </div>

            <div class="skill-item">
                <div class="skill-info">
                    <span><i class="fa-brands fa-css3-alt"></i> CSS3 (Glassmorphism, Flexbox, Animation)</span>
                    <span>60%</span>
                </div>
                <div class="progress-bar-bg">
                    <div class="progress-bar-fill" data-progress="60%"></div>
                </div>
            </div>

            <div class="skill-item">
                <div class="skill-info">
                    <span><i class="fa-brands fa-js"></i> JavaScript Interaktif & Canvas</span>
                    <span>55%</span>
                </div>
                <div class="progress-bar-bg">
                    <div class="progress-bar-fill" data-progress="55%"></div>
                </div>
            </div>

            <div class="skill-item">
                <div class="skill-info">
                    <span><i class="fa-solid fa-robot"></i> Prompt Engineering & Web UI/UX</span>
                    <span>95%</span>
                </div>
                <div class="progress-bar-bg">
                    <div class="progress-bar-fill" data-progress="95%"></div>
                </div>
            </div>
        </div>
    </section>

    <section id="kontak" class="section-container reveal">
        <h2 class="judul"><i class="fa-solid fa-paper-plane"></i> Kontak Saya</h2>
        <p class="sub-judul">Jangan ragu untuk menghubungi saya melalui saluran informasi di bawah ini</p>

        <div class="kontak-grid">
            <div class="kontak-card">
                <div class="card-spotlight"></div>
                <div class="kontak-icon">
                    <i class="fa-solid fa-school"></i>
                </div>
                <h4>Sekolah</h4>
                <p>SMK Negeri 2 Magelang</p>
            </div>

            <div class="kontak-card">
                <div class="card-spotlight"></div>
                <div class="kontak-icon">
                    <i class="fa-solid fa-envelope"></i>
                </div>
                <h4>Email</h4>
                <a href="mailto:Evelynfineshyt@gmail.com">Evelynfineshyt@gmail.com</a>
            </div>

            <div class="kontak-card">
                <div class="card-spotlight"></div>
                <div class="kontak-icon">
                    <i class="fa-brands fa-instagram"></i>
                </div>
                <h4>Instagram</h4>
                <a href="https://instagram.com" target="_blank">@Evelyns</a>
            </div>
        </div>
    </section>

    <footer>
        <p>&copy; 2026 Lin Lin | Dibuat dengan HTML5, CSS3 Glassmorphism & JavaScript ❄️</p>
    </footer>

    <audio id="bgMusic" loop preload="none">
        <source src="original sound - spadeclipping_19_musicaldown.com_1791442792.mp3" type="audio/mpeg">
    </audio>

    <div class="floating-socials">
        <a href="https://www.tiktok.com/@linevelyns" target="_blank" class="social-btn tiktok magnetic-element" title="Ikuti di TikTok">
            <i class="fa-brands fa-tiktok"></i>
        </a>
        <a href="https://www.roblox.com/users/profile?username=lintangbai106" target="_blank" class="social-btn roblox magnetic-element" title="Profil Roblox">
            <i class="fa-solid fa-cube"></i>
        </a>
        <button class="music-player magnetic-element" id="musicButton" type="button" aria-label="Putar Musik Background" title="Putar / Hentikan Musik">
            <i class="fa-solid fa-music music-icon"></i>
        </button>
    </div>

    <script>
        document.addEventListener("DOMContentLoaded", () => {
            let isMusicPlaying = false;

            /* SINTESIS AUDIO EFEK DENTING ES BERFREKUENSI GANDA (WEB AUDIO API) */
            function playIceChimeSound() {
                try {
                    const audioCtx = new (window.AudioContext || window.webkitAudioContext)();
                    const osc1 = audioCtx.createOscillator();
                    const osc2 = audioCtx.createOscillator();
                    const gain = audioCtx.createGain();

                    osc1.type = 'sine';
                    osc2.type = 'triangle';

                    osc1.frequency.setValueAtTime(1800, audioCtx.currentTime); 
                    osc1.frequency.exponentialRampToValueAtTime(3200, audioCtx.currentTime + 0.18);

                    osc2.frequency.setValueAtTime(2400, audioCtx.currentTime); 
                    osc2.frequency.exponentialRampToValueAtTime(4200, audioCtx.currentTime + 0.18);

                    gain.gain.setValueAtTime(0.15, audioCtx.currentTime);
                    gain.gain.exponentialRampToValueAtTime(0.001, audioCtx.currentTime + 0.28);

                    osc1.connect(gain);
                    osc2.connect(gain);
                    gain.connect(audioCtx.destination);

                    osc1.start();
                    osc2.start();
                    osc1.stop(audioCtx.currentTime + 0.28);
                    osc2.stop(audioCtx.currentTime + 0.28);
                } catch (e) {}
            }

            /* EFEK LEDAKAN KRISTAL ES (CRYSTAL BURST) */
            function createIceBurst(x, y) {
                const shardCount = 16;
                for (let i = 0; i < shardCount; i++) {
                    const shard = document.createElement('div');
                    shard.className = 'ice-shard';
                    const size = Math.random() * 8 + 4;
                    const angle = (Math.PI * 2 / shardCount) * i;
                    const dist = Math.random() * 80 + 35;
                    const dx = Math.cos(angle) * dist + 'px';
                    const dy = Math.sin(angle) * dist + 'px';

                    shard.style.width = `${size}px`;
                    shard.style.height = `${size}px`;
                    shard.style.left = `${x}px`;
                    shard.style.top = `${y}px`;
                    shard.style.setProperty('--dx', dx);
                    shard.style.setProperty('--dy', dy);

                    document.body.appendChild(shard);
                    setTimeout(() => shard.remove(), 600);
                }
            }

            /* 1. TYPING EFFECT UNTUK SUBTITLE HERO */
            const heroSubtitle = document.querySelector('.hero h2');
            const textArray = [
                "Siswa PPLG SMKN 2 Magelang", 
                "Frontend Web Developer Enthusiast", 
                "Pecinta UI/UX Futuristic Glassmorphism"
            ];
            let textIndex = 0, charIndex = 0, isDeleting = false;

            function typeEffect() {
                const currentText = textArray[textIndex];
                if (isDeleting) {
                    heroSubtitle.textContent = currentText.substring(0, charIndex - 1);
                    charIndex--;
                } else {
                    heroSubtitle.textContent = currentText.substring(0, charIndex + 1);
                    charIndex++;
                }

                let speed = isDeleting ? 40 : 80;
                if (!isDeleting && charIndex === currentText.length) {
                    speed = 2200;
                    isDeleting = true;
                } else if (isDeleting && charIndex === 0) {
                    isDeleting = false;
                    textIndex = (textIndex + 1) % textArray.length;
                    speed = 400;
                }
                setTimeout(typeEffect, speed);
            }
            typeEffect();

            /* 2. INTERACTIVE SNOW PHYSICS CANVAS WITH MOUSE & MUSIC INTERACTION */
            const canvas = document.getElementById("snowCanvas");
            const ctx = canvas.getContext("2d");
            let width = (canvas.width = window.innerWidth);
            let height = (canvas.height = window.innerHeight);

            let mouseX = -1000;
            let mouseY = -1000;

            const cursorOrb = document.getElementById('cursorOrb');

            window.addEventListener("resize", () => {
                width = canvas.width = window.innerWidth;
                height = canvas.height = window.innerHeight;
            });

            window.addEventListener("mousemove", (e) => {
                mouseX = e.clientX;
                mouseY = e.clientY;

                if (cursorOrb) {
                    cursorOrb.style.left = `${mouseX}px`;
                    cursorOrb.style.top = `${mouseY}px`;
                }
            });

            const numFlakes = 130;
            const flakes = [];

            for (let i = 0; i < numFlakes; i++) {
                flakes.push({
                    x: Math.random() * width,
                    y: Math.random() * height,
                    r: Math.random() * 3.5 + 1,
                    d: Math.random() * numFlakes,
                    vx: 0,
                    vy: 0
                });
            }

            function drawSnow() {
                ctx.clearRect(0, 0, width, height);
                ctx.fillStyle = "rgba(224, 242, 254, 0.85)";
                ctx.beginPath();

                for (let i = 0; i < numFlakes; i++) {
                    const f = flakes[i];
                    ctx.moveTo(f.x, f.y);
                    ctx.arc(f.x, f.y, f.r, 0, Math.PI * 2, true);
                }
                ctx.fill();
                moveSnow();
            }

            let angle = 0;
            function moveSnow() {
                angle += 0.01;
                const speedBoost = isMusicPlaying ? 1.8 : 1.0;

                for (let i = 0; i < numFlakes; i++) {
                    const f = flakes[i];

                    const dx = f.x - mouseX;
                    const dy = f.y - mouseY;
                    const dist = Math.sqrt(dx * dx + dy * dy);
                    const maxDist = 140;

                    if (dist < maxDist) {
                        const force = (maxDist - dist) / maxDist;
                        f.vx += (dx / dist) * force * 3;
                        f.vy += (dy / dist) * force * 3;
                    }

                    f.y += (Math.cos(angle + f.d) + 1.2 + f.r / 2 + f.vy) * speedBoost;
                    f.x += Math.sin(angle) * 1.5 + f.vx;

                    f.vx *= 0.91;
                    f.vy *= 0.91;

                    if (f.x > width + 10 || f.x < -10 || f.y > height) {
                        flakes[i] = {
                            x: Math.random() * width,
                            y: -10,
                            r: f.r,
                            d: f.d,
                            vx: 0,
                            vy: 0
                        };
                    }
                }
            }

            function animateSnow() {
                drawSnow();
                requestAnimationFrame(animateSnow);
            }
            animateSnow();

            /* SHOCKWAVE BLAST PADA SALJU SAAT DIKLIK */
            window.addEventListener('click', (e) => {
                for (let i = 0; i < numFlakes; i++) {
                    const f = flakes[i];
                    const dx = f.x - e.clientX;
                    const dy = f.y - e.clientY;
                    const dist = Math.sqrt(dx * dx + dy * dy);
                    if (dist < 220) {
                        const force = (220 - dist) / 220;
                        f.vx += (dx / (dist || 1)) * force * 15;
                        f.vy += (dy / (dist || 1)) * force * 15;
                    }
                }
            });

            /* 3. FREEZE SCREEN OVERLAY EFFECT WITH TEXT INSTRUCTIONS & SCRATCHING */
            const freezeCanvas = document.getElementById('freezeCanvas');
            const freezeCtx = freezeCanvas.getContext('2d');
            const freezeBtn = document.getElementById('freezeToggleBtn');
            let isFrozen = false;
            let isMousedown = false;

            function initFreezeCanvas() {
                freezeCanvas.width = window.innerWidth;
                freezeCanvas.height = window.innerHeight;
            }
            initFreezeCanvas();
            window.addEventListener('resize', initFreezeCanvas);

            function fillFrostOverlay() {
                freezeCtx.save();
                freezeCtx.fillStyle = 'rgba(165, 243, 252, 0.45)';
                freezeCtx.fillRect(0, 0, freezeCanvas.width, freezeCanvas.height);
                
                freezeCtx.strokeStyle = 'rgba(255, 255, 255, 0.7)';
                freezeCtx.lineWidth = 1.5;
                for (let i = 0; i < 55; i++) {
                    freezeCtx.beginPath();
                    const x = Math.random() * freezeCanvas.width;
                    const y = Math.random() * freezeCanvas.height;
                    freezeCtx.arc(x, y, Math.random() * 90 + 20, 0, Math.PI * 2);
                    freezeCtx.stroke();
                }

                // Teks instruksi di tengah
                freezeCtx.fillStyle = '#ffffff';
                freezeCtx.font = 'bold 24px "Plus Jakarta Sans", sans-serif';
                freezeCtx.textAlign = 'center';
                freezeCtx.shadowColor = '#0284c7';
                freezeCtx.shadowBlur = 15;
                freezeCtx.fillText('❄️ Usap/Gosok Layar untuk Mencairkan Es! ❄️', freezeCanvas.width / 2, freezeCanvas.height / 2);
                freezeCtx.restore();
            }

            if (freezeBtn) {
                freezeBtn.addEventListener('click', (e) => {
                    playIceChimeSound();
                    createIceBurst(e.clientX, e.clientY);
                    isFrozen = !isFrozen;
                    if (isFrozen) {
                        fillFrostOverlay();
                        freezeCanvas.classList.add('active');
                        freezeBtn.querySelector('span').textContent = "Cairkan Es";
                    } else {
                        freezeCanvas.classList.remove('active');
                        freezeBtn.querySelector('span').textContent = "Bekukan Layar";
                    }
                });
            }

            function scratchFrost(x, y) {
                if (!isFrozen) return;
                freezeCtx.globalCompositeOperation = 'destination-out';
                freezeCtx.beginPath();
                freezeCtx.arc(x, y, 60, 0, Math.PI * 2);
                freezeCtx.fill();
                freezeCtx.globalCompositeOperation = 'source-over';

                if(Math.random() > 0.4) {
                    playIceChimeSound();
                }
            }

            freezeCanvas.addEventListener('mousedown', (e) => { isMousedown = true; scratchFrost(e.clientX, e.clientY); });
            freezeCanvas.addEventListener('mousemove', (e) => { if (isMousedown) scratchFrost(e.clientX, e.clientY); });
            freezeCanvas.addEventListener('mouseup', () => { isMousedown = false; });

            freezeCanvas.addEventListener('touchstart', (e) => { isMousedown = true; scratchFrost(e.touches[0].clientX, e.touches[0].clientY); });
            freezeCanvas.addEventListener('touchmove', (e) => { if (isMousedown) scratchFrost(e.touches[0].clientX, e.touches[0].clientY); });
            freezeCanvas.addEventListener('touchend', () => { isMousedown = false; });

            /* 4. PARALLAX SCROLL & SCROLL PROGRESS BAR */
            const progressBar = document.getElementById('progressBar');
            const parallaxElements = document.querySelectorAll('[data-speed]');

            window.addEventListener('scroll', () => {
                const scrollTop = window.scrollY;
                const docHeight = document.documentElement.scrollHeight - window.innerHeight;
                const scrollPercent = (scrollTop / docHeight) * 100;
                
                if (progressBar) {
                    progressBar.style.width = scrollPercent + '%';
                }

                parallaxElements.forEach(el => {
                    const speed = parseFloat(el.getAttribute('data-speed'));
                    el.style.transform = `translateY(${scrollTop * speed}px)`;
                });
            });

            /* 5. TAB SYSTEM INTERACTIVE SWITCHING */
            const tabBtns = document.querySelectorAll('.tab-btn');
            const tabContents = document.querySelectorAll('.tab-content');

            tabBtns.forEach(btn => {
                btn.addEventListener('click', (e) => {
                    playIceChimeSound();
                    createIceBurst(e.clientX, e.clientY);
                    const targetTab = btn.getAttribute('data-tab');

                    tabBtns.forEach(b => b.classList.remove('active'));
                    tabContents.forEach(c => c.classList.remove('active'));

                    btn.classList.add('active');
                    document.getElementById(targetTab).classList.add('active');
                });
            });

            /* 6. SCROLL REVEAL ANIMATION & SKILL BAR ANIMATION */
            const reveals = document.querySelectorAll('.reveal');
            const progressFills = document.querySelectorAll('.progress-bar-fill');

            function checkReveal() {
                const windowHeight = window.innerHeight;
                const revealPoint = 130;

                reveals.forEach(reveal => {
                    const revealTop = reveal.getBoundingClientRect().top;
                    if (revealTop < windowHeight - revealPoint) {
                        reveal.classList.add('active');
                    }
                });

                progressFills.forEach(fill => {
                    const rect = fill.getBoundingClientRect();
                    if (rect.top < windowHeight && rect.bottom >= 0) {
                        const targetWidth = fill.getAttribute('data-progress');
                        fill.style.width = targetWidth;
                    }
                });
            }

            window.addEventListener('scroll', checkReveal);
            checkReveal();

            /* 7. HIGHLIGHT NAVBAR ITEM ON SCROLL */
            const sections = document.querySelectorAll('section');
            const navLinks = document.querySelectorAll('.nav-menu a');

            window.addEventListener('scroll', () => {
                let current = '';
                sections.forEach(section => {
                    const sectionTop = section.offsetTop - 150;
                    if (window.scrollY >= sectionTop) {
                        current = section.getAttribute('id');
                    }
                });

                navLinks.forEach(link => {
                    link.classList.remove('active');
                    if (link.getAttribute('href') === `#${current}`) {
                        link.classList.add('active');
                    }
                });
            });

            /* 8. 3D TILT EFFECT & SPOTLIGHT ON CARDS */
            const cards = document.querySelectorAll('.card, .kontak-card');
            cards.forEach(card => {
                card.addEventListener('mousemove', (e) => {
                    const rect = card.getBoundingClientRect();
                    const x = e.clientX - rect.left;
                    const y = e.clientY - rect.top;
                    
                    card.style.setProperty('--mouse-x', `${x}px`);
                    card.style.setProperty('--mouse-y', `${y}px`);

                    const centerX = rect.width / 2;
                    const centerY = rect.height / 2;
                    const rotateX = (y - centerY) / 12;
                    const rotateY = (centerX - x) / 12;

                    card.style.transform = `perspective(1000px) rotateX(${rotateX}deg) rotateY(${rotateY}deg) translateY(-6px)`;
                });

                card.addEventListener('mouseleave', () => {
                    card.style.transform = 'perspective(1000px) rotateX(0) rotateY(0) translateY(0)';
                });
            });

            /* MAGNETIC BUTTONS / ELEMENTS EFFECT */
            const magneticElems = document.querySelectorAll('.magnetic-element');
            magneticElems.forEach(elem => {
                elem.addEventListener('mousemove', (e) => {
                    const rect = elem.getBoundingClientRect();
                    const x = e.clientX - rect.left - rect.width / 2;
                    const y = e.clientY - rect.top - rect.height / 2;
                    elem.style.transform = `translate(${x * 0.28}px, ${y * 0.28}px)`;
                });
                elem.addEventListener('mouseleave', () => {
                    elem.style.transform = 'translate(0px, 0px)';
                });
            });

            /* INTERAKTIF KLIK FOTO PROFIL (EFEK REACTION) */
            const heroWrapper = document.getElementById('heroImageWrapper');
            if(heroWrapper) {
                heroWrapper.addEventListener('click', (e) => {
                    playIceChimeSound();
                    createIceBurst(e.clientX, e.clientY);
                });
            }

            /* 9. CURSOR CRYSTAL SPARKLE TRAIL */
            document.addEventListener('mousemove', (e) => {
                if (Math.random() > 0.65) {
                    const p = document.createElement('span');
                    p.textContent = ['❄', '✨', '🧊', '✦', '✧'][Math.floor(Math.random() * 5)];
                    p.style.cssText = `position:fixed;left:${e.clientX}px;top:${e.clientY}px;font-size:${Math.random()*14+10}px;pointer-events:none;z-index:9998;opacity:0.9;color:#a5f3fc;text-shadow:0 0 10px #38bdf8;transition:all 0.9s linear;`;
                    document.body.appendChild(p);
                    setTimeout(() => {
                        p.style.transform = `translateY(${Math.random()*40+20}px) scale(0)`;
                        p.style.opacity = '0';
                    }, 50);
                    setTimeout(() => p.remove(), 950);
                }
            });

            /* 10. WATER/ICE RIPPLE CLICK EFFECT */
            document.addEventListener('click', (e) => {
                const ripple = document.createElement('div');
                ripple.className = 'click-ripple';
                ripple.style.left = `${e.clientX}px`;
                ripple.style.top = `${e.clientY}px`;
                document.body.appendChild(ripple);
                setTimeout(() => ripple.remove(), 600);
            });

            /* 11. MUSIC PLAYER CONTROL */
            const music = document.getElementById("bgMusic");
            const musicBtn = document.getElementById("musicButton");
            const musicIcon = musicBtn.querySelector(".music-icon");

            musicBtn.addEventListener("click", (e) => {
                playIceChimeSound();
                createIceBurst(e.clientX, e.clientY);
                if (music.paused) {
                    music.play().then(() => {
                        isMusicPlaying = true;
                        musicBtn.classList.add("playing");
                        musicIcon.className = "fa-solid fa-compact-disc fa-spin music-icon";
                    }).catch(() => {
                        alert("Gagal memutar audio. Pastikan file audio tersedia.");
                    });
                } else {
                    music.pause();
                    isMusicPlaying = false;
                    musicBtn.classList.remove("playing");
                    musicIcon.className = "fa-solid fa-music music-icon";
                }
            });
        });
    </script>
</body>
</html>
