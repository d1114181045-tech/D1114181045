# D1114181045
<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <title>打地鼠遊戲</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

<h1>🎯 打地鼠遊戲</h1>
<p>分數：<span id="score">0</span></p>
<button onclick="startGame()">開始遊戲</button>

<div id="game">
    <div class="hole" onclick="hit(this)"></div>
    <div class="hole" onclick="hit(this)"></div>
    <div class="hole" onclick="hit(this)"></div>
    <div class="hole" onclick="hit(this)"></div>
    <div class="hole" onclick="hit(this)"></div>
    <div class="hole" onclick="hit(this)"></div>
</div>

<script src="script.js"></script>
</body>
</html>

body {
    text-align: center;
    font-family: Arial;
}

#game {
    width: 300px;
    margin: auto;
    display: grid;
    grid-template-columns: repeat(3, 100px);
    gap: 10px;
}

.hole {
    width: 100px;
    height: 100px;
    background-color: brown;
    border-radius: 50%;
    cursor: pointer;
}

let score = 0;
let gameInterval;

function startGame() {
    score = 0;
    document.getElementById("score").innerText = score;

    gameInterval = setInterval(() => {
        let holes = document.querySelectorAll(".hole");
        holes.forEach(h => h.classList.remove("active"));

        let randomHole = holes[Math.floor(Math.random() * holes.length)];
        randomHole.classList.add("active");
    }, 800);
}

function hit(element) {
    if (element.classList.contains("active")) {
        score++;
        document.getElementById("score").innerText = score;
        element.classList.remove("active");
    }
}
.active {
    background-color: green;
}
