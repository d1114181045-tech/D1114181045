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
