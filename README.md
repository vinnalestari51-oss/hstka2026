<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Hasil Tes Kemampuan Akademik SMPN 1 Lingga 2026</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap" rel="stylesheet">

    <style>
        /* --- RESET & GLOBAL STYLES --- */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Plus Jakarta Sans', sans-serif;
            -webkit-tap-highlight-color: transparent;
        }

        body {
            background-color: #f0f7ff;
            color: #1e293b;
            display: flex;
            justify-content: center;
            align-items: flex-start;
            min-height: 100vh;
            overflow-x: hidden;
            padding-bottom: 90px;
        }

        /* --- MOBILE FIRST CONTAINER --- */
        .container-mobile {
            width: 100%;
            max-width: 440px;
            padding: 20px 16px;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        /* --- SCHOOL HEADER PANEL --- */
        .header-panel {
            background: rgba(255, 255, 255, 0.85);
            backdrop-filter: blur(20px);
            -webkit-backdrop-filter: blur(20px);
            border: 1px solid rgba(255, 255, 255, 0.9);
            border-radius: 24px;
            padding: 20px;
            text-align: center;
            box-shadow: 0 8px 32px 0 rgba(31, 38, 135, 0.04);
        }

        .header-panel h1 {
            font-size: 18px;
            font-weight: 800;
            color: #0f172a;
            letter-spacing: -0.5px;
            margin-bottom: 4px;
            text-transform: uppercase;
        }

        .header-panel p {
            font-size: 13px;
            color: #64748b;
            font-weight: 500;
        }

        .header-panel .badge-school {
            display: inline-block;
            background: #e0f2fe;
            color: #0369a1;
            padding: 4px 12px;
            border-radius: 12px;
            font-size: 11px;
            font-weight: 700;
            margin-top: 8px;
        }

        /* --- SCREEN VIEW SYSTEM --- */
        .screen-view {
            display: none;
            width: 100%;
            flex-direction: column;
            gap: 16px;
        }

        .screen-view.active {
            display: flex;
        }

        /* --- GLASSMORPHISM BASE BOX --- */
        .m3-glass {
            background: rgba(255, 255, 255, 0.8);
            backdrop-filter: blur(20px);
            -webkit-backdrop-filter: blur(20px);
            border: 1px solid rgba(255, 255, 255, 0.9);
            border-radius: 24px;
            padding: 20px;
            box-shadow: 0 8px 32px 0 rgba(31, 38, 135, 0.04);
        }

        /* --- SEARCH & INPUT AREA --- */
        .search-title {
            font-size: 15px;
            font-weight: 700;
            color: #1e293b;
            margin-bottom: 12px;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .input-wrapper {
            position: relative;
            width: 100%;
        }

        .input-wrapper i {
            position: absolute;
            left: 16px;
            top: 50%;
            transform: translateY(-50%);
            color: #94a3b8;
            font-size: 16px;
        }

        .input-nisn {
            width: 100%;
            padding: 14px 16px 14px 44px;
            border-radius: 16px;
            border: 1.5px solid #e2e8f0;
            background: rgba(255, 255, 255, 0.9);
            font-size: 14px;
            font-weight: 600;
            color: #0f172a;
            outline: none;
            transition: all 0.2s ease;
        }

        .input-nisn:focus {
            border-color: #3b82f6;
            box-shadow: 0 0 0 4px rgba(59, 130, 246, 0.1);
        }

        /* --- INDIVIDUAL RESULTS LIST --- */
        .results-list {
            display: flex;
            flex-direction: column;
            gap: 12px;
            margin-top: 4px;
        }

        .student-item-btn {
            width: 100%;
            background: rgba(255, 255, 255, 0.7);
            border: 1px solid rgba(255, 255, 255, 0.8);
            padding: 14px 16px;
            border-radius: 16px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            cursor: pointer;
            text-align: left;
            transition: all 0.2s ease;
        }

        .student-item-btn:active {
            transform: scale(0.98);
            background: rgba(255, 255, 255, 0.9);
        }

        .student-item-info h4 {
            font-size: 14px;
            font-weight: 700;
            color: #1e293b;
        }

        .student-item-info p {
            font-size: 12px;
            color: #64748b;
            margin-top: 2px;
        }

        .btn-open-envelope {
            background: #2563eb;
            color: #ffffff;
            border: none;
            padding: 8px 14px;
            border-radius: 12px;
            font-size: 12px;
            font-weight: 700;
            display: flex;
            align-items: center;
            gap: 6px;
        }

        /* --- LOADING SPINNER --- */
        .loading-container {
            display: none;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            padding: 40px 20px;
            gap: 16px;
        }

        .spinner {
            width: 44px;
            height: 44px;
            border: 4px solid rgba(37, 99, 235, 0.1);
            border-top: 4px solid #2563eb;
            border-radius: 50%;
            animation: spin 1s linear infinite;
        }

        .loading-text {
            font-size: 13px;
            font-weight: 600;
            color: #2563eb;
            animation: pulse 1.2s ease-in-out infinite;
        }

        /* --- DRAMATIC ENVELOPE SURPRISE CARD --- */
        .envelope-card {
            display: none;
            flex-direction: column;
            gap: 16px;
            animation: bounceIn 0.8s cubic-bezier(0.175, 0.885, 0.32, 1.275) forwards;
        }

        /* Rank 1 Styling (Juara 1) */
        .envelope-card.rank-1 {
            background: linear-gradient(135deg, #d1fae5 0%, #a7f3d0 100%);
            border: 2px solid #34d399;
            box-shadow: 0 10px 25px rgba(52, 211, 153, 0.25), inset 0 0 20px rgba(255,255,255,0.4);
            position: relative;
            overflow: hidden;
        }
        .envelope-card.rank-1::after {
            content: '';
            position: absolute;
            top: -50%; left: -50%; right: -50%; bottom: -50%;
            background: linear-gradient(to bottom right, rgba(255,255,255,0) 0%, rgba(255,255,255,0) 40%, rgba(255,255,255,0.4) 50%, rgba(255,255,255,0) 60%, rgba(255,255,255,0) 100%);
            background-size: 200% 200%;
            animation: shimmer 3s infinite linear;
            pointer-events: none;
        }

        /* Rank 2 Styling (Juara 2) */
        .envelope-card.rank-2 {
            background: linear-gradient(135deg, #e0f2fe 0%, #bfdbfe 100%);
            border: 2px solid #60a5fa;
            box-shadow: 0 10px 25px rgba(96, 165, 251, 0.2);
        }

        /* Rank 3 Styling (Juara 3) */
        .envelope-card.rank-3 {
            background: linear-gradient(135deg, #ffedd5 0%, #fdbb74 100%);
            border: 2px solid #fb923c;
            box-shadow: 0 10px 25px rgba(251, 146, 60, 0.2);
        }

        /* CARD CORE ELEMENTS */
        .card-top {
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            border-bottom: 1px dashed rgba(30, 41, 59, 0.1);
            padding-bottom: 12px;
        }

        .student-meta h2 {
            font-size: 16px;
            font-weight: 800;
            color: #0f172a;
        }

        .student-meta p {
            font-size: 12px;
            color: #475569;
            margin-top: 2px;
            font-weight: 500;
        }

        .rank-badge {
            padding: 6px 12px;
            border-radius: 12px;
            font-size: 12px;
            font-weight: 800;
            display: flex;
            align-items: center;
            gap: 6px;
        }
        .rank-1 .rank-badge { background: #047857; color: #ffffff; }
        .rank-2 .rank-badge { background: #1d4ed8; color: #ffffff; }
        .rank-3 .rank-badge { background: #c2410c; color: #ffffff; }
        .rank-normal .rank-badge { background: #475569; color: #ffffff; }

        /* SCORE ROW LAYOUT (ANTI-TABRAKAN) */
        .score-box-container {
            display: flex;
            flex-direction: column;
            gap: 10px;
        }

        .score-row-item {
            background: rgba(255, 255, 255, 0.6);
            border-radius: 16px;
            padding: 12px 16px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            border: 1px solid rgba(255,255,255,0.5);
        }

        .subject-side {
            display: flex;
            flex-direction: column;
            gap: 4px;
            align-items: flex-start;
        }

        .subject-title {
            font-size: 13px;
            font-weight: 700;
            color: #334155;
        }

        .predicate-tag {
            font-size: 11px;
            font-weight: 700;
            padding: 2px 8px;
            border-radius: 6px;
            width: auto; /* Mencegah pelebaran kaku */
        }
        .pred-baik { background-color: #d1fae5; color: #065f46; }
        .pred-memadai { background-color: #dbeafe; color: #1e40af; }
        .pred-kurang { background-color: #fee2e2; color: #991b1b; }

        .score-number-side {
            font-size: 22px;
            font-weight: 800;
            color: #0f172a;
            text-align: right;
        }

        .card-footer-average {
            background: rgba(15, 23, 42, 0.04);
            border-radius: 14px;
            padding: 12px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-top: 4px;
        }

        .card-footer-average span {
            font-size: 12px;
            font-weight: 700;
            color: #475569;
        }

        .card-footer-average .avg-val {
            font-size: 16px;
            font-weight: 800;
            color: #0f172a;
        }

        /* --- STATS LAYOUT (HOME SCREEN) --- */
        .stats-grid-row {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 12px;
        }

        .stat-card-mini {
            background: rgba(255, 255, 255, 0.7);
            border-radius: 18px;
            padding: 14px;
            text-align: center;
            border: 1px solid rgba(255,255,255,0.6);
        }

        .stat-card-mini i {
            font-size: 20px;
            color: #2563eb;
            margin-bottom: 6px;
        }

        .stat-card-mini p {
            font-size: 11px;
            color: #64748b;
            font-weight: 600;
        }

        .stat-card-mini h3 {
            font-size: 18px;
            font-weight: 800;
            color: #0f172a;
            margin-top: 2px;
        }

        .chart-section-title {
            font-size: 13px;
            font-weight: 800;
            color: #475569;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            margin: 8px 0 4px 0;
            display: flex;
            align-items: center;
            gap: 6px;
        }

        /* MANUAL DIV CUSTOM BAR CHART */
        .custom-bar-chart {
            display: flex;
            flex-direction: column;
            gap: 10px;
            margin-top: 8px;
        }

        .bar-row {
            display: flex;
            flex-direction: column;
            gap: 4px;
        }

        .bar-label-group {
            display: flex;
            justify-content: space-between;
            font-size: 11px;
            font-weight: 600;
            color: #475569;
        }

        .bar-track {
            width: 100%;
            height: 10px;
            background: #e2e8f0;
            border-radius: 5px;
            overflow: hidden;
        }

        .bar-fill {
            height: 100%;
            border-radius: 5px;
            width: 0%; /* Diisi via JS */
            transition: width 1s ease-out;
        }
        .fill-baik { background: #10b981; }
        .fill-memadai { background: #3b82f6; }
        .fill-kurang { background: #ef4444; }

        /* --- FIXED BOTTOM NAVBAR --- */
        .bottom-navbar {
            position: fixed;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 100%;
            max-width: 440px;
            height: 68px;
            background: rgba(255, 255, 255, 0.85);
            backdrop-filter: blur(25px);
            -webkit-backdrop-filter: blur(25px);
            border-top: 1px solid rgba(255, 255, 255, 0.8);
            display: grid;
            grid-template-columns: 1fr 1fr;
            padding: 6px 10px;
            z-index: 999;
            box-shadow: 0 -4px 20px rgba(0, 0, 0, 0.03);
        }

        .nav-item {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            background: none;
            border: none;
            color: #94a3b8;
            cursor: pointer;
            gap: 4px;
            transition: all 0.2s ease;
        }

        .nav-item i {
            font-size: 18px;
        }

        .nav-item span {
            font-size: 11px;
            font-weight: 700;
        }

        .nav-item.active {
            color: #2563eb;
        }

        /* --- CSS KEYFRAMES ANIMATIONS --- */
        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        @keyframes pulse {
            0%, 100% { opacity: 0.6; }
            50% { opacity: 1; }
        }

        @keyframes bounceIn {
            0% { opacity: 0; transform: scale(0.3); }
            50% { opacity: 0.9; transform: scale(1.04); }
            70% { transform: scale(0.98); }
            100% { opacity: 1; transform: scale(1); }
        }

        @keyframes shimmer {
            0% { background-position: -200% -200%; }
            100% { background-position: 200% 200%; }
        }
    </style>
</head>
<body>

    <div class="container-mobile">
        
        <div class="header-panel">
            <h1>TKA ACADEMIC PORTAL</h1>
            <p>SMP NEGERI 1 LINGGA • TAHUN 2026</p>
            <div class="badge-school">Resmi Dinas Pendidikan</div>
        </div>

        <div id="screen-home" class="screen-view">
            <div class="m3-glass">
                <div class="search-title">
                    <i class="fa-solid fa-chart-line" style="color: #2563eb;"></i>
                    <span>Rangkuman Akademik Kelas</span>
                </div>
                
                <div class="stats-grid-row">
                    <div class="stat-card-mini">
                        <i class="fa-solid fa-calculator"></i>
                        <p>Rata-Rata Matematika</p>
                        <h3 id="class-avg-mat">0.00</h3>
                    </div>
                    <div class="stat-card-mini">
                        <i class="fa-solid fa-book-open"></i>
                        <p>Rata-Rata B. Indonesia</p>
                        <h3 id="class-avg-indo">0.00</h3>
                    </div>
                </div>

                <hr style="border: none; border-top: 1px solid #e2e8f0; margin: 16px 0;">

                <div class="chart-section-title">
                    <i class="fa-solid fa-chart-bar"></i> Distribusi Matematika
                </div>
                <div class="custom-bar-chart" id="chart-mat">
                    </div>

                <div class="chart-section-title" style="margin-top: 18px;">
                    <i class="fa-solid fa-chart-bar"></i> Distribusi Bahasa Indonesia
                </div>
                <div class="custom-bar-chart" id="chart-indo">
                    </div>
            </div>
        </div>

        <div id="screen-nilaiku" class="screen-view active">
            
            <div class="m3-glass">
                <div class="search-title">
                    <i class="fa-solid fa-magnifying-glass" style="color: #2563eb;"></i>
                    <span>Cari Amplop Nilai Pribadi</span>
                </div>
                <div class="input-wrapper">
                    <i class="fa-solid fa-id-card"></i>
                    <input type="number" id="search-input" class="input-nisn" placeholder="Masukkan Nomor NISN Anda...">
                </div>
            </div>

            <div id="search-results-container" class="results-list"></div>

            <div id="loading-spinner" class="loading-container m3-glass">
                <div class="spinner"></div>
                <div class="loading-text">Membuka Segel Amplop Nilai...</div>
            </div>

            <div id="envelope-result-card" class="m3-glass envelope-card">
                <div class="card-top">
                    <div class="student-meta">
                        <h2 id="res-nama">-</h2>
                        <p id="res-nisn">-</p>
                        <p id="res-ttl" style="font-size: 11px; color: #64748b; font-weight: 500;"></p>
                    </div>
                    <div id="res-badge" class="rank-badge">
                        </div>
                </div>

                <div class="score-box-container">
                    <div class="score-row-item">
                        <div class="subject-side">
                            <span class="subject-title">Matematika</span>
                            <span id="res-mat-pred" class="predicate-tag">-</span>
                        </div>
                        <div id="res-mat-score" class="score-number-side">0.00</div>
                    </div>
                    <div class="score-row-item">
                        <div class="subject-side">
                            <span class="subject-title">Bahasa Indonesia</span>
                            <span id="res-indo-pred" class="predicate-tag">-</span>
                        </div>
                        <div id="res-indo-score" class="score-number-side">0.00</div>
                    </div>
                </div>

                <div class="card-footer-average">
                    <span>RATA-RATA KOMBINASI</span>
                    <span id="res-avg-score" class="avg-val">0.00</span>
                </div>
            </div>

        </div>

    </div>

    <nav class="bottom-navbar">
        <button class="nav-item" onclick="switchTab('home', this)">
            <i class="fa-solid fa-chart-simple"></i>
            <span>Home</span>
        </button>
        <button class="nav-item active" onclick="switchTab('nilaiku', this)">
            <i class="fa-solid fa-address-card"></i>
            <span>Nilaiku</span>
        </button>
    </nav>

    <script>
        // --- 1. DATA EXTRACTION LENGKAP TANPA ADA YANG TERLEWAT ---
        const rawStudentsData = [
            { no: 1, nisn: "0113067688", nama: "Riska Sari", ttl: "Panggak Darat, 7 April 2011", mat: 20.00, matPred: "Kurang", indo: 60.00, indoPred: "Memadai" },
            { no: 2, nisn: "0113559822", nama: "MECA ADELYA CAHYANI", ttl: "Daik Lingga, 2 Maret 2011", mat: 50.00, matPred: "Memadai", indo: 90.00, indoPred: "Baik" },
            { no: 3, nisn: "0115427698", nama: "Dzikri Harith Haziq", ttl: "Air Berani, 30 Agustus 2011", mat: 50.00, matPred: "Memadai", indo: 70.00, indoPred: "Memadai" },
            { no: 4, nisn: "0123776337", nama: "VANDERSAR MEICHAEL NAINGGOLAN", ttl: "PALEMBANG, 12 Mei 2012", mat: 23.33, matPred: "Kurang", indo: 86.67, indoPred: "Baik" },
            { no: 5, nisn: "0114844674", nama: "Syifa Syaqirah", ttl: "Daik Lingga, 17 Maret 2011", mat: 33.33, matPred: "Memadai", indo: 63.33, indoPred: "Memadai" },
            { no: 6, nisn: "0117775355", nama: "QIAN FERDINAND", ttl: "TOAPAYA, 24 Mei 2011", mat: 36.67, matPred: "Memadai", indo: 46.67, indoPred: "Kurang" },
            { no: 7, nisn: "0116942061", nama: "SYARIFAH NAJWA SAFIZ", ttl: "TANJUNGPINANG, 9 Agustus 2011", mat: null, matPred: "Kurang", indo: 83.33, indoPred: "Baik" },
            { no: 8, nisn: "0119458667", nama: "SUHARAYAH", ttl: "DAIK LINGGA, 12 Juli 2011", mat: 26.67, matPred: "Kurang", indo: 63.33, indoPred: "Memadai" },
            { no: 9, nisn: "0111929206", nama: "AIRIN DWI RAMADHANI", ttl: "DAIK LINGGA, 18 Agustus 2011", mat: 40.00, matPred: "Memadai", indo: 63.33, indoPred: "Memadai" },
            { no: 10, nisn: "0094409765", nama: "Imam Syahibbullah", ttl: "Daik Lingga, 23 Juni 2009", mat: null, matPred: "Kurang", indo: 53.33, indoPred: "Memadai" },
            { no: 11, nisn: "0119416095", nama: "Deby Septiani", ttl: "Daik Lingga, 7 September 2011", mat: 43.33, matPred: "Memadai", indo: 80.00, indoPred: "Baik" },
            { no: 12, nisn: "0112474826", nama: "Ibnu Shalim", ttl: "Batam, 3 Maret 2011", mat: 26.67, matPred: "Kurang", indo: 43.33, indoPred: "Kurang" },
            { no: 13, nisn: "0117387487", nama: "LIPIANA SUCI RAMARANI", ttl: "TANJUNG PINANG, 25 Agustus 2011", mat: 50.00, matPred: "Memadai", indo: 86.67, indoPred: "Baik" },
            { no: 14, nisn: "0111805260", nama: "irvan kurnia", ttl: "KP. BUDUS, 7 Mei 2011", mat: 16.67, matPred: "Kurang", indo: 43.33, indoPred: "Kurang" },
            { no: 15, nisn: "0086621206", nama: "Arya Imam Risnanda", ttl: "Seranggas, 3 Juni 2008", mat: 43.33, matPred: "Memadai", indo: 80.00, indoPred: "Baik" },
            { no: 16, nisn: "0118621492", nama: "Raisa Idadi", ttl: "Daik, 16 Maret 2011", mat: 30.00, matPred: "Kurang", indo: 66.67, indoPred: "Memadai" },
            { no: 17, nisn: "0116566978", nama: "Kafha Azri Ilhamsyah", ttl: "Daik Lingga, 6 Mei 2011", mat: 43.33, matPred: "Memadai", indo: 73.33, indoPred: "Memadai" },
            { no: 18, nisn: "0114962861", nama: "Muhammad Erwan Zarka", ttl: "Daik, 11 Maret 2011", mat: 36.67, matPred: "Memadai", indo: 63.33, indoPred: "Memadai" },
            { no: 19, nisn: "0105152266", nama: "Adonia Najla Raissa", ttl: "DAIK LINGGA, 16 November 2010", mat: 40.00, matPred: "Memadai", indo: 66.67, indoPred: "Memadai" },
            { no: 20, nisn: "0099948557", nama: "KHASBI NOVALDI", ttl: "DAIK LINGGA, 18 November 2009", mat: 36.67, matPred: "Memadai", indo: 56.67, indoPred: "Memadai" },
            { no: 21, nisn: "0107778998", nama: "Sabrina Embun Pertiwi", ttl: "Daik Lingga, 31 Juli 2010", mat: 40.00, matPred: "Memadai", indo: 60.00, indoPred: "Memadai" },
            { no: 22, nisn: "0116938426", nama: "Syarifah Zilfa Natasya", ttl: "Tanjung Pinang, 26 Mei 2011", mat: 43.33, matPred: "Memadai", indo: 80.00, indoPred: "Baik" },
            { no: 23, nisn: "0119879134", nama: "SHAZIA ZARA ALISHA", ttl: "TANJUNG PINANG, 24 Maret 2011", mat: 46.67, matPred: "Memadai", indo: 60.00, indoPred: "Memadai" },
            { no: 24, nisn: "0117587242", nama: "sapinah", ttl: "merawang, 1 September 2011", mat: 26.67, matPred: "Kurang", indo: 46.67, indoPred: "Kurang" },
            { no: 25, nisn: "0115247372", nama: "Meisya Awalun Nurhasanah", ttl: "Daik Lingga, 6 Mei 2011", mat: 26.67, matPred: "Kurang", indo: 53.33, indoPred: "Memadai" },
            { no: 26, nisn: "0113332240", nama: "NUR RAFNI YASMADI", ttl: "KOTA SOLOK, 27 Januari 2011", mat: 33.33, matPred: "Memadai", indo: 50.00, indoPred: "Memadai" },
            { no: 27, nisn: "0114298991", nama: "ZAI ISRAKMIDIAH", ttl: "Tanjungpinang, 29 Juni 2011", mat: 36.67, matPred: "Memadai", indo: 66.67, indoPred: "Memadai" },
            { no: 28, nisn: "0112792471", nama: "AISH GHAZIYA RAFIFA", ttl: "DAIK LINGGA, 7 Agustus 2011", mat: 50.00, matPred: "Memadai", indo: 63.33, indoPred: "Memadai" },
            { no: 29, nisn: "0105796473", nama: "GUNAWAN FAUZI", ttl: "DAIK LINGGA, 1 Desember 2010", mat: 33.33, matPred: "Memadai", indo: 43.33, indoPred: "Kurang" },
            { no: 30, nisn: "0112376775", nama: "ISNAINI", ttl: "DAIK LINGGA, 6 Juni 2011", mat: 36.67, matPred: "Memadai", indo: 36.67, indoPred: "Kurang" },
            { no: 31, nisn: "0101111863", nama: "Ananda Ibnu Fahrezi", ttl: "Daik Lingga, 10 November 2010", mat: 33.33, matPred: "Memadai", indo: 76.67, indoPred: "Baik" },
            { no: 32, nisn: "0111647237", nama: "Faqiha Tazkiatun Nufus", ttl: "Daik Lingga, 27 Agustus 2011", mat: 36.67, matPred: "Memadai", indo: 70.00, indoPred: "Memadai" },
            { no: 33, nisn: "0113654663", nama: "MUHAMMAD MUFLIH HIBATULLAH NURVAL", ttl: "DAIK LINGGA, 6 Juni 2011", mat: 50.00, matPred: "Memadai", indo: 46.67, indoPred: "Kurang" },
            { no: 34, nisn: "0113688046", nama: "rati junila", ttl: "air sesap, 21 Juni 2011", mat: 33.33, matPred: "Memadai", indo: 70.00, indoPred: "Memadai" },
            { no: 35, nisn: "0112757766", nama: "ZALFA MUFIDAH INAYAH", ttl: "AIR BERANI, 1 Juni 2011", mat: 50.00, matPred: "Memadai", indo: 70.00, indoPred: "Memadai" },
            { no: 36, nisn: "0117042213", nama: "Dyra Altha Funisya", ttl: "Daik Lingga, 9 Juli 2011", mat: 53.33, matPred: "Memadai", indo: 76.67, indoPred: "Baik" },
            { no: 37, nisn: "0114103715", nama: "RAFADIL ANΑΝΤΑ", ttl: "Daik Lingga, 11 Januari 2011", mat: 46.67, matPred: "Memadai", indo: 73.33, indoPred: "Memadai" },
            { no: 38, nisn: "0112333526", nama: "RINA RIYANTI", ttl: "DUARA, 20 Juli 2011", mat: 46.67, matPred: "Memadai", indo: 53.33, indoPred: "Memadai" },
            { no: 39, nisn: "0107287635", nama: "NATASYA ZULHAFIFAH", ttl: "DAIK LINGGA, 28 November 2010", mat: 16.67, matPred: "Kurang", indo: 66.67, indoPred: "Memadai" },
            { no: 40, nisn: "0114766625", nama: "Sheril Gianda Utami", ttl: "Daik Lingga, 15 Oktober 2011", mat: 30.00, matPred: "Kurang", indo: 43.33, indoPred: "Kurang" },
            { no: 41, nisn: "0113394958", nama: "SYARIFAH NAFIA SAFIZ", ttl: "TANJUNG PINANG, 9 Agustus 2011", mat: 50.00, matPred: "Memadai", indo: 80.00, indoPred: "Baik" },
            { no: 42, nisn: "0113962310", nama: "RISNA ULKA ARYANI", ttl: "DAIK LINGGA, 7 Januari 2011", mat: 33.33, matPred: "Memadai", indo: 60.00, indoPred: "Memadai" },
            { no: 43, nisn: "0101800405", nama: "REFAN PINANDO", ttl: "TANJUNG PINANG, 29 November 2010", mat: 56.67, matPred: "Baik", indo: 40.00, indoPred: "Kurang" },
            { no: 44, nisn: "0106977903", nama: "VIKY ADITYA SYAPUTRA", ttl: "DAIK LINGGA, 4 April 2010", mat: 46.67, matPred: "Memadai", indo: 40.00, indoPred: "Kurang" },
            { no: 45, nisn: "0112026378", nama: "SILA ADELIA", ttl: "DAIK LINGGA, 19 Februari 2011", mat: 33.33, matPred: "Memadai", indo: 63.33, indoPred: "Memadai" },
            { no: 46, nisn: "0114122561", nama: "Liyana Zahira", ttl: "Kijang, 14 April 2011", mat: 23.33, matPred: "Kurang", indo: 60.00, indoPred: "Memadai" },
            { no: 47, nisn: "0115557747", nama: "adelia dwi nurmansyah", ttl: "kampung budus, 30 April 2011", mat: 43.33, matPred: "Memadai", indo: 80.00, indoPred: "Baik" },
            { no: 48, nisn: "0112426972", nama: "JEANTRIKA SAPUTERA", ttl: "DAIK LINGGA, 5 Juli 2011", mat: 50.00, matPred: "Memadai", indo: 46.67, indoPred: "Kurang" },
            { no: 49, nisn: "0097680988", nama: "Delvry Anggara Panjaitan", ttl: "Daik, 14 Desember 2009", mat: 53.33, matPred: "Memadai", indo: 70.00, indoPred: "Memadai" },
            { no: 50, nisn: "0115755742", nama: "Zatia Maysya", ttl: "Daik, 8 Februari 2011", mat: 53.33, matPred: "Memadai", indo: 83.33, indoPred: "Baik" },
            { no: 51, nisn: "0113402279", nama: "RIZKA INDRI ADELIASA", ttl: "DAIK LINGGA, 5 Januari 2011", mat: 43.33, matPred: "Memadai", indo: 53.33, indoPred: "Memadai" },
            { no: 52, nisn: "0118789434", nama: "RAJA FATHUR ABDILLAH", ttl: "DAIK LINGGA, 30 Agustus 2011", mat: 60.00, matPred: "Baik", indo: 73.33, indoPred: "Memadai" },
            { no: 53, nisn: "0118177962", nama: "MARWA DWI RAMADANI", ttl: "SERANGGAS, 22 Agustus 2011", mat: 53.33, matPred: "Memadai", indo: 86.67, indoPred: "Baik" },
            { no: 54, nisn: "0112631039", nama: "Dafitra Ariansyah", ttl: "Daik Lingga, 20 Januari 2011", mat: 46.67, matPred: "Memadai", indo: 60.00, indoPred: "Memadai" },
            { no: 55, nisn: "0102053051", nama: "Muhammad Gibran Assyafari", ttl: "Kerandin, 13 Februari 2010", mat: 50.00, matPred: "Memadai", indo: 66.67, indoPred: "Memadai" },
            { no: 56, nisn: "0109121124", nama: "Ghastan Gautama Ginarda", ttl: "Tangerang, 25 Januari 2010", mat: 60.00, matPred: "Baik", indo: 86.67, indoPred: "Baik" },
            { no: 57, nisn: "0118552573", nama: "Muhammad Fadhil Ardiansyah", ttl: "Daik, 21 November 2010", mat: 40.00, matPred: "Memadai", indo: 66.67, indoPred: "Memadai" },
            { no: 58, nisn: "0116317492", nama: "SUKMASARI", ttl: "NEREKEH, 18 Juli 2011", mat: 33.33, matPred: "Memadai", indo: 60.00, indoPred: "Memadai" },
            { no: 59, nisn: "0105395625", nama: "ZIFARA OKTIA GISKA", ttl: "DABO SINGKEP, 7 Oktober 2010", mat: 56.67, matPred: "Baik", indo: 66.67, indoPred: "Memadai" },
            { no: 60, nisn: "0128826786", nama: "M.BAYU RIZKITULLAH", ttl: "SUKAJADI, 20 Januari 2012", mat: 63.33, matPred: "Baik", indo: 53.33, indoPred: "Memadai" },
            { no: 61, nisn: "0102542618", nama: "Herisusanti", ttl: "Daik Lingga, 1 Desember 2010", mat: 53.33, matPred: "Memadai", indo: 86.67, indoPred: "Baik" },
            { no: 62, nisn: "0118960096", nama: "Dzakiyya Naila Sakhi", ttl: "Daik Lingga, 14 Juli 2011", mat: 50.00, matPred: "Memadai", indo: 80.00, indoPred: "Baik" },
            { no: 63, nisn: "0117249653", nama: "Suci Safira Putri", ttl: "Batam, 18 Januari 2011", mat: 53.33, matPred: "Memadai", indo: 70.00, indoPred: "Memadai" },
            { no: 64, nisn: "0115867734", nama: "RIZKA ALFIA AZ ZAHRA", ttl: "DABO SINGKEP, 14 Agustus 2011", mat: 56.67, matPred: "Baik", indo: 80.00, indoPred: "Baik" },
            { no: 65, nisn: "0119453195", nama: "NAZILA MAHARANI", ttl: "TANJUNGPINANG, 24 November 2011", mat: 30.00, matPred: "Kurang", indo: 83.33, indoPred: "Baik" },
            { no: 66, nisn: "0118730407", nama: "Mulhuda", ttl: "Panggak Darat, 13 Mei 2011", mat: 46.67, matPred: "Memadai", indo: 66.67, indoPred: "Memadai" },
            { no: 67, nisn: "0119247555", nama: "HANY BAZLINDA", ttl: "NEREKEH, 24 April 2011", mat: 56.67, matPred: "Baik", indo: 83.33, indoPred: "Baik" },
            { no: 68, nisn: "0105795746", nama: "Sahrini Ramadani", ttl: "Daik Lingga, 11 Agustus 2010", mat: 43.33, matPred: "Memadai", indo: 26.67, indoPred: "Kurang" },
            { no: 69, nisn: "0114699199", nama: "RISKY ARDIAN MISKA SACHPUTRA", ttl: "DAIK LINGGA, 15 April 2011", mat: 40.00, matPred: "Memadai", indo: 53.33, indoPred: "Memadai" },
            { no: 70, nisn: "0106306052", nama: "NI'A ROSA", ttl: "DAIK LINGGA, 21 September 2010", mat: 46.67, matPred: "Memadai", indo: 63.33, indoPred: "Memadai" },
            { no: 71, nisn: "0114478647", nama: "ACHAI ANDREAS", ttl: "MENTENGAH, 2 Mei 2011", mat: 46.67, matPred: "Memadai", indo: 63.33, indoPred: "Memadai" },
            { no: 72, nisn: "0111751808", nama: "SYARIFAH IZZATI AQILA", ttl: "DAIK LINGGA, 27 Januari 2011", mat: 40.00, matPred: "Memadai", indo: 76.67, indoPred: "Baik" },
            { no: 73, nisn: "0119149285", nama: "ANUGRAH AGUSTI RAMADHANI", ttl: "DAIK LINGGA, 12 Agustus 2011", mat: 56.67, matPred: "Baik", indo: 80.00, indoPred: "Baik" },
            { no: 74, nisn: "0091754679", nama: "HESTY YOLANDA SIRABANG", ttl: "Medan, 18 Desember 2009", mat: 46.67, matPred: "Memadai", indo: 76.67, indoPred: "Baik" },
            { no: 75, nisn: "0111226881", nama: "usman", ttl: "daik lingga, 13 Februari 2011", mat: 43.33, matPred: "Memadai", indo: 60.00, indoPred: "Memadai" },
            { no: 76, nisn: "0106504994", nama: "ZURRIATI FARHANA", ttl: "DAIK LINGGA, 25 September 2010", mat: 26.67, matPred: "Kurang", indo: 76.67, indoPred: "Baik" },
            { no: 77, nisn: "0116283543", nama: "Erina Nazira", ttl: "Daik Lingga, 21 Juli 2011", mat: 43.33, matPred: "Memadai", indo: 63.33, indoPred: "Memadai" },
            { no: 78, nisn: "0102191383", nama: "WINDA AULIA", ttl: "DAIK LINGGA, 1 Oktober 2010", mat: 30.00, matPred: "Kurang", indo: 46.67, indoPred: "Kurang" },
            { no: 79, nisn: "0113021378", nama: "ARFA", ttl: "TANJUNG PINANG, 26 Mei 2011", mat: 43.33, matPred: "Memadai", indo: 63.33, indoPred: "Memadai" },
            { no: 80, nisn: "0103349505", nama: "Novita Adha Riah", ttl: "Daik Lingga, 17 November 2010", mat: 46.67, matPred: "Memadai", indo: 53.33, indoPred: "Memadai" },
            { no: 81, nisn: "0093969948", nama: "NOVRIAN SAPUTRA", ttl: "DAIK LINGGA, 13 November 2009", mat: 40.00, matPred: "Memadai", indo: 36.67, indoPred: "Kurang" },
            { no: 82, nisn: "0119656574", nama: "SILVIA FRANSISKA NATALIA", ttl: "MENTENGAH, 23 September 2011", mat: 43.33, matPred: "Memadai", indo: 73.33, indoPred: "Memadai" },
            { no: 83, nisn: "0107212771", nama: "ANGGARA PRATAMA", ttl: "DAIK LINGGA, 8 Juli 2010", mat: 33.33, matPred: "Memadai", indo: 33.33, indoPred: "Kurang" },
            { no: 84, nisn: "0119389544", nama: "Nazriel Alfarizqy Yuniar", ttl: "Pompanua, 8 Juli 2011", mat: 46.67, matPred: "Memadai", indo: 76.67, indoPred: "Baik" },
            { no: 85, nisn: "0102286678", nama: "Faiz Fayzul Haq", ttl: "Daik Lingga, 2 Oktober 2010", mat: 46.67, matPred: "Memadai", indo: 83.33, indoPred: "Baik" },
            { no: 86, nisn: "0115970688", nama: "Rahmanda Pratama", ttl: "Panggak Darat, 24 Februari 2011", mat: 26.67, matPred: "Kurang", indo: 46.67, indoPred: "Kurang" },
            { no: 87, nisn: "0118701232", nama: "megawati", ttl: "daik lingga, 27 Juli 2011", mat: 56.67, matPred: "Baik", indo: 76.67, indoPred: "Baik" },
            { no: 88, nisn: "0108287271", nama: "MAHARANI DEWI", ttl: "DAIK LINGGA, 5 Desember 2010", mat: 53.33, matPred: "Memadai", indo: 60.00, indoPred: "Memadai" }
        ];

        let processedStudents = [];

        // --- 2. ENGINE PEMROSES DATA & RANKING OTOMATIS ---
        function initDataProcessing() {
            processedStudents = rawStudentsData.map(student => {
                // Konversi null menjadi 0 untuk kalkulasi rata-rata adil
                const matVal = student.mat || 0;
                const indoVal = student.indo || 0;
                const average = (matVal + indoVal) / 2;
                return { ...student, average: parseFloat(average.toFixed(2)) };
            });

            // Urutkan Rata-rata dari Tertinggi ke Terendah
            processedStudents.sort((a, b) => b.average - a.average);

            // Pasang Variabel Peringkat Otomatis
            processedStudents = processedStudents.map((student, index) => {
                return { ...student, rank: index + 1 };
            });
        }

        // --- 3. HITUNG STATISTIK ANONIM (LAMAN HOME) ---
        function generateClassStatistics() {
            let totalMat = 0, validMatCount = 0;
            let totalIndo = 0, validIndoCount = 0;

            let matDist = { Baik: 0, Memadai: 0, Kurang: 0 };
            let indoDist = { Baik: 0, Memadai: 0, Kurang: 0 };

            rawStudentsData.forEach(s => {
                if(s.mat !== null) { totalMat += s.mat; validMatCount++; }
                if(s.indo !== null) { totalIndo += s.indo; validIndoCount++; }

                matDist[s.matPred]++;
                indoDist[s.indoPred]++;
            });

            const avgMat = totalMat / validMatCount;
            const avgIndo = totalIndo / validIndoCount;

            document.getElementById('class-avg-mat').innerText = avgMat.toFixed(2);
            document.getElementById('class-avg-indo').innerText = avgIndo.toFixed(2);

            // Render Custom HTML Bar Charts
            renderBarChart('chart-mat', matDist, rawStudentsData.length);
            renderBarChart('chart-indo', indoDist, rawStudentsData.length);
        }

        function renderBarChart(elementId, distObj, total) {
            const container = document.getElementById(elementId);
            container.innerHTML = '';

            const keys = ['Baik', 'Memadai', 'Kurang'];
            const classes = { Baik: 'fill-baik', Memadai: 'fill-memadai', Kurang: 'fill-kurang' };

            keys.forEach(key => {
                const count = distObj[key];
                const pct = ((count / total) * 100).toFixed(1);

                const barRow = document.createElement('div');
                barRow.className = 'bar-row';
                barRow.innerHTML = `
                    <div class="bar-label-group">
                        <span>${key}</span>
                        <span>${count} Siswa (${pct}%)</span>
                    </div>
                    <div class="bar-track">
                        <div class="bar-fill ${classes[key]}" style="width: 0%"></div>
                    </div>
                `;
                container.appendChild(barRow);

                // Efek animasi transisi tumbuh grafik
                setTimeout(() => {
                    barRow.querySelector('.bar-fill').style.width = pct + '%';
                }, 100);
            });
        }

        // --- 4. ENGINE PENCARIAN REAL-TIME & FILTER NISN ---
        const searchInput = document.getElementById('search-input');
        const resultsContainer = document.getElementById('search-results-container');
        const loadingSpinner = document.getElementById('loading-spinner');
        const envelopeCard = document.getElementById('envelope-result-card');

        searchInput.addEventListener('input', function() {
            const query = this.value.trim();
            envelopeCard.style.display = 'none'; // Sembunyikan kartu amplop saat mengetik ulang

            if (query.length < 2) {
                resultsContainer.innerHTML = '';
                return;
            }

            const filtered = processedStudents.filter(student => 
                student.nisn.toUpperCase().includes(query.toUpperCase())
            );

            renderSearchResults(filtered);
        });

        function renderSearchResults(list) {
            resultsContainer.innerHTML = '';
            if (list.length === 0) {
                resultsContainer.innerHTML = `
                    <div style="text-align:center; padding: 16px; font-size:13px; color:#64748b; font-weight:600;">
                        <i class="fa-solid fa-triangle-exclamation" style="margin-right:6px;"></i> NISN Tidak Ditemukan
                    </div>`;
                return;
            }

            list.forEach(student => {
                const btn = document.createElement('button');
                btn.className = 'student-item-btn';
                btn.onclick = () => triggerEnvelopeSurprise(student.rank);
                btn.innerHTML = `
                    <div class="student-item-info">
                        <h4>${student.nama.toUpperCase()}</h4>
                        <p>NISN: ${student.nisn}</p>
                    </div>
                    <div class="btn-open-envelope">
                        <i class="fa-solid fa-envelope-open"></i> Buka
                    </div>
                `;
                resultsContainer.appendChild(btn);
            });
        }

        // --- 5. DRAMATIC LOADING & SURPRISE EFFECT GENERATOR ---
        function triggerEnvelopeSurprise(rankId) {
            resultsContainer.innerHTML = '';
            searchInput.value = '';
            envelopeCard.style.display = 'none';
            loadingSpinner.style.display = 'flex';

            // Timer Delay 1.2 Detik Membangun Ketegangan Positif Siswa
            setTimeout(() => {
                loadingSpinner.style.display = 'none';
                displayIndividualCard(rankId);
            }, 1200);
        }

        function displayIndividualCard(rankId) {
            const student = processedStudents.find(s => s.rank === rankId);
            if (!student) return;

            // Reset Class Rank pada Kartu
            envelopeCard.className = 'm3-glass envelope-card';

            // Pilih Desain & Lencana Berdasarkan Perangkingan Kelas
            const badgeEl = document.getElementById('res-badge');
            if (student.rank === 1) {
                envelopeCard.classList.add('rank-1');
                badgeEl.innerHTML = '<i class="fa-solid fa-trophy"></i> Juara 1';
            } else if (student.rank === 2) {
                envelopeCard.classList.add('rank-2');
                badgeEl.innerHTML = '<i class="fa-solid fa-medal"></i> Juara 2';
            } else if (student.rank === 3) {
                envelopeCard.classList.add('rank-3');
                badgeEl.innerHTML = '<i class="fa-solid fa-medal"></i> Juara 3';
            } else {
                envelopeCard.classList.add('rank-normal');
                badgeEl.innerHTML = `<i class="fa-solid fa-award"></i> Rank ${student.rank}`;
            }

            // Pasang Komponen Data Individu
            document.getElementById('res-nama').innerText = student.nama.toUpperCase();
            document.getElementById('res-nisn').innerText = `NISN: ${student.nisn}`;
            document.getElementById('res-ttl').innerText = student.ttl;

            // Atur Score & Tag Kategori Nilai Matematika
            const matScoreStr = student.mat !== null ? student.mat.toFixed(2) : '0.00';
            document.getElementById('res-mat-score').innerText = matScoreStr;
            const matPredEl = document.getElementById('res-mat-pred');
            matPredEl.innerText = student.matPred;
            matPredEl.className = 'predicate-tag ' + (student.matPred === 'Baik' ? 'pred-baik' : student.matPred === 'Memadai' ? 'pred-memadai' : 'pred-kurang');

            // Atur Score & Tag Kategori Nilai Bahasa Indonesia
            const indoScoreStr = student.indo !== null ? student.indo.toFixed(2) : '0.00';
            document.getElementById('res-indo-score').innerText = indoScoreStr;
            const indoPredEl = document.getElementById('res-indo-pred');
            indoPredEl.innerText = student.indoPred;
            indoPredEl.className = 'predicate-tag ' + (student.indoPred === 'Baik' ? 'pred-baik' : student.indoPred === 'Memadai' ? 'pred-memadai' : 'pred-kurang');

            // Rata-rata Kombinasi Akhir
            document.getElementById('res-avg-score').innerText = student.average.toFixed(2);

            // Jalankan Trigger Tampilan Card
            envelopeCard.style.display = 'flex';
        }

        // --- 6. SWITCH SISTEM NAVIGASI TAB NAVBAR ---
        function switchTab(screenId, element) {
            // Reset Status Active Semua Nav Item
            document.querySelectorAll('.nav-item').forEach(btn => btn.classList.remove('active'));
            // Reset Status Active Semua Screen View
            document.querySelectorAll('.screen-view').forEach(scr => scr.classList.remove('active'));

            // Aktifkan Item Pilihan
            element.classList.add('active');
            document.getElementById(`screen-${screenId}`).classList.add('active');

            // Membersihkan Sisa State Pencarian Sebelumnya Jika Berpindah
            if(screenId === 'home') {
                generateClassStatistics();
            } else {
                resultsContainer.innerHTML = '';
                envelopeCard.style.display = 'none';
                searchInput.value = '';
            }
        }

        // --- CORE RUNNER ON LOAD ---
        window.addEventListener('DOMContentLoaded', () => {
            initDataProcessing();
            // Default awal terkunci pada screen Nilaiku sesuai instruksi
        });
    </script>
</body>
</html>
