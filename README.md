<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Daftar Kolektif Hasil Tes Kemampuan Akademik 2026</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        :root {
            --primary: #1e3a8a;
            --primary-light: #3b82f6;
            --success: #10b981;
            --warning: #f59e0b;
            --danger: #ef4444;
            --background: #f8fafc;
            --text-main: #1e293b;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Inter', sans-serif;
        }

        body {
            background-color: var(--background);
            color: var(--text-main);
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            padding: 20px;
        }

        .app-container {
            width: 100%;
            max-width: 500px;
            background: #ffffff;
            border-radius: 24px;
            box-shadow: 0 10px 25px rgba(30, 58, 138, 0.08);
            overflow: hidden;
            display: flex;
            flex-direction: column;
            min-height: 600px;
        }

        /* Header Aplikasi */
        .app-header {
            background: linear-gradient(135deg, var(--primary), #0f172a);
            color: #ffffff;
            padding: 24px;
            text-align: center;
        }
        .app-header h1 {
            font-size: 1.1rem;
            font-weight: 600;
            letter-spacing: 0.5px;
            line-height: 1.4;
        }
        .app-header p {
            font-size: 0.8rem;
            opacity: 0.8;
            margin-top: 4px;
        }

        /* Konten Utama */
        .app-content {
            flex: 1;
            padding: 24px;
            position: relative;
        }

        .app-page {
            display: none;
        }
        .app-page.active {
            display: block;
        }

        /* Glassmorphism Box */
        .m3-glass {
            background: #f1f5f9;
            border-radius: 16px;
            padding: 20px;
            border: 1px solid #e2e8f0;
        }

        .search-title {
            font-size: 0.95rem;
            font-weight: 600;
            margin-bottom: 12px;
            color: var(--primary);
        }

        /* Input Wrapper */
        .input-wrapper {
            position: relative;
            display: flex;
            align-items: center;
            background: #ffffff;
            border: 2px solid #cbd5e1;
            border-radius: 12px;
            padding: 0 14px;
            transition: all 0.3s ease;
        }
        .input-wrapper:focus-within {
            border-color: var(--primary-light);
            box-shadow: 0 0 0 4px rgba(59, 130, 246, 0.15);
        }
        .input-wrapper i {
            color: #94a3b8;
            margin-right: 10px;
            font-size: 1.1rem;
        }
        .input-nisn {
            width: 100%;
            border: none;
            outline: none;
            padding: 14px 0;
            font-size: 1rem;
            font-weight: 500;
            color: var(--text-main);
        }
        /* Menghilangkan panah spinner input number */
        .input-nisn::-webkit-outer-spin-button,
        .input-nisn::-webkit-inner-spin-button {
            -webkit-appearance: none;
            margin: 0;
        }

        /* Tombol Utama */
        .btn-search {
            width: 100%;
            background: var(--primary-light);
            color: #ffffff;
            border: none;
            border-radius: 12px;
            padding: 14px;
            font-size: 0.95rem;
            font-weight: 600;
            margin-top: 14px;
            cursor: pointer;
            transition: background 0.2s ease;
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 8px;
        }
        .btn-search:hover {
            background: #2563eb;
        }

        /* Error Message */
        .error-message {
            display: none;
            background: #fef2f2;
            border: 1px solid #fca5a5;
            color: var(--danger);
            border-radius: 12px;
            padding: 12px;
            margin-top: 16px;
            font-size: 0.85rem;
            font-weight: 500;
            gap: 8px;
            align-items: center;
        }

        /* Loading Spinner */
        .loading-container {
            display: none;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            padding: 30px 0;
            gap: 12px;
        }
        .spinner {
            width: 36px;
            height: 36px;
            border: 4px solid #e2e8f0;
            border-top-color: var(--primary-light);
            border-radius: 50%;
            animation: spin 0.8s linear infinite;
        }
        .pulse-text {
            font-size: 0.85rem;
            color: #64748b;
            font-weight: 500;
        }

        /* Kartu Nilai Hasil Akhir */
        .result-envelope {
            display: none;
            margin-top: 20px;
            animation: slideUp 0.4s ease-out;
        }
        .student-card {
            background: #ffffff;
            border: 2px solid #e2e8f0;
            border-radius: 16px;
            padding: 20px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.02);
        }
        .student-name {
            font-size: 1.1rem;
            font-weight: 700;
            color: var(--primary);
            text-transform: uppercase;
            margin-bottom: 4px;
        }
        .student-meta {
            font-size: 0.8rem;
            color: #64748b;
            margin-bottom: 16px;
            border-bottom: 1px dashed #e2e8f0;
            padding-bottom: 12px;
        }
        .score-row {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 10px;
            background: #f8fafc;
            padding: 10px 14px;
            border-radius: 8px;
        }
        .score-label {
            font-size: 0.9rem;
            font-weight: 500;
        }
        .score-value {
            font-size: 0.95rem;
            font-weight: 700;
            display: flex;
            align-items: center;
            gap: 6px;
        }
        .badge {
            font-size: 0.75rem;
            padding: 2px 8px;
            border-radius: 6px;
            font-weight: 600;
        }
        .badge.baik { background: #d1fae5; color: #065f46; }
        .badge.memadai { background: #e0f2fe; color: #0369a1; }
        .badge.kurang { background: #fee2e2; color: #991b1b; }

        /* Bottom Navigation Bar */
        .bottom-nav {
            display: flex;
            border-top: 1px solid #e2e8f0;
            background: #ffffff;
        }
        .nav-item {
            flex: 1;
            text-align: center;
            padding: 14px 0;
            color: #94a3b8;
            cursor: pointer;
            font-size: 0.75rem;
            font-weight: 500;
            transition: all 0.2s;
        }
        .nav-item i {
            font-size: 1.2rem;
            display: block;
            margin-bottom: 4px;
        }
        .nav-item.active {
            color: var(--primary-light);
        }

        /* Animations */
        @keyframes spin { to { transform: rotate(360deg); } }
        @keyframes slideUp {
            from { opacity: 0; transform: translateY(15px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body>

<div class="app-container">
    
    <div class="app-header">
        <h1 id="school-title">SMP NEGERI 1 LINGGA</h1>
        <p id="school-subtitle">Kolektif Hasil Tes Kemampuan Akademik 2026</p>
    </div>

    <div class="app-content">

        <div id="page-home" class="app-page">
            <div class="m3-glass" style="text-align: center; padding: 40px 20px;">
                <i class="fa-solid fa-graduation-cap" style="font-size: 3.5rem; color: var(--primary-light); margin-bottom: 16px;"></i>
                <h2 style="font-size: 1.2rem; margin-bottom: 8px;">Selamat Datang di Portal Nilai</h2>
                <p style="font-size: 0.85rem; color: #64748b; line-height: 1.5; margin-bottom: 20px;">
                    Gunakan aplikasi ini untuk memeriksa dokumen hasil Tes Kemampuan Akademik pribadi Anda secara aman.
                </p>
                <button class="btn-search" onclick="pindahLaman('nilaiku')">
                    Mulai Cari Nilai <i class="fa-solid fa-arrow-right"></i>
                </button>
            </div>
        </div>

        <div id="page-nilaiku" class="app-page active">
            
            <div class="m3-glass search-box">
                <div class="search-title">Cari Amplop Nilai Pribadi</div>
                
                <div class="input-wrapper">
                    <i class="fa-solid fa-id-card-clip"></i>
                    <input type="number" id="input-search-nisn" class="input-nisn" placeholder="Masukkan 10 digit NISN Anda..." pattern="[0-9]*" inputmode="numeric" oninput="if(this.value.length > 10) this.value = this.value.slice(0, 10);">
                </div>

                <button class="btn-search" onclick="prosesBukaAmplop()">
                    <i class="fa-solid fa-envelope-open-text"></i> Buka Amplop Nilai
                </button>
            </div>

            <div id="search-error" class="error-message"></div>

            <div id="search-loading" class="loading-container">
                <div class="spinner"></div>
                <div class="pulse-text">Memvalidasi NISN & Membuka Kunci Dokumen...</div>
            </div>

            <div id="envelope-target" class="result-envelope"></div>

        </div>

    </div>

    <div class="bottom-nav">
        <div id="nav-home" class="nav-item" onclick="pindahLaman('home')">
            <i class="fa-solid fa-house"></i>
            Home
        </div>
        <div id="nav-nilaiku" class="nav-item active" onclick="pindahLaman('nilaiku')">
            <i class="fa-solid fa-address-card"></i>
            Nilai Ku
        </div>
    </div>

</div>

<script>
// DATA REKAP RESMI DARI DOKUMEN HASIL TES AKADEMIK 2026
const RAW_STUDENT_DATA = [
    { num: 1, nisn: "0113067688", name: "Riska Sari", m_score: "20.00", m_label: "Kurang", b_score: "60.00", b_label: "Memadai" },
    { num: 2, nisn: "0113559822", name: "MECA ADELYA CAHYANI", m_score: "50.00", m_label: "Memadai", b_score: "90.00", b_label: "Baik" },
    { num: 3, nisn: "0115427698", name: "Dzikri Harith Haziq", m_score: "50.00", m_label: "Memadai", b_score: "70.00", b_label: "Memadai" },
    { num: 4, nisn: "0123776337", name: "VANDERSAR MEICHAEL NAINGGOLAN", m_score: "23.33", m_label: "Kurang", b_score: "86.67", b_label: "Baik" },
    { num: 5, nisn: "0114844674", name: "Syifa Syaqirah", m_score: "33.33", m_label: "Memadai", b_score: "63.33", b_label: "Memadai" },
    { num: 6, nisn: "0117775355", name: "QIAN FERDINAND", m_score: "36.67", m_label: "Memadai", b_score: "46.67", b_label: "Kurang" },
    { num: 7, nisn: "0116942061", name: "SYARIFAH NAJWA SAFIZ", m_score: "-", m_label: "Tidak Ada Data", b_score: "83.33", b_label: "Baik" },
    { num: 8, nisn: "0119458667", name: "SUHARAYAH", m_score: "26.67", m_label: "Kurang", b_score: "63.33", b_label: "Memadai" },
    { num: 9, nisn: "0111929206", name: "AIRIN DWI RAMADHANI", m_score: "40.00", m_label: "Memadai", b_score: "63.33", b_label: "Memadai" },
    { num: 10, nisn: "0094409765", name: "Imam Syahibbullah", m_score: "-", m_label: "Tidak Ada Data", b_score: "53.33", b_label: "Memadai" },
    { num: 11, nisn: "0119416095", name: "Deby Septiani", m_score: "43.33", m_label: "Memadai", b_score: "80.00", b_label: "Baik" },
    { num: 12, nisn: "0112474826", name: "Ibnu Shalim", m_score: "26.67", m_label: "Kurang", b_score: "43.33", b_label: "Kurang" },
    { num: 13, nisn: "0117387487", name: "LIPIANA SUCI RAMARANI", m_score: "50.00", m_label: "Memadai", b_score: "86.67", b_label: "Baik" },
    { num: 14, nisn: "0111805260", name: "irvan kurnia", m_score: "16.67", m_label: "Kurang", b_score: "43.33", b_label: "Kurang" },
    { num: 15, nisn: "0086621206", name: "Arya Imam Risnanda", m_score: "43.33", m_label: "Memadai", b_score: "80.00", b_label: "Baik" },
    { num: 16, nisn: "0118621492", name: "Raisa Idadi", m_score: "30.00", m_label: "Kurang", b_score: "66.67", m_label: "Memadai" },
    { num: 17, nisn: "0116566978", name: "Kafha Azri Ilhamsyah", m_score: "43.33", m_label: "Memadai", b_score: "73.33", b_label: "Memadai" },
    { num: 18, nisn: "0114962861", name: "Muhammad Erwan Zarka", m_score: "36.67", m_label: "Memadai", b_score: "63.33", b_label: "Memadai" },
    { num: 19, nisn: "0105152266", name: "Adonia Najla Raissa", m_score: "40.00", m_label: "Memadai", b_score: "66.67", b_label: "Memadai" },
    { num: 20, nisn: "0099948557", name: "KHASBI NOVALDI", m_score: "36.67", m_label: "Memadai", b_score: "56.67", b_label: "Memadai" },
    { num: 21, nisn: "0107778998", name: "Sabrina Embun Pertiwi", m_score: "40.00", m_label: "Memadai", b_score: "60.00", b_label: "Memadai" },
    { num: 22, nisn: "0116938426", name: "Syarifah Zilfa Natasya", m_score: "43.33", m_label: "Memadai", b_score: "80.00", b_label: "Baik" },
    { num: 23, nisn: "0119879134", name: "SHAZIA ZARA ALISHA", m_score: "46.67", m_label: "Memadai", b_score: "60.00", b_label: "Memadai" },
    { num: 24, nisn: "0117587242", name: "sapinah", m_score: "26.67", m_label: "Kurang", b_score: "46.67", b_label: "Kurang" },
    { num: 25, nisn: "0115247372", name: "Meisya Awalun Nurhasanah", m_score: "26.67", m_label: "Kurang", b_score: "53.33", b_label: "Memadai" },
    { num: 26, nisn: "0113332240", name: "NUR RAFNI YASMADI", m_score: "33.33", m_label: "Memadai", b_score: "50.00", b_label: "Memadai" },
    { num: 27, nisn: "0114298991", name: "ZAI ISRAKMIDIAH", m_score: "36.67", m_label: "Memadai", b_score: "66.67", b_label: "Memadai" },
    { num: 28, nisn: "0112792471", name: "AISH GHAZIYA RAFIFA", m_score: "50.00", m_label: "Memadai", b_score: "63.33", b_label: "Memadai" },
    { num: 29, nisn: "0105796473", name: "GUNAWAN FAUZI", m_score: "33.33", m_label: "Memadai", b_score: "43.33", b_label: "Kurang" },
    { num: 30, nisn: "0112376775", name: "ISNAINI", m_score: "36.67", m_label: "Memadai", b_score: "36.67", b_label: "Kurang" },
    { num: 31, nisn: "0101111863", name: "Ananda Ibnu Fahrezi", m_score: "33.33", m_label: "Memadai", b_score: "76.67", b_label: "Baik" },
    { num: 32, nisn: "0111647237", name: "Faqiha Tazkiatun Nufus", m_score: "36.67", m_label: "Memadai", b_score: "70.00", b_label: "Memadai" },
    { num: 33, nisn: "0113654663", name: "MUHAMMAD MUFLIH HIBATULLAH NURVAL", m_score: "50.00", m_label: "Memadai", b_score: "46.67", b_label: "Kurang" },
    { num: 34, nisn: "0113688046", name: "rati junila", m_score: "33.33", m_label: "Memadai", b_score: "70.00", b_label: "Memadai" },
    { num: 35, nisn: "0112757766", name: "ZALFA MUFIDAH INAYAH", m_score: "50.00", m_label: "Memadai", b_score: "70.00", b_label: "Memadai" },
    { num: 36, nisn: "0117042213", name: "Dyra Altha Funisya", m_score: "53.33", m_label: "Memadai", b_score: "76.67", b_label: "Baik" },
    { num: 37, nisn: "0114103715", name: "RAFADIL ANΑΝΤΑ", m_score: "46.67", m_label: "Memadai", b_score: "73.33", b_label: "Memadai" },
    { num: 38, nisn: "0112333526", name: "RINA RIYANTI", m_score: "46.67", m_label: "Memadai", b_score: "53.33", b_label: "Memadai" },
    { num: 39, nisn: "0107287635", name: "NATASYA ZULHAFIFAH", m_score: "16.67", m_label: "Kurang", b_score: "66.67", b_label: "Memadai" },
    { num: 40, nisn: "0114766625", name: "Sheril Gianda Utami", m_score: "30.00", m_label: "Kurang", b_score: "43.33", b_label: "Kurang" },
    { num: 41, nisn: "0113394958", name: "SYARIFAH NAFIA SAFIZ", m_score: "50.00", m_label: "Memadai", b_score: "80.00", b_label: "Baik" },
    { num: 42, nisn: "0113962310", name: "RISNA ULKA ARYANI", m_score: "33.33", m_label: "Memadai", b_score: "60.00", b_label: "Memadai" },
    { num: 43, nisn: "0101800405", name: "REFAN PINANDO", m_score: "56.67", m_label: "Baik", b_score: "40.00", b_label: "Kurang" },
    { num: 44, nisn: "0106977903", name: "VIKY ADITYA SYAPUTRA", m_score: "46.67", m_label: "Memadai", b_score: "40.00", b_label: "Kurang" },
    { num: 45, nisn: "0112026378", name: "SILA ADELIA", m_score: "33.33", m_label: "Memadai", b_score: "63.33", b_label: "Memadai" },
    { num: 46, nisn: "0114122561", name: "Liyana Zahira", m_score: "23.33", m_label: "Kurang", b_score: "60.00", b_label: "Memadai" },
    { num: 47, nisn: "0115557747", name: "adelia dwi nurmansyah", m_score: "43.33", m_label: "Memadai", b_score: "80.00", b_label: "Baik" },
    { num: 48, nisn: "0112426972", name: "JEANTRIKA SAPUTERA", m_score: "50.00", m_label: "Memadai", b_score: "46.67", b_label: "Kurang" },
    { num: 49, nisn: "0097680988", name: "Delvry Anggara Panjaitan", m_score: "53.33", m_label: "Memadai", b_score: "70.00", m_label: "Memadai" },
    { num: 50, nisn: "0115755742", name: "Zatia Maysya", m_score: "53.33", m_label: "Memadai", b_score: "83.33", b_label: "Baik" },
    { num: 51, nisn: "0113402279", name: "RIZKA INDRI ADELIASA", m_score: "43.33", m_label: "Memadai", b_score: "53.33", b_label: "Memadai" },
    { num: 52, nisn: "0118789434", name: "RAJA FATHUR ABDILLAH", m_score: "60.00", m_label: "Baik", b_score: "73.33", b_label: "Memadai" },
    { num: 53, nisn: "0118177962", name: "MARWA DWI RAMADANI", m_score: "53.33", m_label: "Memadai", b_score: "86.67", b_label: "Baik" },
    { num: 54, nisn: "0112631039", name: "Dafitra Ariansyah", m_score: "46.67", m_label: "Memadai", b_score: "60.00", b_label: "Memadai" },
    { num: 55, nisn: "0102053051", name: "Muhammad Gibran Assyafari", m_score: "50.00", m_label: "Memadai", b_score: "66.67", b_label: "Memadai" },
    { num: 56, nisn: "0109121124", name: "Ghastan Gautama Ginarda", m_score: "60.00", m_label: "Baik", b_score: "86.67", b_label: "Baik" },
    { num: 57, nisn: "0118552573", name: "Muhammad Fadhil Ardiansyah", m_score: "40.00", m_label: "Memadai", b_score: "66.67", b_label: "Memadai" },
    { num: 58, nisn: "0116317492", name: "SUKMASARI", m_score: "33.33", m_label: "Memadai", b_score: "60.00", b_label: "Memadai" },
    { num: 59, nisn: "0105395625", name: "ZIFARA OKTIA GISKA", m_score: "56.67", m_label: "Baik", b_score: "66.67", b_label: "Memadai" },
    { num: 60, nisn: "0128826786", name: "M.BAYU RIZKITULLAH", m_score: "63.33", m_label: "Baik", b_score: "53.33", b_label: "Memadai" },
    { num: 61, nisn: "0102542618", name: "Herisusanti", m_score: "53.33", m_label: "Memadai", b_score: "86.67", b_label: "Baik" },
    { num: 62, nisn: "0118960096", name: "Dzakiyya Naila Sakhi", m_score: "50.00", m_label: "Memadai", b_score: "80.00", b_label: "Baik" },
    { num: 63, nisn: "0117249653", name: "Suci Safira Putri", m_score: "53.33", m_label: "Memadai", b_score: "70.00", b_label: "Memadai" },
    { num: 64, nisn: "0115867734", name: "RIZKA ALFIA AZ ZAHRA", m_score: "56.67", m_label: "Baik", b_score: "80.00", b_label: "Baik" },
    { num: 65, nisn: "0119453195", name: "NAZILA MAHARANI", m_score: "30.00", m_label: "Kurang", b_score: "83.33", b_label: "Baik" },
    { num: 66, nisn: "0118730407", name: "Mulhuda", m_score: "46.67", m_label: "Memadai", b_score: "66.67", b_label: "Memadai" },
    { num: 67, nisn: "0119247555", name: "HANY BAZLINDA", m_score: "56.67", m_label: "Baik", b_score: "83.33", b_label: "Baik" },
    { num: 68, nisn: "0105795746", name: "Sahrini Ramadani", m_score: "43.33", m_label: "Memadai", b_score: "26.67", b_label: "Kurang" },
    { num: 69, nisn: "0114699199", name: "RISKY ARDIAN MISKA SACHPUTRA", m_score: "40.00", m_label: "Memadai", b_score: "53.33", m_label: "Memadai" },
    { num: 70, nisn: "0106306052", name: "NI'A ROSA", m_score: "46.67", m_label: "Memadai", b_score: "63.33", b_label: "Memadai" },
    { num: 71, nisn: "0114478647", name: "ACHAI ANDREAS", m_score: "46.67", m_label: "Memadai", b_score: "63.33", b_label: "Memadai" },
    { num: 72, nisn: "0111751808", name: "SYARIFAH IZZATI AQILA", m_score: "40.00", m_label: "Memadai", b_score: "76.67", b_label: "Baik" },
    { num: 73, nisn: "0119149285", name: "ANUGRAH AGUSTI RAMADHANI", m_score: "56.67", m_label: "Baik", b_score: "80.00", b_label: "Baik" },
    { num: 74, nisn: "0091754679", name: "HESTY YOLANDA SIRABANG", m_score: "46.67", m_label: "Memadai", b_score: "76.67", b_label: "Baik" },
    { num: 75, nisn: "0111226881", name: "usman", m_score: "43.33", m_label: "Memadai", b_score: "60.00", b_label: "Memadai" },
    { num: 76, nisn: "0106504994", name: "ZURRIATI FARHANA", m_score: "26.67", m_label: "Kurang", b_score: "76.67", b_label: "Baik" },
    { num: 77, nisn: "0116283543", name: "Erina Nazira", m_score: "43.33", m_label: "Memadai", b_score: "63.33", b_label: "Memadai" },
    { num: 78, nisn: "0102191383", name: "WINDA AULIA", m_score: "30.00", m_label: "Kurang", b_score: "46.67", b_label: "Kurang" },
    { num: 79, nisn: "0113021378", name: "ARFA", m_score: "43.33", m_label: "Memadai", b_score: "63.33", b_label: "Memadai" },
    { num: 80, nisn: "0103349505", name: "Novita Adha Riah", m_score: "46.67", m_label: "Memadai", b_score: "53.33", b_label: "Memadai" },
    { num: 81, nisn: "0093969948", name: "NOVRIAN SAPUTRA", m_score: "40.00", m_label: "Memadai", b_score: "36.67", b_label: "Kurang" },
    { num: 82, nisn: "0119656574", name: "SILVIA FRANSISKA NATALIA", m_score: "43.33", m_label: "Memadai", b_score: "73.33", b_label: "Memadai" },
    { num: 83, nisn: "0107212771", name: "ANGGARA PRATAMA", m_score: "33.33", m_label: "Memadai", b_score: "33.33", b_label: "Kurang" },
    { num: 84, nisn: "0119389544", name: "Nazriel Alfarizqy Yuniar", m_score: "46.67", m_label: "Memadai", b_score: "76.67", b_label: "Baik" },
    { num: 85, nisn: "0102286678", name: "Faiz Fayzul Haq", m_score: "46.67", m_label: "Memadai", b_score: "83.33", b_label: "Baik" },
    { num: 86, nisn: "0115970688", name: "Rahmanda Pratama", m_score: "26.67", m_label: "Kurang", b_score: "46.67", b_label: "Kurang" },
    { num: 87, nisn: "0118701232", name: "megawati", m_score: "56.67", m_label: "Baik", b_score: "76.67", b_label: "Baik" },
    { num: 88, nisn: "0108287271", name: "MAHARANI DEWI", m_score: "53.33", m_label: "Memadai", b_score: "60.00", b_label: "Memadai" }
];

// FUNGSI NAVIGASI PINDAH HALAMAN TAB
function pindahLaman(pageId) {
    // Sembunyikan semua halaman & reset nav class
    document.querySelectorAll('.app-page').forEach(p => p.classList.remove('active'));
    document.querySelectorAll('.nav-item').forEach(n => n.classList.remove('active'));
    
    // Aktifkan target halaman & nav yang dipilih
    document.getElementById(`page-${pageId}`).classList.add('active');
    document.getElementById(`nav-${pageId}`).classList.add('active');
}

// FUNGSI TOMBOL CHECK UTAMA (Sistem Steril Tanpa Live Auto-Filter)
function prosesBukaAmplop() {
    const inputField = document.getElementById('input-search-nisn');
    const targetEnvelope = document.getElementById('envelope-target');
    const errorBox = document.getElementById('search-error');
    const loadingBox = document.getElementById('search-loading');

    // Reset view state awal agar bersih
    targetEnvelope.style.display = 'none';
    errorBox.style.display = 'none';
    errorBox.innerHTML = '';

    const queryNisn = inputField.value.trim();

    // 1. Validasi Keamanan: Kolom Input Masih Kosong
    if (queryNisn === "") {
        errorBox.style.display = 'flex';
        errorBox.innerHTML = '<i class="fa-solid fa-triangle-exclamation"></i> Harap masukkan nomor NISN Anda terlebih dahulu.';
        return;
    }

    // 2. Validasi Keamanan: Wajib Mengetik Lengkap Pas 10 Digit
    if (queryNisn.length !== 10) {
        errorBox.style.display = 'flex';
        errorBox.innerHTML = '<i class="fa-solid fa-circle-info"></i> Keamanan Ketat: Masukkan NISN secara lengkap (10 digit angka) untuk membuka dokumen.';
        return;
    }

    // 3. Pencocokan Sempurna (Strict Match "===" membuang kesamaan sebagian teks)
    const resultMatch = RAW_STUDENT_DATA.filter(student => student.nisn === queryNisn);

    // 4. Validasi Keamanan: NISN Salah / Tidak Ada di Database
    if (resultMatch.length === 0) {
        errorBox.style.display = 'flex';
        errorBox.innerHTML = '<i class="fa-solid fa-triangle-exclamation"></i> Maaf, nomor NISN tidak ditemukan dalam database sekolah. Periksa kembali.';
        return;
    }

    // 5. Sukses Validasi: Jalankan Simulasi Enkripsi Loading
    loadingBox.style.display = 'flex';

    setTimeout(() => {
        loadingBox.style.display = 'none';
        
        // Mengunci hasil ke satu-satunya index data yang cocok
        const student = resultMatch[0];
        
        // Buat konten kartu
        renderKartuHasilIndividu(student);
        
        // Tampilkan wadah dokumen amplop ke layar secara eksklusif
        targetEnvelope.style.display = 'block';
    }, 1200);
}

// FUNGSI UNTUK GENERATE KARTU NILAI SISWA
function renderKartuHasilIndividu(data) {
    const targetEnvelope = document.getElementById('envelope-target');
    
    // Penentuan class badge warna berdasarkan label nilai kompetensi
    const mBadgeClass = data.m_label.toLowerCase();
    const bBadgeClass = data.b_label.toLowerCase();

    targetEnvelope.innerHTML = `
        <div class="student-card">
            <div class="student-name">${data.name}</div>
            <div class="student-meta">NISN: ${data.nisn} &bull; Urut Absen: ${data.num}</div>
            
            <div class="score-row">
                <span class="score-label">Matematika</span>
                <span class="score-value">
                    ${data.m_score} 
                    <span class="badge ${mBadgeClass}">${data.m_label}</span>
                </span>
            </div>
            
            <div class="score-row">
                <span class="score-label">Bahasa Indonesia</span>
                <span class="score-value">
                    ${data.b_score} 
                    <span class="badge ${bBadgeClass}">${data.b_label}</span>
                </span>
            </div>
        </div>
    `;
}
</script>

</body>
</html>
