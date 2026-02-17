<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>My Valentine 💘</title>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;600&display=swap" rel="stylesheet">

<style>
body {
    margin: 0;
    font-family: 'Poppins', sans-serif;
    background: linear-gradient(135deg, #ff9a9e, #fad0c4);
    overflow-x: hidden;
    text-align: center;
    color: white;
}

h1 {
    margin-top: 30px;
    font-size: 2.5em;
}

.gallery {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 20px;
    margin: 30px;
}

.card {
    background: rgba(255,255,255,0.15);
    backdrop-filter: blur(10px);
    border-radius: 20px;
    padding: 15px;
    width: 280px;
    transition: transform 0.4s ease;
}

.card:hover {
    transform: scale(1.05);
}

.card img {
    width: 100%;
    border-radius: 15px;
}

.spotify-section {
    margin: 40px 20px;
}

.spotify-card {
    background: rgba(255,255,255,0.2);
    padding: 20px;
    border-radius: 20px;
    margin: 20px auto;
    width: 300px;
}

.spotify-card img {
    width: 150px;
    margin: 10px 0;
}

.spotify-btn {
    display: inline-block;
    padding: 10px 20px;
    background: #1DB954;
    color: white;
    border-radius: 30px;
    text-decoration: none;
    margin-top: 10px;
}

.love-meter-container {
    margin: 40px;
}

.love-meter {
    width: 80%;
    height: 25px;
    background: rgba(255,255,255,0.3);
    border-radius: 20px;
    margin: auto;
    overflow: hidden;
}

.love-fill {
    height: 100%;
    width: 0%;
    background: red;
    animation: fillLove 5s forwards;
}

@keyframes fillLove {
    to { width: 100%; }
}

/* Heart Rain */
.heart {
    position: fixed;
    top: -10px;
    color: red;
    animation: fall linear infinite;
}

@keyframes fall {
    to {
        transform: translateY(100vh);
    }
}
</style>
</head>

<body>

<h1>Happy Valentine's My Love 💖</h1>

<div class="gallery">
    <div class="card">
        <img src="pic1.jpg" alt="Her Photo 1">
    </div>

    <div class="card">
        <img src="pic2.jpg" alt="Her Photo 2">
    </div>
</div>

<div class="love-meter-container">
    <h2>Our Love Meter 💘</h2>
    <div class="love-meter">
        <div class="love-fill"></div>
    </div>
</div>

<div class="spotify-section">
    <h2>Our Songs 🎶</h2>

    <div class="spotify-card">
        <h3>Song 1</h3>
        <img src="https://api.qrserver.com/v1/create-qr-code/?size=150x150&data=https://open.spotify.com/track/3mvDG5E5xabgrSCmDt8J0T" alt="QR Code 1">
        <br>
        <a class="spotify-btn" href="https://open.spotify.com/track/3mvDG5E5xabgrSCmDt8J0T" target="_blank">
            Listen on Spotify 💚
        </a>
    </div>

    <div class="spotify-card">
        <h3>Song 2</h3>
        <img src="https://api.qrserver.com/v1/create-qr-code/?size=150x150&data=https://open.spotify.com/track/05S7VaTrGBdizlcLGcnEQb" alt="QR Code 2">
        <br>
        <a class="spotify-btn" href="https://open.spotify.com/track/05S7VaTrGBdizlcLGcnEQb" target="_blank">
            Listen on Spotify 💚
        </a>
    </div>
</div>

<audio autoplay loop>
    <source src="https://www.bensound.com/bensound-music/bensound-romantic.mp3" type="audio/mp3">
</audio>

<script>
// Heart Rain
function createHeart() {
    const heart = document.createElement("div");
    heart.classList.add("heart");
    heart.innerText = "💖";
    heart.style.left = Math.random() * 100 + "vw";
    heart.style.animationDuration = Math.random() * 3 + 2 + "s";
    heart.style.fontSize = Math.random() * 20 + 10 + "px";
    document.body.appendChild(heart);

    setTimeout(() => {
        heart.remove();
    }, 5000);
}

setInterval(createHeart, 300);
</script>

</body>
</html>
