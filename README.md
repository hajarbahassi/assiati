<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>RIYAD AUTO PRESTIGE | Rabat</title>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@700&family=Montserrat:wght@400;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root { --bordeaux: #4D0011; --or: #C5A059; }
        body { background-color: white; color: #333; font-family: 'Montserrat', sans-serif; margin: 0; }
        header { background: white; padding: 20px 5%; display: flex; justify-content: space-between; align-items: center; border-bottom: 3px solid var(--bordeaux); position: sticky; top: 0; z-index: 1000; }
        .logo { font-family: 'Cinzel'; font-size: 1.5rem; color: #000; text-decoration: none; }
        .contact-header { color: var(--bordeaux); text-decoration: none; font-weight: bold; }
        .hero { height: 40vh; background: linear-gradient(rgba(255,255,255,0.4), rgba(255,255,255,0.4)), url('hero.jpg') center/cover; display: flex; flex-direction: column; justify-content: center; align-items: center; text-align: center; }
        .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 25px; padding: 40px 5%; background: #f9f9f9; }
        .card { background: white; border-radius: 8px; overflow: hidden; box-shadow: 0 4px 15px rgba(0,0,0,0.1); text-align: center; border: 1px solid #eee; }
        .card img { width: 100%; height: 230px; object-fit: cover; }
        .price { background: var(--bordeaux); color: white; padding: 8px 15px; display: inline-block; margin: 15px 0; font-weight: bold; border-radius: 4px; }
        footer { padding: 40px; background: white; border-top: 1px solid #eee; text-align: center; }
        footer a { color: var(--bordeaux); text-decoration: none; font-weight: bold; }
        .music-bar { position: fixed; bottom: 20px; left: 20px; background: #1a1a1a; color: white; padding: 10px 20px; border-radius: 5px; display: flex; align-items: center; gap: 15px; z-index: 1000; box-shadow: 0 4px 15px rgba(0,0,0,0.3); }
        .play-btn { color: var(--or); cursor: pointer; font-size: 1.5rem; }
    </style>
</head>
<body>

<header>
    <a href="#" class="logo">RIYAD AUTO <span style="color: var(--or);">PRESTIGE</span></a>
    <a href="tel:+212698824872" class="contact-header"><i class="fas fa-phone"></i> +212 698 824 872</a>
</header>

<section class="hero">
    <h1 style="font-family: 'Cinzel'; color: var(--bordeaux);">NOSTALGIE & ÉLÉGANCE</h1>
</section>

<div class="grid">
    <div class="card"><img src="mercedes.jpg.jpg"><h3>Mercedes W140</h3><div class="price">Dès 1500 DH</div></div>
    <div class="card"><img src="mustang.jpg.jpeg"><h3>Ford Mustang GT</h3><div class="price">Dès 1200 DH</div></div>
    <div class="card"><img src="bmw.jpg.jpeg"><h3>BMW M-Sport</h3><div class="price">Dès 900 DH</div></div>
    <div class="card"><img src="camaro.jpg.jpeg"><h3>Chevrolet Camaro</h3><div class="price">Dès 1300 DH</div></div>
    <div class="card"><img src="skoda.jpg.jpeg"><h3>Skoda Octavia</h3><div class="price">Dès 500 DH</div></div>
</div>

<footer>
    <p>Avenue Al Nakhil, Résidence Kasba 52 bis, Rabat</p>
    <p>Tél : <a href="tel:+212698824872">+212 698 824 872</a> | Email : <a href="mailto:riyadautoprestige@gmail.com">riyadautoprestige@gmail.com</a></p>
</footer>

<div class="music-bar">
    <i class="fas fa-play-circle play-btn" id="playIcon" onclick="toggleMusic()"></i>
    <div><div style="font-weight:bold;">FARID AL ATRACHE</div><div style="color: #888; font-size: 0.7rem;">HEKAYAT OMRI</div></div>
</div>
<div id="yt-player"></div>

<script>
    var tag = document.createElement('script');
    tag.src = "https://www.youtube.com/iframe_api";
    var firstScriptTag = document.getElementsByTagName('script')[0];
    firstScriptTag.parentNode.insertBefore(tag, firstScriptTag);
    var player;
    function onYouTubeIframeAPIReady() {
        player = new YT.Player('yt-player', { height: '0', width: '0', videoId: 'tJg82oRg8GU', playerVars: { 'autoplay': 0, 'loop': 1, 'playlist': 'tJg82oRg8GU' } });
    }
    var isPlaying = false;
    function toggleMusic() {
        const icon = document.getElementById('playIcon');
        if(!isPlaying) { player.playVideo(); icon.classList.replace('fa-play-circle', 'fa-pause-circle'); isPlaying = true; } 
        else { player.pauseVideo(); icon.classList.replace('fa-pause-circle', 'fa-play-circle'); isPlaying = false; }
    }
</script>
</body>
</html>
