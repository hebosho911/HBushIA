# HBushIA
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
    }

    .parallax-container {
      height: 100vh;
      overflow-x: hidden;
      overflow-y: hidden;
      position: relative;
    }

    .parallax-section {
      position: absolute;
      width: 100%;
      height: 100%;
      background-position: center;
      background-size: cover;
    }

    .parallax-section1 {
      background-image: url('image1.jpg');
      z-index: 1;
    }

    .parallax-section2 {
      background-image: url('image2.jpg');
      z-index: 2;
    }

    /* Add more sections as needed */

    .content {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      color: white;
      text-align: center;
    }
  </style>
</head>
<body>
  <div class="parallax-container">
    <div class="parallax-section parallax-section1"></div>
    <div class="parallax-section parallax-section2"></div>
    <!-- Add more sections as needed -->

    <div class="content">
      <h1>Your Content Goes Here</h1>
      <p>This is a sample parallax-scrolling webpage.</p>
    </div>
  </div>

  <script>
    document.addEventListener('scroll', function () {
      const offsetY = window.pageYOffset;

      // Adjust the background positions for parallax effect
      document.querySelector('.parallax-section1').style.backgroundPositionY = -offsetY * 0.5 + 'px';
      document.querySelector('.parallax-section2').style.backgroundPositionY = -offsetY * 0.8 + 'px';
      // Add more sections if needed
    });
  </script>
</body>
</html>