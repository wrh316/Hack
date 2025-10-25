<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hacker Simulator</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Courier New', monospace;
        }
        
        body {
            background-color: #0a0a0a;
            color: #00ff00;
            padding: 20px;
            min-height: 100vh;
            overflow-x: hidden;
            background-image: 
                radial-gradient(circle at 10% 20%, rgba(0, 255, 0, 0.05) 0%, transparent 20%),
                radial-gradient(circle at 90% 80%, rgba(0, 255, 0, 0.05) 0%, transparent 20%);
        }
        
        .container {
            max-width: 800px;
            margin: 0 auto;
            position: relative;
        }
        
        .header {
            text-align: center;
            margin-bottom: 30px;
            padding: 15px;
            border-bottom: 1px solid #00ff00;
            position: relative;
            overflow: hidden;
        }
        
        .header::before {
            content: "";
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(0, 255, 0, 0.1), transparent);
            animation: shine 3s infinite;
        }
        
        @keyframes shine {
            0% { left: -100%; }
            100% { left: 100%; }
        }
        
        h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
            text-shadow: 0 0 10px #00ff00;
        }
        
        .subtitle {
            color: #00aa00;
            font-size: 1.1rem;
        }
        
        .input-section {
            display: flex;
            margin-bottom: 20px;
            background: rgba(0, 20, 0, 0.5);
            padding: 15px;
            border: 1px solid #008800;
            border-radius: 4px;
        }
        
        #nInput {
            flex: 1;
            background: rgba(0, 10, 0, 0.8);
            border: 1px solid #00aa00;
            color: #00ff00;
            padding: 12px;
            font-size: 16px;
            border-radius: 4px;
        }
        
        #nInput:focus {
            outline: none;
            box-shadow: 0 0 10px rgba(0, 255, 0, 0.5);
        }
        
        #hackButton {
            background: rgba(0, 30, 0, 0.8);
            border: 1px solid #00aa00;
            color: #00ff00;
            padding: 12px 24px;
            cursor: pointer;
            margin-left: 10px;
            transition: all 0.3s;
            border-radius: 4px;
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 1px;
        }
        
        #hackButton:hover {
            background: #00aa00;
            color: #000;
            box-shadow: 0 0 15px rgba(0, 255, 0, 0.7);
        }
        
        .output {
            height: 400px;
            overflow-y: auto;
            border: 1px solid #00aa00;
            padding: 15px;
            margin-bottom: 20px;
            background-color: rgba(0, 10, 0, 0.7);
            border-radius: 4px;
            box-shadow: inset 0 0 20px rgba(0, 0, 0, 0.5);
        }
        
        .output-line {
            margin-bottom: 8px;
            line-height: 1.4;
            padding: 5px;
            border-left: 2px solid transparent;
            padding-left: 10px;
            animation: fadeIn 0.3s ease-in;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateX(-10px); }
            to { opacity: 1; transform: translateX(0); }
        }
        
        .stats {
            display: flex;
            justify-content: space-between;
            margin-top: 20px;
            padding: 15px;
            border-top: 1px solid #00aa00;
            background: rgba(0, 20, 0, 0.5);
            border-radius: 4px;
            font-size: 1.2rem;
        }
        
        .success {
            color: #00ff00;
            text-shadow: 0 0 5px #00ff00;
        }
        
        .failure {
            color: #ff0000;
            text-shadow: 0 0 5px #ff0000;
        }
        
        .invalid {
            color: #808080;
        }
        
        .points {
            color: #ffff00;
            text-shadow: 0 0 5px #ffff00;
        }
        
        .blink {
            animation: blink 1.5s infinite;
        }
        
        @keyframes blink {
            0% { opacity: 1; }
            50% { opacity: 0.7; }
            100% { opacity: 1; }
        }
        
        .scan-line {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 2px;
            background: rgba(0, 255, 0, 0.5);
            animation: scan 4s linear infinite;
            pointer-events: none;
            z-index: 10;
            box-shadow: 0 0 10px rgba(0, 255, 0, 0.7);
        }
        
        @keyframes scan {
            0% { top: 0; }
            100% { top: 100%; }
        }
        
        .matrix-bg {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
            opacity: 0.1;
        }
        
        .glitch {
            position: relative;
        }
        
        .glitch::before, .glitch::after {
            content: attr(data-text);
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
        }
        
        .glitch::before {
            left: 2px;
            text-shadow: -2px 0 #ff00ff;
            clip: rect(44px, 450px, 56px, 0);
            animation: glitch-anim 5s infinite linear alternate-reverse;
        }
        
        .glitch::after {
            left: -2px;
            text-shadow: -2px 0 #00ffff;
            clip: rect(44px, 450px, 56px, 0);
            animation: glitch-anim2 5s infinite linear alternate-reverse;
        }
        
        @keyframes glitch-anim {
            0% { clip: rect(42px, 9999px, 44px, 0); }
            5% { clip: rect(12px, 9999px, 59px, 0); }
            10% { clip: rect(48px, 9999px, 29px, 0); }
            15% { clip: rect(42px, 9999px, 73px, 0); }
            20% { clip: rect(63px, 9999px, 27px, 0); }
            25% { clip: rect(34px, 9999px, 55px, 0); }
            30% { clip: rect(86px, 9999px, 73px, 0); }
            35% { clip: rect(20px, 9999px, 20px, 0); }
            40% { clip: rect(26px, 9999px, 60px, 0); }
            45% { clip: rect(25px, 9999px, 66px, 0); }
            50% { clip: rect(57px, 9999px, 98px, 0); }
            55% { clip: rect(5px, 9999px, 46px, 0); }
            60% { clip: rect(82px, 9999px, 31px, 0); }
            65% { clip: rect(54px, 9999px, 27px, 0); }
            70% { clip: rect(28px, 9999px, 99px, 0); }
            75% { clip: rect(45px, 9999px, 69px, 0); }
            80% { clip: rect(23px, 9999px, 85px, 0); }
            85% { clip: rect(54px, 9999px, 84px, 0); }
            90% { clip: rect(45px, 9999px, 47px, 0); }
            95% { clip: rect(37px, 9999px, 20px, 0); }
            100% { clip: rect(4px, 9999px, 91px, 0); }
        }
        
        @keyframes glitch-anim2 {
            0% { clip: rect(65px, 9999px, 100px, 0); }
            5% { clip: rect(52px, 9999px, 74px, 0); }
            10% { clip: rect(79px, 9999px, 85px, 0); }
            15% { clip: rect(75px, 9999px, 5px, 0); }
            20% { clip: rect(67px, 9999px, 61px, 0); }
            25% { clip: rect(14px, 9999px, 79px, 0); }
            30% { clip: rect(1px, 9999px, 66px, 0); }
            35% { clip: rect(86px, 9999px, 30px, 0); }
            40% { clip: rect(23px, 9999px, 98px, 0); }
            45% { clip: rect(85px, 9999px, 72px, 0); }
            50% { clip: rect(71px, 9999px, 75px, 0); }
            55% { clip: rect(2px, 9999px, 48px, 0); }
            60% { clip: rect(30px, 9999px, 16px, 0); }
            65% { clip: rect(59px, 9999px, 50px, 0); }
            70% { clip: rect(41px, 9999px, 62px, 0); }
            75% { clip: rect(2px, 9999px, 82px, 0); }
            80% { clip: rect(47px, 9999px, 73px, 0); }
            85% { clip: rect(3px, 9999px, 27px, 0); }
            90% { clip: rect(26px, 9999px, 55px, 0); }
            95% { clip: rect(42px, 9999px, 97px, 0); }
            100% { clip: rect(38px, 9999px, 49px, 0); }
        }
        
        .success .output-line {
            border-left-color: #00ff00;
            background: rgba(0, 255, 0, 0.05);
        }
        
        .failure .output-line {
            border-left-color: #ff0000;
            background: rgba(255, 0, 0, 0.05);
        }
        
        .invalid .output-line {
            border-left-color: #808080;
            background: rgba(128, 128, 128, 0.05);
        }
        
        .typing {
            overflow: hidden;
            border-right: 2px solid #00ff00;
            white-space: nowrap;
            margin: 0 auto;
            animation: typing 3.5s steps(40, end), blink-caret 0.75s step-end infinite;
        }
        
        @keyframes typing {
            from { width: 0 }
            to { width: 100% }
        }
        
        @keyframes blink-caret {
            from, to { border-color: transparent }
            50% { border-color: #00ff00; }
        }
    </style>
</head>
<body>
    <div class="matrix-bg" id="matrixBg"></div>
    <div class="scan-line"></div>
    
    <div class="container">
        <div class="header">
            <h1 class="blink glitch" data-text="HACKER SIMULATOR">HACKER SIMULATOR</h1>
            <p class="subtitle">Enter a number and initiate simulated cyber attacks</p>
        </div>
        
        <div class="input-section">
            <input type="number" id="nInput" placeholder="Enter number (n)" min="1" value="10">
            <button id="hackButton">INITIATE ATTACK</button>
        </div>
        
        <div class="output" id="output">
            <div class="output-line">System ready...</div>
            <div class="output-line">Initializing attack modules...</div>
            <div class="output-line">Awaiting input...</div>
        </div>
        
        <div class="stats">
            <div class="success">+<span id="successCount">0</span></div>
            <div class="invalid">:</div>
            <div class="failure">-<span id="failureCount">0</span></div>
            <div class="points">Points: <span id="points">0</span></div>
        </div>
    </div>

    <script>
        let successCount = 0;
        let failureCount = 0;
        let points = 0;
        
        // Matrix background effect
        function createMatrix() {
            const canvas = document.createElement('canvas');
            const container = document.getElementById('matrixBg');
            container.appendChild(canvas);
            const ctx = canvas.getContext('2d');
            
            canvas.width = container.clientWidth;
            canvas.height = container.clientHeight;
            
            const chars = "01";
            const charArray = chars.split("");
            const fontSize = 14;
            const columns = canvas.width / fontSize;
            const drops = [];
            
            for (let i = 0; i < columns; i++) {
                drops[i] = Math.floor(Math.random() * canvas.height / fontSize);
            }
            
            function draw() {
                ctx.fillStyle = "rgba(0, 0, 0, 0.04)";
                ctx.fillRect(0, 0, canvas.width, canvas.height);
                
                ctx.fillStyle = "#0F0";
                ctx.font = fontSize + "px monospace";
                
                for (let i = 0; i < drops.length; i++) {
                    const text = charArray[Math.floor(Math.random() * charArray.length)];
                    ctx.fillText(text, i * fontSize, drops[i] * fontSize);
                    
                    if (drops[i] * fontSize > canvas.height && Math.random() > 0.975) {
                        drops[i] = 0;
                    }
                    drops[i]++;
                }
            }
            
            setInterval(draw, 33);
        }
        
        document.getElementById('hackButton').addEventListener('click', function() {
            const n = parseInt(document.getElementById('nInput').value);
            if (isNaN(n) || n < 1) {
                addOutputLine("Invalid input", "invalid");
                return;
            }
            
            const output = document.getElementById('output');
            const attempts = Math.floor(Math.random() * 16) + 1;
            
            for (let i = 0; i < attempts; i++) {
                const randomValue = Math.random();
                
                if (Math.floor(Math.random() * n) === 0) {
                    addOutputLine("Successful hacking attempt(wa)", "success");
                    successCount++;
                    points += 100;
                } else if (Math.floor(Math.random() * n) === 1) {
                    addOutputLine("Successful hacking attempt(tl)", "success");
                    successCount++;
                    points += 100;
                } else if (Math.random() > n / 100) {
                    addOutputLine("Unsuccessful hacking attempt", "failure");
                    failureCount++;
                    points -= 50;
                } else {
                    addOutputLine("Invalid input", "invalid");
                }
            }
            
            updateStats();
        });
        
        function addOutputLine(text, type) {
            const output = document.getElementById('output');
            const line = document.createElement('div');
            line.className = `output-line ${type}`;
            line.textContent = text;
            output.appendChild(line);
            output.scrollTop = output.scrollHeight;
        }
        
        function updateStats() {
            document.getElementById('successCount').textContent = successCount;
            document.getElementById('failureCount').textContent = failureCount;
            document.getElementById('points').textContent = points;
        }
        
        // Add initial output for effect
        setTimeout(() => {
            addOutputLine("Scanning network...", "invalid");
        }, 500);
        
        setTimeout(() => {
            addOutputLine("Targets identified...", "invalid");
        }, 1200);
        
        setTimeout(() => {
            addOutputLine("Preparing attack vectors...", "invalid");
        }, 2000);
        
        // Initialize matrix background
        window.addEventListener('load', createMatrix);
        window.addEventListener('resize', function() {
            document.getElementById('matrixBg').innerHTML = '';
            createMatrix();
        });
    </script>
</body>
</html>
