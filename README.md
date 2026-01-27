#<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Will you be My Valentine 💖</title>

<style>
  body {
    margin: 0;
    height: 100vh;
    background: linear-gradient(135deg, #ffd6e8, #ffe6f2);
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: 'Poppins', sans-serif;
    overflow: hidden;
  }

  .card {
    background: white;
    padding: 30px;
    border-radius: 25px;
    text-align: center;
    max-width: 350px;
    width: 90%;
    box-shadow: 0 20px 40px rgba(0,0,0,0.15);
    animation: fadeIn 2s ease;
  }

  h1 {
    color: #ff4d88;
    font-size: 24px;
    margin-bottom: 15px;
  }

  p {
    color: #555;
    font-size: 16px;
    min-height: 40px;
  }

  button {
    margin: 15px 10px 0;
    padding: 12px 25px;
    border: none;
    border-radius: 25px;
    font-size: 16px;
    cursor: pointer;
    transition: transform 0.3s;
  }

  .yes {
    background: #ff4d88;
    color: white;
  }

  .yes:hover {
    transform: scale(1.1);
  }

  .heart {
    position: absolute;
    color: rgba(255, 77, 136, 0.7);
    animation: floatUp 6s linear infinite;
  }

  @keyframes floatUp {
    from { bottom: -10%; opacity: 1; }
    to { bottom: 110%; opacity: 0; }
  }

  @keyframes fadeIn {
    from { opacity: 0; transform: scale(0.8); }
    to { opacity: 1; transform: scale(1); }
  }
</style>
</head>

<body>

<div class="card">
  <h1>Hey My Sexy Big Mama❤️🥵💕</h1>
  <p id="text"></p>

  <button class="yes" onclick="accepted()">YES 💖</button>
  <button class="yes" onclick="accepted()">ABSOLUTELY 😍</button>
</div>

<script>
  const message = "I was wondering... will you be my Valentine? 🌹💌";
  let i = 0;
  const speed = 50;

  function typeWriter() {
    if (i < message.length) {
      document.getElementById("text").innerHTML += message.charAt(i);
      i++;
      setTimeout(typeWriter, speed);
    }
  }
  typeWriter();

  function accepted() {
    document.body.innerHTML = `
      <div class="card">
        <h1>YESSAI!!! 💞🥰🕺🏾</h1>
        <p>Thank you so much baby,hope this makes up for last year😭💖</p>
      </div>
    `;
  }

  setInterval(() => {
    const heart = document.createElement("div");
    heart.className = "heart";
    heart.innerHTML = "❤️";
    heart.style.left = Math.random() * 100 + "vw";
    heart.style.fontSize = Math.random() * 30 + 20 + "px";
    document.body.appendChild(heart);
    setTimeout(() => heart.remove(), 6000);
  }, 300);
</script>

</body>
</html>
