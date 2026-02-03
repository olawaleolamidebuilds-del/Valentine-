<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>For Iyaniwuraolami ❤️</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #ffeef2;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            overflow: hidden;
            text-align: center;
        }

        .container {
            background: rgba(255, 255, 255, 0.9);
            padding: 2rem;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            z-index: 10;
        }

        h1 { color: #d63384; font-size: 2rem; }
        p { color: #555; font-size: 1.2rem; }

        .buttons {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 30px;
            position: relative;
        }

        button {
            padding: 12px 25px;
            font-size: 1.1rem;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            transition: 0.3s;
            font-weight: bold;
        }

        #yesBtn { background-color: #ff4d6d; color: white; }
        #noBtn { background-color: #adb5bd; color: white; position: absolute; left: 160px;}

        .hidden { display: none; }
        
        .celebration h1 { color: #ff4d6d; font-size: 3rem; animation: heartbeat 1.2s infinite; }
        
        @keyframes heartbeat {
            0% { transform: scale(1); }
            50% { transform: scale(1.1); }
            100% { transform: scale(1); }
        }
    </style>
</head>
<body>

    <div class="container" id="mainContainer">
        <h1>Hi Iyaniwuraolami... ❤️</h1>
        <p>You make every day feel like 2026 already. <br> Will you be my Valentine?</p>
        
        <div class="buttons">
            <button id="yesBtn">YES!</button>
            <button id="noBtn">No</button>
        </div>
    </div>

    <div class="container hidden" id="successContainer">
        <div class="celebration">
            <h1>YAY! ❤️🌹</h1>
            <p>I knew you'd say yes, Iyaniwuraolami! <br> Best Valentine's ever!</p>
        </div>
    </div>

    <script>
        const noBtn = document.getElementById('noBtn');
        const yesBtn = document.getElementById('yesBtn');
        const mainContainer = document.getElementById('mainContainer');
        const successContainer = document.getElementById('successContainer');

        let yesSize = 1;

        // The "Runaway" No Button
        noBtn.addEventListener('mouseover', moveButton);
        noBtn.addEventListener('touchstart', moveButton);

        function moveButton() {
            const x = Math.random() * (window.innerWidth - noBtn.offsetWidth);
            const y = Math.random() * (window.innerHeight - noBtn.offsetHeight);
            
            noBtn.style.position = 'fixed';
            noBtn.style.left = x + 'px';
            noBtn.style.top = y + 'px';

            // Make the "Yes" button grow every time she tries to hit No!
            yesSize += 0.2;
            yesBtn.style.transform = `scale(${yesSize})`;
        }

        // The Success Action
        yesBtn.addEventListener('click', () => {
            mainContainer.classList.add('hidden');
            successContainer.classList.remove('hidden');
            noBtn.classList.add('hidden');
        });
    </script>
</body>
</html>
