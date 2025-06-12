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
    }
    h1 {
      font-size: 2.5em;
      margin-bottom: 0.3em;
      text-align: center;
    }
    .container {
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 40px;
      flex-wrap: nowrap;
      max-width: 1200px;
      margin: 0 auto;
    }
    .carousel {
      width: 200px;
      height: 350px;
      overflow: hidden;
      border-radius: 20px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.15);
      background: white;
      position: relative;
    }
    .carousel img {
      width: 100%;
      height: 350px;
      object-fit: cover;
      position: absolute;
      top: 0;
      left: 0;
      opacity: 0;
      transition: opacity 1s ease-in-out;
    }
    .carousel img.active {
      opacity: 1;
      position: relative;
    }
    .middle-content {
      max-width: 500px;
      background: white;
      padding: 20px;
      border-radius: 16px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
      text-align: center;
    }
    .counter {
      font-size: 1.5em;
      margin: 20px 0;
      font-weight: bold;
    }
    .declaration p {
      margin: 0.7em 0;
      line-height: 1.4em;
    }
    .whatsapp-button {
      display: inline-block;
      padding: 12px 25px;
      background: #25D366;
      color: white;
      font-weight: bold;
      text-decoration: none;
      border-radius: 50px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.2);
      transition: background 0.3s;
      margin-top: 10px;
    }
    .whatsapp-button:hover {
      background: #1ebc59;
    }
    footer {
      margin-top: 2em;
      font-size: 0.8em;
      color: #555;
      text-align: center;
    }
    .qr-code {
      margin-top: 20px;
    }
  </style>
</head>
<body>
  <h1>Kaique ❤️ Laís</h1>

  <div class="container">
    <!-- Carrossel Esquerda -->
    <div class="carousel" id="carouselLeft">
      <img src="https://picsum.photos/id/1015/200/350" class="active" alt="Imagem 1"/>
      <img src="https://picsum.photos/id/1016/200/350" alt="Imagem 2"/>
      <img src="https://picsum.photos/id/1018/200/350" alt="Imagem 3"/>
      <img src="https://picsum.photos/id/1020/200/350" alt="Imagem 4"/>
      <img src="https://picsum.photos/id/1024/200/350" alt="Imagem 5"/>
    </div>

    <!-- Texto e Contador no meio -->
    <div class="middle-content">
      <div class="declaration">
        <p>Nem no meu melhor sonho eu poderia imaginar que você voltaria para a minha vida e que, junto com você, viria uma revolução dentro de mim.</p>
        <p>Você me fez crescer, me fez evoluir como homem. Você se tornou a minha base, meu pilar mais forte e mais importante.</p>
        <p>Hoje, é impossível imaginar a vida sem o seu amor, sem o seu carinho, o seu desejo, a sua energia. Ao seu lado vivi momentos incríveis que jamais pensei que um dia teria.</p>
        <p>Com você, eu aprendi o que é amar com toda a minha essência.</p>
        <p>Tudo o que mais quero agora é construir um novo mundo com você. Um mundo só nosso.</p>
        <p>Nesses últimos anos, eu cresci tanto... e grande parte dessa evolução foi por sua causa por ter encontrado o amor da minha vida.</p>
        <p>Com você, eu descobri sentimentos novos, prazeres únicos, alegrias profundas. E hoje eu anseio por tudo que ainda vamos viver, pelo futuro lindo que estamos construindo juntos.</p>
        <p>Como diz a nossa música: "Um mundo ideal". E esse mundo, com você ao meu lado, é belo. É sereno. É tranquilo. É magnífico.</p>
        <p>Eu te amo com toda a minha existência, Laís.</p>
        <p>Feliz Dia dos Namorados, minha pequena. 💖</p>
      </div>

      <div class="counter">
        Estamos juntos há <span id="daysTogether">...</span>!
      </div>

      <a href="https://wa.me/5591999999999" class="whatsapp-button" target="_blank" rel="noopener noreferrer">Falar no WhatsApp</a>

      <div class="qr-code">
        <img src="https://api.qrserver.com/v1/create-qr-code/?size=150x150&data=https://wa.me/5591999999999" alt="QR Code WhatsApp"/>
      </div>
    </div>

    <!-- Carrossel Direita -->
    <div class="carousel" id="carouselRight">
      <img src="https://picsum.photos/id/1027/200/350" class="active" alt="Imagem 1"/>
      <img src="https://picsum.photos/id/1031/200/350" alt="Imagem 2"/>
      <img src="https://picsum.photos/id/1035/200/350" alt="Imagem 3"/>
      <img src="https://picsum.photos/id/1039/200/350" alt="Imagem 4"/>
      <img src="https://picsum.photos/id/1043/200/350" alt="Imagem 5"/>
    </div>
  </div>

  <!-- Música embutida oculta -->
  <audio src="https://drive.google.com/uc?export=download&id=1IOdCm2ewNLEV9pmfPtMeFXaYV75U6AKT" autoplay loop controls style="display:none;"></audio>

  <script>
    // Contador de tempo juntos
    function updateCounter() {
      const startDate = new Date(2023, 0, 4, 0, 0, 0); // 04/01/2023
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
        `${hours}h ${minutes}m ${seconds}s`;
    }

    setInterval(updateCounter, 1000);
    updateCounter();

    // Carrossel automático para os dois lados
    function carouselEffect(carouselId) {
      const carousel = document.getElementById(carouselId);
      const images = carousel.querySelectorAll('img');
      let current = 0;

      setInterval(() => {
        images[current].classList.remove('active');
        current = (current + 1) % images.length;
        images[current].classList.add('active');
      }, 4000);
    }

    carouselEffect('carouselLeft');
    carouselEffect('carouselRight');
  </script>
</body>
</html>
