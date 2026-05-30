# Anniversary-
3 years 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>3 Years of Love & Memories</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            overflow-x: hidden;
        }

        /* Animated background */
        .animated-bg {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(-45deg, #ee7752, #e73c7e, #23a6d5, #23d5ab);
            background-size: 400% 400%;
            animation: gradient 15s ease infinite;
            z-index: -1;
        }

        @keyframes gradient {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        /* Floating hearts background */
        .hearts-container {
            position: fixed;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            z-index: 0;
            pointer-events: none;
        }

        .heart {
            position: absolute;
            width: 30px;
            height: 30px;
            opacity: 0.3;
            animation: float 6s infinite ease-in;
        }

        @keyframes float {
            0% {
                transform: translateY(100vh) rotate(0deg);
                opacity: 0;
            }
            10% {
                opacity: 0.3;
            }
            90% {
                opacity: 0.3;
            }
            100% {
                transform: translateY(-100vh) rotate(360deg);
                opacity: 0;
            }
        }

        /* Main container */
        .container {
            position: relative;
            z-index: 10;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            padding: 20px;
        }

        /* Header section */
        .header {
            text-align: center;
            margin-bottom: 40px;
            animation: slideInDown 1s ease-out;
        }

        @keyframes slideInDown {
            from {
                opacity: 0;
                transform: translateY(-50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .header h1 {
            font-size: 3.5em;
            color: white;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
            margin-bottom: 10px;
            letter-spacing: 2px;
        }

        .header .subtitle {
            font-size: 1.5em;
            color: #ffe66d;
            text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.3);
            font-style: italic;
        }

        /* Counter section */
        .counter-section {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 40px;
            margin: 30px 0;
            box-shadow: 0 8px 32px 0 rgba(31, 38, 135, 0.37);
            border: 1px solid rgba(255, 255, 255, 0.18);
            animation: slideInUp 1s ease-out;
            max-width: 500px;
            width: 100%;
        }

        @keyframes slideInUp {
            from {
                opacity: 0;
                transform: translateY(50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .counter {
            display: flex;
            justify-content: space-around;
            margin: 20px 0;
        }

        .counter-item {
            text-align: center;
            animation: pulse 2s ease-in-out infinite;
        }

        .counter-item:nth-child(2) {
            animation-delay: 0.2s;
        }

        .counter-item:nth-child(3) {
            animation-delay: 0.4s;
        }

        @keyframes pulse {
            0%, 100% {
                transform: scale(1);
            }
            50% {
                transform: scale(1.1);
            }
        }

        .counter-number {
            font-size: 2.5em;
            font-weight: bold;
            color: #ffe66d;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
        }

        .counter-label {
            color: white;
            font-size: 0.9em;
            margin-top: 5px;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        /* Gallery section */
        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin: 40px 0;
            max-width: 900px;
            width: 100%;
        }

        .gallery-item {
            position: relative;
            overflow: hidden;
            border-radius: 15px;
            box-shadow: 0 8px 32px 0 rgba(31, 38, 135, 0.37);
            animation: zoomIn 0.8s ease-out;
            cursor: pointer;
            transform: perspective(1000px) rotateY(0deg);
            transition: transform 0.3s ease;
        }

        .gallery-item:hover {
            transform: perspective(1000px) rotateY(-5deg) scale(1.05);
        }

        @keyframes zoomIn {
            from {
                opacity: 0;
                transform: scale(0.8);
            }
            to {
                opacity: 1;
                transform: scale(1);
            }
        }

        .gallery-item img {
            width: 100%;
            height: 250px;
            object-fit: cover;
            display: block;
        }

        .gallery-item-overlay {
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: rgba(0, 0, 0, 0.5);
            display: flex;
            align-items: center;
            justify-content: center;
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .gallery-item:hover .gallery-item-overlay {
            opacity: 1;
        }

        .gallery-item-overlay p {
            color: white;
            font-size: 1.2em;
            text-align: center;
        }

        /* Messages section */
        .messages-section {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 40px;
            margin: 40px 0;
            box-shadow: 0 8px 32px 0 rgba(31, 38, 135, 0.37);
            border: 1px solid rgba(255, 255, 255, 0.18);
            max-width: 600px;
            width: 100%;
            animation: slideInUp 1s ease-out 0.3s backwards;
        }

        .messages-section h2 {
            color: white;
            font-size: 2em;
            margin-bottom: 20px;
            text-align: center;
        }

        .message-card {
            background: rgba(255, 255, 255, 0.15);
            border-left: 4px solid #ffe66d;
            padding: 20px;
            margin: 15px 0;
            border-radius: 10px;
            animation: slideInLeft 0.8s ease-out;
            color: white;
            line-height: 1.6;
        }

        .message-card:nth-child(2) {
            animation-delay: 0.2s;
            border-left-color: #ff6b9d;
        }

        .message-card:nth-child(3) {
            animation-delay: 0.4s;
            border-left-color: #c44569;
        }

        @keyframes slideInLeft {
            from {
                opacity: 0;
                transform: translateX(-50px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }

        /* Footer */
        .footer {
            margin-top: 60px;
            text-align: center;
            color: white;
            animation: fadeIn 1.5s ease-out;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
            }
            to {
                opacity: 1;
            }
        }

        .footer p {
            font-size: 1.2em;
            margin: 10px 0;
        }

        .love-animation {
            display: inline-block;
            animation: heartbeat 1.2s infinite;
        }

        @keyframes heartbeat {
            0%, 100% {
                transform: scale(1);
            }
            50% {
                transform: scale(1.2);
            }
        }

        /* Responsive */
        @media (max-width: 768px) {
            .header h1 {
                font-size: 2.5em;
            }

            .header .subtitle {
                font-size: 1.2em;
            }

            .counter-number {
                font-size: 2em;
            }

            .gallery {
                grid-template-columns: 1fr;
            }

            .messages-section {
                padding: 25px;
            }
        }

        /* Particle effects */
        .particle {
            position: absolute;
            pointer-events: none;
        }

        .confetti {
            width: 10px;
            height: 10px;
            background: #ffe66d;
            animation: confetti-fall 3s infinite;
        }

        @keyframes confetti-fall {
            to {
                transform: translateY(100vh) rotate(360deg);
                opacity: 0;
            }
        }
    </style>
</head>
<body>
    <div class="animated-bg"></div>
    <div class="hearts-container" id="heartsContainer"></div>

    <div class="container">
        <!-- Header -->
        <div class="header">
            <h1>🎉 3 Years Together 🎉</h1>
            <p class="subtitle">A Journey of Love, Laughter & Forever Memories</p>
        </div>

        <!-- Counter Section -->
        <div class="counter-section">
            <h2 style="color: white; text-align: center; margin-bottom: 20px;">Our Love Story Counter</h2>
            <div class="counter">
                <div class="counter-item">
                    <div class="counter-number" id="years">3</div>
                    <div class="counter-label">Years</div>
                </div>
                <div class="counter-item">
                    <div class="counter-number" id="months">0</div>
                    <div class="counter-label">Months</div>
                </div>
                <div class="counter-item">
                    <div class="counter-number" id="days">0</div>
                    <div class="counter-label">Days</div>
                </div>
            </div>
        </div>

        <!-- Gallery Section -->
        <div class="gallery" id="gallery">
            <div class="gallery-item">
                <img src="https://via.placeholder.com/300x250/FF6B9D/FFFFFF?text=Your+Photo+1" alt="Memory 1">
                <div class="gallery-item-overlay">
                    <p>Our First Meeting</p>
                </div>
            </div>
            <div class="gallery-item">
                <img src="https://via.placeholder.com/300x250/C44569/FFFFFF?text=Your+Photo+2" alt="Memory 2">
                <div class="gallery-item-overlay">
                    <p>A Beautiful Moment</p>
                </div>
            </div>
            <div class="gallery-item">
                <img src="https://via.placeholder.com/300x250/23D5AB/FFFFFF?text=Your+Photo+3" alt="Memory 3">
                <div class="gallery-item-overlay">
                    <p>Forever & Always</p>
                </div>
            </div>
        </div>

        <!-- Messages Section -->
        <div class="messages-section">
            <h2>💌 Our Moments</h2>
            <div class="message-card">
                <p><strong>To My Love,</strong><br>
                Every day with you is a blessing. In these 3 years, you've become my greatest adventure, my sweetest dream, and my reason to smile. Here's to many more years of laughter, love, and unforgettable memories together. 💕</p>
            </div>
            <div class="message-card">
                <p><strong>What Makes Us Special,</strong><br>
                It's not just the big moments - it's the quiet mornings, the silly inside jokes, the way you make me feel understood, and how we've grown together. You are my home. ✨</p>
            </div>
            <div class="message-card">
                <p><strong>Forever Grateful,</strong><br>
                Thank you for choosing me, believing in us, and making every single day an adventure. I love you more today than yesterday, and less than tomorrow. Happy Anniversary! 🎊</p>
            </div>
        </div>

        <!-- Footer -->
        <div class="footer">
            <p>With all my love <span class="love-animation">❤️</span></p>
            <p style="font-size: 1em; margin-top: 20px; color: #ffe66d;">🌹 May our love story continue to blossom forever 🌹</p>
        </div>
    </div>

    <script>
        // Generate floating hearts
        function generateHearts() {
            const container = document.getElementById('heartsContainer');
            const heartSymbols = ['❤️', '💕', '💖', '💝', '💗'];
            
            for (let i = 0; i < 15; i++) {
                const heart = document.createElement('div');
                heart.className = 'heart';
                heart.textContent = heartSymbols[Math.floor(Math.random() * heartSymbols.length)];
                heart.style.left = Math.random() * 100 + '%';
                heart.style.animationDuration = (Math.random() * 3 + 4) + 's';
                heart.style.animationDelay = Math.random() * 2 + 's';
                container.appendChild(heart);
            }
        }

        // Calculate time together
        function updateCounter() {
            // Change this to your actual anniversary date
            const anniversaryDate = new Date('2022-05-30').getTime();
            const today = new Date().getTime();
            const difference = today - anniversaryDate;

            const years = Math.floor(difference / (1000 * 60 * 60 * 24 * 365));
            const months = Math.floor((difference % (1000 * 60 * 60 * 24 * 365)) / (1000 * 60 * 60 * 24 * 30));
            const days = Math.floor((difference % (1000 * 60 * 60 * 24 * 30)) / (1000 * 60 * 60 * 24));

            document.getElementById('years').textContent = years;
            document.getElementById('months').textContent = months;
            document.getElementById('days').textContent = days;
        }

        // Create confetti effect on page load
        function createConfetti() {
            const container = document.body;
            for (let i = 0; i < 50; i++) {
                const confetti = document.createElement('div');
                confetti.className = 'confetti';
                confetti.style.left = Math.random() * 100 + '%';
                confetti.style.animationDelay = Math.random() * 0.5 + 's';
                confetti.style.opacity = Math.random();
                container.appendChild(confetti);
                setTimeout(() => confetti.remove(), 3000);
            }
        }

        // Click to create confetti
        document.addEventListener('click', (e) => {
            const colors = ['#ffe66d', '#ff6b9d', '#c44569', '#23d5ab'];
            const confetti = document.createElement('div');
            confetti.className = 'confetti';
            confetti.style.left = e.clientX + 'px';
            confetti.style.top = e.clientY + 'px';
            confetti.style.background = colors[Math.floor(Math.random() * colors.length)];
            confetti.style.position = 'fixed';
            confetti.style.pointerEvents = 'none';
            confetti.style.animation = 'confetti-fall 2s forwards';
            document.body.appendChild(confetti);
            setTimeout(() => confetti.remove(), 2000);
        });

        // Initialize
        window.addEventListener('load', () => {
            generateHearts();
            updateCounter();
            createConfetti();
        });

        // Update counter every second
        setInterval(updateCounter, 1000);
    </script>
</body>
</html>
