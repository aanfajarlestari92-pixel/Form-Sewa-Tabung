<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Form Perjanjian Sewa Tabung Oksigen</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #00b4db 0%, #0083b0 100%);
            padding: 20px;
            line-height: 1.6;
            min-height: 100vh;
        }
        
        .container {
            max-width: 900px;
            margin: 0 auto;
            background: white;
            padding: 0;
            border-radius: 15px;
            box-shadow: 0 15px 50px rgba(0,0,0,0.3);
            overflow: hidden;
        }
        
        .hero-section {
            background: linear-gradient(135deg, #00b4db 0%, #0083b0 100%);
            padding: 40px;
            text-align: center;
            color: white;
            position: relative;
            overflow: hidden;
        }
        
        .hero-section::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -10%;
            width: 300px;
            height: 300px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
        }
        
        .hero-section::after {
            content: '';
            position: absolute;
            bottom: -50%;
            left: -10%;
            width: 250px;
            height: 250px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
        }
        
        .oxygen-tank-image {
            width: 200px;
            height: auto;
            margin: 20px auto;
            filter: drop-shadow(0 10px 25px rgba(0,0,0,0.4));
            position: relative;
            z-index: 1;
            display: block;
        }
        
        .hero-section h1 {
            font-size: 2.5em;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.2);
            position: relative;
            z-index: 1;
        }
        
        .hero-section p {
            font-size: 1.2em;
            margin-bottom: 20px;
            position: relative;
            z-index: 1;
        }
        
        .location-badge {
            display: inline-block;
            background: rgba(255, 255, 255, 0.2);
            backdrop-filter: blur(10px);
            padding: 15px 25px;
            border-radius: 50px;
            margin-top: 15px;
            border: 2px solid rgba(255, 255, 255, 0.3);
            position: relative;
            z-index: 1;
        }
        
        .location-badge strong {
            display: block;
            font-size: 0.9em;
            margin-bottom: 5px;
            text-transform: uppercase;
            letter-spacing: 1px;
        }
        
        .form-content {
            padding: 40px;
        }
        
        .header {
            text-align: center;
            padding-bottom: 20px;
            margin-bottom: 30px;
        }
        
        .header h1 {
            color: #0083b0;
            font-size: 2em;
            margin-bottom: 10px;
        }
        
        .header p {
            color: #666;
            font-size: 1.1em;
        }
        
        .section {
            margin-bottom: 30px;
        }
        
        .section h2 {
            color: #0083b0;
            font-size: 1.4em;
            margin-bottom: 15px;
            padding-bottom: 10px;
            border-bottom: 2px solid #e0e0e0;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        label {
            display: block;
            font-weight: 600;
            color: #333;
            margin-bottom: 8px;
        }
        
        input[type="text"],
        input[type="tel"],
        input[type="email"],
        input[type="date"],
        textarea,
        select {
            width: 100%;
            padding: 12px;
            border: 2px solid #e0e0e0;
            border-radius: 5px;
            font-size: 1em;
            transition: border-color 0.3s;
        }
        
        input:focus,
        textarea:focus,
        select:focus {
            outline: none;
            border-color: #00b4db;
            box-shadow: 0 0 0 3px rgba(0, 180, 219, 0.1);
        }
        
        .form-row {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
        }
        
        .terms-box {
            background: linear-gradient(135deg, #e3f2fd 0%, #bbdefb 100%);
            padding: 20px;
            border-radius: 8px;
            border-left: 4px solid #00b4db;
            max-height: 400px;
            overflow-y: auto;
            margin-bottom: 20px;
            font-size: 0.95em;
        }
        
        .terms-box h3 {
            color: #0083b0;
            margin-bottom: 10px;
        }
        
        .terms-box ul {
            margin-left: 20px;
            margin-bottom: 15px;
        }
        
        .terms-box li {
            margin-bottom: 8px;
        }
        
        .checkbox-group {
            display: flex;
            align-items: start;
            margin: 20px 0;
            padding: 15px;
            background: #fff3cd;
            border-radius: 5px;
            border: 2px solid #ffc107;
        }
        
        .checkbox-group input[type="checkbox"] {
            width: 20px;
            height: 20px;
            margin-right: 10px;
            margin-top: 2px;
            cursor: pointer;
        }
        
        .checkbox-group label {
            margin-bottom: 0;
            cursor: pointer;
            font-weight: 500;
        }
        
        .signature-section {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 30px;
            margin-top: 40px;
        }
        
        .signature-box {
            text-align: center;
        }
        
        .signature-pad {
            width: 100%;
            height: 200px;
            border: 2px solid #00b4db;
            border-radius: 8px;
            background: #fafafa;
            cursor: crosshair;
            touch-action: none;
        }
        
        .signature-label {
            font-weight: 600;
            color: #333;
            margin-bottom: 10px;
            display: block;
        }
        
        .signature-name {
            margin-top: 10px;
            padding: 10px;
            border-top: 2px solid #333;
            display: inline-block;
            min-width: 200px;
        }
        
        .button-group {
            display: flex;
            gap: 10px;
            justify-content: center;
            margin-top: 10px;
        }
        
        button {
            padding: 12px 30px;
            border: none;
            border-radius: 5px;
            font-size: 1em;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
        }
        
        .btn-clear {
            background: #dc3545;
            color: white;
        }
        
        .btn-clear:hover {
            background: #c82333;
        }
        
        .btn-submit {
            background: linear-gradient(135deg, #00b4db 0%, #0083b0 100%);
            color: white;
            font-size: 1.1em;
            padding: 15px 50px;
            margin-top: 30px;
        }
        
        .btn-submit:hover {
            background: linear-gradient(135deg, #0083b0 0%, #006d94 100%);
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0, 180, 219, 0.4);
        }
        
        .btn-submit:disabled {
            background: #ccc;
            cursor: not-allowed;
            transform: none;
        }
        
        .btn-download {
            background: #28a745;
            color: white;
            display: none;
        }
        
        .btn-download:hover {
            background: #218838;
        }
        
        .btn-whatsapp {
            background: #25D366;
            color: white;
        }
        
        .btn-whatsapp:hover {
            background: #20BA5A;
        }
        
        .config-section {
            background: #fff3cd;
            border: 2px solid #ffc107;
            border-radius: 10px;
            padding: 20px;
            margin-bottom: 30px;
        }
        
        .config-section h3 {
            color: #856404;
            margin-bottom: 15px;
            font-size: 1.2em;
        }
        
        .config-info {
            background: white;
            padding: 15px;
            border-radius: 5px;
            margin-top: 10px;
            font-size: 0.9em;
            color: #666;
        }
        
        .alert {
            padding: 15px;
            border-radius: 5px;
            margin-bottom: 20px;
            display: none;
        }
        
        .alert-success {
            background: #d4edda;
            border: 1px solid #c3e6cb;
            color: #155724;
        }
        
        .alert-danger {
            background: #f8d7da;
            border: 1px solid #f5c6cb;
            color: #721c24;
        }
        
        @media print {
            body {
                background: white;
                padding: 0;
            }
            
            .container {
                box-shadow: none;
                padding: 20px;
            }
            
            button {
                display: none;
            }
            
            .signature-pad {
                border: 1px solid #000;
            }
        }
        
        @media (max-width: 768px) {
            .container {
                padding: 20px;
            }
            
            .form-row,
            .signature-section {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="hero-section">
            <img src="https://images.unsplash.com/photo-1584820927498-cfe5211fd8bf?w=400&h=400&fit=crop" 
                 alt="Tabung Oksigen 1M3" 
                 class="oxygen-tank-image"
                 onerror="this.src='https://cdn.pixabay.com/photo/2020/04/18/08/33/oxygen-5058184_1280.png'">
            
            <h1>🏥 PERJANJIAN SEWA TABUNG OKSIGEN</h1>
            <p>Tabung Oksigen Medis 1M³ - Siap Pakai</p>
            
            <div class="location-badge">
                <strong>📍 Lokasi Pengambilan</strong>
                <div style="font-size: 1.1em; margin-top: 5px;">
                    Karangturi RT 07, Baturetno<br>
                    Banguntapan, Bantul, Yogyakarta
                </div>
                <a href="https://maps.app.goo.gl/xYFTLhLqdjn4i35i7" 
                   target="_blank" 
                   style="display: inline-block; margin-top: 15px; padding: 10px 25px; background: white; color: #0083b0; text-decoration: none; border-radius: 25px; font-weight: 600; transition: all 0.3s; box-shadow: 0 4px 15px rgba(0,0,0,0.2);"
                   onmouseover="this.style.transform='translateY(-2px)'; this.style.boxShadow='0 6px 20px rgba(0,0,0,0.3)'"
                   onmouseout="this.style.transform='translateY(0)'; this.style.boxShadow='0 4px 15px rgba(0,0,0,0.2)'">
                    🗺️ Buka Google Maps
                </a>
            </div>
        </div>
        
        <div class="form-content">
        
        <div id="alertBox" class="alert"></div>
        
        <form id="rentalForm">
            <!-- Data Penyewa -->
            <div class="section">
                <h2>👤 Data Penyewa</h2>
                <div class="form-group">
                    <label for="nama">Nama Lengkap *</label>
                    <input type="text" id="nama" name="nama" required>
                </div>
                
                <div class="form-row">
                    <div class="form-group">
                        <label for="nik">NIK/No. Identitas *</label>
                        <input type="text" id="nik" name="nik" required>
                    </div>
                    <div class="form-group">
                        <label for="jenisId">Jenis Identitas *</label>
                        <select id="jenisId" name="jenisId" required>
                            <option value="">Pilih Jenis Identitas</option>
                            <option value="KTP">KTP</option>
                            <option value="SIM">SIM</option>
                            <option value="Paspor">Paspor</option>
                        </select>
                    </div>
                </div>
                
                <div class="form-group">
                    <label for="alamat">Alamat Lengkap *</label>
                    <textarea id="alamat" name="alamat" rows="3" required></textarea>
                </div>
                
                <div class="form-row">
                    <div class="form-group">
                        <label for="telepon">No. Telepon/WhatsApp *</label>
                        <input type="tel" id="telepon" name="telepon" required>
                    </div>
                    <div class="form-group">
                        <label for="email">Email</label>
                        <input type="email" id="email" name="email">
                    </div>
                </div>
            </div>
            
            <!-- Detail Sewa -->
            <div class="section">
                <h2>📦 Detail Sewa</h2>
                <div class="form-row">
                    <div class="form-group">
                        <label for="tanggalMulai">Tanggal Mulai Sewa *</label>
                        <input type="date" id="tanggalMulai" name="tanggalMulai" required>
                    </div>
                    <div class="form-group">
                        <label for="durasi">Durasi Sewa (Bulan) *</label>
                        <input type="text" id="durasi" name="durasi" value="1" required>
                    </div>
                </div>
                
                <div class="form-row">
                    <div class="form-group">
                        <label for="noTabung">No. Tabung Oksigen</label>
                        <input type="text" id="noTabung" name="noTabung" placeholder="Diisi oleh pemilik">
                    </div>
                    <div class="form-group">
                        <label for="biayaSewa">Biaya Sewa/Bulan *</label>
                        <input type="text" id="biayaSewa" name="biayaSewa" value="Rp 150.000" readonly>
                    </div>
                </div>
            </div>
            
            <!-- Syarat dan Ketentuan -->
            <div class="section">
                <h2>📜 Syarat dan Ketentuan</h2>
                <div class="terms-box">
                    <h3>Ketentuan Sewa:</h3>
                    <ul>
                        <li>Tarif sewa: <strong>Rp 150.000/bulan</strong></li>
                        <li>Pembayaran dilakukan di muka setiap awal periode sewa</li>
                        <li>Isi ulang oksigen menjadi tanggung jawab penyewa</li>
                        <li>Keterlambatan pembayaran > 7 hari dikenakan denda Rp 10.000/hari</li>
                    </ul>
                    
                    <h3>Jaminan:</h3>
                    <ul>
                        <li>Wajib menyerahkan <strong>1 (satu) identitas asli</strong></li>
                        <li>Identitas dikembalikan setelah tabung dikembalikan dalam kondisi baik</li>
                    </ul>
                    
                    <h3>Kewajiban Penyewa:</h3>
                    <ul>
                        <li>Menggunakan tabung sesuai fungsi dan petunjuk</li>
                        <li>Menjaga kondisi tabung tetap baik dan layak pakai</li>
                        <li>Tidak memindahtangankan ke pihak lain</li>
                        <li>Melaporkan segera jika terjadi kerusakan</li>
                    </ul>
                    
                    <h3>Biaya Kerusakan/Kehilangan:</h3>
                    <ul>
                        <li>Valve rusak: Rp 100.000</li>
                        <li>Regulator rusak: Rp 150.000</li>
                        <li>Tabung penyok/bocor: Rp 1.500.000</li>
                        <li>Tabung hilang: Rp 2.500.000</li>
                    </ul>
                    
                    <h3>Larangan:</h3>
                    <ul>
                        <li>Merokok atau menyalakan api di dekat tabung</li>
                        <li>Menyimpan di tempat suhu tinggi (>50°C)</li>
                        <li>Membongkar atau memodifikasi tabung</li>
                        <li>Memindahtangankan kepada pihak lain</li>
                    </ul>
                </div>
                
                <div class="checkbox-group">
                    <input type="checkbox" id="agree" name="agree" required>
                    <label for="agree">
                        Saya telah membaca, memahami, dan menyetujui seluruh syarat dan ketentuan di atas. 
                        Saya bersedia menyerahkan 1 (satu) identitas asli sebagai jaminan dan akan mengembalikan 
                        tabung dalam kondisi baik.
                    </label>
                </div>
            </div>
            
            <!-- Tanda Tangan -->
            <div class="section">
                <h2>✍️ Tanda Tangan Penyewa</h2>
                <p style="margin-bottom: 20px; color: #666;">
                    Silakan tanda tangan pada kotak di bawah menggunakan mouse atau sentuhan layar
                </p>
                
                <div style="max-width: 500px; margin: 0 auto;">
                    <div class="signature-box">
                        <span class="signature-label">Tanda Tangan Penyewa</span>
                        <canvas id="signaturePenyewa" class="signature-pad"></canvas>
                        <div class="button-group">
                            <button type="button" class="btn-clear" onclick="clearSignature('signaturePenyewa')">
                                🗑️ Hapus
                            </button>
                        </div>
                        <div class="signature-name" id="namaPenyewa">________________</div>
                        <div style="margin-top: 5px; font-size: 0.9em; color: #666;">
                            Tanggal: <span id="tanggalPenyewa"></span>
                        </div>
                    </div>
                </div>
                
                <div style="text-align: center; margin-top: 30px; padding: 20px; background: #f8f9fa; border-radius: 8px;">
                    <p style="color: #666; margin-bottom: 10px;">
                        Dengan menandatangani form ini, saya menyetujui semua syarat dan ketentuan yang berlaku.
                    </p>
                    <p style="color: #999; font-size: 0.9em;">
                        Data akan dikirim ke pemilik dan dapat dicetak sebagai dokumen resmi.
                    </p>
                </div>
            </div>
            
            <!-- Submit Button -->
            <div style="text-align: center;">
                <button type="submit" class="btn-submit" id="submitBtn">
                    📤 Kirim via WhatsApp
                </button>
                <button type="button" class="btn-download btn-submit" id="downloadBtn" onclick="downloadPDF()">
                    📥 Download PDF
                </button>
                <button type="button" class="btn-submit" onclick="window.print()" style="background: #6c757d; margin-left: 10px;">
                    🖨️ Print
                </button>
            </div>
        </form>
        
        <!-- Tips Penyimpanan Data -->
        <div class="section" style="margin-top: 40px; background: #e8f5e9; padding: 20px; border-radius: 10px; border-left: 4px solid #4caf50;">
            <h2>💡 Cara Mendapatkan File PDF yang Sudah Ditandatangani</h2>
            <div style="line-height: 2; color: #333;">
                <p><strong>Setelah penyewa mengisi dan mengirim form:</strong></p>
                <ol style="margin-left: 20px; margin-top: 15px;">
                    <li>✅ Penyewa akan mengirim data via WhatsApp ke nomor Anda</li>
                    <li>✅ Penyewa juga bisa <strong>klik "Download PDF"</strong> atau <strong>"Print"</strong> di form</li>
                    <li>✅ File PDF akan berisi semua data + tanda tangan penyewa</li>
                    <li>✅ Penyewa bisa kirim file PDF tersebut via WhatsApp/Email ke Anda</li>
                </ol>
                
                <div style="background: white; padding: 15px; border-radius: 5px; margin-top: 15px;">
                    <strong>💼 Rekomendasi Alur:</strong><br>
                    1. Penyewa isi form online → kirim via WA<br>
                    2. Penyewa download/print PDF → kirim file PDF ke Anda<br>
                    3. Anda simpan PDF sebagai arsip resmi<br>
                    4. Pesan WhatsApp sebagai backup data
                </div>
            </div>
        </div>
        <!-- Petunjuk Publish -->
        <div class="section" style="margin-top: 20px; background: #fff3e0; padding: 20px; border-radius: 10px; border-left: 4px solid #ff9800;">
            <h2>🚀 Cara Publish Form Ini (Gratis & Mudah)</h2>
            <div style="line-height: 2; color: #333;">
                
                <h3 style="color: #f57c00; margin-top: 20px;">📱 Opsi 1: Kirim File HTML (Paling Mudah)</h3>
                <ol style="margin-left: 20px;">
                    <li>Klik tombol <strong>"Get code"</strong> di pojok kanan atas artifact ini</li>
                    <li>Copy semua kode HTML</li>
                    <li>Paste ke Notepad/text editor → Save as <code>form-sewa-oksigen.html</code></li>
                    <li>Kirim file HTML via WhatsApp/Email ke penyewa</li>
                    <li>Penyewa tinggal buka file di browser (Chrome/Firefox/Safari)</li>
                    <li>✅ <strong>Langsung bisa dipakai tanpa internet!</strong></li>
                </ol>
                
                <h3 style="color: #f57c00; margin-top: 20px;">🌐 Opsi 2: Hosting Online (Bisa Dibagikan Link)</h3>
                <div style="background: white; padding: 15px; border-radius: 5px; margin-top: 10px;">
                    <strong>A. Menggunakan Netlify Drop (Super Mudah - Tanpa Daftar):</strong>
                    <ol style="margin-left: 20px; margin-top: 10px;">
                        <li>Buka <a href="https://app.netlify.com/drop" target="_blank" style="color: #00b4db; font-weight: 600;">app.netlify.com/drop</a></li>
                        <li>Drag & drop file HTML Anda ke halaman tersebut</li>
                        <li>Dalam 5 detik, form Anda sudah online dengan link unik!</li>
                        <li>Copy link → bagikan ke penyewa via WhatsApp/Instagram</li>
                    </ol>
                </div>
                
                <div style="background: white; padding: 15px; border-radius: 5px; margin-top: 10px;">
                    <strong>B. Menggunakan GitHub Pages (Gratis Selamanya):</strong>
                    <ol style="margin-left: 20px; margin-top: 10px;">
                        <li>Daftar di <a href="https://github.com" target="_blank" style="color: #00b4db; font-weight: 600;">GitHub.com</a> (gratis)</li>
                        <li>Klik <strong>New repository</strong></li>
                        <li>Nama repo: <code>form-sewa-oksigen</code> → Create</li>
                        <li>Upload file HTML Anda dengan nama <code>index.html</code></li>
                        <li>Ke Settings → Pages → pilih <strong>main branch</strong></li>
                        <li>Link form: <code>username.github.io/form-sewa-oksigen</code></li>
                    </ol>
                </div>
                
                <div style="background: #d4edda; padding: 15px; border-radius: 5px; margin-top: 15px; border: 1px solid #c3e6cb;">
                    <strong>✅ Rekomendasi:</strong> Gunakan <strong>Netlify Drop</strong> untuk tercepat (1 menit), 
                    atau <strong>GitHub Pages</strong> untuk link permanen yang bisa diupdate kapan saja.
                </div>
            </div>
        </div>
        
        </div>
    </div>
    
    <script>
        // Initialize signature pads
        let canvases = {
            signaturePenyewa: document.getElementById('signaturePenyewa')
        };
        
        let contexts = {
            signaturePenyewa: canvases.signaturePenyewa.getContext('2d')
        };
        
        let isDrawing = {
            signaturePenyewa: false
        };
        
        let hasSignature = {
            signaturePenyewa: false
        };
        
        // Set canvas size
        Object.keys(canvases).forEach(key => {
            const canvas = canvases[key];
            canvas.width = canvas.offsetWidth;
            canvas.height = canvas.offsetHeight;
            contexts[key].lineWidth = 2;
            contexts[key].lineCap = 'round';
            contexts[key].strokeStyle = '#000';
        });
        
        // Drawing functions
        function startDrawing(e, canvasId) {
            isDrawing[canvasId] = true;
            const rect = canvases[canvasId].getBoundingClientRect();
            const x = (e.clientX || e.touches[0].clientX) - rect.left;
            const y = (e.clientY || e.touches[0].clientY) - rect.top;
            contexts[canvasId].beginPath();
            contexts[canvasId].moveTo(x, y);
        }
        
        function draw(e, canvasId) {
            if (!isDrawing[canvasId]) return;
            e.preventDefault();
            const rect = canvases[canvasId].getBoundingClientRect();
            const x = (e.clientX || e.touches[0].clientX) - rect.left;
            const y = (e.clientY || e.touches[0].clientY) - rect.top;
            contexts[canvasId].lineTo(x, y);
            contexts[canvasId].stroke();
            hasSignature[canvasId] = true;
        }
        
        function stopDrawing(canvasId) {
            isDrawing[canvasId] = false;
        }
        
        // Add event listeners for both canvases
        Object.keys(canvases).forEach(canvasId => {
            const canvas = canvases[canvasId];
            
            // Mouse events
            canvas.addEventListener('mousedown', (e) => startDrawing(e, canvasId));
            canvas.addEventListener('mousemove', (e) => draw(e, canvasId));
            canvas.addEventListener('mouseup', () => stopDrawing(canvasId));
            canvas.addEventListener('mouseout', () => stopDrawing(canvasId));
            
            // Touch events
            canvas.addEventListener('touchstart', (e) => startDrawing(e, canvasId));
            canvas.addEventListener('touchmove', (e) => draw(e, canvasId));
            canvas.addEventListener('touchend', () => stopDrawing(canvasId));
        });
        
        function clearSignature(canvasId) {
            contexts[canvasId].clearRect(0, 0, canvases[canvasId].width, canvases[canvasId].height);
            hasSignature[canvasId] = false;
        }
        
        // Set current date
        const today = new Date().toISOString().split('T')[0];
        document.getElementById('tanggalMulai').value = today;
        document.getElementById('tanggalMulai').min = today;
        
        // Set display dates
        const displayDate = new Date().toLocaleDateString('id-ID', {
            day: 'numeric',
            month: 'long',
            year: 'numeric'
        });
        document.getElementById('tanggalPenyewa').textContent = displayDate;
        
        // Form submission
        document.getElementById('rentalForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const alertBox = document.getElementById('alertBox');
            
            // Validate signatures
            if (!hasSignature.signaturePenyewa) {
                alertBox.className = 'alert alert-danger';
                alertBox.textContent = '⚠️ Mohon lengkapi tanda tangan penyewa!';
                alertBox.style.display = 'block';
                window.scrollTo({ top: 0, behavior: 'smooth' });
                return;
            }
            
            // Your WhatsApp number (hardcoded)
            const waNumber = '6289608068804';
            
            // Collect form data
            const formData = {
                nama: document.getElementById('nama').value,
                nik: document.getElementById('nik').value,
                jenisId: document.getElementById('jenisId').value,
                alamat: document.getElementById('alamat').value,
                telepon: document.getElementById('telepon').value,
                email: document.getElementById('email').value,
                tanggalMulai: document.getElementById('tanggalMulai').value,
                durasi: document.getElementById('durasi').value,
                noTabung: document.getElementById('noTabung').value,
                biayaSewa: document.getElementById('biayaSewa').value
            };
            
            // Update nama penyewa di tanda tangan
            document.getElementById('namaPenyewa').textContent = formData.nama;
            
            // Create WhatsApp message
            const message = `*PERJANJIAN SEWA TABUNG OKSIGEN 1M³*

📋 *DATA PENYEWA*
Nama: ${formData.nama}
NIK: ${formData.nik}
Jenis Identitas: ${formData.jenisId}
Alamat: ${formData.alamat}
Telepon: ${formData.telepon}
Email: ${formData.email}

📦 *DETAIL SEWA*
Tanggal Mulai: ${formData.tanggalMulai}
Durasi: ${formData.durasi} bulan
No. Tabung: ${formData.noTabung || 'Belum diisi'}
Biaya Sewa: ${formData.biayaSewa}

📍 *LOKASI PENGAMBILAN*
Karangturi RT 07, Baturetno
Banguntapan, Bantul, Yogyakarta
https://maps.app.goo.gl/xYFTLhLqdjn4i35i7

✅ Penyewa menyetujui semua syarat dan ketentuan yang berlaku.

_Dokumen ini dikirim otomatis dari Form Perjanjian Sewa Tabung Oksigen_`;
            
            // Open WhatsApp
            const waUrl = `https://wa.me/${waNumber}?text=${encodeURIComponent(message)}`;
            window.open(waUrl, '_blank');
            
            // Show success message
            alertBox.className = 'alert alert-success';
            alertBox.textContent = '✅ Data berhasil disiapkan! WhatsApp akan terbuka otomatis untuk mengirim ke pemilik.';
            alertBox.style.display = 'block';
            
            // Show download button
            document.getElementById('downloadBtn').style.display = 'inline-block';
            
            window.scrollTo({ top: 0, behavior: 'smooth' });
        });
        
        function downloadPDF() {
            window.print();
        }
    </script>
</body>
</html>
