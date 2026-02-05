# Valentine-<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Happy Valentine 💖</title>
<style>
  body {
    background: linear-gradient(135deg, #ff4d6d, #ff8fa3);
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    overflow: hidden;
    font-family: 'Poppins', sans-serif;
  }

  h1 {
    color: white;
    font-size: 3rem;
    text-align: center;
    animation: glow 2s infinite alternate;
  }

  .heart {
    position: absolute;
    color: red;
    font-size: 20px;
    animation: float 4s linear infinite;
  }

  @keyframes float {
    0% { transform: translateY(0); opacity: 1; }
    100% { transform: translateY(-600px); opacity: 0; }
  }

  @keyframes glow {
    from { text-shadow: 0 0 10px white; }
    to { text-shadow: 0 0 25px yellow; }
  }

  button {
    margin-top: 20px;
    padding: 12px 25px;
    border: none;
    border-radius: 30px;
    background: white;
    color: #ff4d6d;
    font-size: 1rem;
    cursor: pointer;
    transition: 0.3s;
  }

  button:hover {
    transform: scale(1.1);
  }
</style>
</head>
<body>

<div>
  <h1 id="text">Happy Valentine 💕</h1>
  <button onclick="changeText()">Click Me 💘</button>
</div>

<script>
function createHeart() {
  const heart = document.createElement("div");
  heart.className = "heart";
  heart.innerHTML = "❤️";
  heart.style.left = Math.random() * 100 + "vw";
  heart.style.fontSize = Math.random() * 30 + 15 + "px";
  document.body.appendChild(heart);

  setTimeout(() => {
    heart.remove();
  }, 4000);
}

setInterval(createHeart, 200);

function changeText() {
  const messages = [
    "I Love You 💖",
    "You're My Valentine 💘",
    "Forever Us ❤️",
    "You Are Special 💕"
  ];
  document.getElementById("text").innerText =
    messages[Math.floor(Math.random() * messages.length)];
}
</script>

</body>
</html>
