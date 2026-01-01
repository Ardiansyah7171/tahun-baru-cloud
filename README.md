<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cloud Tahun Baru 2026 - GitHub Pages</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', system-ui, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #0c0c2e 0%, #1a1a3e 50%, #2d1b69 100%);
            color: #fff;
            min-height: 100vh;
            overflow-x: hidden;
        }
        
        /* Efek Kembang Api */
        .fireworks {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 1;
        }
        
        .firework {
            position: absolute;
            width: 5px;
            height: 5px;
            border-radius: 50%;
            box-shadow: 0 0 10px #fff;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
            position: relative;
            z-index: 2;
        }
        
        header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
            margin-bottom: 30px;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .logo {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .logo i {
            font-size: 2.8rem;
            color: #ffd700;
            filter: drop-shadow(0 0 10px rgba(255, 215, 0, 0.5));
        }
        
        .logo h1 {
            font-size: 2rem;
            background: linear-gradient(to right, #ffd700, #ff8c00, #ff4500);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            text-shadow: 0 0 15px rgba(255, 215, 0, 0.3);
        }
        
        .github-badge {
            display: flex;
            align-items: center;
            gap: 8px;
            background: rgba(255, 255, 255, 0.1);
            padding: 8px 15px;
            border-radius: 50px;
            text-decoration: none;
            color: white;
            font-weight: 600;
            backdrop-filter: blur(10px);
            transition: all 0.3s;
        }
        
        .github-badge:hover {
            background: rgba(255, 255, 255, 0.15);
            transform: translateY(-2px);
        }
        
        .new-year-badge {
            background: linear-gradient(45deg, #ff0000, #ff8c00, #ffd700);
            padding: 8px 20px;
            border-radius: 50px;
            font-weight: bold;
            font-size: 1.2rem;
            animation: glow 2s infinite alternate;
        }
        
        @keyframes glow {
            from { box-shadow: 0 0 10px #ff4500; }
            to { box-shadow: 0 0 20px #ffd700, 0 0 30px #ff8c00; }
        }
        
        .user-info {
            display: flex;
            align-items: center;
            gap: 10px;
            background-color: rgba(255, 255, 255, 0.1);
            padding: 10px 20px;
            border-radius: 50px;
            backdrop-filter: blur(10px);
        }
        
        .user-info i {
            color: #ffd700;
            font-size: 1.5rem;
        }
        
        .new-year-message {
            background: linear-gradient(45deg, rgba(255, 140, 0, 0.2), rgba(255, 215, 0, 0.2));
            border-left: 5px solid #ffd700;
            padding: 25px;
            border-radius: 15px;
            margin-bottom: 30px;
            text-align: center;
            backdrop-filter: blur(5px);
        }
        
        .new-year-message h2 {
            font-size: 2.2rem;
            margin-bottom: 10px;
            background: linear-gradient(to right, #ffd700, #ff8c00);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }
        
        .new-year-message p {
            font-size: 1.1rem;
            color: rgba(255, 255, 255, 0.9);
        }
        
        .countdown {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-bottom: 40px;
        }
        
        .countdown-item {
            background: rgba(255, 255, 255, 0.1);
            padding: 25px 15px;
            border-radius: 15px;
            min-width: 100px;
            text-align: center;
            backdrop-filter: blur(5px);
            border: 1px solid rgba(255, 215, 0, 0.2);
            transition: transform 0.3s;
        }
        
        .countdown-item:hover {
            transform: translateY(-10px);
            background: rgba(255, 255, 255, 0.15);
        }
        
        .countdown-number {
            font-size: 2.8rem;
            font-weight: bold;
            color: #ffd700;
            text-shadow: 0 0 10px rgba(255, 215, 0, 0.5);
        }
        
        .countdown-label {
            font-size: 1rem;
            color: rgba(255, 255, 255, 0.8);
            margin-top: 5px;
        }
        
        .storage-info {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            padding: 25px;
            margin-bottom: 30px;
            backdrop-filter: blur(5px);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .storage-info h2 {
            margin-bottom: 15px;
            color: #ffd700;
            font-size: 1.5rem;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .storage-bar {
            height: 20px;
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 10px;
            margin-bottom: 10px;
            overflow: hidden;
        }
        
        .storage-used {
            height: 100%;
            background: linear-gradient(to right, #ff8c00, #ffd700);
            border-radius: 10px;
            width: 65%;
            transition: width 0.5s ease;
            position: relative;
            overflow: hidden;
        }
        
        .storage-used::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
            animation: shimmer 2s infinite;
        }
        
        @keyframes shimmer {
            0% { transform: translateX(-100%); }
            100% { transform: translateX(100%); }
        }
        
        .storage-stats {
            display: flex;
            justify-content: space-between;
            color: rgba(255, 255, 255, 0.8);
            font-size: 0.9rem;
        }
        
        .action-buttons {
            display: flex;
            gap: 15px;
            margin-bottom: 30px;
            flex-wrap: wrap;
        }
        
        .btn {
            padding: 14px 28px;
            border: none;
            border-radius: 10px;
            font-weight: 600;
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 10px;
            transition: all 0.3s ease;
            font-size: 1rem;
        }
        
        .btn-primary {
            background: linear-gradient(45deg, #ff8c00, #ffd700);
            color: #0c0c2e;
        }
        
        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(255, 140, 0, 0.3);
        }
        
        .btn-secondary {
            background: rgba(255, 255, 255, 0.1);
            color: white;
            border: 1px solid rgba(255, 215, 0, 0.3);
        }
        
        .btn-secondary:hover {
            background: rgba(255, 255, 255, 0.15);
            transform: translateY(-3px);
        }
        
        .files-container {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            padding: 25px;
            margin-bottom: 30px;
            backdrop-filter: blur(5px);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .files-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
        }
        
        .files-header h2 {
            color: #ffd700;
            font-size: 1.5rem;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .search-box {
            display: flex;
            align-items: center;
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 10px;
            padding: 10px 15px;
            width: 300px;
            border: 1px solid rgba(255, 215, 0, 0.2);
        }
        
        .search-box i {
            color: #ffd700;
            margin-right: 10px;
        }
        
        .search-box input {
            border: none;
            background: transparent;
            width: 100%;
            outline: none;
            color: white;
        }
        
        .search-box input::placeholder {
            color: rgba(255, 255, 255, 0.6);
        }
        
        .files-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 20px;
        }
        
        .file-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            padding: 20px;
            transition: all 0.3s ease;
            border: 1px solid rgba(255, 255, 255, 0.05);
            position: relative;
            overflow: hidden;
        }
        
        .file-card:hover {
            transform: translateY(-10px);
            background: rgba(255, 255, 255, 0.08);
            border-color: rgba(255, 215, 0, 0.3);
        }
        
        .file-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 4px;
            background: linear-gradient(to right, #ff8c00, #ffd700);
        }
        
        .file-icon {
            width: 60px;
            height: 60px;
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 15px;
            font-size: 1.8rem;
        }
        
        .file-name {
            font-weight: 600;
            margin-bottom: 5px;
            color: white;
        }
        
        .file-details {
            display: flex;
            justify-content: space-between;
            color: rgba(255, 255, 255, 0.7);
            font-size: 0.9rem;
            margin-top: 10px;
        }
        
        .file-actions {
            display: flex;
            justify-content: space-between;
            margin-top: 15px;
        }
        
        .file-action-btn {
            background: none;
            border: none;
            color: rgba(255, 255, 255, 0.6);
            cursor: pointer;
            font-size: 1.1rem;
            transition: color 0.2s;
        }
        
        .file-action-btn:hover {
            color: #ffd700;
        }
        
        .new-year-resolution {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            padding: 25px;
            margin-bottom: 30px;
            backdrop-filter: blur(5px);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .new-year-resolution h2 {
            color: #ffd700;
            font-size: 1.5rem;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .resolution-list {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }
        
        .resolution-item {
            display: flex;
            align-items: center;
            gap: 15px;
            padding: 15px;
            background: rgba(255, 255, 255, 0.03);
            border-radius: 10px;
            transition: all 0.3s;
        }
        
        .resolution-item:hover {
            background: rgba(255, 255, 255, 0.06);
        }
        
        .resolution-checkbox {
            width: 24px;
            height: 24px;
            border-radius: 50%;
            border: 2px solid rgba(255, 215, 0, 0.5);
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            flex-shrink: 0;
        }
        
        .resolution-checkbox.checked {
            background: #ffd700;
            color: #0c0c2e;
        }
        
        .resolution-text {
            flex-grow: 1;
            color: rgba(255, 255, 255, 0.9);
        }
        
        .github-section {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            padding: 25px;
            margin-bottom: 30px;
            backdrop-filter: blur(5px);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .github-section h2 {
            color: #ffd700;
            font-size: 1.5rem;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .github-stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }
        
        .github-stat {
            background: rgba(255, 255, 255, 0.03);
            padding: 20px;
            border-radius: 10px;
            text-align: center;
        }
        
        .github-stat-number {
            font-size: 2.5rem;
            font-weight: bold;
            color: #ffd700;
            margin-bottom: 5px;
        }
        
        .github-stat-label {
            color: rgba(255, 255, 255, 0.7);
            font-size: 0.9rem;
        }
        
        footer {
            text-align: center;
            padding: 30px 0;
            color: rgba(255, 255, 255, 0.7);
            font-size: 0.9rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            margin-top: 30px;
        }
        
        .firework-icon {
            color: #ffd700;
            margin: 0 5px;
            animation: bounce 1s infinite alternate;
        }
        
        @keyframes bounce {
            from { transform: translateY(0); }
            to { transform: translateY(-10px); }
        }
        
        @media (max-width: 768px) {
            header {
                flex-direction: column;
                gap: 15px;
                align-items: flex-start;
            }
            
            .countdown {
                flex-wrap: wrap;
            }
            
            .countdown-item {
                min-width: 80px;
                padding: 15px 10px;
            }
            
            .countdown-number {
                font-size: 2rem;
            }
            
            .action-buttons {
                flex-direction: column;
            }
            
            .btn {
                width: 100%;
                justify-content: center;
            }
            
            .search-box {
                width: 100%;
                margin-top: 15px;
            }
            
            .files-header {
                flex-direction: column;
                align-items: flex-start;
            }
            
            .new-year-message h2 {
                font-size: 1.8rem;
            }
        }
        
        .snowflake {
            position: fixed;
            top: -10px;
            color: white;
            font-size: 1rem;
            opacity: 0.8;
            z-index: 1;
            pointer-events: none;
        }
        
        .confetti {
            position: fixed;
            width: 10px;
            height: 10px;
            opacity: 0.8;
            z-index: 1;
            pointer-events: none;
        }
        
        /* Animasi untuk kembang api */
        @keyframes fireworkAnimation {
            0% { transform: translateY(0) scale(1); opacity: 1; }
            50% { transform: translateY(-20px) scale(1.2); opacity: 0.8; }
            100% { transform: translateY(-40px) scale(0.8); opacity: 0; }
        }
        
        @keyframes fallingSnow {
            0% { transform: translateY(-10px) translateX(0); opacity: 0.8; }
            100% { transform: translateY(100vh) translateX(20px); opacity: 0; }
        }
        
        @keyframes confettiAnimation {
            0% { transform: translateY(0) rotate(0deg); opacity: 1; }
            100% { transform: translateY(20px) rotate(180deg); opacity: 0.5; }
        }
    </style>
</head>
<body>
    <!-- Efek Kembang Api -->
    <div class="fireworks" id="fireworks"></div>
    
    <!-- Efek Salju -->
    <div id="snowflakes"></div>
    
    <!-- Efek Konfeti -->
    <div id="confetti"></div>
    
    <div class="container">
        <header>
            <div class="logo">
                <i class="fas fa-cloud"></i>
                <h1>Cloud Tahun Baru</h1>
            </div>
            <div style="display: flex; gap: 15px; align-items: center;">
                <a href="https://github.com" class="github-badge" target="_blank">
                    <i class="fab fa-github"></i>
                    GitHub
                </a>
                <div class="new-year-badge">
                    <span id="yearDisplay">2026</span>
                </div>
            </div>
            <div class="user-info">
                <i class="fas fa-user-circle"></i>
                <span>Selamat Tahun Baru!</span>
            </div>
        </header>
        
        <section class="new-year-message">
            <h2>Selamat Tahun Baru 2026! 🎉</h2>
            <p>Semoga di tahun yang baru ini, semua file dan kenangan indah tersimpan aman di cloud kebahagiaan kita.</p>
            <p style="margin-top: 10px; font-size: 0.9rem; color: rgba(255, 255, 255, 0.7);">
                <i class="fab fa-github"></i> Hosting di GitHub Pages | Deploy otomatis dengan GitHub Actions
            </p>
        </section>
        
        <div class="countdown" id="countdown">
            <!-- Countdown akan diisi oleh JavaScript -->
        </div>
        
        <section class="storage-info">
            <h2><i class="fas fa-cloud-upload-alt"></i> Penyimpanan Kenangan 2025</h2>
            <div class="storage-bar">
                <div class="storage-used"></div>
            </div>
            <div class="storage-stats">
                <span>6.5 GB dari 10 GB kenangan tersimpan</span>
                <span>65%</span>
            </div>
        </section>
        
        <div class="action-buttons">
            <button class="btn btn-primary" id="uploadBtn">
                <i class="fas fa-cloud-upload-alt"></i> Unggah Kenangan Baru
            </button>
            <button class="btn btn-secondary" id="shareBtn">
                <i class="fas fa-share-alt"></i> Bagikan Kebahagiaan
            </button>
            <button class="btn btn-secondary" id="memoryBtn">
                <i class="fas fa-images"></i> Lihat Kenangan 2025
            </button>
            <button class="btn btn-secondary" id="githubBtn">
                <i class="fab fa-github"></i> Lihat di GitHub
            </button>
        </div>
        
        <section class="files-container">
            <div class="files-header">
                <h2><i class="fas fa-file-alt"></i> File Spesial Tahun Baru</h2>
                <div class="search-box">
                    <i class="fas fa-search"></i>
                    <input type="text" placeholder="Cari kenangan spesial..." id="searchInput">
                </div>
            </div>
            
            <div class="files-grid" id="filesGrid">
                <!-- File akan ditambahkan di sini oleh JavaScript -->
            </div>
        </section>
        
        <section class="new-year-resolution">
            <h2><i class="fas fa-star"></i> Resolusi Cloud 2026</h2>
            <div class="resolution-list" id="resolutionList">
                <!-- Resolusi akan ditambahkan di sini oleh JavaScript -->
            </div>
        </section>
        
        <section class="github-section">
            <h2><i class="fab fa-github"></i> Statistik GitHub</h2>
            <p>Proyek ini dihosting di GitHub Pages dengan teknologi modern:</p>
            <div class="github-stats">
                <div class="github-stat">
                    <div class="github-stat-number">100%</div>
                    <div class="github-stat-label">Uptime</div>
                </div>
                <div class="github-stat">
                    <div class="github-stat-number">2026</div>
                    <div class="github-stat-label">Tahun Aktif</div>
                </div>
                <div class="github-stat">
                    <div class="github-stat-number">∞</div>
                    <div class="github-stat-label">Penyimpanan</div>
                </div>
                <div class="github-stat">
                    <div class="github-stat-number">24/7</div>
                    <div class="github-stat-label">Akses Global</div>
                </div>
            </div>
        </section>
        
        <footer>
            <p>
                <i class="fas fa-firework firework-icon"></i>
                Cloud Tahun Baru 2026 - Hosting di GitHub Pages
                <i class="fas fa-firework firework-icon"></i>
            </p>
            <p style="margin-top: 10px;">© 2025-2026 Cloud Tahun Baru. Seluruh kenangan dilindungi. | 
                <a href="https://github.com" style="color: #ffd700; text-decoration: none;" target="_blank">
                    <i class="fab fa-github"></i> GitHub Repository
                </a>
            </p>
        </footer>
    </div>

    <script>
        // Data file spesial Tahun Baru (diperbarui untuk 2026)
        const newYearFiles = [
            { name: "Foto Pesta Tahun Baru 2026.jpg", type: "image", size: "5.2 MB", date: "1 Jan 2026", color: "#FF8C00", icon: "fa-camera" },
            { name: "Video Kembang Api 2026.mp4", type: "video", size: "45.5 MB", date: "1 Jan 2026", color: "#FF4500", icon: "fa-fire" },
            { name: "Resolusi 2026.pdf", type: "document", size: "1.3 MB", date: "31 Des 2025", color: "#FFD700", icon: "fa-file-alt" },
            { name: "Playlist Lagu Tahun Baru 2026.mp3", type: "audio", size: "22.7 MB", date: "30 Des 2025", color: "#1E90FF", icon: "fa-music" },
            { name: "Ucapan Selamat Tahun Baru.docx", type: "document", size: "0.9 MB", date: "29 Des 2025", color: "#32CD32", icon: "fa-envelope" },
            { name: "Foto Bersama Keluarga 2025.jpg", type: "image", size: "6.3 MB", date: "25 Des 2025", color: "#9370DB", icon: "fa-users" },
            { name: "Proyek GitHub 2026.zip", type: "archive", size: "12.4 MB", date: "15 Des 2025", color: "#6A5ACD", icon: "fa-file-archive" },
            { name: "Dokumentasi Website.md", type: "code", size: "0.5 MB", date: "10 Des 2025", color: "#20B2AA", icon: "fa-code" }
        ];
        
        // Data resolusi Tahun Baru 2026
        const resolutions = [
            "Belajar teknologi web terbaru di GitHub",
            "Membuat lebih banyak proyek open source",
            "Berkontribusi ke repository GitHub",
            "Menggunakan GitHub Actions untuk CI/CD",
            "Mempelajari GitHub Pages secara mendalam"
        ];
        
        // Fungsi untuk membuat efek kembang api
        function createFireworks() {
            const fireworksContainer = document.getElementById('fireworks');
            const colors = ['#FFD700', '#FF8C00', '#FF4500', '#FF0000', '#FFFFFF', '#1E90FF'];
            
            for (let i = 0; i < 60; i++) {
                const firework = document.createElement('div');
                firework.className = 'firework';
                
                // Posisi acak
                firework.style.left = Math.random() * 100 + 'vw';
                firework.style.top = Math.random() * 100 + 'vh';
                
                // Warna acak
                firework.style.backgroundColor = colors[Math.floor(Math.random() * colors.length)];
                firework.style.boxShadow = `0 0 10px ${firework.style.backgroundColor}, 0 0 20px ${firework.style.backgroundColor}`;
                
                // Ukuran acak
                const size = Math.random() * 8 + 2;
                firework.style.width = size + 'px';
                firework.style.height = size + 'px';
                
                // Animasi
                firework.style.animation = `fireworkAnimation ${Math.random() * 3 + 2}s infinite alternate`;
                
                fireworksContainer.appendChild(firework);
            }
        }
        
        // Fungsi untuk membuat efek salju
        function createSnowflakes() {
            const snowflakesContainer = document.getElementById('snowflakes');
            const snowflakeChars = ['❄', '✽', '❅', '❆', '•'];
            
            for (let i = 0; i < 100; i++) {
                const snowflake = document.createElement('div');
                snowflake.className = 'snowflake';
                snowflake.innerHTML = snowflakeChars[Math.floor(Math.random() * snowflakeChars.length)];
                
                // Posisi dan animasi acak
                snowflake.style.left = Math.random() * 100 + 'vw';
                snowflake.style.fontSize = (Math.random() * 20 + 10) + 'px';
                snowflake.style.opacity = Math.random() * 0.7 + 0.3;
                snowflake.style.animationDuration = Math.random() * 10 + 5 + 's';
                snowflake.style.animationDelay = Math.random() * 5 + 's';
                snowflake.style.animationTimingFunction = 'linear';
                snowflake.style.animationName = 'fallingSnow';
                
                snowflakesContainer.appendChild(snowflake);
            }
        }
        
        // Fungsi untuk membuat efek konfeti
        function createConfetti() {
            const confettiContainer = document.getElementById('confetti');
            const colors = ['#FFD700', '#FF8C00', '#FF4500', '#FF0000', '#1E90FF', '#32CD32', '#9370DB', '#6A5ACD'];
            
            for (let i = 0; i < 150; i++) {
                const confetti = document.createElement('div');
                confetti.className = 'confetti';
                
                // Posisi acak
                confetti.style.left = Math.random() * 100 + 'vw';
                confetti.style.top = Math.random() * 100 + 'vh';
                
                // Warna acak
                confetti.style.backgroundColor = colors[Math.floor(Math.random() * colors.length)];
                
                // Bentuk acak (persegi atau lingkaran)
                if (Math.random() > 0.5) {
                    confetti.style.borderRadius = '50%';
                }
                
                // Ukuran acak
                const size = Math.random() * 12 + 3;
                confetti.style.width = size + 'px';
                confetti.style.height = size + 'px';
                
                // Animasi
                confetti.style.animation = `confettiAnimation ${Math.random() * 5 + 3}s infinite alternate`;
                
                confettiContainer.appendChild(confetti);
            }
        }
        
        // Fungsi untuk countdown menuju Tahun Baru 2026
        function setupCountdown() {
            const countdownContainer = document.getElementById('countdown');
            
            // Tanggal target: 1 Januari 2026
            const targetDate = new Date('January 1, 2026 00:00:00').getTime();
            
            // Render countdown awal
            const countdownItems = [
                { id: 'days', label: 'HARI', value: '00' },
                { id: 'hours', label: 'JAM', value: '00' },
                { id: 'minutes', label: 'MENIT', value: '00' },
                { id: 'seconds', label: 'DETIK', value: '00' }
            ];
            
            countdownItems.forEach(item => {
                const countdownItem = document.createElement('div');
                countdownItem.className = 'countdown-item';
                countdownItem.innerHTML = `
                    <div class="countdown-number" id="${item.id}">${item.value}</div>
                    <div class="countdown-label">${item.label}</div>
                `;
                countdownContainer.appendChild(countdownItem);
            });
            
            // Update countdown setiap detik
            const countdownInterval = setInterval(() => {
                const now = new Date().getTime();
                const distance = targetDate - now;
                
                if (distance < 0) {
                    clearInterval(countdownInterval);
                    document.querySelector('.new-year-message h2').textContent = 'SELAMAT TAHUN BARU 2026! 🎉🎊';
                    document.querySelector('.new-year-message p').innerHTML = 'Tahun baru telah tiba! Semoga penuh berkah dan kebahagiaan!<br><small>Hosting di GitHub Pages</small>';
                    
                    // Tampilkan pesan tahun baru
                    showNewYearMessage();
                    return;
                }
                
                // Hitung hari, jam, menit, detik
                const days = Math.floor(distance / (1000 * 60 * 60 * 24));
                const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
                const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
                const seconds = Math.floor((distance % (1000 * 60)) / 1000);
                
                // Update tampilan
                document.getElementById('days').textContent = days.toString().padStart(2, '0');
                document.getElementById('hours').textContent = hours.toString().padStart(2, '0');
                document.getElementById('minutes').textContent = minutes.toString().padStart(2, '0');
                document.getElementById('seconds').textContent = seconds.toString().padStart(2, '0');
            }, 1000);
        }
        
        // Fungsi untuk menampilkan pesan tahun baru
        function showNewYearMessage() {
            // Tambahkan lebih banyak efek visual
            createFireworks();
            createConfetti();
            
            // Tampilkan alert khusus
            setTimeout(() => {
                alert("🎉 SELAMAT TAHUN BARU 2026! 🎊\n\nWebsite ini dihosting di GitHub Pages!\n\nSemoga tahun ini membawa kebahagiaan, kesehatan, dan kesuksesan untuk kita semua!");
            }, 1000);
        }
        
        // Render file spesial Tahun Baru
        function renderFiles() {
            const filesGrid = document.getElementById('filesGrid');
            filesGrid.innerHTML = '';
            
            newYearFiles.forEach(file => {
                const fileCard = document.createElement('div');
                fileCard.className = 'file-card';
                fileCard.setAttribute('data-name', file.name.toLowerCase());
                
                fileCard.innerHTML = `
                    <div class="file-icon" style="background-color: ${file.color}20; color: ${file.color};">
                        <i class="fas ${file.icon}"></i>
                    </div>
                    <div class="file-name">${file.name}</div>
                    <div class="file-details">
                        <span>${file.size}</span>
                        <span>${file.date}</span>
                    </div>
                    <div class="file-actions">
                        <button class="file-action-btn" title="Lihat" onclick="viewFile('${file.name}')">
                            <i class="fas fa-eye"></i>
                        </button>
                        <button class="file-action-btn" title="Bagikan" onclick="shareFile('${file.name}')">
                            <i class="fas fa-share-alt"></i>
                        </button>
                        <button class="file-action-btn" title="Simpan" onclick="downloadFile('${file.name}')">
                            <i class="fas fa-download"></i>
                        </button>
                    </div>
                `;
                
                filesGrid.appendChild(fileCard);
            });
        }
        
        // Render resolusi Tahun Baru
        function renderResolutions() {
            const resolutionList = document.getElementById('resolutionList');
            resolutionList.innerHTML = '';
            
            resolutions.forEach((resolution, index) => {
                const resolutionItem = document.createElement
