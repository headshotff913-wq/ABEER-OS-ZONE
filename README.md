# ABEER-OS-ZONE
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Abeer Tech OS Pro | Free ISOs & Advanced Tools</title>
    <!-- QR Code Library Link (Free) -->
    <script src="https://cloudflare.com"></script>
    <style>
        body {
            background-color: #0a0a0a;
            color: #e0e0e0;
            font-family: 'Segoe UI', Arial, sans-serif;
            margin: 0;
            padding: 0;
        }
        header {
            background: linear-gradient(180deg, #111, #0a0a0a);
            text-align: center;
            padding: 60px 20px;
            border-bottom: 2px solid #00ffcc;
        }
        .dev-badge {
            background-color: #00ffcc;
            color: #000;
            padding: 5px 15px;
            font-weight: bold;
            border-radius: 20px;
            font-size: 0.9rem;
            display: inline-block;
            margin-bottom: 15px;
            box-shadow: 0 0 10px rgba(0, 255, 204, 0.4);
        }
        header h1 {
            color: #ffffff;
            font-size: 2.8rem;
            margin: 0;
        }
        header h1 span {
            color: #00ffcc;
            text-shadow: 0 0 15px rgba(0, 255, 204, 0.6);
        }
        .site-description {
            max-width: 700px;
            margin: 20px auto 0 auto;
            color: #aaa;
            font-size: 1.1rem;
            line-height: 1.6;
        }
        .container {
            max-width: 1100px;
            margin: 40px auto;
            padding: 0 20px;
        }
        h2 {
            color: #00ffcc;
            border-left: 4px solid #00ffcc;
            padding-left: 10px;
            margin-top: 40px;
        }
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 25px;
        }
        .card {
            background-color: #121212;
            border: 1px solid #222;
            border-radius: 12px;
            padding: 25px;
            transition: all 0.3s ease;
        }
        .card:hover {
            border-color: #00ffcc;
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(0, 255, 204, 0.1);
        }
        .btn {
            background-color: #00ffcc;
            color: #000;
            padding: 12px 20px;
            border: none;
            border-radius: 6px;
            font-weight: bold;
            cursor: pointer;
            width: 100%;
            margin-top: 15px;
            transition: 0.2s;
        }
        .btn:hover {
            background-color: #00ccaa;
        }
        input {
            width: 100%;
            padding: 10px;
            background-color: #1a1a1a;
            border: 1px solid #333;
            color: #fff;
            border-radius: 6px;
            margin-top: 10px;
            box-sizing: border-box;
        }
        .result-box {
            background-color: #1a1a1a;
            padding: 12px;
            border-radius: 6px;
            margin-top: 15px;
            word-break: break-all;
            text-align: center;
            border: 1px dashed #444;
        }
        #qrcode img {
            margin: 0 auto;
        }
        footer {
            text-align: center;
            padding: 40px;
            color: #555;
            border-top: 1px solid #222;
            margin-top: 60px;
        }
    </style>
</head>
<body>

    <header>
        <div class="dev-badge">PROJECT BY A YOUNG TECH GENIUS</div>
        <h1>Welcome to <span>Abeer Tech OS Pro</span></h1>
        
        <!-- Professional Description -->
        <p class="site-description">
            Hi, I am <strong>Abeer</strong>. I have personally tested and configured multiple Android operating systems on real hardware. This platform provides the most optimized, lightweight Android ISO files tailored for older and low-end laptops, packed alongside everyday advanced web utilities to boost your productivity.
        </p>
    </header>

    <div class="container">
        
        <!-- OS Directory Section -->
        <h2>1. Tested Android OS ISOs by Abeer</h2>
        <div class="grid">
            <div class="card">
                <h3>Bliss OS 14 (Android 11)</h3>
                <p><strong>Best For:</strong> Dell Latitude E5540, HP ProBook (Intel 4th/5th Gen).</p>
                <p>Perfect for daily tasks, smooth UI, and great battery saving on older laptops.</p>
                <button class="btn" onclick="alert('ISO Download Link Here')">Download ISO</button>
            </div>
            <div class="card">
                <h3>Prime OS (Classic)</h3>
                <p><strong>Best For:</strong> Low-end Intel/AMD Laptops (2GB/4GB RAM).</p>
                <p>Best for PUBG/FreeFire gaming with built-in keyboard keymapping tools.</p>
                <button class="btn" onclick="alert('ISO Download Link Here')">Download ISO</button>
            </div>
        </div>

        <!-- Web Tools Section -->
        <h2>2. Advanced Web Utilities</h2>
        <div class="grid">
            <!-- Password Generator -->
            <div class="card">
                <h3>Password Generator</h3>
                <p>Generate secure, un-hackable passwords instantly.</p>
                <button class="btn" onclick="generatePassword()">Generate Password</button>
                <div class="result-box" id="passResult">Click generate above...</div>
            </div>

            <!-- QR Code Generator -->
            <div class="card">
                <h3>QR Code Generator</h3>
                <p>Enter text or link to create a QR code.</p>
                <input type="text" id="qrText" placeholder="Paste link or text here...">
                <button class="btn" onclick="makeQR()">Generate QR Code</button>
                <div class="result-box" style="display:none;" id="qrContainer">
                    <div id="qrcode"></div>
                </div>
            </div>
        </div>

    </div>

    <footer>
        &copy; 2026 Abeer Tech OS Pro. Designed & Developed by Abeer. All Rights Reserved.
    </footer>

    <!-- JavaScript Functions for Tools -->
    <script>
        function generatePassword() {
            const chars = "abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789!@#$%^&*()_+";
            let password = "";
            for (let i = 0; i < 12; i++) {
                password += chars.charAt(Math.floor(Math.random() * chars.length));
            }
            document.getElementById("passResult").innerText = password;
        }

        function makeQR() {
            let text = document.getElementById("qrText").value;
            if(!text) {
                alert("Pehle koi text ya link likhein!");
                return;
            }
            document.getElementById("qrContainer").style.display = "block";
            document.getElementById("qrcode").innerHTML = ""; 
            new QRCode(document.getElementById("qrcode"), {
                text: text,
                width: 128,
                height: 128,
                colorDark : "#000000",
                colorLight : "#ffffff"
            });
        }
    </script>
</body>
</html>
