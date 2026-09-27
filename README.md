# angelrose
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Birthday! 🐱🎂</title>

    <style>
        * {
            box-sizing: border-box;
        }

        body {
            margin: 0;
            min-height: 100vh;
            font-family: "Trebuchet MS", Arial, sans-serif;
            background:
                radial-gradient(circle at 20% 20%, #fff 0 2px, transparent 3px),
                radial-gradient(circle at 80% 30%, #fff 0 2px, transparent 3px),
                radial-gradient(circle at 40% 70%, #fff 0 2px, transparent 3px),
                linear-gradient(135deg, #ffc4df, #cdb8ff, #aee7ff);
            background-size: 180px 180px, 220px 220px, 150px 150px, 100% 100%;
            overflow-x: hidden;
            color: #60456f;
        }

        /* FLOATING DECORATIONS */

        .decor {
            position: fixed;
            z-index: 1;
            pointer-events: none;
            animation: float 4s ease-in-out infinite;
        }

        .balloon {
            font-size: 55px;
        }

        .star {
            font-size: 25px;
        }

        .heart {
            font-size: 30px;
        }

        @keyframes float {
            0%, 100% {
                transform: translateY(0) rotate(-5deg);
            }

            50% {
                transform: translateY(-18px) rotate(5deg);
            }
        }

        .b1 {
            top: 7%;
            left: 5%;
        }

        .b2 {
            top: 12%;
            right: 5%;
            animation-delay: 1s;
        }

        .s1 {
            top: 20%;
            left: 18%;
            animation-delay: .5s;
        }

        .s2 {
            top: 25%;
            right: 18%;
            animation-delay: 1.5s;
        }

        .h1 {
            bottom: 12%;
            left: 8%;
            animation-delay: 1s;
        }

        .h2 {
            bottom: 18%;
            right: 8%;
            animation-delay: 2s;
        }

        /* MAIN */

        .container {
            width: 92%;
            max-width: 900px;
            margin: 40px auto;
            position: relative;
            z-index: 2;
        }

        .card {
            background: rgba(255, 255, 255, 0.88);
            backdrop-filter: blur(10px);
            border: 3px solid rgba(255,255,255,.9);
            border-radius: 35px;
            padding: 35px 25px;
            text-align: center;
            box-shadow:
                0 20px 60px rgba(91, 54, 117, .25),
                inset 0 0 30px rgba(255,255,255,.5);
        }

        .ribbon {
            display: inline-block;
            background: #ff78ad;
            color: white;
            padding: 8px 22px;
            border-radius: 30px;
            font-weight: bold;
            letter-spacing: 2px;
            box-shadow: 0 6px 15px rgba(255,120,173,.35);
        }

        .cat {
            font-size: 120px;
            margin-top: 15px;
            display: inline-block;
            filter: drop-shadow(0 8px 5px rgba(0,0,0,.12));
            animation: catBounce 2s ease-in-out infinite;
        }

        @keyframes catBounce {
            0%, 100% {
                transform: translateY(0);
            }

            50% {
                transform: translateY(-12px);
            }
        }

        h1 {
            margin: 5px 0;
            font-size: clamp(38px, 8vw, 75px);
            color: #ff5c9a;
            text-shadow:
                3px 3px 0 #fff,
                0 0 18px rgba(255,92,154,.45);
            animation: glow 2s infinite alternate;
        }

        @keyframes glow {
            from {
                text-shadow: 3px 3px 0 #fff,
                             0 0 10px rgba(255,92,154,.3);
            }

            to {
                text-shadow: 3px 3px 0 #fff,
                             0 0 28px rgba(255,92,154,.8);
            }
        }

        .subtitle {
            font-size: 21px;
            color: #8c67b7;
            font-weight: bold;
            margin-bottom: 25px;
        }

        /* CAKE */

        .cake-area {
            margin: 15px auto 25px;
        }

        .cake {
            font-size: 75px;
            animation: cake 1.5s infinite alternate;
        }

        @keyframes cake {
            from {
                transform: scale(1);
            }

            to {
                transform: scale(1.08);
            }
        }

        /* MESSAGE */

        .message-box {
            max-width: 650px;
            margin: auto;
            background: linear-gradient(135deg, #fff0f7, #f1eaff);
            padding: 25px;
            border-radius: 25px;
            border: 2px dashed #ff91bd;
            box-shadow: inset 0 0 20px rgba(255,255,255,.8);
        }

        .message-box p {
            font-size: 18px;
            line-height: 1.7;
            margin: 8px 0;
        }

        .highlight {
            color: #ff5795;
            font-weight: bold;
        }

        /* BUTTON */

        .surprise-btn {
            margin-top: 25px;
            padding: 16px 28px;
            border: none;
            border-radius: 50px;
            background: linear-gradient(135deg, #ff5e9f, #a979ed);
            color: white;
            font-size: 17px;
            font-weight: bold;
            cursor: pointer;
            box-shadow: 0 8px 20px rgba(168,110,220,.35);
            transition: .3s;
        }

        .surprise-btn:hover {
            transform: scale(1.08);
            box-shadow: 0 12px 25px rgba(168,110,220,.45);
        }

        /* SURPRISE */

        #surprise {
            display: none;
            margin-top: 30px;
            animation: appear .8s ease;
        }

        @keyframes appear {
            from {
                opacity: 0;
                transform: translateY(20px) scale(.9);
            }

            to {
                opacity: 1;
                transform: translateY(0) scale(1);
            }
        }

        .gift {
            font-size: 75px;
            animation: shake 1s infinite;
        }

        @keyframes shake {
            0%, 100% {
                transform: rotate(0);
            }

            25% {
                transform: rotate(-8deg);
            }

            75% {
                transform: rotate(8deg);
            }
        }

        .secret {
            background: white;
            padding: 22px;
            border-radius: 25px;
            border: 3px solid #ffd0e3;
        }

        .secret h2 {
            color: #ff5b99;
        }

        /* FOOTER */

        .footer {
            margin-top: 25px;
            color: #9275a3;
            font-size: 14px;
        }

        /* CONFETTI */

        .confetti {
            position: fixed;
            top: -20px;
            font-size: 20px;
            z-index: 10;
            pointer-events: none;
            animation: fall linear forwards;
        }

        @keyframes fall {
            to {
                transform: translateY(110vh) rotate(720deg);
                opacity: 0;
            }
        }

        /* MOBILE */

        @media (max-width: 600px) {
            .card {
                padding: 25px 15px;
            }

            .cat {
                font-size: 90px;
            }

            .message-box p {
                font-size: 16px;
            }

            .balloon {
                font-size: 40px;
            }
        }
    </style>
</head>

<body>

    <!-- FLOATING DECORATIONS -->

    <div class="decor balloon b1">🎈</div>
    <div class="decor balloon b2">🎈</div>

    <div class="decor star s1">✨</div>
    <div class="decor star s2">⭐</div>

    <div class="decor heart h1">💗</div>
    <div class="decor heart h2">💕</div>


    <!-- MAIN CARD -->

    <div class="container">

        <div class="card">

            <div class="ribbon">
                🎀 A SPECIAL DAY 🎀
            </div>

            <div class="cat">
                🐱
            </div>

            <h1>Happy Birthday!</h1>

            <div class="subtitle">
                ✨ Today is all about YOU! ✨
            </div>


            <!-- CAKE -->

            <div class="cake-area">
                <div class="cake">🎂</div>
            </div>


            <!-- MESSAGE -->

            <div class="message-box">

                <p>
                    🎉 <span class="highlight">Happy Birthday!</span> 🎉
                </p>

                <p>
                    I hope your special day is filled with
                    happiness, laughter, love, and beautiful memories.
                    May all your wishes slowly come true. 💗
                </p>

                <p>
                    Keep smiling, keep being yourself,
                    and never forget how special you are. 🐱✨
                </p>

                <p>
                    Enjoy your day because today is
                    <span class="highlight">YOUR DAY!</span> 🎀
                </p>

            </div>


            <!-- BUTTON -->

            <button class="surprise-btn" onclick="openSurprise()">
                🎁 Open Your Birthday Surprise
            </button>


            <!-- SECRET MESSAGE -->

            <div id="surprise">

                <div class="gift">
                    🎁
                </div>

                <div class="secret">

                    <h2>💌 A Little Birthday Message</h2>

                    <p>
                        May this new chapter of your life bring
                        you more happiness, good memories,
                        success, and reasons to smile. 🌷
                    </p>

                    <p>
                        Don't forget to enjoy the little things,
                        chase your dreams, and always believe
                        in yourself. ✨
                    </p>

                    <h2>
                        🐱💗 Happy Birthday! 💗🐱
                    </h2>

                    <p>
                        From someone who prepared this little
                        surprise just for you. 🎀
                    </p>

                </div>

            </div>


            <div class="footer">
                Made with 💗, 🎀 & 🐱
            </div>

        </div>

    </div>


    <script>

        function openSurprise() {

            document.getElementById("surprise").style.display = "block";

            // CONFETTI
            const emojis = ["🎉", "🎀", "💗", "💕", "✨", "⭐", "🐱"];

            for (let i = 0; i < 45; i++) {

                let confetti = document.createElement("div");

                confetti.className = "confetti";

                confetti.innerHTML =
                    emojis[Math.floor(Math.random() * emojis.length)];

                confetti.style.left =
                    Math.random() * 100 + "vw";

                confetti.style.animationDuration =
                    (2 + Math.random() * 3) + "s";

                confetti.style.fontSize =
                    (15 + Math.random() * 20) + "px";

                document.body.appendChild(confetti);

                setTimeout(() => {
                    confetti.remove();
                }, 5000);
            }

            // Scroll to surprise
            setTimeout(() => {
                document.getElementById("surprise")
                    .scrollIntoView({
                        behavior: "smooth"
                    });
            }, 200);
        }

    </script>

</body>
</html>