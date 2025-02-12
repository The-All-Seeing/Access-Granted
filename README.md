<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>The All Seeing</title>
  <style>
    /* General styling */
    body {
      background-color: #000;
      color: #00FF41;
      font-family: 'Courier New', Courier, monospace;
      margin: 0;
      padding: 0;
      text-align: center;
    }

    h1, p {
      text-shadow: 0 0 5px #00FF41, 0 0 10px #00FF41, 0 0 20px #00FF41;
    }

    input, button {
      background-color: #111;
      color: #00FF41;
      border: 2px solid #00FF41;
      border-radius: 5px;
      padding: 10px;
      margin: 5px;
      font-size: 16px;
    }

    button:hover {
      color: #ff0000;
      cursor: pointer;
    }

    /* Option menu */
    .options {
      display: flex;
      justify-content: space-around;
      margin-top: 20px;
    }

    .option {
      padding: 20px;
      border: 1px solid #00FF41;
      border-radius: 10px;
    }

    .option a {
      color: #00FF41;
      text-decoration: none;
    }

    footer {
      margin-top: 30px;
      font-size: 12px;
      color: #888;
    }

    /* Disclaimer styling */
    .disclaimer {
      font-size: 12px;
      color: #ff0000;
      margin-bottom: 20px;
    }

    /* Eye page */
    .eye-container {
      margin: 20px auto;
      position: relative;
      width: 200px;
      height: 200px;
      display: inline-block;
      animation: lookAround 8s infinite ease-in-out;
    }

    .eye {
      width: 100%;
      height: 100%;
      background: radial-gradient(circle at 50% 50%, #FFFFFF 30%, #aaa 80%, #555);
      border-radius: 50%;
      position: relative;
      box-shadow: 0 0 50px rgba(0, 255, 65, 0.5);
      overflow: hidden;
    }

    .pupil {
      position: absolute;
      width: 50px;
      height: 50px;
      top: 50%;
      left: 50%;
      background: radial-gradient(circle, #000000 30%, #333);
      border-radius: 50%;
      transform: translate(-50%, -50%);
      z-index: 2;
      animation: pupilMove 4.5s infinite ease-in-out;
    }

    .eyelid-top, .eyelid-bottom {
      position: absolute;
      width: 100%;
      height: 50%;
      background: #000;
      z-index: 3;
    }

    .eyelid-top {
      top: 0;
      transform-origin: top;
      animation: blink 6s infinite ease-in-out;
    }

    .eyelid-bottom {
      bottom: 0;
      transform-origin: bottom;
      animation: blink 6s infinite ease-in-out;
    }

    /* Blinking animation */
    @keyframes blink {
      0%, 20%, 60%, 100% {
        transform: scaleY(1);
      }
      25%, 55% {
        transform: scaleY(0.1);
      }
    }

    /* Pupil movement animation */
    @keyframes pupilMove {
      0%, 100% { top: 50%; left: 50%; }
      25% { top: 30%; left: 60%; }
      50% { top: 60%; left: 40%; }
      75% { top: 40%; left: 50%; }
    }

    @keyframes lookAround {
      0%, 100% { transform: rotate(0deg); }
      50% { transform: rotate(10deg); }
      75% { transform: rotate(-10deg); }
    }

    .text-below {
      margin-top: 30px;
      font-size: 20px;
    }

    .bold-text {
      font-size: 30px;
      color: #ff0000;
      margin-top: 20px;
      font-weight: bold;
    }

    /* Final Page Styling */
    .final-page {
      background-color: #000;
      color: #ff0000;
      font-family: 'Courier New', Courier, monospace;
      text-align: center;
    }

    h1.final-text {
      font-size: 50px;
      margin-top: 20%;
      text-shadow: 0 0 5px #ff0000, 0 0 10px #ff0000, 0 0 20px #ff0000;
    }
  </style>
  <script>
    function redirectToFinalPage() {
      setTimeout(() => {
        window.location.href = "#final";
      }, 5000);
    }
  </script>
</head>
<body>
  <h1>Welcome to The All Seeing</h1>
  <div class="options">
    <div class="option">
      <h2><a href="#hacking">Hacking</a></h2>
      <p>We crack the code. We own the web.</p>
    </div>
    <div class="option">
      <h2><a href="#eye-page">Eyes</a></h2>
      <p>The eyes that see all. Nothing is hidden.</p>
    </div>
  </div>

  <footer>
    &copy; 2025 The All Seeing | Hackers of the Dark Web
  </footer>

  <!-- Form for Hacking Info -->
  <div id="hacking" style="margin-top:50px;">
    <h1>Stalking Information Form</h1>
    <p class="disclaimer">Disclaimer: This is purely for entertainment purposes. Do not input any real information.</p>
    <form action="#eye-page">
      <p>Target Name:</p>
      <input type="text" name="target" required><br>
      <p>Location:</p>
      <input type="text" name="location" required><br>
      <p>Describe what we need to know:</p>
      <input type="text" name="details" required><br>
      <button type="submit" onclick="redirectToFinalPage()">Submit</button>
    </form>
  </div>

  <!-- Eye Page -->
  <div id="eye-page">
    <h1>The All Seeing Has Heard Your Prayer</h1>
    <div class="eye-container">
      <div class="eye">
        <div class="pupil"></div>
        <div class="eyelid-top"></div>
        <div class="eyelid-bottom"></div>
      </div>
    </div>
    <p class="text-below">Offer us your eyes.</p>
    <p class="bold-text">OFFER US YOUR EYES</p>
  </div>

  <!-- Final Page -->
  <div id="final" class="final-page">
    <h1 class="final-text">Your Eyes Will Be Mine</h1>
  </div>
</body>
</html>
