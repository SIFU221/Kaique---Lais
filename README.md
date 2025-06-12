<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Kaique & Laís - Carrossel Fotos & Texto & Música</title>
  <style>
    body {
      margin: 0;
      background: #111;
      color: #f0f0f0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      display: flex;
      height: 100vh;
      overflow: hidden;
      align-items: center;
      justify-content: center;
      gap: 30px;
      padding: 20px;
      flex-direction: column;
    }

    .main-content {
      display: flex;
      align-items: center;
      gap: 30px;
      flex: 1 1 auto;
      width: 100%;
      max-width: 1200px;
      overflow: hidden;
    }

    .carousel-container {
      width: 280px;
      height: 400px;
      overflow: hidden;
      border-radius: 15px;
      box-shadow: 0 0 20px rgba(255,255,255,0.2);
      position: relative;
      background: #222;
      flex-shrink: 0;
    }

    .carousel {
      display: flex;
      flex-direction: column;
      height: 100%;
      animation-timing-function: linear;
    }

    /* Animações para scroll vertical */
    .carousel.left {
      animation-name: scrollUp;
      animation-duration: 40s;
      animation-iteration-count: infinite;
    }
    .carousel.right {
      animation-name: scrollDown;
      animation-duration: 40s;
      animation-iteration-count: infinite;
    }

    @keyframes scrollUp {
      0% { transform: translateY(0); }
      100% { transform: translateY(-50%); }
    }

    @keyframes scrollDown {
      0% { transform: translateY(-50%); }
      100% { transform: translateY(0); }
    }

    .carousel img {
      width: 100%;
      height: 280px;
      object-fit: cover;
      border-bottom: 3px solid #444;
      user-select: none;
      pointer-events: none;
    }

    .center-text {
      max-width: 600px;
      padding: 30px 20px;
      background: rgba(30, 30, 30, 0.85);
      border-radius: 15px;
      box-shadow: 0 0 20px rgba(255,255,255,0.1);
      text-align: center;
      overflow-y: auto;
      max-height: 400px;
      flex-shrink: 1;
    }

    .center-text h1 {
      font-size: 3rem;
      margin-bottom: 20px;
      color: #ff4060;
    }

    .center-text p {
      margin-bottom: 15px;
      font-size: 1.1rem;
      line-height: 1.5;
    }

    /* Scrollbar personalizada */
    .center-text::-webkit-scrollbar {
      width: 8px;
    }
    .center-text::-webkit-scrollbar-thumb {
      background-color: #ff4060;
      border-radius: 4px;
    }

    /* Player musica */
    .music-player {
      margin-top: 15px;
      width: 100%;
      max-width: 600px;
      text-align: center;
    }

    audio {
      width: 100%;
      outline: none;
      border-radius: 8px;
      box-shadow: 0 0 10px #ff4060aa;
    }

    /* Responsividade */
    @media (max-width: 1000px) {
      .main-content {
        flex-direction: column;
        max-width: 90vw;
        gap: 30px;
      }
      .carousel-container {
        width: 90vw;
        height: 250px;
      }
      .carousel img {
        height: 180px;
      }
      .center-text {
        max-width: 90vw;
        max-height: none;
      }
    }
  </style>
</head>
<body>

  <div class="main-content">
    <div class="carousel-container">
      <div class="carousel left" id="carousel-left"></div>
    </div>

    <div class="center-text">
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

    <div class="carousel-container">
      <div class="carousel right" id="carousel-right"></div>
    </div>
  </div>

  <div class="music-player">
    <audio controls loop>
      <source src="https://drive.google.com/uc?export=view&id=1IOdCm2ewNLEV9pmfPtMeFXaYV75U6AKT" type="audio/mpeg" />
      Seu navegador não suporta o elemento de áudio.
    </audio>
  </div>

<script>
  // Lista dos IDs das imagens divididas em duas partes (primeiras 15 na esquerda, resto na direita)
  const allImageIds = [
    "1b4_jjHmz3uvtuJ-ioPT_CWk8UGQFsTZh",
    "1TECYPXZOjPT_81S8Ln0LBs7-VIGs4vKO",
    "1vBa7L-JD94slg6Oj37lKVNBHAciGFSpV",
    "1LE1hU7avGLPktt-43mbScU2VzVghuX1v",
    "1W5bB8HedOE04oje2491V-ns0MNdDHSXh",
    "1DN7ild0A5qManalSEOP6eXtWal2bOHzX",
    "1dnYGFg0YiNHDEgzV9a8GFSwAAbl4YD2u",
    "1EycDhYHKZjzD057xpZG84TIZ-Vnw9q8e",
    "15LBdyWxILbUnPzrzcEJLf0ePz_xs8AGR",
    "1KtPu1pWqby3jsOIB7bQIRT5wuBl7OfOZ",
    "1UlxOsaTX8BSakrUW6m_Xxt01d8GGB64m",
    "1Yt0C2NYFwjgnyf9tQSvVtRt_7UhzU0cN",
    "1yBVoej6KxXHRwiSj5L9_vrso_vB7gJFS",
    "1WTWiEhPPNdMS_7j_o0j1upBBIHCTpK6t",
    "1QZLaCkWeiJMu4e7USNvTIrpEb6ZDU4hh",
    "1ydiXhj1uPNlBegAM6YiZH1tPxLI5JhpI",
    "1E5LWmtXmoIGv0vEZ1VKiWrAOigxTP6nM",
    "1XZBFhMqqR5JqHO31thaSBRCqi3sVQ6tN",
    "1OXHWaHBQX54H_5FKiR6gtZwTR9vDJkLC",
    "1vHKt_gAJRJOv3VjcrjoaL-rTMm1caf6Y",
    "1ufnp0c7BJIB4WuWePnmiNjV3DhMkqVmg",
    "1gj5Y8Q7HnBvU2h2zmlflj1tM3NdNlPL3",
    "1utWIp_-DxTDnSYGkkx0aVrdhyhfKAIbW",
    "1cerhBMfN7JXtpyJ2aExqV5YqPRv2ibGo",
    "1JtXN7D_2vjMhl2BrwKDRiMv4ZwNl9ht1",
    "1XkEL7kLE3ELmzi-a__e2lgF45iJYjpz9",
    "1bsyIy-wWIEkZZeRtKs21jsalRYMoewvq",
    "1ibtGOSzMTsaQPM_HKgAnnEuvt-bJk01I",
    "1oUSl0UGqN-OZCS7_trn09nMKdQ90h9xH",
    "1pWHYJXlmec4hZtDkAn2cJu-C_Iq5rwzj",
    "1pG1QSqNbOmpd2lJwfAXsA54tTRF21ntm",
    "14x8v6g2mlxtvp0M3a9pZ44XKhyS2HRfR"
  ];

  // Separar os IDs para carrossel esquerdo e direito
  const leftImages = allImageIds.slice(0, 15);
  const rightImages = allImageIds.slice(15);

  function populateCarousel(containerId, imageIds) {
    const container = document.getElementById(containerId);
    // Para o scroll contínuo duplicamos a lista
    const imgs = imageIds.concat(imageIds);
    imgs.forEach(id => {
      const img = document.createElement('img');
      img.src = `https://drive.google.com/uc?export=view&id=${id}`;
      img.alt = "Foto Kaique & Laís";
      container.appendChild(img);
    });
  }

  populateCarousel('carousel-left', leftImages);
  populateCarousel('carousel-right', rightImages);
</script>

</body>
</html>
