<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Kaique & Laís - Carrossel Fotos & Texto</title>
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
    }

    .carousel-container {
      width: 300px;
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
      animation-duration: 30s;
      animation-iteration-count: infinite;
    }
    .carousel.right {
      animation-name: scrollDown;
      animation-duration: 30s;
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
      height: 300px;
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

    /* Responsividade */
    @media (max-width: 1000px) {
      body {
        flex-direction: column;
        height: auto;
        padding: 40px 10px;
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

<script>
  // URLs das imagens — verifique se estão "Públicas" no Google Drive!
  const leftImages = [
    'https://drive.google.com/uc?export=view&id=1b4_jjHmz3uvtuJ-ioPT_CWk8UGQFsTZh',
    'https://drive.google.com/uc?export=view&id=1TECYPXZOjPT_81S8Ln0LBs7-VIGs4vKO',
    'https://drive.google.com/uc?export=view&id=1vBa7L-JD94slg6Oj37lKVNBHAciGFSpV',
    'https://drive.google.com/uc?export=view&id=1LE1hU7avGLPktt-43mbScU2VzVghuX1v',
    'https://drive.google.com/uc?export=view&id=1W5bB8HedOE04oje2491V-ns0MNdDHSXh',
    'https://drive.google.com/uc?export=view&id=1DN7ild0A5qManalSEOP6eXtWal2bOHzX',
    'https://drive.google.com/uc?export=view&id=1dnYGFg0YiNHDEgzV9a8GFSwAAbl4YD2u',
    'https://drive.google.com/uc?export=view&id=1EycDhYHKZjzD057xpZG84TIZ-Vnw9q8e'
  ];

  const rightImages = [
    'https://drive.google.com/uc?export=view&id=15LBdyWxILbUnPzrzcEJLf0ePz_xs8AGR',
    'https://drive.google.com/uc?export=view&id=1KtPu1pWqby3jsOIB7bQIRT5wuBl7OfOZ',
    'https://drive.google.com/uc?export=view&id=1UlxOsaTX8BSakrUW6m_Xxt01d8GGB64m',
    'https://drive.google.com/uc?export=view&id=1Yt0C2NYFwjgnyf9tQSvVtRt_7UhzU0cN',
    'https://drive.google.com/uc?export=view&id=1yBVoej6KxXHRwiSj5L9_vrso_vB7gJFS',
    'https://drive.google.com/uc?export=view&id=1WTWiEhPPNdMS_7j_o0j1upBBIHCTpK6t',
    'https://drive.google.com/uc?export=view&id=1QZLaCkWeiJMu4e7USNvTIrpEb6ZDU4hh',
    'https://drive.google.com/uc?export=view&id=1ydiXhj1uPNlBegAM6YiZH1tPxLI5JhpI'
  ];

  function populateCarousel(carouselId, images) {
    const carousel = document.getElementById(carouselId);
    // Duplica as imagens para o efeito contínuo
    const imagesRepeated = images.concat(images);
    imagesRepeated.forEach(src => {
      const img = document.createElement('img');
      img.src = src;
      img.alt = "Foto Kaique & Laís";
      carousel.appendChild(img);
    });
  }

  populateCarousel('carousel-left', leftImages);
  populateCarousel('carousel-right', rightImages);
</script>

</body>
</html>
