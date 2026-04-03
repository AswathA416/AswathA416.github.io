<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>PlayAchu Hub</title>

<style>
body {
  margin: 0;
  font-family: Arial;
  background: #0f172a;
  color: white;
}

header {
  background: #020617;
  padding: 15px;
  text-align: center;
  font-size: 24px;
  font-weight: bold;
}

.hero {
  text-align: center;
  padding: 40px;
  background: linear-gradient(135deg,#2563eb,#9333ea);
}

button {
  padding: 12px 20px;
  border: none;
  background: #22c55e;
  color: white;
  font-size: 16px;
  border-radius: 8px;
  cursor: pointer;
}

.section {
  padding: 20px;
}

.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit,minmax(220px,1fr));
  gap: 15px;
}

.card {
  background: #1e293b;
  padding: 10px;
  border-radius: 10px;
  text-align: center;
}

iframe {
  width: 100%;
  height: 160px;
  border-radius: 8px;
}

.search {
  text-align: center;
  margin: 20px;
}

input {
  padding: 10px;
  width: 60%;
  border-radius: 8px;
  border: none;
}

footer {
  text-align: center;
  padding: 15px;
  background: #020617;
}
</style>
</head>

<body>

<header>🎮 PlayFlix Hub</header>

<div class="hero">
  <h1>Play Games & Watch Movies</h1>
  <p>Instant entertainment. No downloads.</p>
  <button onclick="scrollToGames()">Start Playing</button>
</div>

<div class="search">
  <input type="text" id="search" placeholder="Search games..." onkeyup="filterGames()">
</div>

<div class="section" id="games">
<h2>🎮 Games</h2>

<div class="grid" id="gameList">

<div class="card" data-name="tetris">
<h3>Tetris</h3>
<iframe src="https://tetris.com/play-tetris"></iframe>
</div>

<div class="card" data-name="pacman">
<h3>Pacman</h3>
<iframe src="https://www.retrogames.cc/embed/13632-pac-man.html"></iframe>
</div>

<div class="card" data-name="snake">
<h3>Snake</h3>
<iframe src="https://playsnake.org/"></iframe>
</div>

<div class="card" data-name="chess">
<h3>Chess</h3>
<iframe src="https://www.chess.com/play/computer"></iframe>
</div>

<div class="card" data-name="2048">
<h3>2048</h3>
<iframe src="https://play2048.co/"></iframe>
</div>

</div>
</div>

<div class="section">
<h2>🎬 Free Movies</h2>

<div class="grid">

<div class="card">
<h3>Classic Movie</h3>
<iframe src="https://archive.org/embed/night_of_the_living_dead"></iframe>
</div>

<div class="card">
<h3>Another Movie</h3>
<iframe src="https://archive.org/embed/HisGirlFriday"></iframe>
</div>

</div>
</div>

<footer>
© 2026 PlayFlix Hub
</footer>

<script>
function scrollToGames() {
  document.getElementById("games").scrollIntoView({behavior:"smooth"});
}

function filterGames() {
  let input = document.getElementById("search").value.toLowerCase();
  let games = document.querySelectorAll(".card");

  games.forEach(game => {
    let name = game.getAttribute("data-name");
    game.style.display = name.includes(input) ? "block" : "none";
  });
}
</script>

</body>
</html>
