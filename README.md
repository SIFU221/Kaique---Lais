<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Kaique ❤️ Laís</title>
  <style>
    body {
      font-family: 'Arial', sans-serif;
      background: linear-gradient(to right, #ffdde1, #ee9ca7);
      margin: 0;
      padding: 20px;
      color: #333;
      overflow-x: hidden;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      gap: 20px;
    }

    .carousel-container {
      width: 150px;
      height: 400px;
      overflow: hidden;
      border-radius: 20px;
      box-shadow: 0 4px 15px rgba(0,0,0,0.2);
      background: white;
    }

    .carousel {
      display: flex;
      flex-direction: column;
      animation-timing-function: linear;
      animation-iteration-count: infinite;
      animation-name: scroll;
      animation-duration: 45s;
      gap: 10px;
      padding: 10px 0;
    }

    .carousel.right {
      animation-direction: reverse;
    }

    @keyframes scroll {
      0% { transform: translateY(0); }
      100% { transform: translateY(-50%); }
    }

    .carousel img {
      width: 120px;
      height: 120px;
      object-fit: cover;
      border-radius: 15px;
      user-select: none;
      pointer-events: none;
    }

    .center-content {
      max-width: 600px;
      background: #fff;
      border-radius: 20px;
      padding: 25px;
      box-shadow: 0 4px 15px rgba(0,0,0,0.1);
      text-align: center;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      height: 400px;
      overflow-y: auto;
    }

    h1 {
      font-size: 2.5em;
      margin-bottom: 0.3em;
      color: #e91e63;
    }

    .declaration p {
      margin: 10px 0;
      line-height: 1.4em;
      font-size: 1.1em;
      color: #333;
    }

    .counter {
      font-size: 1.3em;
      margin: 15px 0 25px 0;
      font-weight: bold;
      color: #555;
    }

    .whatsapp-button {
      display: inline-block;
      padding: 15px 30px;
      background: #25D366;
      color: white;
      font-weight: bold;
      text-decoration: none;
      border-radius: 50px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.2);
      transition: background 0.3s;
      margin-bottom: 15px;
    }

    .whatsapp-button:hover {
      background: #1ebc59;
    }

    footer {
      font-size: 0.8em;
      color: #777;
      margin-top: 10px;
    }

    #qrcode {
      margin-top: 10px;
      display: inline-block;
    }
  </style>
