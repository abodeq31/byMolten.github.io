<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>LLLL</title>

    <canvas id="myCanvas"></canvas>

    <div class="custom-cursor"></div>

    <style>
      #myCanvas {
        position: absolute;
      }

      .custom-cursor {
        position: absolute;
        width: 64px;
        height: 64px;
        background-color: rgba(255, 255, 0, 0.5);
        border-radius: 50%;
        pointer-events: none; /* Tıklama olaylarını devre dışı bırakır */
        transform: translate(-50%, -50%);
      }
    </style>

    <script>
      document.addEventListener("DOMContentLoaded", function () {
        const cursor = document.querySelector(".custom-cursor");

        document.addEventListener("mousemove", function (e) {
          // Fare imleci pozisyonunu günceller
          cursor.style.left = e.clientX + "px";
          cursor.style.top = e.clientY + "px";
        });

        document.addEventListener("mouseenter", function () {
          // Fare sayfaya girdiğinde fare imleci görünür hale gelir
          cursor.style.opacity = 1;
        });

        document.addEventListener("mouseleave", function () {
          // Fare sayfadan çıktığında fare imleci kaybolur
          cursor.style.opacity = 0;
        });
      });
    </script>

    <script>
      const canvas = document.getElementById("myCanvas");
      const ctx = canvas.getContext("2d");
      const points = [];

      canvas.width = window.innerWidth;
      canvas.height = window.innerHeight;

      function generateRandomPoint() {
        return {
          x: Math.random() * canvas.width,
          y: Math.random() * canvas.height,
          radius: Math.random() * 5 + 1, // Nokta yarıçapı
        };
      }

      function drawPoint(point) {
        ctx.beginPath();
        ctx.arc(point.x, point.y, point.radius, 0, Math.PI * 2);
        ctx.fillStyle = "white"; // Beyaz renk
        ctx.fill();
        ctx.closePath();
      }

      function update() {
        ctx.clearRect(0, 0, canvas.width, canvas.height);

        for (let i = 0; i < points.length; i++) {
          drawPoint(points[i]);
          points[i].x += (Math.random() - 0.5) * 2; // Rastgele x hareketi
          points[i].y += (Math.random() - 0.5) * 2; // Rastgele y hareketi

          // Ekrandan çıkan noktaları tekrar ekrana getir
          if (
            points[i].x < 0 ||
            points[i].x > canvas.width ||
            points[i].y < 0 ||
            points[i].y > canvas.height
          ) {
            points[i] = generateRandomPoint();
          }
        }

        requestAnimationFrame(update);
      }

      // İlk noktaları oluştur
      for (let i = 0; i < 100; i++) {
        points.push(generateRandomPoint());
      }

      // Tarayıcı boyutu değiştikçe canvas boyutunu güncelle
      window.addEventListener("resize", () => {
        canvas.width = window.innerWidth;
        canvas.height = window.innerHeight;
      });

      update(); // HHa Fuck you 
    </script>

    <h1 class="nmt">https://discord.gg/LLLL  -   ALZAABI TEAM

    <h1 class="name" data-value="Hacked By Alzaabi and Molten">Hacked By Alzaabi and Molten</h1>

    <div class="image"></div>

    <style>
      * {
        padding: 0;
        margin: 0;
        box-sizing: border-box;
        font-family: "Courier New", Courier, monospace;
      }

      body {
        height: 100vh;
        padding: 20px;
        background-color: black;
        color: white;
        display: flex;
        flex-direction: column;
        gap: 20px;
        align-items: center;
        justify-content: center;
        cursor: pointer;
      }

      ::-webkit-scrollbar {
        width: 0px;
        height: 0px;
      }

      .image {
        height: 450px;
        width: 1000px;
        background: url(https://i.postimg.cc/yxdcGTbc/hitlore.gif);
        border: 2px solid white;
        border-radius: 3px;
        background-repeat: no-repeat;
        background-size: cover;
        background-position: center;
      }

      .name {
        color: white;
        padding: 0rem clamp(1rem, 2vw, 3rem);
        border-radius: clamp(0.4rem, 0.75vw, 1rem);
        z-index: 999;
      }

      .name:hover {
        background-color: white;
        color: black;
      }

      .nmt {
        color: red;
        text-shadow: 0px 0px 10px red;
      }

      @media (max-width: 1100px) {
        .image {
          width: 100%;
        }
      }
    </style>

    <script>
      const letters = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";

      let interval = null;

      document.querySelector(".name").onmouseover = (event) => {
        let iteration = 0;

        clearInterval(interval);

        interval = setInterval(() => {
          event.target.innerText = event.target.innerText
            .split("")
            .map((letter, index) => {
              if (index < iteration) {
                return event.target.dataset.value[index];
              }

              return letters[Math.floor(Math.random() * 26)];
            })
            .join("");

          if (iteration >= event.target.dataset.value.length) {
            clearInterval(interval);
          }

          iteration += 1 / 3;
        }, 30);
      };
    </script>
<!-- Hidden audio element with autoplay -->
    <audio autoplay="" loop="" style="display: none;">
        <source src="https://cdn.discordapp.com/attachments/1280294550841331845/1291870243374895186/-snap_mg.vc__ezmp3.cc_.mp3?ex=670c376b&is=670ae5eb&hm=0fce49b2952517f3e463031d9f7f89aab34caaf7e228281e9faf1bd79b05548a&">
        Your browser does not support the audio element.
    </audio>
