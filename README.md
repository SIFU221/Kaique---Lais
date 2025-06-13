<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=1920, initial-scale=1" />
<title>Kaique ❤️ Laís</title>
<style>
  * { box-sizing: border-box; }
  body {
    margin: 0;
    background: #000;
    color: #eee;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    min-height: 100vh;
    min-width: 100vw;
    overflow-x: hidden;
    overflow-y: auto;
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
    padding: 40px 80px;
    box-shadow: 0 8px 32px #000a;
    display: flex;
    flex-direction: column;
    align-items: center;
    cursor: pointer;
    transition: transform 0.2s;
    border: 4px solid #ff5c5c;
    max-width: 90vw;
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
  .feed-container {
    width: 100vw;
    min-height: 100vh;
    display: none;
    flex-direction: column;
    align-items: center;
    justify-content: flex-start;
    background: #000;
    overflow-x: hidden;
    padding-top: 40px;
    padding-bottom: 40px;
  }
  .feed-post {
    background: #181818;
    border-radius: 18px;
    box-shadow: 0 2px 16px #0006;
    margin-bottom: 40px;
    width: 500px;
    max-width: 96vw;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 24px 18px 18px 18px;
    position: relative;
  }
  .feed-img {
    width: 100%;
    max-height: 500px;
    object-fit: cover;
    border-radius: 12px;
    margin-bottom: 18px;
    box-shadow: 0 2px 8px #0008;
  }
  .feed-caption {
    color: #fff;
    font-size: 1.1rem;
    font-weight: bold;
    text-align: center;
    margin-bottom: 8px;
  }
  .feed-text {
    color: #ddd;
    font-size: 1rem;
    text-align: center;
    margin-bottom: 0;
    font-weight: bold;
  }
  .feed-title {
    color: #ff5c5c;
    font-size: 2rem;
    font-weight: bold;
    margin-bottom: 12px;
    text-align: center;
  }
  @media (max-width: 700px) {
    .feed-post {
      width: 98vw;
      padding: 10px 2vw 10px 2vw;
    }
    .feed-title {
      font-size: 1.3rem;
    }
    .feed-caption, .feed-text {
      font-size: 0.95rem;
    }
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

<div class="feed-container" id="mainContent">
  <!-- Os "posts" do feed serão inseridos aqui pelo JS -->
</div>

<script>
  // Imagens do "feed"
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

  // Texto principal
  const feedText = `
    <div class="feed-title">Kaique ❤️ Laís</div>
    <div class="feed-caption">Nem no meu melhor sonho eu poderia imaginar que você voltaria para a minha vida e que, junto com você, viria uma revolução dentro de mim.</div>
    <div class="feed-text">Você me fez crescer, me fez evoluir como homem. Você se tornou a minha base, meu pilar mais forte e mais importante.</div>
    <div class="feed-text">Hoje, é impossível imaginar a vida sem o seu amor, sem o seu carinho, o seu desejo, a sua energia. Ao seu lado vivi momentos incríveis que jamais pensei que um dia teria.</div>
    <div class="feed-text">Com você, eu aprendi o que é amar com toda a minha essência.</div>
    <div class="feed-text">Tudo o que mais quero agora é construir um novo mundo com você. Um mundo só nosso.</div>
    <div class="feed-text">Nesses últimos anos, eu cresci tanto... e grande parte dessa evolução foi por sua causa por ter encontrado o amor da minha vida.</div>
    <div class="feed-text">Com você, eu descobri sentimentos novos, prazeres únicos, alegrias profundas. E hoje eu anseio por tudo que ainda vamos viver, pelo futuro lindo que estamos construindo juntos.</div>
    <div class="feed-text">Eu te amo com toda a minha existência, Laís. 💖</div>
  `;

  // Monta o feed igual Instagram
  function montarFeed() {
    const main = document.getElementById('mainContent');
    main.innerHTML = '';

    // Primeiro post: só o texto
    const postTexto = document.createElement('div');
    postTexto.className = 'feed-post';
    postTexto.innerHTML = feedText;
    main.appendChild(postTexto);

    // Demais posts: imagem + legenda opcional
    images.forEach((src, idx) => {
      const post = document.createElement('div');
      post.className = 'feed-post';
      post.innerHTML = `
        <img class="feed-img" src="${src}" alt="Foto Kaique e Laís" />
      `;
      main.appendChild(post);
    });
  }

  // Só mostra o conteúdo após abrir o presente
  document.getElementById('presentBox').addEventListener('click', function() {
    document.getElementById('presentOverlay').style.opacity = '0';
    setTimeout(() => {
      document.getElementById('presentOverlay').style.display = 'none';
      document.getElementById('mainContent').style.display = 'flex';
      montarFeed();
      // Música
      const music = document.getElementById("backgroundMusic");
      music.play();
    }, 500);
  });
</script>

</body>
</html>
