
<html lang="pt-br">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Kaique ❤️ Laís</title>
<style>
  * { box-sizing: border-box; }
  body {
    margin: 0;
    background: #000;
    color: #eee;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    height: 100vh;
    overflow: hidden;
  }
  .present-overlay {
    position: fixed;
    inset: 0;
    background: #000d;
    display: flex;
    align-items: center;
    justify-content: center;
    z-index: 100;
    transition: opacity 0.5s;
  }
  .present-box {
    background: #fff;
    border-radius: 20px;
    padding: 40px 60px;
    box-shadow: 0 8px 32px #000a;
    display: flex;
    flex-direction: column;
    align-items: center;
    cursor: pointer;
    transition: transform 0.2s;
    border: 4px solid #ff5c5c;
  }
  .present-box:hover {
    transform: scale(1.05);
    box-shadow: 0 12px 40px #ff5c5c88;
  }
  .present-emoji {
    font-size: 5rem;
    margin-bottom: 20px;
    animation: bounce 1.2s infinite;
  }
  @keyframes bounce {
    0%, 100% { transform: translateY(0);}
    50% { transform: translateY(-20px);}
  }
  .present-text {
    font-size: 1.3rem;
    color: #222;
    font-weight: bold;
    text-align: center;
  }
  .container, .music-control {
    position: relative;
    z-index: 1;
  }
  .container {
    flex: 1;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 20px;
    padding: 10px;
    min-height: 100vh;
    display: none; /* só aparece depois */
  }
  .text-center {
    width: 40%;
    max-width: 600px;
    text-align: center;
    line-height: 1.5;
    font-weight: bold;
  }
  .text-center h1 {
    font-size: 2.5rem;
    margin-bottom: 0.5rem;
    color: #ff5c5c;
    font-weight: bold;
  }
  .text-center p {
    font-size: 1.1rem;
    margin: 0.5rem 0;
    color: #ddd;
    font-weight: bold;
  }
  .carousel {
    width: 25%;
    height: 80vh;
    overflow: hidden;
    position: relative;
    border-radius: 12px;
    border: 2px solid #ff5c5c;
    background: #222b;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 0;
  }
  .carousel-track {
    position: absolute;
    width: 100%;
    left: 0;
  }
  .carousel img {
    display: block;
    width: 90%;
    margin: 10px auto;
    border-radius: 8px;
    box-shadow: 0 2px 8px #0008;
  }
  .carousel-left .carousel-track {
    animation: scroll-up 40s linear infinite;
  }
  .carousel-right .carousel-track {
    animation: scroll-down 40s linear infinite;
  }
  @keyframes scroll-up {
    0% { top: 0; }
    100% { top: -50%; }
  }
  @keyframes scroll-down {
    0% { top: -50%; }
    100% { top: 0; }
  }
</style>
</head>
<body>

<!-- Caixa de presente -->
<div class="present-overlay" id="presentOverlay">
  <div class="present-box" id="presentBox">
    <div class="present-emoji">🎁</div>
    <div class="present-text">Clique no presente para abrir sua surpresa!</div>
  </div>
</div>

<!-- Áudio -->
<audio id="backgroundMusic" loop preload="auto" src="https://www.dropbox.com/scl/fi/9vw0p8krii3munrdgsfzc/Melim-Um-Mundo-Ideal-De-Aladdin-Official-Video-1.mp3?rlkey=ycq1iukki2b3tdh8qnbzs9xah&st=wz86fxn3&raw=1"></audio>

