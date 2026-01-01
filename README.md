                body {
            background: linear-gradient(135deg, #0a0a23 0%, #1a1a3e 100%);
            color: #fff;
            min-height: 100vh;
            display: flex;
        }
        
        /* Sidebar */
        .sidebar {
            width: 250px;
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            border-right: 1px solid rgba(255, 255, 255, 0.1);
            padding: 25px 20px;
            display: flex;
            flex-direction: column;
            position: fixed;
            height: 100vh;
            overflow-y: auto;
        }
        
        .logo {
            display: flex;
            align-items: center;
            gap: 15px;
            margin-bottom: 40px;
        }
        
        .logo i {
            font-size: 2.5rem;
            color: #ffd700;
            filter: drop-shadow(0 0 10px rgba(255, 215, 0, 0.3));
        }
        
        .logo h1 {
            font-size: 1.5rem;
            background: linear-gradient(to right, #ffd700, #ff8c00);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }
        
        .nav-menu {
            display: flex;
            flex-direction: column;
            gap: 10px;
            margin-bottom: 40px;
        }
        
        .nav-item {
            display: flex;
            align-items: center;
            gap: 15px;
            padding: 15px;
            border-radius: 10px;
            color: rgba(255, 255, 255, 0.7);
            text-decoration: none;
            transition: all 0.3s;
        }
        
        .nav-item:hover, .nav-item.active {
            background: rgba(255, 215, 0, 0.1);
            color: #ffd700;
        }
        
        .nav-item i {
            font-size: 1.2rem;
            width: 24px;
            text-align: center;
        }
        
        .storage-info {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            padding: 20px;
            margin-top: auto;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .storage-info h3 {
            color: #ffd700;
            font-size: 1rem;
            margin-bottom: 10px;
        }
        
        .storage-bar {
            height: 8px;
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 4px;
            margin-bottom: 10px;
            overflow: hidden;
        }
        
        .storage-used {
            height: 100%;
            background: linear-gradient(to right, #ff8c00, #ffd700);
            border-radius: 4px;
            width: 65%;
        }
        
        .storage-stats {
            display: flex;
            justify-content: space-between;
            color: rgba(255, 255, 255, 0.7);
            font-size: 0.8rem;
        }
        
        /* Main Content */
        .main-content {
            flex: 1;
            margin-left: 250px;
            padding: 25px;
            overflow-y: auto;
        }
        
        /* Header */
        .main-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 30px;
            padding-bottom: 20px;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .header-left h2 {
            font-size: 1.8rem;
            color: #ffd700;
            margin-bottom: 5px;
        }
        
        .header-left p {
            color: rgba(255, 255, 255, 0.7);
            font-size: 0.9rem;
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
        
        /* File Grid */
        .files-section {
            margin-bottom: 40px;
        }
        
        .section-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
        }
        
        .section-header h3 {
            font-size: 1.5rem;
            color: #ffd700;
        }
        
        .search-box {
            display: flex;
            align-items: center;
            background-color: rgba(255, 255, 255, 0.05);
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
        
        .files-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
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
            transform: translateY(-5px);
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
            width: 50px;
            height: 50px;
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 15px;
            font-size: 1.5rem;
        }
        
        .file-name {
            font-weight: 600;
            margin-bottom: 5px;
            color: white;
            font-size: 0.95rem;
        }
        
        .file-details {
            display: flex;
            justify-content: space-between;
            color: rgba(255, 255, 255, 0.7);
            font-size: 0.8rem;
            margin-top: 10px;
        }
        
        /* Upload Section */
        .upload-section {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            padding: 30px;
            margin-bottom: 40px;
            border: 2px dashed rgba(255, 215, 0, 0.3);
            text-align: center;
        }
        
        .upload-icon {
            font-size: 3rem;
            color: #ffd700;
            margin-bottom: 15px;
        }
        
        .upload-text h3 {
            font-size: 1.5rem;
            color: #ffd700;
            margin-bottom: 10px;
        }
        
        .upload-text p {
            color: rgba(255, 255, 255, 0.7);
            margin-bottom: 20px;
        }
        
        .upload-btn {
            background: linear-gradient(45deg, #ff8c00, #ffd700);
            color: #0a0a23;
            border: none;
            padding: 12px 30px;
            border-radius: 10px;
            font-weight: 600;
            cursor: pointer;
            display: inline-flex;
            align-items: center;
            gap: 10px;
            transition: all 0.3s;
        }
        
        .upload-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(255, 140, 0, 0.3);
        }
        
        /* Recent Activity */
        .activity-section {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            padding: 25px;
        }
        
        .activity-list {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        .activity-item {
            display: flex;
            align-items: center;
            gap: 15px;
            padding-bottom: 15px;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .activity-icon {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background-color: rgba(255, 215, 0, 0.1);
            display: flex;
            align-items: center;
            justify-content: center;
            color: #ffd700;
        }
        
        .activity-details h4 {
            color: white;
            margin-bottom: 5px;
            font-size: 0.95rem;
        }
        
        .activity-details p {
            color: rgba(255, 255, 255, 0.7);
            font-size: 0.8rem;
        }
        
        /* GitHub Info */
        .github-info {
            display: flex;
            align-items: center;
            gap: 10px;
            background: rgba(255, 255, 255, 0.05);
            padding: 15px;
            border-radius: 10px;
            margin-top: 30px;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .github-info i {
            color: #ffd700;
            font-size: 1.5rem;
        }
        
        .github-info span {
            color: rgba(255, 255, 255, 0.9);
        }
        
        /* Responsive */
        @media (max-width: 1024px) {
            .sidebar {
                width: 220px;
            }
            
            .main-content {
                margin-left: 220px;
            }
        }
        
        @media (max-width: 768px) {
            body {
                flex-direction: column;
            }
            
            .sidebar {
                width: 100%;
                height: auto;
                position: relative;
                padding: 20px;
            }
            
            .nav-menu {
                flex-direction: row;
                overflow-x: auto;
                margin-bottom: 20px;
            }
            
            .nav-item {
                white-space: nowrap;
            }
            
            .main-content {
                margin-left: 0;
                padding: 20px;
            }
            
            .files-grid {
                grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
            }
            
            .search-box {
                width: 100%;
                margin-top: 15px;
            }
            
            .section-header {
                flex-direction: column;
                align-items: flex-start;
            }
        }
        
        /* Animations */
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }
        
        .new-year-badge {
            animation: pulse 2s infinite, glow 2s infinite alternate;
        }
        
        /* Efek kembang api sederhana */
        .firework {
            position: fixed;
            width: 5px;
            height: 5px;
            border-radius: 50%;
            pointer-events: none;
            z-index: -1;
        }
    </style>
</head>
<body>
    <!-- Sidebar -->
    <div class="sidebar">
        <div class="logo">
            <i class="fas fa-cloud"></i>
            <h1>Cloud 2026</h1>
        </div>
        
        <div class="nav-menu">
            <a href="#" class="nav-item active">
                <i class="fas fa-home"></i>
                <span>Dashboard</span>
            </a>
            <a href="#" class="nav-item">
                <i class="fas fa-folder"></i>
                <span>File Saya</span>
            </a>
            <a href="#" class="nav-item">
                <i class="fas fa-share-alt"></i>
                <span>Dibagikan</span>
            </a>
            <a href="#" class="nav-item">
                <i class="fas fa-history"></i>
                <span>Terbaru</span>
            </a>
            <a href="#" class="nav-item">
                <i class="fas fa-star"></i>
                <span>Favorit</span>
            </a>
            <a href="#" class="nav-item">
                <i class="fas fa-trash"></i>
                <span>Sampah</span>
            </a>
            <a href="#" class="nav-item">
                <i class="fab fa-github"></i>
                <span>GitHub</span>
            </a>
        </div>
        
        <div class="storage-info">
            <h3>Penyimpanan</h3>
            <div class="storage-bar">
                <div class="storage-used" id="storageBar"></div>
            </div>
            <div class="storage-stats">
                <span>6.5 GB digunakan</span>
                <span>65%</span>
            </div>
        </div>
    </div>
    
    <!-- Main Content -->
    <div class="main-content">
        <!-- Header -->
        <div class="main-header">
            <div class="header-left">
                <h2>Selamat Tahun Baru 2026! 🎉</h2>
                <p>Selamat datang di Cloud Storage dengan tema Tahun Baru</p>
            </div>
            <div class="new-year-badge">
                <span id="yearDisplay">2026</span>
            </div>
        </div>
        
        <!-- Upload Section -->
        <div class="upload-section">
            <div class="upload-icon">
                <i class="fas fa-cloud-upload-alt"></i>
            </div>
            <div class="upload-text">
                <h3>Unggah Kenangan Tahun Baru</h3>
                <p>Seret dan lepas file di sini atau klik untuk mengunggah</p>
            </div>
            <button class="upload-btn" id="uploadBtn">
                <i class="fas fa-cloud-upload-alt"></i>
                Unggah File
            </button>
        </div>
        
        <!-- Recent Files Section -->
        <div class="files-section">
            <div class="section-header">
                <h3>File Terbaru</h3>
                <div class="search-box">
                    <i class="fas fa-search"></i>
                    <input type="text" placeholder="Cari file...">
                </div>
            </div>
            
            <div class="files-grid" id="filesGrid">
                <!-- File akan ditambahkan di sini oleh JavaScript -->
            </div>
        </div>
        
        <!-- Recent Activity -->
        <div class="activity-section">
            <h3 style="color: #ffd700; margin-bottom: 20px;">Aktivitas Terbaru</h3>
            <div class="activity-list" id="activityList">
                <!-- Aktivitas akan ditambahkan di sini oleh JavaScript -->
            </div>
        </div>
        
        <!-- GitHub Info -->
        <div class="github-info">
            <i class="fab fa-github"></i>
            <span>Website ini dihosting di GitHub Pages. Klik untuk melihat repository.</span>
        </div>
    </div>

    <script>
        // Data file untuk Tahun Baru 2026
        const newYearFiles = [
            { 
                name: "Foto Tahun Baru.jpg", 
                type: "image", 
                size: "4.2 MB", 
                date: "1 Jan 2026", 
                color: "#FF8C00", 
                icon: "fa-image" 
            },
            { 
                name: "Video Perayaan.mp4", 
                type: "video", 
                size: "32.5 MB", 
                date: "1 Jan 2026", 
                color: "#FF4500", 
                icon: "fa-video" 
            },
            { 
                name: "Resolusi 2026.pdf", 
                type: "document", 
                size: "1.1 MB", 
                date: "31 Des 2025", 
                color: "#FFD700", 
                icon: "fa-file-pdf" 
            },
            { 
                name: "Lagu Tahun Baru.mp3", 
                type: "audio", 
                size: "8.7 MB", 
                date: "30 Des 2025", 
                color: "#1E90FF", 
                icon: "fa-music" 
            },
            { 
                name: "Dokumen GitHub.md", 
                type: "code", 
                size: "0.5 MB", 
                date: "15 Des 2025", 
                color: "#20B2AA", 
                icon: "fa-code" 
            },
            { 
                name: "Foto Keluarga.jpg", 
                type: "image", 
                size: "5.3 MB", 
                date: "25 Des 2025", 
                color: "#9370DB", 
                icon: "fa-users" 
            }
        ];
        
        // Data aktivitas terbaru
        const recentActivities = [
            { 
                action: "upload", 
                description: "Anda mengunggah Foto Tahun Baru.jpg", 
                time: "2 jam yang lalu",
                icon: "fa-cloud-upload-alt"
            },
            { 
                action: "share", 
                description: "Budi membagikan Video Perayaan.mp4", 
                time: "Kemarin",
                icon: "fa-share-alt"
            },
            { 
                action: "edit", 
                description: "Siti mengedit Resolusi 2026.pdf", 
                time: "2 hari yang lalu",
                icon: "fa-edit"
            },
            { 
                action: "github", 
                description: "Proyek diupdate ke GitHub", 
                time: "3 hari yang lalu",
                icon: "fab fa-github"
            }
        ];
        
        // Render file ke grid
        function renderFiles() {
            const filesGrid = document.getElementById('filesGrid');
            filesGrid.innerHTML = '';
            
            newYearFiles.forEach(file => {
                const fileCard = document.createElement('div');
                fileCard.className = 'file-card';
                
                fileCard.innerHTML = `
                    <div class="file-icon" style="background-color: ${file.color}20; color: ${file.color};">
                        <i class="fas ${file.icon}"></i>
                    </div>
                    <div class="file-name">${file.name}</div>
                    <div class="file-details">
                        <span>${file.size}</span>
                        <span>${file.date}</span>
                    </div>
                `;
                
                filesGrid.appendChild(fileCard);
            });
        }
        
        // Render aktivitas terbaru
        function renderActivities() {
            const activityList = document.getElementById('activityList');
            activityList.innerHTML = '';
            
            recentActivities.forEach(activity => {
                const activityItem = document.createElement('div');
                activityItem.className = 'activity-item';
                
                activityItem.innerHTML = `
                    <div class="activity-icon">
                        <i class="${activity.icon}"></i>
                    </div>
                    <div class="activity-details">
                        <h4>${activity.description}</h4>
                        <p>${activity.time}</p>
                    </div>
                `;
                
                activityList.appendChild(activityItem);
            });
        }
        
        // Tambahkan efek kembang api sederhana
        function createFireworks() {
            const colors = ['#FFD700', '#FF8C00', '#FF4500', '#FFFFFF'];
            
            for (let i = 0; i < 20; i++) {
                const firework = document.createElement('div');
                firework.className = 'firework';
                
                // Posisi acak
                firework.style.left = Math.random() * 100 + 'vw';
                firework.style.top = Math.random() * 100 + 'vh';
                
                // Warna acak
                firework.style.backgroundColor = colors[Math.floor(Math.random() * colors.length)];
                firework.style.boxShadow = `0 0 10px ${firework.style.backgroundColor}`;
                
                // Ukuran acak
                const size = Math.random() * 6 + 2;
                firework.style.width = size + 'px';
                firework.style.height = size + 'px';
                
                // Animasi
                firework.style.animation = `fireworkAnimation ${Math.random() * 3 + 2}s infinite alternate`;
                
                document.body.appendChild(firework);
            }
            
            // Tambahkan style untuk animasi
            const style = document.createElement('style');
            style.textContent = `
                @keyframes fireworkAnimation {
                    0% { transform: translateY(0) scale(1); opacity: 1; }
                    50% { transform: translateY(-20px) scale(1.2); opacity: 0.8; }
                    100% { transform: translateY(-40px) scale(0.8); opacity: 0; }
                }
            `;
            document.head.appendChild(style);
        }
        
        // Event listeners
        document.getElementById('uploadBtn').addEventListener('click', function() {
            alert('🎉 Selamat Tahun Baru 2026! Siap mengunggah kenangan baru Anda.');
        });
        
        // Update tahun display
        document.getElementById('yearDisplay').textContent = new Date().getFullYear();
        
        // Animasi progress bar
        function animateProgressBar() {
            const storageBar = document.getElementById('storageBar');
            let width = 0;
            const targetWidth = 65;
            const interval = setInterval(() => {
                if (width >= targetWidth) {
                    clearInterval(interval);
                } else {
                    width++;
                    storageBar.style.width = width + '%';
                }
            }, 20);
        }
        
        // Inisialisasi saat halaman dimuat
        document.addEventListener('DOMContentLoaded', function() {
            renderFiles();
            renderActivities();
            animateProgressBar();
            createFireworks();
            
            // Tambahkan efek hover pada nav items
            const navItems = document.querySelectorAll('.nav-item');
            navItems.forEach(item => {
                item.addEventListener('click', function(e) {
                    e.preventDefault();
                    navItems.forEach(nav => nav.classList.remove('active'));
                    this.classList.add('active');
                });
            });
            
            // Efek untuk GitHub info
            const githubInfo = document.querySelector('.github-info');
            githubInfo.addEventListener('click', function() {
                window.open('https://github.com', '_blank');
            });
        });
    </script>
</body>
</html>
