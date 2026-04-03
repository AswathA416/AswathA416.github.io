<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>@drippyfr</title>

<style>
body {
  margin: 0;
  font-family: Arial, sans-serif;
  color: white;
  background: black;
  overflow-x: hidden;
}

/* 🌌 Animated stars */
body::before {
  content: "";
  position: fixed;
  width: 200%;
  height: 200%;
  background: url("https://www.transparenttextures.com/patterns/stardust.png");
  animation: moveStars 60s linear infinite;
  z-index: -1;
}

@keyframes moveStars {
  from { transform: translate(0,0); }
  to { transform: translate(-500px,-500px); }
}

header {
  text-align: center;
  padding: 20px;
  font-size: 28px;
  font-weight: bold;
  background: rgba(0,0,0,0.6);
  backdrop-filter: blur(10px);
}

/* Navigation */
nav {
  display: flex;
  justify-content: center;
  gap: 15px;
  padding: 15px;
}

button {
  padding: 10px 20px;
  border: none;
  border-radius: 20px;
  background: linear-gradient(45deg,#3b82f6,#9333ea);
  color: white;
  cursor: pointer;
  transition: 0.3s;
}

button:hover {
  transform: scale(1.1);
}

/* Sections */
.section {
  display: none;
  padding: 40px;
  text-align: center;
}

.active {
  display: block;
}

/* Cards */
.card {
  background: rgba(255,255,255,0.1);
  padding: 20px;
  margin: 10px;
  border-radius: 15px;
  backdrop-filter: blur(10px);
}
</style>
</head>

<body>

<header>🌌 @drippyfr</header>

<nav>
  <button onclick="showSection('home')">Home</button>
  <button onclick="showSection('games')">Games</button>
  <button onclick="showSection('about')">About Me</button>
  <button onclick="showSection('other')">Other</button>
</nav>

<!-- HOME -->
<div id="home" class="section active">
  <h1>Welcome to My Space 🚀</h1>
  <p>This is my personal galaxy on the internet.</p>
</div>

<!-- GAMES -->
<div id="games" class="section">
  <h1>🎮 Games</h1>

  <div class="card">
    <h3>Snake</h3>
    <iframe src="https://playsnake.org/" width="300" height="200"></iframe>
  </div>

  <div class="card">
    <h3>2048</h3>
    <iframe src="https://play2048.co/" width="300" height="200"></iframe>
  </div>

</div>

<!-- ABOUT -->
<div id="about" class="section">
  <h1>👤 About Me</h1>
  <p>Hey, I'm @drippyfr 🚀</p>
  <p>I like games, coding, and building cool stuff.</p>
</div>

<!-- OTHER -->
<div id="other" class="section">
  <h1>✨ Other</h1>
  <p>More content coming soon...</p>
</div>

<script>
function showSection(sectionId) {
  let sections = document.querySelectorAll(".section");
  sections.forEach(sec => sec.classList.remove("active"));

  document.getElementById(sectionId).classList.add("active");
}
</script>

</body>
</html>
