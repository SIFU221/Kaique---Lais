<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Kaique ❤️ Laís</title>
<style>
  * {
    box-sizing: border-box;
  }
  body {
    margin: 0;
    background: #111;
    color: #eee;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    display: flex;
    height: 100vh;
    overflow: hidden;
    /* Imagem de fundo fixa */
    background-image: url('https://i.imgur.com/0sRJbDK.jpg');
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
  }
  body::before {
    content: "";
    position: fixed;
    inset: 0;
    background: rgba(17,17,17,0.7);
    z-index: 0;
    pointer-events: none;
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
  }
  .text-center {
    width: 40%;
    max-width: 600px;
    text-align: center;
    line-height: 1.5;
  }
  .text-center h1 {
    font-size: 2.5rem;
    margin-bottom: 0.5rem;
    color: #ff5c5c;
  }
  .text-center p {
    font-size: 1.1rem;
    margin: 0.5rem 0;
    color: #ddd;
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
  .music-control {
    position: fixed;
    top: 20px;
    right: 30px;
    background: #ff5c5c;
    color: white;
    border: none;
    padding: 12px 24px;
    font-size: 1.2rem;
    border-radius: 30px;
    cursor: pointer;
    box-shadow: 0 0 10px #ff5c5c;
    user-select: none;
    z-index: 10;
  }
  .music-control:hover {
    background: #ff3a3a;
  }
</style>
</head>
<body>

<!-- Botão de controle da música -->
<button class="music-control" id="musicControl">Tocar Música</button>
<audio id="backgroundMusic" loop preload="auto" src="https://www.dropbox.com/scl/fi/9vw0p8krii3munrdgsfzc/Melim-Um-Mundo-Ideal-De-Aladdin-Official-Video-1.mp3?rlkey=ycq1iukki2b3tdh8qnbzs9xah&st=wz86fxn3&raw=1"></audio>

<div class="container">

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
    // Duas vezes para looping suave
    for(let i=0; i<2; i++) {
      imgs.forEach(src => {
        const img = document.createElement("img");
        img.src = src;
        img.alt = "Foto Kaique e Laís";
        container.appendChild(img);
      });
    }
  }

  populateCarousel("carouselLeft", images); // cima para baixo
  populateCarousel("carouselRight", [...images].reverse()); // baixo para cima

  // Música
  const music = document.getElementById("backgroundMusic");
  const btn = document.getElementById("musicControl");

  btn.addEventListener("click", () => {
    if(music.paused) {
      music.play();
      btn.textContent = "Pausar Música";
    } else {
      music.pause();
      btn.textContent = "Tocar Música";
    }
  });
</script>

</body>
</html>
