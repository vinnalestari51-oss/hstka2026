<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hasil Tes Kemampuan Akademik 2026 - SMPN 1 Lingga</title>
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
        }

        /* --- CONTAINER MOBILE-FIRST (MAX 440PX) --- */
        .container-mobile {
            width: 100%;
            max-width: 440px;
            min-height: 100vh;
            background-color: #f8fafc;
            position: relative;
            padding: 24px 20px 100px 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.03);
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        /* --- UTILITY CLASS: MATERIAL 3 EXPRESSIVE GLASS --- */
        .m3-glass {
            background: rgba(255, 255, 255, 0.85);
            backdrop-filter: blur(20px);
            -webkit-backdrop-filter: blur(20px);
            border: 1px solid rgba(255, 255, 255, 0.9);
            border-radius: 24px;
            padding: 20px;
            box-shadow: 0 8px 32px rgba(31, 38, 135, 0.04);
        }

        /* --- HEADER BRANDING --- */
        .header-brand {
            display: flex;
            align-items: center;
            gap: 14px;
            margin-bottom: 4px;
        }

        .header-brand .icon-edu {
            width: 48px;
            height: 48px;
            background: linear-gradient(135deg, #2563eb, #3b82f6);
            border-radius: 16px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #ffffff;
            font-size: 20px;
            box-shadow: 0 4px 14px rgba(37, 99, 235, 0.2);
        }

        .header-brand h1 {
            font-size: 16px;
            font-weight: 800;
            color: #1e3a8a;
            line-height: 1.2;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }

        .header-brand p {
            font-size: 11px;
            color: #64748b;
            font-weight: 500;
            margin-top: 2px;
        }

        /* --- APP PAGES STATE MANAGEMENT --- */
        .app-page {
            display: none;
            width: 100%;
            animation: fadeIn 0.4s ease-out;
        }

        .app-page.active {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(8px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* --- FIXED BOTTOM NAVBAR --- */
        .bottom-navbar {
            position: fixed;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 100%;
            max-width: 440px;
            height: 72px;
            background: rgba(255, 255, 255, 0.92);
            backdrop-filter: blur(15px);
            -webkit-backdrop-filter: blur(15px);
            border-top: 1px solid rgba(226, 232, 240, 0.8);
            display: flex;
            justify-content: space-around;
            align-items: center;
            z-index: 999;
            padding: 0 12px;
        }

        .nav-item {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            gap: 6px;
            background: none;
            border: none;
            cursor: pointer;
            width: 64px;
            height: 100%;
            color: #64748b;
            transition: all 0.25s ease;
            position: relative;
        }

        .nav-item i {
            font-size: 20px;
            transition: transform 0.2s ease;
        }

        .nav-item span {
            font-size: 11px;
            font-weight: 600;
            letter-spacing: 0.2px;
        }

        .nav-item.active {
            color: #2563eb;
        }

        .nav-item.active i {
            transform: translateY(-2px);
        }

        .nav-item.active::after {
            content: '';
            position: absolute;
            top: 0;
            width: 28px;
            height: 4px;
            background-color: #2563eb;
            border-radius: 0 0 4px 4px;
        }

        /* --- KONTEN LAMAN: HOME (STATISTIK ANONIM) --- */
        .stats-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 12px;
        }

        .stat-card {
            background: #ffffff;
            border-radius: 20px;
            padding: 16px;
            border: 1px solid #e2e8f0;
            display: flex;
            flex-direction: column;
            gap: 6px;
        }

        .stat-card .label {
            font-size: 11px;
            font-weight: 600;
            color: #64748b;
            display: flex;
            align-items: center;
            gap: 6px;
        }

        .stat-card .value {
            font-size: 24px;
            font-weight: 800;
            color: #1e293b;
        }

        .section-title {
            font-size: 14px;
            font-weight: 700;
            color: #334155;
            margin-bottom: 4px;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        /* CUSTOM CSS MANUAL PROGRESS BAR (GRAFIK DISTRIBUSI) */
        .chart-group {
            display: flex;
            flex-direction: column;
            gap: 12px;
            margin-top: 8px;
        }

        .chart-row {
            display: flex;
            flex-direction: column;
            gap: 4px;
        }

        .chart-label-container {
            display: flex;
            justify-content: space-between;
            font-size: 11px;
            font-weight: 600;
            color: #475569;
        }

        .bar-container {
            width: 100%;
            height: 10px;
            background: #e2e8f0;
            border-radius: 10px;
            overflow: hidden;
        }

        .bar-fill {
            height: 100%;
            border-radius: 10px;
            transition: width 1s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .bar-baik { background: linear-gradient(90deg, #10b981, #34d399); }
        .bar-memadai { background: linear-gradient(90deg, #3b82f6, #60a5fa); }
        .bar-kurang { background: linear-gradient(90deg, #f59e0b, #fbbf24); }

        /* --- KONTEN LAMAN: NILAIKU (PENCARIAN AMPLUP) --- */
        .search-box {
            display: flex;
            flex-direction: column;
            gap: 14px;
        }

        .search-title {
            font-size: 15px;
            font-weight: 700;
            color: #1e3a8a;
            text-align: center;
            line-height: 1.4;
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
            height: 54px;
            background: #ffffff;
            border: 2px solid #e2e8f0;
            border-radius: 16px;
            padding: 0 16px 0 46px;
            font-size: 15px;
            font-weight: 600;
            color: #1e293b;
            outline: none;
            transition: all 0.2s ease;
        }

        .input-nisn:focus {
            border-color: #2563eb;
            box-shadow: 0 0 0 4px rgba(37, 99, 235, 0.1);
        }

        .btn-search {
            width: 100%;
            height: 52px;
            background: linear-gradient(135deg, #1e3a8a, #2563eb);
            border: none;
            border-radius: 16px;
            color: #ffffff;
            font-size: 15px;
            font-weight: 700;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            box-shadow: 0 4px 12px rgba(37, 99, 235, 0.2);
            transition: transform 0.1s ease, opacity 0.2s;
        }

        .btn-search:active {
            transform: scale(0.98);
        }

        /* --- ANIMASI LOADING DRAMATIS --- */
        .loading-container {
            display: none;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            padding: 40px 20px;
            gap: 16px;
        }

        .spinner {
            width: 48px;
            height: 48px;
            border: 5px solid rgba(37, 99, 235, 0.1);
            border-top-color: #2563eb;
            border-radius: 50%;
            animation: spin 1s linear infinite;
        }

        .pulse-text {
            font-size: 13px;
            font-weight: 600;
            color: #2563eb;
            animation: pulse 1.2s infinite ease-in-out;
        }

        @keyframes spin { to { transform: rotate(360deg); } }
        @keyframes pulse {
            0%, 100% { opacity: 0.6; transform: scale(0.98); }
            50% { opacity: 1; transform: scale(1.02); }
        }

        /* --- SURPRISE BOUNCE EFFECT CARD --- */
        .result-envelope {
            display: none;
            width: 100%;
        }

        .result-card {
            width: 100%;
            border-radius: 24px;
            padding: 24px;
            display: flex;
            flex-direction: column;
            gap: 18px;
            position: relative;
            overflow: hidden;
            animation: surpriseBounce 0.65s cubic-bezier(0.175, 0.885, 0.32, 1.275) both;
        }

        @keyframes surpriseBounce {
            0% { opacity: 0; transform: scale(0.4) translateY(120px); }
            70% { transform: scale(1.05) translateY(-8px); }
            100% { opacity: 1; transform: scale(1) translateY(0); }
        }

        /* --- THEME VARIATION RANK KARTU INDIVIDU --- */
        
        /* RANK 1: GRADASI HIJAU PASTEL + SHIMMER EFFECT */
        .card-rank-1 {
            background: linear-gradient(135deg, #d1fae5, #a7f3d0);
            border: 3px solid #34d399;
            box-shadow: 0 12px 24px rgba(52, 211, 153, 0.25);
            background-size: 200% 200%;
            animation: surpriseBounce 0.65s cubic-bezier(0.175, 0.885, 0.32, 1.275) both, shimmerBackground 4s ease infinite;
        }
        @keyframes shimmerBackground {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        /* RANK 2: GRADASI BIRU PASTEL */
        .card-rank-2 {
            background: linear-gradient(135deg, #dbaefe, #bfdbfe);
            border: 2px solid #60a5fa;
            box-shadow: 0 10px 20px rgba(96, 165, 250, 0.2);
        }

        /* RANK 3: GRADASI ORANYE PASTEL WARM */
        .card-rank-3 {
            background: linear-gradient(135deg, #ffedd5, #fdbb74);
            border: 2px solid #fb923c;
            box-shadow: 0 10px 20px rgba(251, 146, 60, 0.2);
        }

        /* RANK GENERAL (4 KE BAWAH) */
        .card-rank-general {
            background: rgba(255, 255, 255, 0.9);
            border: 1px solid #e2e8f0;
            box-shadow: 0 8px 24px rgba(0, 0, 0, 0.02);
        }

        /* CARD ELEMENTS LAYOUT */
        .card-header {
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            border-bottom: 1px dashed rgba(0,0,0,0.08);
            padding-bottom: 14px;
        }

        .student-bio h2 {
            font-size: 18px;
            font-weight: 800;
            color: #0f172a;
            letter-spacing: -0.3px;
        }

        .student-bio p {
            font-size: 12px;
            color: #475569;
            font-weight: 600;
            margin-top: 2px;
        }

        .badge-rank {
            padding: 8px 14px;
            border-radius: 12px;
            font-size: 12px;
            font-weight: 800;
            display: flex;
            align-items: center;
            gap: 6px;
        }

        .badge-rank-1 { background: #10b981; color: #ffffff; }
        .badge-rank-2 { background: #2563eb; color: #ffffff; }
        .badge-rank-3 { background: #ea580c; color: #ffffff; }
        .badge-rank-general { background: #64748b; color: #ffffff; }

        /* KELURUSAN BARIS NILAI (LAYOUT VERTIKAL ANTI-NABRAK HP SEMPIT) */
        .scores-vertical-stack {
            display: flex;
            flex-direction: column;
            gap: 10px;
        }

        .score-row-box {
            background: rgba(255, 255, 255, 0.6);
            border-radius: 16px;
            padding: 12px 16px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            border: 1px solid rgba(255, 255, 255, 0.5);
        }

        .score-left-info {
            display: flex;
            flex-direction: column;
            gap: 4px;
            align-items: flex-start;
        }

        .subject-name {
            font-size: 13px;
            font-weight: 700;
            color: #334155;
        }

        /* Tag Kategori Lebar Otomatis (Width Auto) */
        .score-tag-predikat {
            width: auto;
            padding: 3px 8px;
            border-radius: 6px;
            font-size: 10px;
            font-weight: 700;
            text-transform: uppercase;
        }

        .tag-baik { background-color: #d1fae5; color: #065f46; }
        .tag-memadai { background-color: #dbeafe; color: #1e40af; }
        .tag-kurang { background-color: #fef3c7; color: #92400e; }

        .score-right-value {
            font-size: 24px;
            font-weight: 800;
            color: #0f172a;
        }

        /* FOOTER KARTU */
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

        .card-footer-average .final-avg-val {
            font-size: 16px;
            font-weight: 800;
            color: #1e293b;
        }

        .error-message {
            display: none;
            background: #fef2f2;
            border: 1px solid #fee2e2;
            border-radius: 16px;
            padding: 14px;
            color: #991b1b;
            font-size: 12px;
            font-weight: 600;
            text-align: center;
            align-items: center;
            justify-content: center;
            gap: 8px;
        }
    </style>
</head>
<body>

    <div class="container-mobile">
        
        <div class="m3-glass header-brand">
            <div class="icon-edu">
                <i class="fa-solid fa-graduation-cap"></i>
            </div>
            <div>
                <h1>SMP Negeri 1 Lingga</h1>
                <p>Kolektif Hasil Tes Kemampuan Akademik 2026</p>
            </div>
        </div>

        <div id="page-home" class="app-page">
            
            <div class="stats-grid">
                <div class="stat-card">
                    <div class="label">
                        <i class="fa-solid fa-calculator" style="color:#2563eb;"></i> MTK Kelas
                    </div>
                    <div class="value" id="avg-mtk-kelas">0.00</div>
                </div>
                <div class="stat-card">
                    <div class="label">
                        <i class="fa-solid fa-book" style="color:#10b981;"></i> B. IND Kelas
                    </div>
                    <div class="value" id="avg-ind-kelas">0.00</div>
                </div>
            </div>

            <div class="m3-glass">
                <div class="section-title">
                    <i class="fa-solid fa-chart-bar" style="color:#2563eb;"></i> Distribusi Matematika
                </div>
                <div class="chart-group" id="distribusi-mtk-chart">
                    </div>
            </div>

            <div class="m3-glass">
                <div class="section-title">
                    <i class="fa-solid fa-chart-bar" style="color:#10b981;"></i> Distribusi B. Indonesia
                </div>
                <div class="chart-group" id="distribusi-ind-chart">
                    </div>
            </div>

        </div>

        <div id="page-nilaiku" class="app-page active">
            
            <div class="m3-glass search-box">
                <div class="search-title">Masukkan NISN Siswa Untuk Membuka Amplop Hasil Kelulusan</div>
                
                <div class="input-wrapper">
                    <i class="fa-solid fa-id-card-clip"></i>
                    <input type="number" id="input-search-nisn" class="input-nisn" placeholder="Contoh: 0113559822" pattern="[0-9]*" inputmode="numeric">
                </div>

                <button class="btn-search" onclick="prosesBukaAmplop()">
                    <i class="fa-solid fa-envelope-open-text"></i> Buka Amplop Nilai
                </button>
            </div>

            <div id="search-error" class="error-message">
                <i class="fa-solid fa-triangle-exclamation"></i> Maaf, NISN tidak ditemukan. Periksa kembali angka yang dimasukkan.
            </div>

            <div id="search-loading" class="loading-container">
                <div class="spinner"></div>
                <div class="pulse-text">Membuka Kunci Dokumen Amplop...</div>
            </div>

            <div id="envelope-target" class="result-envelope">
                </div>

        </div>

        <nav class="bottom-navbar">
            <button class="nav-item" id="nav-home" onclick="pindahLaman('home')">
                <i class="fa-solid fa-chart-simple"></i>
                <span>Home</span>
            </button>
            <button class="nav-item active" id="nav-nilaiku" onclick="pindahLaman('nilaiku')">
                <i class="fa-solid fa-address-card"></i>
                <span>Nilaiku</span>
            </button>
        </nav>

    </div>

    <script>
        // DATA EXTRACED & CLEANED DARI SELURUH 88 SISWA DI PDF
        const RAW_STUDENT_DATA = [
            { no: 1, nisn: "0113067688", nama: "Riska Sari", mtk: 20.00, mtk_pred: "Kurang", ind: 60.00, ind_pred: "Memadai" },
            { no: 2, nisn: "0113559822", nama: "MECA ADELYA CAHYANI", mtk: 50.00, mtk_pred: "Memadai", ind: 90.00, ind_pred: "Baik" },
            { no: 3, nisn: "0115427698", nama: "Dzikri Harith Haziq", mtk: 50.00, mtk_pred: "Memadai", ind: 70.00, ind_pred: "Memadai" },
            { no: 4, nisn: "0123776337", nama: "VANDERSAR MEICHAEL NAINGGOLAN", mtk: 23.33, mtk_pred: "Kurang", ind: 86.67, ind_pred: "Baik" },
            { no: 5, nisn: "0114844674", nama: "Syifa Syaqirah", mtk: 33.33, mtk_pred: "Memadai", ind: 63.33, ind_pred: "Memadai" },
            { no: 6, nisn: "0117775355", nama: "QIAN FERDINAND", mtk: 36.67, mtk_pred: "Memadai", ind: 46.67, ind_pred: "Kurang" },
            { no: 7, nisn: "0116942061", nama: "SYARIFAH NAJWA SAFIZ", mtk: 0.00, mtk_pred: "Kurang", ind: 83.33, ind_pred: "Baik" },
            { no: 8, nisn: "0119458667", nama: "SUHARAYAH", mtk: 26.67, mtk_pred: "Kurang", ind: 63.33, ind_pred: "Memadai" },
            { no: 9, nisn: "0111929206", nama: "AIRIN DWI RAMADHANI", mtk: 40.00, mtk_pred: "Memadai", ind: 63.33, ind_pred: "Memadai" },
            { no: 10, nisn: "0094409765", nama: "Imam Syahibbullah", mtk: 0.00, mtk_pred: "Kurang", ind: 53.33, ind_pred: "Memadai" },
            { no: 11, nisn: "0119416095", nama: "Deby Septiani", mtk: 43.33, mtk_pred: "Memadai", ind: 80.00, ind_pred: "Baik" },
            { no: 12, nisn: "0112474826", nama: "Ibnu Shalim", mtk: 26.67, mtk_pred: "Kurang", ind: 43.33, ind_pred: "Kurang" },
            { no: 13, nisn: "0117387487", nama: "LIPIANA SUCI RAMARANI", mtk: 50.00, mtk_pred: "Memadai", ind: 86.67, ind_pred: "Baik" },
            { no: 14, nisn: "0111805260", nama: "irvan kurnia", mtk: 16.67, mtk_pred: "Kurang", ind: 43.33, ind_pred: "Kurang" },
            { no: 15, nisn: "0086621206", nama: "Arya Imam Risnanda", mtk: 43.33, mtk_pred: "Memadai", ind: 80.00, ind_pred: "Baik" },
            { no: 16, nisn: "0118621492", nama: "Raisa Idadi", mtk: 30.00, mtk_pred: "Kurang", ind: 66.67, ind_pred: "Memadai" },
            { no: 17, nisn: "0116566978", nama: "Kafha Azri Ilhamsyah", mtk: 43.33, mtk_pred: "Memadai", ind: 73.33, ind_pred: "Memadai" },
            { no: 18, nisn: "0114962861", nama: "Muhammad Erwan Zarka", mtk: 36.67, mtk_pred: "Memadai", ind: 63.33, mtk_pred: "Memadai" },
            { no: 19, nisn: "0105152266", nama: "Adonia Najla Raissa", mtk: 40.00, mtk_pred: "Memadai", ind: 66.67, ind_pred: "Memadai" },
            { no: 20, nisn: "0099948557", nama: "KHASBI NOVALDI", mtk: 36.67, mtk_pred: "Memadai", ind: 56.67, ind_pred: "Memadai" },
            { no: 21, nisn: "0107778998", nama: "Sabrina Embun Pertiwi", mtk: 40.00, mtk_pred: "Memadai", ind: 60.00, ind_pred: "Memadai" },
            { no: 22, nisn: "0116938426", nama: "Syarifah Zilfa Natasya", mtk: 43.33, mtk_pred: "Memadai", ind: 80.00, ind_pred: "Baik" },
            { no: 23, nisn: "0119879134", nama: "SHAZIA ZARA ALISHA", mtk: 46.67, mtk_pred: "Memadai", ind: 60.00, ind_pred: "Memadai" },
            { no: 24, nisn: "0117587242", nama: "sapinah", mtk: 26.67, mtk_pred: "Kurang", ind: 46.67, ind_pred: "Kurang" },
            { no: 25, nisn: "0115247372", nama: "Meisya Awalun Nurhasanah", mtk: 26.67, mtk_pred: "Kurang", ind: 53.33, ind_pred: "Memadai" },
            { no: 26, nisn: "0113332240", nama: "NUR RAFNI YASMADI", mtk: 33.33, mtk_pred: "Memadai", ind: 50.00, ind_pred: "Memadai" },
            { no: 27, nisn: "0114298991", nama: "ZAI ISRAKMIDIAH", mtk: 36.67, mtk_pred: "Memadai", ind: 66.67, ind_pred: "Memadai" },
            { no: 28, nisn: "0112792471", nama: "AISH GHAZIYA RAFIFA", mtk: 50.00, mtk_pred: "Memadai", ind: 63.33, ind_pred: "Memadai" },
            { no: 29, nisn: "0105796473", nama: "GUNAWAN FAUZI", mtk: 33.33, mtk_pred: "Memadai", ind: 43.33, ind_pred: "Kurang" },
            { no: 30, nisn: "0112376775", nama: "ISNAINI", mtk: 36.67, mtk_pred: "Memadai", ind: 36.67, ind_pred: "Kurang" },
            { no: 31, nisn: "0101111863", nama: "Ananda Ibnu Fahrezi", mtk: 33.33, mtk_pred: "Memadai", ind: 76.67, ind_pred: "Baik" },
            { no: 32, nisn: "0111647237", nama: "Faqiha Tazkiatun Nufus", mtk: 36.67, mtk_pred: "Memadai", ind: 70.00, ind_pred: "Memadai" },
            { no: 33, nisn: "0113654663", nama: "MUHAMMAD MUFLIH HIBATULLAH NURVAL", mtk: 50.00, mtk_pred: "Memadai", ind: 46.67, ind_pred: "Kurang" },
            { no: 34, nisn: "0113688046", nama: "rati junila", mtk: 33.33, mtk_pred: "Memadai", ind: 70.00, ind_pred: "Memadai" },
            { no: 35, nisn: "0112757766", nama: "ZALFA MUFIDAH INAYAH", mtk: 50.00, mtk_pred: "Memadai", ind: 70.00, ind_pred: "Memadai" },
            { no: 36, nisn: "0117042213", nama: "Dyra Altha Funisya", mtk: 53.33, mtk_pred: "Memadai", ind: 76.67, ind_pred: "Baik" },
            { no: 37, nisn: "0114103715", nama: "RAFADIL ANΑΝΤΑ", mtk: 46.67, mtk_pred: "Memadai", ind: 73.33, ind_pred: "Memadai" },
            { no: 38, nisn: "0112333526", nama: "RINA RIYANTI", mtk: 46.67, mtk_pred: "Memadai", ind: 53.33, ind_pred: "Memadai" },
            { no: 39, nisn: "0107287635", nama: "NATASYA ZULHAFIFAH", mtk: 16.67, mtk_pred: "Kurang", ind: 66.67, ind_pred: "Memadai" },
            { no: 40, nisn: "0114766625", nama: "Sheril Gianda Utami", mtk: 30.00, mtk_pred: "Kurang", ind: 43.33, ind_pred: "Kurang" },
            { no: 41, nisn: "0113394958", nama: "SYARIFAH NAFIA SAFIZ", mtk: 50.00, mtk_pred: "Memadai", ind: 80.00, ind_pred: "Baik" },
            { no: 42, nisn: "0113962310", nama: "RISNA ULKA ARYANI", mtk: 33.33, mtk_pred: "Memadai", ind: 60.00, ind_pred: "Memadai" },
            { no: 43, nisn: "0101800405", nama: "REFAN PINANDO", mtk: 56.67, mtk_pred: "Baik", ind: 40.00, ind_pred: "Kurang" },
            { no: 44, nisn: "0106977903", nama: "VIKY ADITYA SYAPUTRA", mtk: 46.67, mtk_pred: "Memadai", ind: 40.00, ind_pred: "Kurang" },
            { no: 45, nisn: "0112026378", nama: "SILA ADELIA", mtk: 33.33, mtk_pred: "Memadai", ind: 63.33, ind_pred: "Memadai" },
            { no: 46, nisn: "0114122561", nama: "Liyana Zahira", mtk: 23.33, mtk_pred: "Kurang", ind: 60.00, ind_pred: "Memadai" },
            { no: 47, nisn: "0115557747", nama: "adelia dwi nurmansyah", mtk: 43.33, mtk_pred: "Memadai", ind: 80.00, ind_pred: "Baik" },
            { no: 48, nisn: "0112426972", nama: "JEANTRIKA SAPUTERA", mtk: 50.00, mtk_pred: "Memadai", ind: 46.67, ind_pred: "Kurang" },
            { no: 49, nisn: "0097680988", nama: "Delvry Anggara Panjaitan", mtk: 53.33, mtk_pred: "Memadai", ind: 70.00, ind_pred: "Memadai" },
            { no: 50, nisn: "0115755742", nama: "Zatia Maysya", mtk: 53.33, mtk_pred: "Memadai", ind: 83.33, ind_pred: "Baik" },
            { no: 51, nisn: "0113402279", nama: "RIZKA INDRI ADELIASA", mtk: 43.33, mtk_pred: "Memadai", ind: 53.33, ind_pred: "Memadai" },
            { no: 52, nisn: "0118789434", nama: "RAJA FATHUR ABDILLAH", mtk: 60.00, mtk_pred: "Baik", ind: 73.33, ind_pred: "Memadai" },
            { no: 53, nisn: "0118177962", nama: "MARWA DWI RAMADANI", mtk: 53.33, mtk_pred: "Memadai", ind: 86.67, ind_pred: "Baik" },
            { no: 54, nisn: "0112631039", nama: "Dafitra Ariansyah", mtk: 46.67, mtk_pred: "Memadai", ind: 60.00, ind_pred: "Memadai" },
            { no: 55, nisn: "0102053051", nama: "Muhammad Gibran Assyafari", mtk: 50.00, mtk_pred: "Memadai", ind: 66.67, ind_pred: "Memadai" },
            { no: 56, nisn: "0109121124", nama: "Ghastan Gautama Ginarda", mtk: 60.00, mtk_pred: "Baik", ind: 86.67, ind_pred: "Baik" },
            { no: 57, nisn: "0118552573", nama: "Muhammad Fadhil Ardiansyah", mtk: 40.00, mtk_pred: "Memadai", ind: 66.67, ind_pred: "Memadai" },
            { no: 58, nisn: "0116317492", nama: "SUKMASARI", mtk: 33.33, mtk_pred: "Memadai", ind: 60.00, ind_pred: "Memadai" },
            { no: 59, nisn: "0105395625", nama: "ZIFARA OKTIA GISKA", mtk: 56.67, mtk_pred: "Baik", ind: 66.67, ind_pred: "Memadai" },
            { no: 60, nisn: "0128826786", nama: "M.BAYU RIZKITULLAH", mtk: 63.33, mtk_pred: "Baik", ind: 53.33, ind_pred: "Memadai" },
            { no: 61, nisn: "0102542618", nama: "Herisusanti", mtk: 53.33, mtk_pred: "Memadai", ind: 86.67, ind_pred: "Baik" },
            { no: 62, nisn: "0118960096", nama: "Dzakiyya Naila Sakhi", mtk: 50.00, mtk_pred: "Memadai", ind: 80.00, ind_pred: "Baik" },
            { no: 63, nisn: "0117249653", nama: "Suci Safira Putri", mtk: 53.33, mtk_pred: "Memadai", ind: 70.00, ind_pred: "Memadai" },
            { no: 64, nisn: "0115867734", nama: "RIZKA ALFIA AZ ZAHRA", mtk: 56.67, mtk_pred: "Baik", ind: 80.00, ind_pred: "Baik" },
            { no: 65, nisn: "0119453195", nama: "NAZILA MAHARANI", mtk: 30.00, mtk_pred: "Kurang", ind: 83.33, ind_pred: "Baik" },
            { no: 66, nisn: "0118730407", nama: "Mulhuda", mtk: 46.67, mtk_pred: "Memadai", ind: 66.67, ind_pred: "Memadai" },
            { no: 67, nisn: "0119247555", nama: "HANY BAZLINDA", mtk: 56.67, mtk_pred: "Baik", ind: 83.33, ind_pred: "Baik" },
            { no: 68, nisn: "0105795746", nama: "Sahrini Ramadani", mtk: 43.33, mtk_pred: "Memadai", ind: 26.67, ind_pred: "Kurang" },
            { no: 69, nisn: "0114699199", nama: "RISKY ARDIAN MISKA SACHPUTRA", mtk: 40.00, mtk_pred: "Memadai", ind: 53.33, ind_pred: "Memadai" },
            { no: 70, nisn: "0106306052", nama: "NI'A ROSA", mtk: 46.67, mtk_pred: "Memadai", ind: 63.33, ind_pred: "Memadai" },
            { no: 71, nisn: "0114478647", nama: "ACHAI ANDREAS", mtk: 46.67, mtk_pred: "Memadai", ind: 63.33, ind_pred: "Memadai" },
            { no: 72, nisn: "0111751808", nama: "SYARIFAH IZZATI AQILA", mtk: 40.00, mtk_pred: "Memadai", ind: 76.67, ind_pred: "Baik" },
            { no: 73, nisn: "0119149285", nama: "ANUGRAH AGUSTI RAMADHANI", mtk: 56.67, mtk_pred: "Baik", ind: 80.00, ind_pred: "Baik" },
            { no: 74, nisn: "0091754679", nama: "HESTY YOLANDA SIRABANG", mtk: 46.67, mtk_pred: "Memadai", ind: 76.67, ind_pred: "Baik" },
            { no: 75, nisn: "0111226881", nama: "usman", mtk: 43.33, mtk_pred: "Memadai", ind: 60.00, ind_pred: "Memadai" },
            { no: 76, nisn: "0106504994", nama: "ZURRIATI FARHANA", mtk: 26.67, mtk_pred: "Kurang", ind: 76.67, ind_pred: "Baik" },
            { no: 77, nisn: "0116283543", nama: "Erina Nazira", mtk: 43.33, mtk_pred: "Memadai", ind: 63.33, ind_pred: "Memadai" },
            { no: 78, nisn: "0102191383", nama: "WINDA AULIA", mtk: 30.00, mtk_pred: "Kurang", ind: 46.67, ind_pred: "Kurang" },
            { no: 79, nisn: "0113021378", nama: "ARFA", mtk: 43.33, mtk_pred: "Memadai", ind: 63.33, ind_pred: "Memadai" },
            { no: 80, nisn: "0103349505", nama: "Novita Adha Riah", mtk: 46.67, mtk_pred: "Memadai", ind: 53.33, ind_pred: "Memadai" },
            { no: 81, nisn: "0093969948", nama: "NOVRIAN SAPUTRA", mtk: 40.00, mtk_pred: "Memadai", ind: 36.67, ind_pred: "Kurang" },
            { no: 82, nisn: "0119656574", nama: "SILVIA FRANSISKA NATALIA", mtk: 43.33, mtk_pred: "Memadai", ind: 73.33, ind_pred: "Memadai" },
            { no: 83, nisn: "0107212771", nama: "ANGGARA PRATAMA", mtk: 33.33, mtk_pred: "Memadai", ind: 33.33, ind_pred: "Kurang" },
            { no: 84, nisn: "0119389544", nama: "Nazriel Alfarizqy Yuniar", mtk: 46.67, mtk_pred: "Memadai", ind: 76.67, ind_pred: "Baik" },
            { no: 85, nisn: "0102286678", nama: "Faiz Fayzul Haq", mtk: 46.67, mtk_pred: "Memadai", ind: 83.33, ind_pred: "Baik" },
            { no: 86, nisn: "0115970688", nama: "Rahmanda Pratama", mtk: 26.67, mtk_pred: "Kurang", ind: 46.67, ind_pred: "Kurang" },
            { no: 87, nisn: "0118701232", nama: "megawati", mtk: 56.67, mtk_pred: "Baik", ind: 76.67, ind_pred: "Baik" },
            { no: 88, nisn: "0108287271", nama: "MAHARANI DEWI", mtk: 53.33, mtk_pred: "Memadai", ind: 60.00, ind_pred: "Memadai" }
        ];

        let processedData = [];

        // 1. ENGINE INISIALISASI DATA: RATARATA & CODES FOR RANKING
        function initAppEngine() {
            // Hitung rata-rata kombinasi individu
            processedData = RAW_STUDENT_DATA.map(student => {
                const kombinasiAvg = (student.mtk + student.ind) / 2;
                return {
                    ...student,
                    avg: parseFloat(kombinasiAvg.toFixed(2))
                };
            });

            // Urutkan berdasarkan rata-rata tertinggi ke terendah
            processedData.sort((a, b) => b.avg - a.avg);

            // Tetapkan urutan peringkat (Rank) otomatis
            processedData = processedData.map((student, index) => {
                return {
                    ...student,
                    rank: index + 1
                };
            });

            // Kalkulasi Statistik Utama & Render Laman Beranda
            hitungStatistikBeranda();
        }

        // 2. KONTEN LAMAN 1: REKAPITULASI DATA GLOBAL KELAS
        function hitungStatistikBeranda() {
            const totalStudents = processedData.length;
            let sumMtk = 0;
            let sumInd = 0;

            let mtkDist = { Baik: 0, Memadai: 0, Kurang: 0 };
            let indDist = { Baik: 0, Memadai: 0, Kurang: 0 };

            processedData.forEach(s => {
                sumMtk += s.mtk;
                sumInd += s.ind;

                // Distribusi Kategori
                if(mtkDist[s.mtk_pred] !== undefined) mtkDist[s.mtk_pred]++;
                if(indDist[s.ind_pred] !== undefined) indDist[s.ind_pred]++;
            });

            // Render nilai rata-rata global kelas
            document.getElementById('avg-mtk-kelas').innerText = (sumMtk / totalStudents).toFixed(2);
            document.getElementById('avg-ind-kelas').innerText = (sumInd / totalStudents).toFixed(2);

            // Render Grafik Batang Persentase Kustom Matematika
            renderChartManual('distribusi-mtk-chart', mtkDist, totalStudents, 'bar-baik', 'bar-memadai', 'bar-kurang');
            // Render Grafik Batang Persentase Kustom Bahasa Indonesia
            renderChartManual('distribusi-ind-chart', indDist, totalStudents, 'bar-baik', 'bar-memadai', 'bar-kurang');
        }

        function renderChartManual(elementId, distObj, total, clsBaik, clsMemadai, clsKurang) {
            const container = document.getElementById(elementId);
            
            const pBaik = ((distObj.Baik / total) * 100).toFixed(1);
            const pMemadai = ((distObj.Memadai / total) * 100).toFixed(1);
            const pKurang = ((distObj.Kurang / total) * 100).toFixed(1);

            container.innerHTML = `
                <div class="chart-row">
                    <div class="chart-label-container">
                        <span>Baik (${distObj.Baik} Siswa)</span>
                        <span>${pBaik}%</span>
                    </div>
                    <div class="bar-container">
                        <div class="bar-fill ${clsBaik}" style="width: ${pBaik}%"></div>
                    </div>
                </div>
                <div class="chart-row">
                    <div class="chart-label-container">
                        <span>Memadai (${distObj.Memadai} Siswa)</span>
                        <span>${pMemadai}%</span>
                    </div>
                    <div class="bar-container">
                        <div class="bar-fill ${clsMemadai}" style="width: ${pMemadai}%"></div>
                    </div>
                </div>
                <div class="chart-row">
                    <div class="chart-label-container">
                        <span>Kurang (${distObj.Kurang} Siswa)</span>
                        <span>${pKurang}%</span>
                    </div>
                    <div class="bar-container">
                        <div class="bar-fill ${clsKurang}" style="width: ${pKurang}%"></div>
                    </div>
                </div>
            `;
        }

        // 3. KONTEN LAMAN 2: SISTEM SEARCHING & SURPRISE LOGIC ENGINE
        function prosesBukaAmplop() {
            const inputField = document.getElementById('input-search-nisn');
            const targetEnvelope = document.getElementById('envelope-target');
            const errorBox = document.getElementById('search-error');
            const loadingBox = document.getElementById('search-loading');

            // Reset View State
            targetEnvelope.style.display = 'none';
            errorBox.style.display = 'none';

            const queryNisn = inputField.value.trim();

            if (queryNisn === "") {
                errorBox.style.display = 'flex';
                errorBox.innerHTML = '<i class="fa-solid fa-triangle-exclamation"></i> Harap masukkan nomor NISN Anda terlebih dahulu.';
                return;
            }

            // Real-time Filtering logic menggunakan .filter() dan pencocokan string .includes()
            const resultMatch = processedData.filter(student => 
                student.nisn.toUpperCase().includes(queryNisn.toUpperCase())
            );

            if (resultMatch.length === 0) {
                errorBox.style.display = 'flex';
                errorBox.innerHTML = '<i class="fa-solid fa-triangle-exclamation"></i> Maaf, NISN tidak ditemukan. Periksa kembali angka yang dimasukkan.';
                return;
            }

            // Aktifkan Efek Loading Dramatis (Kunci Waktu: 1200ms)
            loadingBox.style.display = 'flex';

            setTimeout(() => {
                loadingBox.style.display = 'none';
                
                // Ambil data kecocokan pertama
                const student = resultMatch[0];
                renderKartuHasilIndividu(student);
                
                // Munculkan amplop dengan Bounce Surprise Effect
                targetEnvelope.style.display = 'block';
            }, 1200);
        }

        function renderKartuHasilIndividu(student) {
            const targetContainer = document.getElementById('envelope-target');
            
            let cardThemeClass = "card-rank-general";
            let badgeThemeClass = "badge-rank-general";
            let badgeIcon = `<i class="fa-solid fa-hashtag"></i> Rank`;

            // Penentuan Desain Gradasi Spesifik Sesuai Juara Kelas
            if (student.rank === 1) {
                cardThemeClass = "card-rank-1";
                badgeThemeClass = "badge-rank-1";
                badgeIcon = `<i class="fa-solid fa-trophy"></i> Juara Kelas 1`;
            } else if (student.rank === 2) {
                cardThemeClass = "card-rank-2";
                badgeThemeClass = "badge-rank-2";
                badgeIcon = `<i class="fa-solid fa-medal"></i> Juara Kelas 2`;
            } else if (student.rank === 3) {
                cardThemeClass = "card-rank-3";
                badgeThemeClass = "badge-rank-3";
                badgeIcon = `<i class="fa-solid fa-award"></i> Juara Kelas 3`;
            }

            // Pemetaan Class Warna Tag Predikat Mapel
            const getTagClass = (pred) => {
                if(pred === 'Baik') return 'tag-baik';
                if(pred === 'Memadai') return 'tag-memadai';
                return 'tag-kurang';
            };

            targetContainer.innerHTML = `
                <div class="result-card ${cardThemeClass}">
                    
                    <div class="card-header">
                        <div class="student-bio">
                            <h2>${student.nama.toUpperCase()}</h2>
                            <p>NISN: ${student.nisn}</p>
                        </div>
                        <div class="badge-rank ${badgeThemeClass}">
                            ${badgeIcon} ${student.rank}
                        </div>
                    </div>

                    <div class="scores-vertical-stack">
                        
                        <div class="score-row-box">
                            <div class="score-left-info">
                                <span class="subject-name">Matematika</span>
                                <span class="score-tag-predikat ${getTagClass(student.mtk_pred)}">${student.mtk_pred}</span>
                            </div>
                            <div class="score-right-value">${student.mtk.toFixed(2)}</div>
                        </div>

                        <div class="score-row-box">
                            <div class="score-left-info">
                                <span class="subject-name">Bahasa Indonesia</span>
                                <span class="score-tag-predikat ${getTagClass(student.ind_pred)}">${student.ind_pred}</span>
                            </div>
                            <div class="score-right-value">${student.ind.toFixed(2)}</div>
                        </div>

                    </div>

                    <div class="card-footer-average">
                        <span>Rata-Rata Kombinasi</span>
                        <span class="final-avg-val">${student.avg.toFixed(2)}</span>
                    </div>

                </div>
            `;
        }

        // 4. ROUTING NAVIGASI LAMAN STATE MANAGEMENT
        function pindahLaman(namaLaman) {
            // Hilangkan status aktif di semua halaman & tombol nav
            document.querySelectorAll('.app-page').forEach(page => page.classList.remove('active'));
            document.querySelectorAll('.nav-item').forEach(btn => btn.classList.remove('active'));

            // Aktifkan target halaman dan tombol nav pilihan
            if (namaLaman === 'home') {
                document.getElementById('page-home').classList.add('active');
                document.getElementById('nav-home').classList.add('active');
            } else if (namaLaman === 'nilaiku') {
                document.getElementById('page-nilaiku').classList.add('active');
                document.getElementById('nav-nilaiku').classList.add('active');
            }
        }

        // Jalankan Inisialisasi Engine Saat Dokumen Siap
        window.onload = initAppEngine;
    </script>
</body>
</html>
