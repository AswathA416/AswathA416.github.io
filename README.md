<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>PlayFlix Hub</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #0f172a;
      color: white;
    }

    header {
      background: #1e293b;
      padding: 15px;
      text-align: center;
      font-size: 24px;
      font-weight: bold;
    }

    nav {
      display: flex;
      justify-content: center;
      gap: 20px;
      background: #020617;
      padding: 10px;
    }

    nav a {
      color: #38bdf8;
      text-decoration: none;
      font-weight: bold;
    }

    .hero {
      text-align: center;
      padding: 40px;
      background: linear-gradient(135deg, #1e3a8a, #9333ea);
    }

    .hero h1 {
      font-size: 36px;
    }

    .cta {
      margin-top: 20px;
      padding: 12px 25px;
      background: #22c55e;
      border: none;
      color: white;
      font-size: 18px;
      cursor: pointer;
      border-radius: 8px;
    }

    .section {
      padding: 20px;
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 15px;
    }

    .card {
      background: #1e293b;
      padding: 10px;
      border-radius: 10px;
      text-align: center;
      transition: 0.3s;
    }

    .card:hover {
      transform: scale(1.05);
    }

    iframe {
      width: 100%;
      height: 150px;
      border-radius: 8px;
    }

    footer {
      text-align: center;
      padding: 15px;
      background: #020617;
      margin-top: 20px;
    }
  </style>
</head>

<body>

<header>🎮 PlayFlix Hub</header>

<nav>
  <a href="#games">Games</a>
  <a href="#movies">Movies</a>
</nav>

<div class="hero">
  <h1>Play 50+ Games Instantly</h1>
  <p>No downloads. No waiting. Just fun.</p>
  <button class="cta">Start Playing</button>
</div>

<div class="section" id="games">
  <h2>🔥 Trending Games</h2>
  <div class="grid">

    <!-- Example games (embed more to reach 50+) -->
    <div class="card">
      <h3>Game 1</h3>
      <iframe src="https://example.com"></iframe>
    </div>

    <div class="card">
      <h3>Game 2</h3>
      <iframe src="https://example.com"></iframe>
    </div>

    <div class="card">
      <h3>Game 3</h3>
      <iframe src="https://example.com"></iframe>
    </div>

  </div>
</div>

<div class="section" id="movies">
  <h2>🎬 Watch Movies (Legal Sources)</h2>
  <div class="grid">

    <div class="card">
      <h3>Sample Movie</h3>
      <iframe src="https://archive.org/embed/sample"></iframe>
    </div>

  </div>
</div>

<footer>
  © 2026 PlayFlix Hub
</footer>

</body>
</html>
