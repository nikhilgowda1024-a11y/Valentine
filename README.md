# Valentine
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Valentine 💖</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      background: linear-gradient(135deg, #ff758c, #ff7eb3);
      font-family: 'Segoe UI', sans-serif;
      overflow: hidden;
    }

    .container {
      text-align: center;
      color: white;
    }

    h1 {
      font-size: 2.8rem;
      margin-bottom: 40px;
    }

    .buttons {
      position: relative;
      width: 300px;
      height: 150px;
      margin: auto;
    }

    button {
      border: none;
      padding: 14px 28px;
      font-size: 1.2rem;
      border-radius: 30px;
      cursor: pointer;
      transition: all 0.3s ease;
      position: absolute;
    }

    #yes {
      background: #2ecc71;
      color: white;
      left: 50%;
      transform: translateX(-50%);
    }

    #no {
      background: #e74c3c;
      color: white;
      top: 60px;
      left: 50%;
      transform: translateX(-50%);
    }

    .yay {
      display: none;
      font-size: 4rem;
      margin-top: 20px;
      animation: pop 0.6s ease forwards;
    }

    .gif {
      display: none;
      margin-top: 20px;
    }

    @keyframes pop {
      0% { transform: scale(0); }
      100% { transform: scale(1); }
    }
  </style>
</head>
<body>

  <div class="container">
    <h1>Priya, will you be my Valentine? 💖</h1>

    <div class="buttons">
      <button id="yes">YES 💘</button>
      <button id="no">NO 🙄</button>
    </div>

    <div class="yay">YAY 🎉🥰</div>

    <div class="gif">
      <img src="https://media.giphy.com/media/MDJ9IbxxvDUQM/giphy.gif" width="250">
    </div>
  </div>

  <script>
    const noBtn = document.getElementById("no");
    const yesBtn = document.getElementById("yes");
    const yayText = document.querySelector(".yay");
    const gif = document.querySelector(".gif");

    let yesScale = 1;

    noBtn.addEventListener("mouseover", () => {
      const x = Math.random() * (window.innerWidth - 100);
      const y = Math.random() * (window.innerHeight - 100);

      noBtn.style.left = x + "px";
      noBtn.style.top = y + "px";

      yesScale += 0.1;
      yesBtn.style.transform = `translateX(-50%) scale(${yesScale})`;
    });

    yesBtn.addEventListener("click", () => {
      noBtn.style.display = "none";
      yesBtn.style.display = "none";
      yayText.style.display = "block";
      gif.style.display = "block";
    });
  </script>

</body>
</html>
