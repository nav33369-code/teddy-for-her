<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>For You ❤️</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <style>
    body {
      margin: 0;
      height: 100vh;
      background: linear-gradient(180deg, #ffd6e8, #fff0f6);
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      font-family: 'Comic Sans MS', 'Segoe UI', sans-serif;
      overflow: hidden;
    }

    h1 {
      color: #ff4d88;
      margin-bottom: 10px;
      text-align: center;
    }

    p {
      color: #ff6fa5;
      font-size: 1.2em;
      text-align: center;
      max-width: 300px;
    }

    .teddy {
      font-size: 120px;
      animation: bounce 2s infinite;
      cursor: pointer;
      user-select: none;
    }

    @keyframes bounce {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-20px); }
    }

    .heart {
      position: absolute;
      color: #ff4d88;
      font-size: 20px;
      animation: float 4s linear forwards;
      pointer-events: none;
    }

    @keyframes float {
      0% {
        opacity: 1;
        transform: translateY(0) scale(1);
      }
      100% {
        opacity: 0;
        transform: translateY(-200px) scale(1.5);
      }
    }

    .hint {
      margin-top: 10px;
      font-size: 0.9em;
      color: #ff8fb8;
    }
  </style>
</head>
<body>

  <h1>For My Favorite Person ❤️</h1>
  <p>You make my days warmer, brighter, and happier.</p>

  <div class="teddy" onclick="showLove()">🧸</div>

  <div class="hint">(Tap the teddy)</div>

  <script>
    function showLove() {
      for (let i = 0; i < 8; i++) {
        const heart = document.createElement("div");
        heart.className = "heart";
        heart.innerHTML = "❤️";
        heart.style.left = Math.random() * window.innerWidth + "px";
        heart.style.bottom = "100px";
        heart.style.fontSize = (20 + Math.random() * 20) + "px";
        document.body.appendChild(heart);

        setTimeout(() => {
          heart.remove();
        }, 4000);
      }
    }
  </script>

</body>
</html>
