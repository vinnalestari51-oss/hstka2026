<!DOCTYPE html>
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
            color: #64748
