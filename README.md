<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>JURASSIC DIRT BIRTHDAY BASH!</title>
  <style>
    body {
      margin: 0;
      font-family: 'Comic Sans MS', cursive, sans-serif;
      background: url('https://wallpapercave.com/wp/wp3891508.jpg') no-repeat center center fixed;
      background-size: cover;
      color: #fff;
      text-align: center;
      padding: 40px 20px;
      overflow-x: hidden;
    }

    h1 {
      font-size: 2.5em;
      color: #00ff00;
      text-shadow: 3px 3px 5px #000;
      margin-bottom: 20px;
    }

    .container {
      background-color: rgba(0, 0, 0, 0.75);
      padding: 30px 20px;
      border-radius: 15px;
      display: inline-block;
      max-width: 90%;
      width: 100%;
      box-sizing: border-box;
    }

    .emoji {
      font-size: 2.5em;
      animation: bounce 2s infinite;
    }

    @keyframes bounce {
      0%, 100% {
        transform: translateY(0);
      }
      50% {
        transform: translateY(-15px);
      }
    }

    .info {
      font-size: 1.1em;
      margin-top: 20px;
    }

    .rsvp {
      margin-top: 30px;
      font-size: 1em;
    }

    .button {
      background-color: #ff6600;
      color: white;
      border: none;
      padding: 10px 20px;
      font-size: 1em;
      border-radius: 10px;
      cursor: pointer;
      margin-top: 10px;
    }

    .button:hover {
      background-color: #ff3300;
    }

    #countdown {
      font-size: 1.3em;
      color: #ffd700;
      margin-top: 20px;
    }

    audio {
      display: none;
    }

    /* Mobile adjustments */
    @media (max-width: 480px) {
      h1 {
        font-size: 2em;
      }

      .emoji {
        font-size: 2em;
      }

      .info {
        font-size: 1em;
      }

      #countdown {
        font-size: 1.1em;
      }

      .button {
        font-size: 0.9em;
        padding: 8px 16px;
      }
    }
  </style>
</head>
<body>

  <!-- Background Sound -->
  <audio autoplay loop>
    <source src="https://cdn.pixabay.com/download/audio/2022/03/31/audio_28e4d92d93.mp3?filename=tyrannosaurus-rex-roar-111598.mp3" type="audio/mpeg">
    Your browser does not support the audio element.
  </audio>

  <div class="container">
    <h1>🦖 JURASSIC DIRT BIRTHDAY BASH! 🏍️</h1>
    <div class="emoji">🦕🏍️🦖</div>
    <div class="info">
      <p>You're invited to <strong>Muaadth's 7th Birthday Party!</strong></p>
      <p>Join us for a ROARING adventure and high-speed dirt bike fun!</p>
      <p><strong>Date:</strong> Saturday, August 9th</p>
      <p><strong>Time:</strong> 12:00 PM – 5:00 PM</p>
      <p><strong>Place:</strong> 57 Calendula Drive, Malabar</p>
    </div>

    <div id="countdown">Loading countdown...</div>

    <div class="rsvp">
      <p>Don't forget to RSVP by August 5th!</p>
    </div>
  </div>

  <!-- Countdown Timer Script -->
  <script>
    const partyDate = new Date("August 9, 2025 12:00:00").getTime();
    const countdownElement = document.getElementById("countdown");

    const countdownFunction = setInterval(function () {
      const now = new Date().getTime();
      const distance = partyDate - now;

      if (distance <= 0) {
        clearInterval(countdownFunction);
        countdownElement.innerHTML = "🎉 It's Party Time! 🦖🏍️";
      } else {
        const days = Math.floor(distance / (1000 * 60 * 60 * 24));
        const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
        const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
        const seconds = Math.floor((distance % (1000 * 60)) / 1000);

        countdownElement.innerHTML =
          `⏳ ${days}d ${hours}h ${minutes}m ${seconds}s until the roar begins!`;
      }
    }, 1000);
  </script>
</body>
</html>