</head>
<body>

  <!-- Carrossel esquerda -->
  <div class="carousel-container">
    <div class="carousel left" id="carousel-left">
      <!-- Imagens adicionadas via JS -->
    </div>
  </div>

  <!-- Conteúdo central -->
  <div class="center-content">
    <h1>Kaique ❤️ Laís</h1>

    <div class="declaration">
      <p>Nem no meu melhor sonho eu poderia imaginar que você voltaria para a minha vida e que, junto com você, viria uma revolução dentro de mim.</p>
      <p>Você me fez crescer, me fez evoluir como homem. Você se tornou a minha base, meu pilar mais forte e mais importante.</p>
      <p>Hoje, é impossível imaginar a vida sem o seu amor, sem o seu carinho, o seu desejo, a sua energia. Ao seu lado vivi momentos incríveis que jamais pensei que um dia teria.</p>
      <p>Com você, eu aprendi o que é amar com toda a minha essência.</p>
      <p>Tudo o que mais quero agora é construir um novo mundo com você. Um mundo só nosso.</p>
      <p>Nesses últimos anos, eu cresci tanto... e grande parte dessa evolução foi por sua causa por ter encontrado o amor da minha vida.</p>
      <p>Com você, eu descobri sentimentos novos, prazeres únicos, alegrias profundas.</p>
      <p>E hoje eu anseio por tudo que ainda vamos viver, pelo futuro lindo que estamos construindo juntos.</p>
      <p>Como diz a nossa música: "Um mundo ideal". E esse mundo, com você ao meu lado, é belo. É sereno. É tranquilo. É magnífico.</p>
      <p>Eu te amo com toda a minha existência, Laís.</p>
      <p>Feliz Dia dos Namorados, minha pequena. 💖</p>
    </div>

    <div class="counter">
      Estamos juntos há <span id="daysTogether">...</span>
    </div>

    <a href="https://wa.me/seunumerodetelefone" target="_blank" class="whatsapp-button">💬 Enviar mensagem no WhatsApp</a>

    <div id="qrcode"></div>
  </div>

  <!-- Carrossel direita -->
  <div class="carousel-container">
    <div class="carousel right" id="carousel-right">
      <!-- Imagens adicionadas via JS -->
    </div>
  </div>

  <!-- Música autoplay -->
  <audio autoplay loop>
    <source src="https://drive.google.com/uc?export=download&id=1IOdCm2ewNLEV9pmfPtMeFXaYV75U6AKT" type="audio/mpeg" />
    Seu navegador não suporta o elemento de áudio.
  </audio>

  <!-- QR Code library -->
  <script src="https://cdn.jsdelivr.net/npm/qrcode/build/qrcode.min.js"></script>
  <script>
    // Atualiza o contador
    function updateCounter() {
      const startDate = new Date(2023, 0, 4, 0, 0, 0); // 04/01/2023 início do namoro
      const now = new Date();

      let years = now.getFullYear() - startDate.getFullYear();
      let months = now.getMonth() - startDate.getMonth();
      let days = now.getDate() - startDate.getDate();
      let hours = now.getHours() - startDate.getHours();
      let minutes = now.getMinutes() - startDate.getMinutes();
      let seconds = now.getSeconds() - startDate.getSeconds();

      if (seconds < 0) {
        seconds += 60;
        minutes--;
      }
      if (minutes < 0) {
        minutes += 60;
        hours--;
      }
      if (hours < 0) {
        hours += 24;
        days--;
      }
      if (days < 0) {
        const prevMonth = new Date(now.getFullYear(), now.getMonth(), 0);
        days += prevMonth.getDate();
        months--;
      }
      if (months < 0) {
        months += 12;
        years--;
      }

      document.getElementById('daysTogether').textContent =
        `${years} ano${years !== 1 ? 's' : ''}, ` +
        `${months} mês${months !== 1 ? 'es' : ''}, ` +
        `${days} dia${days !== 1 ? 's' : ''}, ` +
        `${hours} hora${hours !== 1 ? 's' : ''}, ` +
        `${minutes} minuto${minutes !== 1 ? 's' : ''} e ` +
        `${seconds} segundo${seconds !== 1 ? 's' : ''}`;
    }
    updateCounter();
    setInterval(updateCounter, 1000);

    // QR Code com link do WhatsApp
    const phoneNumber = "seunumerodetelefone"; // Troque pelo seu número com DDI e DDD, ex: 5511999999999
    const whatsappUrl = `https://wa.me/${phoneNumber}`;
    QRCode.toCanvas(document.getElementById('qrcode'), whatsappUrl, { width: 120 }, function (error) {
      if (error) console.error(error);
    });

    // Array com os IDs das imagens (30 imagens)
    const imagesLeft = [
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
      "1OXHWaHBQX54H_5FKiR6gtZwTR9vDJkLC"
    ];

    const imagesRight = [
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
      "1pWHYJXlmec4hZtDkAn2cJu-C_Iq5rwzj"
    ];

    // Função para adicionar imagens no carrossel
    function addImagesToCarousel(carouselId, images) {
      const carousel = document.getElementById(carouselId);
      // Dupla repetição para animação infinita suave
      const allImages = images.concat(images);
      allImages.forEach(id => {
        const img = document.createElement('img');
        img.src = `https://drive.google.com/uc?export=download&id=${id}`;
        img.alt = "Foto";
        carousel.appendChild(img);
      });
    }

    addImagesToCarousel('carousel-left', imagesLeft);
    addImagesToCarousel('carousel-right', imagesRight);
  </script>
</body>
</html>