<div class="container" id="mainContent">

  <!-- Carrossel esquerdo -->
  <div class="carousel carousel-left">
    <div class="carousel-track" id="carouselLeft">
      <!-- imagens serão inseridas pelo JS -->
    </div>
  </div>

  <!-- Texto central -->
  <div class="text-center">
    <h1>Kaique ❤️ Laís</h1>
    <p>Nem no meu melhor sonho eu poderia imaginar que você voltaria para a minha vida e que, junto com você, viria uma revolução dentro de mim.</p>
    <p>Você me fez crescer, me fez evoluir como homem. Você se tornou a minha base, meu pilar mais forte e mais importante.</p>
    <p>Hoje, é impossível imaginar a vida sem o seu amor, sem o seu carinho, o seu desejo, a sua energia. Ao seu lado vivi momentos incríveis que jamais pensei que um dia teria.</p>
    <p>Com você, eu aprendi o que é amar com toda a minha essência.</p>
    <p>Tudo o que mais quero agora é construir um novo mundo com você. Um mundo só nosso.</p>
    <p>Nesses últimos anos, eu cresci tanto... e grande parte dessa evolução foi por sua causa por ter encontrado o amor da minha vida.</p>
    <p>Com você, eu descobri sentimentos novos, prazeres únicos, alegrias profundas. E hoje eu anseio por tudo que ainda vamos viver, pelo futuro lindo que estamos construindo juntos.</p>
    <p>Eu te amo com toda a minha existência, Laís. 💖</p>
  </div>

  <!-- Carrossel direito -->
  <div class="carousel carousel-right">
    <div class="carousel-track" id="carouselRight">
      <!-- imagens serão inseridas pelo JS -->
    </div>
  </div>

</div>

<script>
  // Links das imagens no formato direto do imgur
  const images = [
    "https://i.imgur.com/OGCNObf.jpg",
    "https://i.imgur.com/QrxCQYZ.jpg",
    "https://i.imgur.com/RufdWSR.jpg",
    "https://i.imgur.com/RlIF1sK.jpg",
    "https://i.imgur.com/R2wL5H6.jpg",
    "https://i.imgur.com/7x0hdlW.jpg",
    "https://i.imgur.com/r12nESz.jpg",
    "https://i.imgur.com/YH7Stcq.jpg",
    "https://i.imgur.com/Mf2PaKr.jpg",
    "https://i.imgur.com/zfEhgOB.jpg",
    "https://i.imgur.com/gZ6sU4N.jpg",
    "https://i.imgur.com/q5ctADZ.jpg",
    "https://i.imgur.com/CHlBB48.jpg",
    "https://i.imgur.com/zkxVjOD.jpeg",
    "https://i.imgur.com/lN6A0he.jpg",
    "https://i.imgur.com/0fqR5LE.jpg",
    "https://i.imgur.com/LL2dyYp.jpg",
    "https://i.imgur.com/wfpjpKS.jpg",
    "https://i.imgur.com/qnbJBwE.jpg",
    "https://i.imgur.com/7J1qygj.jpg",
    "https://i.imgur.com/bVtMlfL.jpg",
    "https://i.imgur.com/E4VrsgP.jpg",
    "https://i.imgur.com/Rui2F0V.jpg",
    "https://i.imgur.com/rsTSd31.jpg",
    "https://i.imgur.com/Qn3UQLo.jpg",
    "https://i.imgur.com/f7V0ZMR.jpg",
    "https://i.imgur.com/a9POCb4.jpg",
    "https://i.imgur.com/LRlXQYh.jpg",
    "https://i.imgur.com/n1L9jpu.jpg",
    "https://i.imgur.com/bVX9ANW.jpg",
    "https://i.imgur.com/bdDQcZS.jpg",
    "https://i.imgur.com/zSgqCh8.jpg"
  ];

  // Preenche o carrossel duplicando as imagens para efeito de loop
  function populateCarousel(containerId, imgs) {
    const container = document.getElementById(containerId);
    container.innerHTML = "";
    for(let i=0; i<2; i++) {
      imgs.forEach(src => {
        const img = document.createElement("img");
        img.src = src;
        img.alt = "Foto Kaique e Laís";
        container.appendChild(img);
      });
    }
  }

  // Só mostra o conteúdo após abrir o presente
  document.getElementById('presentBox').addEventListener('click', function() {
    document.getElementById('presentOverlay').style.opacity = '0';
    setTimeout(() => {
      document.getElementById('presentOverlay').style.display = 'none';
      document.getElementById('mainContent').style.display = 'flex';
      // Carrosséis
      populateCarousel("carouselLeft", images); // cima para baixo
      populateCarousel("carouselRight", [...images].reverse()); // baixo para cima
      // Música
      const music = document.getElementById("backgroundMusic");
      music.play();
    }, 500);
  });

</script>

</body>
</html>
