<!-- index.html -->
<!DOCTYPE html>
<html lang="uz">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>UzMovie - Reklamasiz Kino</title>
  <link rel="stylesheet" href="style.css">
  <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
  <script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">

</head>
<body>
  <div class="background-overlay"></div>

  <header>
    <h1>Hello movie</h1>
    <p>Reklamasiz bepul kinolarni tomosha qiling!</p>
  </header>

  <main class="video-grid">
    <div class="video-card" onclick="openPlayer('video1')">
      <img src="./video.mp4/m1.mp4" alt="Video 1">
      <h2>Film 1</h2>
    </div>
    <div class="video-card" onclick="openPlayer('video2')">
      <img src="./video.mp4/m2.mp4" alt="Video 2">
      <h2>Film 2</h2>
    </div>
    <div class="video-card" onclick="openPlayer('video3')">
      <img src="./video.mp4/m3.mp4" alt="Video 3">
      <h2>Film 3</h2>
    </div>
  </main>

  <div id="videoModal" class="modal">
    <div class="modal-content">
      <span class="close" onclick="closePlayer()">&times;</span>
      <video id="moviePlayer" controls>
        <source id="source360" src="" type="video/mp4">
        <source id="source720" src="" type="video/mp4">
        Brauzeringiz video pleyerni qo'llab-quvvatlamaydi.
      </video>
      <div class="quality-buttons">
        <button onclick="changeQuality('360')">360p</button>
        <button onclick="changeQuality('720')">720p</button>
      </div>
    </div>
  </div>

  <a href="https://t.me/Codewith_Mac" class="telegram-float" target="_blank">
    <i class="fab fa-telegram-plane"></i>
  </a>

  <script src="script.js"></script>

  <!-- Video oynasi (modal) -->
<div id="videoModal" style="display: none;" class="modal">
  <video id="moviePlayer" controls></video>
</div>

</body>
</html>

body {
  margin: 0;
  font-family: 'Roboto', sans-serif;
  background-color: #0d0d0d;
  color: #fff;
  overflow-x: hidden;
  position: relative;
}

.background-overlay {
  position: fixed;
  top: 0; left: 0;
  width: 100%; height: 100%;
  background: url('https://images.unsplash.com/photo-1524985069026-dd778a71c7b4?auto=format&fit=crop&w=1500&q=80') no-repeat center center/cover;
  opacity: 0.2;
  z-index: -1;
}

header {
  text-align: center;
  padding: 30px;
  background: rgba(0, 0, 0, 0.6);
  box-shadow: 0 2px 10px rgba(0,0,0,0.7);
}

header h1 {
  font-size: 3em;
  color: #00acee;
  margin-bottom: 10px;
}

header p {
  font-size: 1.2em;
  color: #ccc;
}

.video-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 30px;
  padding: 40px;
}

.video-card {
  background-color: rgba(0,0,0,0.5);
  border-radius: 12px;
  overflow: hidden;
  cursor: pointer;
  transition: transform 0.3s, box-shadow 0.3s;
  backdrop-filter: blur(5px);
}

.video-card:hover {
  transform: scale(1.05);
  box-shadow: 0 4px 20px rgba(0, 172, 238, 0.3);
}

.video-card img {
  width: 100%;
  height: 250px;
  object-fit: cover;
}

.video-card h2 {
  text-align: center;
  padding: 15px;
  color: #fff;
}

.modal {
  display: none;
  position: fixed;
  z-index: 1000;
  top: 0; left: 0;
  width: 100%; height: 100%;
  background-color: rgba(0, 0, 0, 0.95);
}

.modal-content {
  position: relative;
  max-width: 800px;
  margin: 50px auto;
  background: #000;
  padding: 20px;
  border-radius: 12px;
  text-align: center;
}

.modal-content video {
  width: 100%;
  border-radius: 10px;
}

.close {
  position: absolute;
  top: 10px;
  right: 20px;
  font-size: 30px;
  cursor: pointer;
  color: white;
}

.quality-buttons button {
  margin: 10px 5px;
  padding: 10px 20px;
  background-color: #00acee;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  font-weight: bold;
  transition: background-color 0.2s;
}

