<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>snoobe Profile</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    body, html {
      width: 100%;
      height: 100%;
      font-family: Arial, sans-serif;
      overflow: hidden;
      background: black;
    }
    #videoBG {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      object-fit: cover;
      z-index: -1;
      display: none;
    }
    .center {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      color: white;
      text-align: center;
    }
    .btn {
      margin-top: 20px;
      padding: 12px 24px;
      font-size: 18px;
      background: white;
      color: black;
      border: none;
      cursor: pointer;
      border-radius: 5px;
    }
  </style>
</head>
<body>

  <!-- 🎬 الفيديو -->
  <video id="videoBG" autoplay muted loop>
    <source src="https://cdn.coverr.co/videos/coverr-working-on-laptop-8572/1080p.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>

  <!-- 👇 الكلام وزر البداية -->
  <div class="center" id="startScreen">
    <h1>اضغط هنا لبدء العرض</h1>
    <button class="btn" onclick="startVideo()">ابدأ</button>
  </div>

  <!-- 🔽 السكربت -->
  <script>
    function startVideo() {
      const video = document.getElementById('videoBG');
      video.style.display = 'block';
      video.play();
      document.getElementById('startScreen').style.display = 'none';
    }
  </script>

</body>
</html>
