# Index.html
Valentine 
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>For Akshaya 💖</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
body {
  margin: 0;
  font-family: 'Segoe UI', sans-serif;
  height: 100vh;
  background: linear-gradient(135deg, #ffe6eb, #fff);
  overflow: hidden;
}

.flowers span {
  position: absolute;
  font-size: 26px;
  animation: float 10s linear infinite;
  opacity: 0.7;
}

@keyframes float {
  0% { transform: translateY(100vh); }
  100% { transform: translateY(-10vh); }
}

.card {
  background: white;
  max-width: 420px;
  padding: 25px;
  border-radius: 20px;
  text-align: center;
  margin: auto;
  position: relative;
  top: 50%;
  transform: translateY(-50%);
  box-shadow: 0 20px 40px rgba(0,0,0,0.15);
}

h1 { color: #e63946; }
p { color: #555; }

button {
  padding: 10px 18px;
  border-radius: 20px;
  border: none;
  font-size: 15px;
  cursor: pointer;
}

.yes { background: #e63946; color: white; }
.no { background: #ccc; position: absolute; }

.options button {
  display: block;
  width: 100%;
  margin: 8px 0;
  background: #f1f1f1;
}

.angry {
  font-size: 30px;
  margin-top: 10px;
}
</style>
</head>

<body>

<!-- Flowers -->
<div class="flowers">
  <span style="left:10%">🤍🌹</span>
  <span style="left:30%">🤍🌸</span>
  <span style="left:50%">🤍🌹</span>
  <span style="left:70%">🤍🌸</span>
  <span style="left:90%">🤍🌹</span>
</div>

<div class="card" id="card">
  <h1>Hey Akshaya 💖</h1>
  <p>
    From <b>Pranav</b><br><br>
    You make my world softer, brighter, and happier.
  </p>

  <h2>Will you be my Valentine? 💘</h2>

  <button class="yes" onclick="startQuiz()">Yes 💖</button>
  <button class="no" id="noBtn">No 🙈</button>
</div>

<script>
const noBtn = document.getElementById("noBtn");

noBtn.addEventListener("mouseover", () => {
  noBtn.style.left = Math.random() * 250 + "px";
  noBtn.style.top = Math.random() * 250 + "px";
});

function startQuiz() {
  document.getElementById("card").innerHTML = `
    <h2>Okayy 💕 One small test 😌</h2>
    <p>When did I propose you?</p>
    <div class="options">
      <button onclick="wrong()">14 Feb</button>
      <button onclick="correct(1)">20 July</button>
      <button onclick="wrong()">1 Jan</button>
      <button onclick="wrong()">5 August</button>
    </div>
    <div id="reaction"></div>
  `;
}

function correct(step) {
  if (step === 1) {
    document.getElementById("card").innerHTML = `
      <h2>Good girl 😌💗</h2>
      <p>What was the first gift I gave you?</p>
      <div class="options">
        <button onclick="wrong()">Chocolate</button>
        <button onclick="wrong()">Teddy</button>
        <button onclick="correct(2)">Flowers</button>
        <button onclick="wrong()">Ring</button>
      </div>
      <div id="reaction"></div>
    `;
  } else if (step === 2) {
    document.getElementById("card").innerHTML = `
      <h2>Almost there 💞</h2>
      <p>What’s my favourite thing?</p>
      <div class="options">
        <button onclick="wrong()">Gym</button>
        <button onclick="wrong()">Food</button>
        <button onclick="correct(3)">Spending time with you</button>
        <button onclick="wrong()">Sleeping</button>
      </div>
      <div id="reaction"></div>
    `;
  } else {
    document.getElementById("card").innerHTML = `
      <h1>YAYYY 🥹❤️</h1>
      <p>
        Of course it’s you, always you.<br><br>
        Happy Valentine’s Day, Akshaya 💐<br>
        Love,<br><b>Pranav</b>
      </p>
      <div style="font-size:40px;">🤍🌹🤍🌸🤍</div>
    `;
  }
}

function wrong() {
  document.getElementById("reaction").innerHTML = `
    <div class="angry">😠</div>
    <p>Think again 😤</p>
  `;
}
</script>

</body>
</html>