.quality-buttons button:hover {
  background-color: #008bb9;
}
.telegram-float {
  position: fixed;
  width: 60px;
  height: 60px;
  bottom: 20px; /* pastki chekkadan 20px */
  right: 20px;  /* o'ng chekkadan 20px */
  background-color: #0088cc; /* Telegram rang */
  color: white;
  border-radius: 50%; /* doira shakli */
  text-align: center;
  font-size: 30px;
  box-shadow: 2px 2px 5px rgba(0,0,0,0.3);
  z-index: 1000;
  display: flex;
  justify-content: center;
  align-items: center;
  text-decoration: none;
  transition: background-color 0.3s;
}

.telegram-float:hover {
  background-color: #020281;
}
.telegram-float {
  position: fixed;
  width: 60px;
  height: 60px;
  bottom: 20px; /* pastki chekkadan 20px */
  right: 20px;  /* o'ng chekkadan 20px */
  background-color: #0088cc; /* Telegram rang */
  color: white;
  border-radius: 50%; /* doira shakli */
  text-align: center;
  font-size: 30px;
  box-shadow: 2px 2px 5px rgba(0,0,0,0.3);
  z-index: 1000;
  display: flex;
  justify-content: center;
  align-items: center;
  text-decoration: none;
  transition: background-color 0.3s;
}

.telegram-float:hover {
  background-color: #007ab8;
}.telegram-float {
  position: fixed;
  width: 60px;
  height: 60px;
  bottom: 20px; /* pastki chekkadan 20px */
  right: 20px;  /* o'ng chekkadan 20px */
  background-color: #0088cc; /* Telegram rang */
  color: white;
  border-radius: 50%; /* doira shakli */
  text-align: center;
  font-size: 30px;
  box-shadow: 2px 2px 5px rgba(0,0,0,0.3);
  z-index: 1000;
  display: flex;
  justify-content: center;
  align-items: center;
  text-decoration: none;
  transition: background-color 0.3s;
}

.telegram-float:hover {
  background-color: #0923cf;
}
.telegram-float:active{
    background-color: #2bb716; /* bosilganda rang */
}

let isFullscreen = false;

// Modalni yopish funksiyasi
function closePlayer() {
  const modal = document.getElementById('videoModal');
  const player = document.getElementById('moviePlayer');
  modal.style.display = 'none';
  player.pause();
  player.currentTime = 0;
  isFullscreen = false;
}

// Video ochish funksiyasi (misol uchun)
function openPlayer(videoId) {
  const modal = document.getElementById('videoModal');
  const player = document.getElementById('moviePlayer');

  // Har xil videolar uchun mos faylni tanlash
  if (videoId === 'video1') {
    player.src = './video.mp4/m1.mp4';
  } else if (videoId === 'video2') {
    player.src = './video.mp4/m2.mp4';
  } else if (videoId === 'video3') {
    player.src = './video.mp4/m3.mp4';
  }

  modal.style.display = 'flex';
  player.play();
}

// VIDEO USTIGA 2 MARTA BOSISH — FULLSCREEN
document.getElementById('moviePlayer').addEventListener('dblclick', function () {
  const video = document.getElementById('moviePlayer');

  if (!isFullscreen) {
    if (video.requestFullscreen) {
      video.requestFullscreen();
    } else if (video.webkitRequestFullscreen) {
      video.webkitRequestFullscreen();
    } else if (video.msRequestFullscreen) {
      video.msRequestFullscreen();
    }
    isFullscreen = true;
  } else {
    if (document.exitFullscreen) {
      document.exitFullscreen();
    } else if (document.webkitExitFullscreen) {
      document.webkitExitFullscreen();
    } else if (document.msExitFullscreen) {
      document.msExitFullscreen();
    }
    isFullscreen = false;
  }
});

// VIDEO TASHQARISIGA 2 MARTA BOSISH — MODALNI YOPISH
document.getElementById('videoModal').addEventListener('dblclick', function (e) {
  if (!e.target.closest('video')) {
    closePlayer();
  }
});


