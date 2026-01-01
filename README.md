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
</style>
