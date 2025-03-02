<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Game Klik</title>
    <style>
        body {
            text-align: center;
            font-family: Arial, sans-serif;
        }
        #gameArea {
            width: 200px;
            height: 200px;
            background-color: red;
            margin: 50px auto;
            display: flex;
            justify-content: center;
            align-items: center;
            color: white;
            font-size: 24px;
            font-weight: bold;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <h1>Game Klik</h1>
    <p>Skor: <span id="score">0</span></p>
    <div id="gameArea" onclick="increaseScore()">Klik Saya!</div>
    
    <script>
        let score = 0;
        function increaseScore() {
            score++;
            document.getElementById("score").innerText = score;
            let gameArea = document.getElementById("gameArea");
            gameArea.style.backgroundColor = getRandomColor();
        }
        function getRandomColor() {
            let letters = '0123456789ABCDEF';
            let color = '#';
            for (let i = 0; i < 6; i++) {
                color += letters[Math.floor(Math.random() * 16)];
            }
            return color;
        }
    </script>
</body>
</html>
