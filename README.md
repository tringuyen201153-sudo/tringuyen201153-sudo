<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Thành thật đi</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      background-color: #fff5f5;
      text-align: center;
      padding: 40px;
      color: #ff6b81;
      overflow: hidden;
    }

    h1 {
      font-size: 24px;
      font-weight: bold;
      margin-bottom: 10px;
    }

    p {
      font-size: 14px;
      margin-bottom: 30px;
    }

    img {
      width: 150px;
      margin-bottom: 30px;
    }

    .button-container {
      position: relative;
      height: 100px;
    }

    button {
      padding: 10px 20px;
      font-size: 16px;
      border-radius: 12px;
      border: 2px solid #ff6b81;
      cursor: pointer;
      transition: all 0.3s;
      position: absolute;
    }

    .yes {
      background-color: #ff6b81;
      color: white;
      left: 30%;
    }

    .no {
      background-color: white;
      color: #ff6b81;
      left: 60%;
    }
  </style>
</head>
<body>
  <h1>Ngoài em ra anh còn nhắn tin với con nào không?</h1>
  <p>Khai thật đi anh, em không giận đâu, em chỉ muốn biết thôi =))</p>
  <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExazU3aGhycHd6OGd3Zml5czl4bHh3OW03ZXR3ZnlqYnpkcjl0Z3gzNiZlcD12MV9naWZzX3NlYXJjaCZjdD1n/g01ZnwAUvutuK8GIQn/giphy.gif" alt="Cute cat" />
  <div class="button-container">
    <button class="yes" id="yesBtn">nhiều em</button>
    <button class="no" onclick="alert('Đúng rùi, chỉ có em nhất thôi 💖')">mỗi em</button>
  </div>

  <script>
    const yesBtn = document.getElementById("yesBtn");

    yesBtn.addEventListener("mouseover", () => {
      const container = document.querySelector(".button-container");
      const containerWidth = container.clientWidth - yesBtn.offsetWidth;
      const containerHeight = container.clientHeight - yesBtn.offsetHeight;

      const randomX = Math.floor(Math.random() * containerWidth);
      const randomY = Math.floor(Math.random() * containerHeight);

      yesBtn.style.left = `${randomX}px`;
      yesBtn.style.top = `${randomY}px`;
    });
  </script>
</body>
</html>
