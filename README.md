<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>StudyFlow</title>

<style>
body {
  margin: 0;
  font-family: Arial;
  background: #0f172a;
  color: white;
  text-align: center;
}

header {
  background: #020617;
  padding: 15px;
  font-size: 24px;
  font-weight: bold;
}

.hero {
  padding: 30px;
  background: linear-gradient(135deg,#2563eb,#9333ea);
}

.container {
  padding: 20px;
}

button {
  padding: 12px 20px;
  margin: 5px;
  border: none;
  background: #22c55e;
  color: white;
  border-radius: 8px;
  cursor: pointer;
}

.timer {
  font-size: 48px;
  margin: 20px;
}

textarea {
  width: 80%;
  height: 150px;
  border-radius: 10px;
  padding: 10px;
  border: none;
}

.stats {
  margin-top: 20px;
}

</style>
</head>

<body>

<header>📚 StudyFlow</header>

<div class="hero">
  <h1>Stay Focused. Study Smarter.</h1>
  <p>Boost your productivity with proven tools.</p>
</div>

<div class="container">

<h2>⏱️ Pomodoro Timer</h2>
<div class="timer" id="timer">25:00</div>

<button onclick="startTimer()">Start</button>
<button onclick="resetTimer()">Reset</button>

<h2>📝 Notes</h2>
<textarea id="notes" placeholder="Write your notes here..."></textarea>

<div class="stats">
<h3>🔥 Sessions Completed: <span id="sessions">0</span></h3>
</div>

</div>

<script>
let time = 1500;
let timerRunning = false;
let interval;
let sessions = localStorage.getItem("sessions") || 0;

document.getElementById("sessions").innerText = sessions;

function startTimer() {
  if (timerRunning) return;
  timerRunning = true;

  interval = setInterval(() => {
    time--;
    updateDisplay();

    if (time <= 0) {
      clearInterval(interval);
      timerRunning = false;
      sessions++;
      localStorage.setItem("sessions", sessions);
      document.getElementById("sessions").innerText = sessions;
      alert("Session complete! Take a break.");
      time = 1500;
    }
  }, 1000);
}

function resetTimer() {
  clearInterval(interval);
  time = 1500;
  timerRunning = false;
  updateDisplay();
}

function updateDisplay() {
  let minutes = Math.floor(time / 60);
  let seconds = time % 60;
  document.getElementById("timer").innerText =
    minutes + ":" + (seconds < 10 ? "0" : "") + seconds;
}

// Auto-save notes
let notes = document.getElementById("notes");
notes.value = localStorage.getItem("notes") || "";

notes.addEventListener("input", () => {
  localStorage.setItem("notes", notes.value);
});
</script>

</body>
</html>
