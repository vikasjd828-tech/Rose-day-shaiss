# Rose-day-shaiss
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Happy Rose Day Shai ❤️</title>

<style>
body {
  margin: 0;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  font-family: 'Segoe UI', sans-serif;
  background: linear-gradient(135deg, #ffd1dc, #ff9a9e);
  overflow: hidden;
}

/* Card */
.card {
  background: rgba(255,255,255,0.9);
  padding: 30px;
  border-radius: 20px;
  text-align: center;
  box-shadow: 0 10px 30px rgba(0,0,0,0.2);
  max-width: 320px;
  z-index: 2;
  animation: pop 1s ease;
}

h1 {
  color: #ff2e63;
}

p {
  color: #444;
  font-size: 16px;
}

.rose {
  font-size: 60px;
  animation: float 2s infinite ease-in-out;
}

/* Floating animation */
@keyframes float {
  0%,100% { transform: translateY(0); }
  50% { transform: translateY(-10px); }
}

@keyframes pop {
  0% { transform: scale(0.8); opacity: 0; }
  100% { transform: scale(1); opacity: 1; }
}

/* Hearts */
.heart {
  position: absolute;
  font-size: 20px;
  animation: hearts 6s linear infinite;
  color: red;
}

@keyframes hearts {
  0% {
    transform: translateY(100vh);
    opacity: 1;
  }
  100% {
    transform: translateY(-10vh);
    opacity: 0;
  }
}

/* Petals */
.petal {
  position: absolute;
  font-size: 22px;
  animation: petals 8s linear infinite;
}

@keyframes petals {
  0% {
    transform: translateY(-10vh) rotate(0deg);
  }
  100% {
    transform: translateY(110vh) rotate(360deg);
  }
}
</style>
</head>

<body>

<div class="card">
  <div class="rose">🌹</div>
  <h1>Happy Rose Day Shai ❤️</h1>
  <p>
    My Dear Shai 💖<br><br>
    Like this beautiful rose,<br>
    you fill my life with love,<br>
    happiness and sweetness 🌸<br><br>
    You make my world brighter every day 😘
  </p>
  <p><strong>— Yours Forever 💕</strong></p>
</div>

<!-- Hearts -->
<script>
function createHeart() {
  const heart = document.createElement("div");
  heart.classList.add("heart");
  heart.innerHTML = "❤️";
  heart.style.left = Math.random() * 100 + "vw";
  heart.style.animationDuration = (3 + Math.random() * 3) + "s";
  document.body.appendChild(heart);

  setTimeout(() => {
    heart.remove();
  }, 6000);
}
setInterval(createHeart, 500);

/* Petals */
function createPetal() {
  const petal = document.createElement("div");
  petal.classList.add("petal");
  petal.innerHTML = "🌸";
  petal.style.left = Math.random() * 100 + "vw";
  petal.style.animationDuration = (5 + Math.random() * 5) + "s";
  document.body.appendChild(petal);

  setTimeout(() => {
    petal.remove();
  }, 8000);
}
setInterval(createPetal, 700);
</script>

</body>
</html>
