<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AMIW - AI Music Generator</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&display=swap');
        body {
            margin: 0;
            font-family: 'Orbitron', sans-serif;
            background: linear-gradient(to right, #8B0000, #4B0082);
            color: white;
            text-align: center;
            overflow: hidden;
        }
        .container {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            position: relative;
        }
        h1 {
            font-size: 3.5rem;
            text-shadow: 0 0 20px gold;
            animation: pulse 2s infinite;
        }
        @keyframes pulse {
            0% { text-shadow: 0 0 10px gold; }
            50% { text-shadow: 0 0 30px gold; }
            100% { text-shadow: 0 0 10px gold; }
        }
        p {
            font-size: 1.3rem;
            max-width: 700px;
            line-height: 1.6;
        }
        .btn {
            background: gold;
            color: black;
            padding: 12px 25px;
            font-size: 1.3rem;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            transition: 0.3s;
            box-shadow: 0 0 15px rgba(255, 215, 0, 0.7);
        }
        .btn:hover {
            background: #ffcc00;
            box-shadow: 0 0 25px rgba(255, 215, 0, 1);
        }
        #dynamicContent {
            margin-top: 20px;
            font-size: 1.5rem;
            color: #ffcc00;
            animation: glow 2s infinite alternate;
        }
        @keyframes glow {
            from { text-shadow: 0 0 10px #ffcc00; }
            to { text-shadow: 0 0 30px #ffcc00; }
        }
        .music-visualizer {
            position: absolute;
            bottom: 20px;
            width: 100%;
            height: 100px;
            display: flex;
            justify-content: center;
            align-items: flex-end;
        }
        .bar {
            width: 10px;
            height: 50px;
            margin: 0 5px;
            background: gold;
            animation: bounce 1.5s infinite alternate ease-in-out;
        }
        @keyframes bounce {
            0% { height: 30px; }
            100% { height: 80px; }
        }
    </style>
    <script>
        function changeContent() {
            let messages = [
                "Unleash your creativity with AMIW!",
                "Generate AI-powered music instantly!",
                "Compose, edit, and enhance like a pro!",
                "Your music, your way - powered by AI!"
            ];
            let randomMessage = messages[Math.floor(Math.random() * messages.length)];
            document.getElementById("dynamicContent").innerText = randomMessage;
        }
        setInterval(changeContent, 3000);
    </script>
</head>
<body>
    <audio autoplay loop>
        <source src="your-background-music.mp3" type="audio/mpeg">
        Your browser does not support the audio tag.
    </audio>
    <div class="container">
        <h1>AMIW - AI Music Generator</h1>
        <p>Create unique lyrics & music with advanced AI. Generate MP3s, MP4s, and customize your sound like never before.</p>
        <button class="btn" onclick="changeContent()">Get Started</button>
        <div id="dynamicContent">Welcome to AMIW!</div>
    </div>
    <div class="music-visualizer">
        <div class="bar" style="animation-delay: 0.1s;"></div>
        <div class="bar" style="animation-delay: 0.2s;"></div>
        <div class="bar" style="animation-delay: 0.3s;"></div>
        <div class="bar" style="animation-delay: 0.4s;"></div>
        <div class="bar" style="animation-delay: 0.5s;"></div>
        <div class="bar" style="animation-delay: 0.6s;"></div>
        <div class="bar" style="animation-delay: 0.7s;"></div>
    </div>
</body>
</html>
