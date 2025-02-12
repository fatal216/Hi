<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Halia, Be My Valentine? 💜</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Pacifico&display=swap');

        body {
            text-align: center;
            font-family: 'Pacifico', cursive;
            background-color: #ffebf7;
        }
        .container {
            margin-top: 50px;
            background: white;
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 0 15px rgba(255, 0, 128, 0.3);
            display: inline-block;
            position: relative;
            border: 5px solid transparent;
            animation: glowing-border 2s infinite alternate;
        }
        @keyframes glowing-border {
            0% { border-color: #ff66b2; }
            100% { border-color: #b266ff; }
        }
        h1 {
            color: #ff4d4d;
            font-size: 30px;
        }
        .hearts {
            font-size: 50px;
            animation: heartbeat 1s infinite alternate;
        }
        @keyframes heartbeat {
            from { transform: scale(1); }
            to { transform: scale(1.2); }
        }
        .btn {
            padding: 12px 25px;
            font-size: 18px;
            border: none;
            cursor: pointer;
            border-radius: 8px;
            margin: 10px;
            transition: 0.3s;
            font-family: 'Arial', sans-serif;
        }
        .yes {
            background-color: #4CAF50;
            color: white;
            font-weight: bold;
        }
        .no {
            background-color: #DC3545;
            color: white;
            position: absolute;
            font-weight: bold;
        }
        .message {
            display: none;
            color: #b266ff;
            font-size: 20px;
            margin-top: 15px;
            transition: opacity 0.5s;
        }
    </style>
</head>
<body>

    <div class="container">
        <div class="hearts">💜🧸💜</div>
        <h1>Halia, will you be my Valentine? 💜</h1>
        <button class="btn yes" onclick="accept()">Yes</button>
        <button class="btn no" onmouseover="moveButton()" onclick="showMessage()">No</button>
        
        <p id="message1" class="message">Pls don't break my heart like that 💔</p>
        <p id="message2" class="message">Pweaseeee Haliaaa 🥺💜</p>
        <p id="message3" class="message">Pweaseeee gala tayo 🥺💜</p>
        <p id="message4" class="message">Pweasee mwah 😘💜</p>
        <p id="message5" class="message">Once a year lang toh 😔💜</p>
        <p id="message6" class="message">Pweaseee kahit saglit lang 🥺💜</p>
        <p id="message7" class="message">Isipin mo yung memories natin 🥰💜</p>
        <p id="message8" class="message">Pweasee last na toh 😭💜</p>
    </div>

    <script>
        let noClickCount = 0;

        function accept() {
            alert("Yay! Can't wait for our Valentine’s day! 💜");
        }

        function moveButton() {
            let button = document.querySelector(".no");
            let x = Math.random() * (window.innerWidth - 100);
            let y = Math.random() * (window.innerHeight - 100);
            button.style.left = `${x}px`;
            button.style.top = `${y}px`;
        }

        function showMessage() {
            noClickCount++;
            let messages = [
                "message1",
                "message2",
                "message3",
                "message4",
                "message5",
                "message6",
                "message7",
                "message8"
            ];
            if (noClickCount <= messages.length) {
                document.getElementById(messages[noClickCount - 1]).style.display = "block";
            }
        }
    </script>

</body>
</html>
