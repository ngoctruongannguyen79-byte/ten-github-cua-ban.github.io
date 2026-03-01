<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8" />
  <title>Gửi người anh yêu 💖</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <style>
    * { box-sizing: border-box; }
    body {
      margin: 0;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      font-family: 'Segoe UI', sans-serif;
      overflow: hidden;
    }
    .card {
      background: white;
      padding: 40px;
      border-radius: 20px;
      text-align: center;
      width: 90%;
      max-width: 420px;
      box-shadow: 0 20px 40px rgba(0,0,0,0.2);
      animation: pop 1s ease;
    }
    h1 {
      color: #ff4d6d;
      margin-bottom: 10px;
    }
    p {
      color: #444;
      font-size: 18px;
      line-height: 1.5;
    }
    .buttons {
      margin-top: 30px;
      display: flex;
      justify-content: space-around;
    }
    button {
      border: none;
      padding: 12px 22px;
      border-radius: 30px;
      font-size: 16px;
      cursor: pointer;
      transition: 0.3s;
    }
    .yes {
      background: #ff4d6d;
      color: white;
    }
    .yes:hover {
      background: #ff1f4a;
      transform: scale(1.1);
    }
    .no {
      background: #ccc;
    }
    .no:hover {
      position: absolute;
      left: Math.random() * 80 + 'vw';
      top: Math.random() * 80 + 'vh';
    }
    .heart {
      position: fixed;
      color: #ff4d6d;
      font-size: 20px;
      animation: float 4s linear infinite;
    }
    @keyframes float {
      from { transform: translateY(0); opacity: 1; }
      to { transform: translateY(-100vh); opacity: 0; }
    }
    @keyframes pop {
      from { transform: scale(0.7); opacity: 0; }
      to { transform: scale(1); opacity: 1; }
    }
  </style>
</head>
<body>
  <div class="card">
    <h1>💌 Gửi em 💌</h1>
    <p>
      Từ lúc gặp em, thế giới của anh tự nhiên nhiều màu hơn 🌈<br>
      Anh không giỏi nói lời hoa mỹ…<br>
      Nhưng anh thật lòng muốn hỏi em một điều 🥺
    </p>
    <h2>Em làm người yêu anh nhé? 💖</h2>
    <div class="buttons">
      <button class="yes" onclick="yesClick()">Dạaaa 💕</button>
      <button class="no" id="noBtn">Không 😭</button>
    </div>
  </div>

  <script>
    const noBtn = document.getElementById('noBtn');
    noBtn.addEventListener('mouseover', () => {
      noBtn.style.left = Math.random() * 70 + 'vw';
      noBtn.style.top = Math.random() * 70 + 'vh';
      noBtn.style.position = 'absolute';
    });

    function yesClick() {
      document.body.innerHTML = '<h1 style="color:white;font-size:40px;">💖 Anh biết màaa 😍 Yêu em nhiều lắm 💖</h1>';
      setInterval(createHeart, 200);
    }

    function createHeart() {
      const heart = document.createElement('div');
      heart.className = 'heart';
      heart.innerText = '❤';
      heart.style.left = Math.random() * 100 + 'vw';
      heart.style.bottom = '0';
      document.body.appendChild(heart);
      setTimeout(() => heart.remove(), 4000);
    }
  </script>
</body>
</html>
