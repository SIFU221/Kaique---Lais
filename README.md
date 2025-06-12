<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Kaique ❤️ Laís - Carrossel Duplo</title>
  <style>
    /* Reset básico */
    * {
      box-sizing: border-box;
    }
    body {
      margin: 0; 
      font-family: Arial, sans-serif;
      background: linear-gradient(to right, #ffdde1, #ee9ca7);
      color: #333;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      overflow: hidden;
    }

    /* Container principal */
    .container {
      display: flex;
      max-width: 1200px;
      width: 100%;
      height: 80vh;
      gap: 20px;
      background: rgba(255,255,255,0.9);
      border-radius: 16px;
      padding: 20px;
      box-shadow: 0 4px 15px rgba(0,0,0,0.2);
    }

    /* Estilo dos carrosseis (esquerda e direita) */
    .carousel {
      flex: 1;
      overflow: hidden;
      border-radius: 12px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
      position: relative;
    }
    .carousel-inner {
      display: flex;
      flex-direction: column;
      gap: 10px;
      animation-timing-function: linear;
      animation-iteration-count: infinite;
    }
    /* animação carrossel esquerdo sobe */
    .left .carousel-inner {
      animation-name: scrollUp;
      animation-duration: 40s;
    }
    /* animação carrossel direito desce */
    .right .carousel-inner {
      animation-name: scrollDown;
      animation-duration: 40s;
    }
    @keyframes scrollUp {
      0% { transform: translateY(0); }
      100% { transform: translateY(-50%); }
    }
    @keyframes scrollDown {
      0% { transform: translateY(-50%); }
      100% { transform: translateY(0); }
    }
    /* imagens do carrossel */
    .carousel-inner img {
      width: 100%;
      border-radius: 8px;
      object-fit: cover;
      height: 120px;
      user-select: none;
      pointer-events: none;
    }

    /* Coluna de texto central */
    .text-center {
      flex: 1.5;
      padding: 0 20px;
      display: flex;
      flex-direction: column;
      justify-content: center;
      text-align: center;
      font-size: 1.1rem;
      line-height: 1.5;
    }
    .text-center h1 {
      font-size: 2.5rem;
      margin-bottom: 1rem;
      color: #d6336c;
    }

    /* Responsividade simples */
    @media (max-width: 900px) {
      .container {
        flex-direction: column;
        height: auto;
      }
      .carousel, .text-center {
        width: 100%;
        flex: none;
      }
      .carousel-inner img {
        height: 100px;
      }
      .text-center h1 {
        font-size: 2rem;
      }
    }
  </style>
</head>
<body>

  <div class="container">
    <div class="carousel left" aria-label="Carrossel de fotos esquerda">
      <div class="carousel-inner" id="left-carousel">
        <!-- Imagens esquerda serão inseridas aqui -->
      </div>
    </div>

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

    <div class="carousel right" aria-label="Carrossel de fotos direita">
      <div class="carousel-inner" id="right-carousel">
        <!-- Imagens direita serão inseridas aqui -->
      </div>
    </div>
  </div>

  <script>
    // IDs das imagens do Google Drive (30 imagens)
    const images = [
      "1b4_jjHmz3uvtuJ-ioPT_CWk8UGQFsTZh",
      "1LE1hU7avGLPktt-43mbScU2VzVghuX1v",
      "1QZLaCkWeiJMu4e7USNvTIrpEb6ZDU4hh",
      "1TECYPXZOjPT_81S8Ln0LBs7-VIGs4vKO",
      "1W5bB8HedOE04oje2491V-ns0MNdDHSXh",
      "1ydiXhj1uPNlBegAM6YiZH1tPxLI5JhpI",
      "1vBa7L-JD94slg6Oj37lKVNBHAciGFSpV",
      "1DN7ild0A5qManalSEOP6eXtWal2bOHzX",
      "1E5LWmtXmoIGv0vEZ1VKiWrAOigxTP6nM",
      "1dnYGFg0YiNHDEgzV9a8GFSwAAbl4YD2u",
      "1EycDhYHKZjzD057xpZG84TIZ-Vnw9q8e",
      "1XZBFhMqqR5JqHO31thaSBRCqi3sVQ6tN",
      "15LBdyWxILbUnPzrzcEJLf0ePz_xs8AGR",
      "1KtPu1pWqby3jsOIB7bQIRT5wuBl7OfOZ",
      "1OXHWaHBQX54H_5FKiR6gtZwTR9vDJkLC",
      "1UlxOsaTX8BSakrUW6m_Xxt01d8GGB64m",
      "1Yt0C2NYFwjgnyf9tQSvVtRt_7UhzU0cN",
      "1vHKt_gAJRJOv3VjcrjoaL-rTMm1caf6Y",
      "1yBVoej6KxXHRwiSj5L9_vrso_vB7gJFS",
      "1WTWiEhPPNdMS_7j_o0j1upBBIHCTpK6t",
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

    // Divide em 2 grupos de 15 imagens para os carrosséis da esquerda e direita
    const leftImages = images.slice(0, 15);
    const rightImages = images.slice(15, 30);

    // Função para criar tag img com URL direta do Google Drive
    function createImgTag(id) {
      return `<img src="https://drive.google.com/uc?export=view&id=${id}" loading="lazy" alt="Foto do casal" />`;
    }

    // Inserir imagens duplicadas para loop suave
    const leftCarousel = document.getElementById("left-carousel");
    leftCarousel.innerHTML = leftImages.map(createImgTag).join('') + leftImages.map(createImgTag).join('');

    const rightCarousel = document.getElementById("right-carousel");
    rightCarousel.innerHTML = rightImages.map(createImgTag).join('') + rightImages.map(createImgTag).join('');
  </script>

</body>
</html>
