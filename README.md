<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Para mi cachito de luz 💖</title>

  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: linear-gradient(135deg, #ffb6c1, #ffe4e1);
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      text-align: center;
      overflow: hidden;
    }

    .card {
      background: rgba(255, 255, 255, 0.92);
      padding: 40px;
      border-radius: 22px;
      box-shadow: 0px 10px 25px rgba(0, 0, 0, 0.25);
      max-width: 450px;
      z-index: 2;
    }

    h1 {
      color: #ff1493;
      font-size: 30px;
      margin-bottom: 15px;
    }

    p {
      font-size: 20px;
      color: #444;
      margin-bottom: 25px;
    }

    button {
      font-size: 18px;
      padding: 12px 22px;
      margin: 10px;
      border: none;
      border-radius: 12px;
      cursor: pointer;
      transition: 0.3s;
    }

    .yes {
      background-color: #ff1493;
      color: white;
    }

    .yes:hover {
      background-color: #ff69b4;
      transform: scale(1.1);
    }

    .no {
      background-color: #ddd;
      color: #444;
    }

    .no:hover {
      background-color: #bbb;
      transform: scale(1.1);
    }

    #response {
      margin-top: 20px;
      font-size: 18px;
      font-weight: bold;
      color: #ff1493;
    }

    .hearts {
      position: absolute;
      width: 100%;
      height: 100%;
      overflow: hidden;
      top: 0;
      left: 0;
      z-index: 1;
    }

    .heart {
      position: absolute;
      font-size: 24px;
      animation: float 6s infinite ease-in-out;
      opacity: 0.8;
    }

    @keyframes float {
      0% {
        transform: translateY(100vh) scale(0.5);
        opacity: 0;
      }
      50% {
        opacity: 1;
      }
      100% {
        transform: translateY(-10vh) scale(1.2);
        opacity: 0;
      }
    }
  </style>
</head>

<body>

  <!-- Música romántica -->
  <audio autoplay loop>
    <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
    Tu navegador no soporta audio.
  </audio>

  <div class="hearts"></div>

  <div class="card">
    <h1>💖 Cachito de luz 💖</h1>

    <p>
      ¿Quieres ser mi novia, mi cachito de luz? 🥺✨
    </p>

    <button class="yes" onclick="yesAnswer()">Sí 💕</button>
    <button class="no" onclick="noAnswer()">No 😢</button>

    <div id="response"></div>

    <p style="margin-top: 25px; font-size: 16px; color:#444;">
      Con cariño: <b>Carlos Raúl</b> 💖
    </p>
  </div>

  <script>
    function yesAnswer() {
      document.getElementById("response").innerHTML =
        "😍💖 ¡Sabía que dirías que sí! Te amo muchísimo 💕✨";
    }

    function noAnswer() {
      document.getElementById("response").innerHTML =
        "😢 Está bien... pero igual eres mi cachito de luz 💖";
    }

    // Corazones flotando
    const heartsContainer = document.querySelector(".hearts");

    function createHeart() {
      const heart = document.createElement("div");
      heart.classList.add("heart");
      heart.innerHTML = "💖";

      heart.style.left = Math.random() * 100 + "vw";
      heart.style.animationDuration = (Math.random() * 3 + 3) + "s";
      heart.style.fontSize = (Math.random() * 20 + 15) + "px";

      heartsContainer.appendChild(heart);

      setTimeout(() => {
        heart.remove();
      }, 6000);
    }

    setInterval(createHeart, 400);
  </script>

</body>
</html>
