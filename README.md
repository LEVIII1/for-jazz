<!DOCTYPE html>
<!-- saved from url=https://https://github.com/LEVIII1/for jazzzzzz/-->
<html><head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
    <title>Pinkkk</title>
    <link href="./for jazzzzzz_files/css2" rel="stylesheet">
    <style>
        :root {
            --color-env: #FFB7C5;
            --color-env2: #ff9aad;
            --color-flap: #ff8da1;
            --color-bg: #ed7fca;
            --color-heart: #ff85a2;
            --color-sparkle: #fff;
            --wax-red: #c04040;
        }

        #envelope {
            position: relative;
            width: 280px;
            height: 180px;
            border-bottom-left-radius: 6px;
            border-bottom-right-radius: 6px;
            margin: 0 auto;
            top: 150px;
            background-color: var(--color-flap);
            box-shadow: 0 4px 20px rgba(0,0,0,.1);
            cursor: pointer;
        }

        .front {
            position: absolute;
            width: 0;
            height: 0;
            z-index: 3;
        }

        .flap {
            border-left: 140px solid transparent;
            border-right: 140px solid transparent;
            border-bottom: 82px solid transparent;
            border-top: 98px solid var(--color-flap);
            transform-origin: top;
            pointer-events: none;
        }

        .pocket {
            border-left: 140px solid var(--color-env);
            border-right: 140px solid var(--color-env);
            border-bottom: 90px solid var(--color-env2);
            border-top: 90px solid transparent;
            border-bottom-left-radius: 6px;
            border-bottom-right-radius: 6px;
        }

        .letter {
            position: relative;
            background-color: #e0d9dd;
            width: 90%;
            margin: 0 auto;
            height: 90%;
            top: 5%;
            border-radius: 6px;
            box-shadow: 0 2px 26px rgba(0,0,0,.08);
            padding: 15px;
            box-sizing: border-box;
        }

        .letter:after {
            content: '';
            position: absolute;
            top: 0;
            bottom: 0;
            left: 0;
            right: 0;
            background-image: linear-gradient(180deg, 
                rgba(255,255,255,0.00) 25%, 
                rgba(255,231,236,0.70) 55%, 
                rgba(255,231,236,1.00) 100%);
        }

        .message {
            position: relative;
            z-index: 2;
            font-family: 'Handlee', cursive;
            color: #d46a84;
            text-align: center;
            line-height: 1;
            padding-top: 0px;
        }

        .message p {
            margin: 10px 0;
            font-size: 1.8em;
            text-shadow: 0 2px 3px rgba(0,0,0,0.1);
        }

        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }

        .envlope-wrapper {
            height: 380px;
            margin-top: 50px;
            animation: float 3s ease-in-out infinite;
        }

        .open .flap {
            transform: rotateX(180deg);
            transition: transform 0.4s ease, z-index 0.6s;
            z-index: 1;
        }

        .close .flap {
            transform: rotateX(0deg);
            transition: transform 0.4s 0.6s ease, z-index 1s;
            z-index: 5;
        }

        .close .letter {
            transform: translateY(0px); 
            transition: transform 0.4s ease, z-index 1s;
            z-index: 1;
        }

        .open .letter {
            transform: translateY(-60px) rotate(-2deg);
            transition: transform 0.4s 0.6s ease, z-index 0.6s;
            z-index: 2;
        }

        

        .letter-corner {
            position: absolute;
            width: 20px;
            height: 20px;
            border: 2px solid #ffd1dc;
            border-radius: 5px;
            z-index: 3;
        }
        .corner-tl { top: 10px; left: 10px; border-right: none; border-bottom: none; }
        .corner-br { bottom: 10px; right: 10px; border-left: none; border-top: none; }

        .hearts, .sparkles {
            position: absolute;
            top: 90px;
            left: 0;
            right: 0;
            z-index: 2;
        }

        .heart, .sparkle {
            position: absolute;
            bottom: 0;
            pointer-events: none;
        }

        .heart:before,
        .heart:after {
            content: "";
            position: absolute;
            left: 25px;
            top: 0;
            width: 25px;
            height: 40px;
            background: var(--color-heart);
            border-radius: 25px 25px 0 0;
            transform: rotate(-45deg);
            transform-origin: 0 100%;
        }

        .heart:after {
            left: 0;
            transform: rotate(45deg);
            transform-origin: 100% 100%;
        }

        .sparkle {
            width: 8px;
            height: 8px;
            background: var(--color-sparkle);
            border-radius: 50%;
            animation: sparkleTwinkle 1s infinite;
        }

        .close .heart,
        .close .sparkle {
            opacity: 0;
            animation: none;
        }

        .a1 { left: 20%; transform: scale(0.6); animation: slideUp 4s linear infinite, sideSway 2s ease-in-out infinite alternate; }
        .a2 { left: 55%; animation: slideUp 5s linear infinite, sideSway 4s ease-in-out infinite alternate; }
        .a3 { left: 10%; transform: scale(0.8); animation: slideUp 7s linear infinite, sideSway 2s ease-in-out infinite alternate; }

        .s1 { left: 30%; animation: sparkleUp 3s linear infinite; }
        .s2 { left: 60%; animation: sparkleUp 4s linear infinite; }
        .s3 { left: 45%; animation: sparkleUp 5s linear infinite; }

        @keyframes slideUp {
            0% { top: 0; }
            100% { top: -600px; }
        }

        @keyframes sideSway {
            0% { margin-left: 0; }
            50% { margin-left: 50px; }
            100% { margin-left: 0; }
        }

        @keyframes sparkleUp {
            0% { transform: translateY(0); opacity: 1; }
            100% { transform: translateY(-500px) rotate(360deg); opacity: 0; }
        }

        @keyframes sparkleTwinkle {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.5); }
        }

        body {
            background-color: var(--color-bg);
            margin: 0;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .reset {
            text-align: center;
            margin-top: 50px;
        }

        .reset button {
            font-weight: 600;
            transition: all 0.3s ease;
            background-color: var(--color-env);
            border: 2px solid var(--color-env2);
            border-radius: 20px;
            color: white;
            padding: 12px 25px;
            margin: 10px;
            font-size: 16px;
            cursor: pointer;
            box-shadow: 0 5px 20px rgba(0,0,0,0.15);
            font-family: Arial, sans-serif;
        }

        .reset button:hover {
            background-color: var(--color-env2);
            transform: translateY(-3px) scale(1.05);
            box-shadow: 0 7px 25px rgba(0,0,0,0.2);
        }
    </style>
</head>
<body>
    <div class="envlope-wrapper">
        <div id="envelope" class="open">
            <div class="wax-seal"></div>
            <div class="front flap"></div>
            <div class="front pocket"></div>
            <div class="letter">
                <div class="letter-corner corner-tl"></div>
                <div class="letter-corner corner-br"></div>
                <div class="message">
                    <p>happy valentines day boss!!!</p>
                    <p>hihi</p>
                </div>
            </div>
            <div class="hearts">
                <div class="heart a1"></div>
                <div class="heart a2"></div>
                <div class="heart a3"></div>
            </div>
            <div class="sparkles">
                <div class="sparkle s1"></div>
                <div class="sparkle s2"></div>
                <div class="sparkle s3"></div>
            </div>
        </div>
    </div>
    <div class="reset">
        <button id="open">Open Envelope</button>
        <button id="reset">Close Envelope</button>
    </div>

    <script src="./for jazzzzzz_files/jquery-3.6.0.min.js.download"></script>
    <script>
        $(document).ready(function() {
            const envelope = $('#envelope');
            const btnOpen = $("#open");
            const btnReset = $("#reset");

            envelope.on('click', open);
            btnOpen.on('click', open);
            btnReset.on('click', close);

            function open() {
                envelope.removeClass("close").addClass("open");
            }

            function close() {
                envelope.removeClass("open").addClass("close");
            }
        });
    </script>

</body></html>
