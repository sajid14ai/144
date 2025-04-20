<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy 13 Months, My Love</title>
    <style>
        /* Setting up a romantic background */
        body {
            margin: 0;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background: linear-gradient(135deg, #f5c0c0, #e2a9e5, #c9b6e4);
            font-family: 'Arial', sans-serif;
            overflow: hidden;
            position: relative;
        }

        /* Creating a container for our message */
        .container {
            text-align: center;
            padding: 2.5rem;
            background: rgba(255, 255, 255, 0.85);
            border-radius: 20px;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
            max-width: 650px;
            position: relative;
            z-index: 1;
            margin: 20px;
        }

        /* Styling the main heading */
        h1 {
            color: #d83f87;
            font-size: 2.8em;
            margin-bottom: 1rem;
            text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.1);
        }

        /* Styling the message text */
        p {
            color: #444;
            font-size: 1.2em;
            line-height: 1.7;
            margin-bottom: 1.5rem;
        }

        /* Creating floating hearts animation */
        .heart {
            position: absolute;
            font-size: 1.8rem;
            animation: float 8s ease-in-out infinite;
            opacity: 0.7;
        }

        @keyframes float {
            0% {
                transform: translateY(0) translateX(0) rotate(0deg);
                opacity: 0;
            }
            50% {
                opacity: 0.7;
            }
            100% {
                transform: translateY(-100vh) translateX(20px) rotate(360deg);
                opacity: 0;
            }
        }

        /* Special text styling */
        .special-text {
            color: #d83f87;
            font-weight: bold;
            font-size: 1.4em;
        }

        /* Month counter styling */
        .month-counter {
            font-size: 4.5rem;
            color: #d83f87;
            font-weight: bold;
            margin: 1.5rem 0;
            text-shadow: 2px 2px 10px rgba(216, 63, 135, 0.3);
            animation: pulse 2s ease infinite;
            display: inline-block;
        }

        /* Border for the container */
        .container::before {
            content: '';
            position: absolute;
            top: -5px;
            left: -5px;
            right: -5px;
            bottom: -5px;
            border: 2px dashed #d83f87;
            border-radius: 25px;
            z-index: -1;
            animation: borderPulse 4s linear infinite;
        }

        /* Animations */
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.1); }
            100% { transform: scale(1); }
        }

        @keyframes borderPulse {
            0%, 100% { opacity: 0.5; }
            50% { opacity: 1; }
        }

        /* Signature styling */
        .signature {
            font-style: italic;
            margin-top: 2rem;
            font-size: 1.3em;
        }

        /* Main heart decoration */
        .main-heart {
            display: inline-block;
            font-size: 2.5rem;
            color: #d83f87;
            margin: 0 10px;
            animation: heartBeat 1.5s ease infinite;
        }

        @keyframes heartBeat {
            0% { transform: scale(1); }
            14% { transform: scale(1.3); }
            28% { transform: scale(1); }
            42% { transform: scale(1.3); }
            70% { transform: scale(1); }
        }
    </style>
</head>
<body>
    <!-- Container for floating hearts -->
    <div id="hearts"></div>

    <div class="container">
        <h1>Happy 13 Months, My Love</h1>
        
        <div class="month-counter">13 <span class="main-heart">❤️</span> Months</div>
        
        <p>To my wonderful wife,</p>
        
        <p>Thirteen months of love, laughter, and beautiful memories together. Each day with you is a blessing that I cherish more than words can express. Your love has painted my world with colors I never knew existed.</p>
        
        <p class="special-text">Every moment with you is a gift <span class="main-heart">❤️</span></p>
        
        <p>From our first hello to today, from morning coffees to midnight talks, from the smallest joys to our biggest dreams - these thirteen months have been the most beautiful chapter of my life.</p>
        
        <p>Thank you for your love, your patience, and for making every day feel like a blessing. Here's to countless more months and years of us.</p>
        
        <p class="special-text">I love you more with each passing day <span class="main-heart">❤️</span></p>
        
        <p class="signature">Forever Yours,<br>Your Loving Husband</p>
    </div>

    <script>
        // Adding floating hearts with different colors and shapes
        function createHearts() {
            const body = document.body;
            const hearts = ['❤️', '💖', '💕', '💗', '💓', '💘', '💞'];
            
            setInterval(() => {
                const heart = document.createElement('div');
                heart.className = 'heart';
                heart.style.left = Math.random() * 100 + 'vw';
                heart.style.animationDuration = 5 + Math.random() * 5 + 's';
                heart.textContent = hearts[Math.floor(Math.random() * hearts.length)];
                body.appendChild(heart);
                
                // Remove heart after animation completes
                setTimeout(() => {
                    heart.remove();
                }, 8000);
            }, 400);
        }

        // Start creating hearts when the page loads
        window.onload = function() {
            createHearts();
        };
    </script>
</body>
</html>
