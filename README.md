<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Kaique ❤️ Laís</title>
<style>
  /* Reset e base */
  body, html {
    margin: 0; padding: 0;
    height: 100%;
    font-family: Arial, sans-serif;
    color: white;
    overflow: hidden;
    background: #111;
    position: relative;
  }

  /* Container principal: centraliza o texto */
  .content {
    position: relative;
    z-index: 10;
    max-width: 700px;
    margin: 0 auto;
    padding: 40px 20px;
    background: rgba(0,0,0,0.7);
    border-radius: 15px;
    top: 50%;
    transform: translateY(-50%);
    text-align: center;
  }

  .content h1 {
    font-size: 3rem;
    color: #ff3366;
    margin-bottom: 20px;
  }
  .content p {
    font-size: 1.1rem;
    line-height: 1.5;
    margin: 10px 0;
  }

  #play-button {
    margin-top: 25px;
    padding: 12px 30px;
    font-size: 1.2rem;
    background: #ff3366;
    border: none;
    border-radius: 30px;
    cursor: pointer;
    color: white;
    transition: background 0.3s ease;
  }
  #play-button:hover {
    background: #e62e5c;
  }

  /* Fundo animado */
  .background-carousel {
    position: fixed;
    top: 0; left: 0; right: 0; bottom: 0;
    overflow: hidden;
    z-index: 1;
    pointer-events: none; /* Para clicar no texto sem interferência */
  }
  .track {
    display: flex;
    flex-direction: column;
    animation: scrollVertical 60s linear infinite;
    height: 200%;
  }
  .track img {
    width: 100vw;
    height: auto;
    opacity: 0.2;
    object-fit: cover;
  }
  @keyframes scrollVertical {
    0% { transform: translateY(0); }
    100% { transform: translateY(-50%); }
  }
</style>
</head>
<body>

<div class="background-carousel">
  <div class="track" id="background-track"></div>
</div>

<div class="content">
  <h1>Kaique ❤️ Laís</h1>
  <p>Nem no meu melhor sonho eu poderia imaginar que você voltaria para a minha vida e que, junto com você, viria uma revolução dentro de mim.</p>
  <p>Você me fez crescer, me fez evoluir como homem. Você se tornou a minha base, meu pilar mais forte e mais importante.</p>
  <p>Hoje, é impossível imaginar a vida sem o seu amor, sem o seu carinho, o seu desejo, a sua energia. Ao seu lado vivi momentos incríveis que jamais pensei que um dia teria.</p>
  <p>Com você, eu aprendi o que é amar com toda a minha essência.</p>
  <p>Tudo o que mais quero agora é construir um novo mundo com você. Um mundo só nosso.</p>
  <p>Nesses últimos anos, eu cresci tanto... e grande parte dessa evolução foi por sua causa por ter encontrado o amor da minha vida.</p>
  <p>Com você, eu descobri sentimentos novos, prazeres únicos, alegrias profundas. E hoje eu anseio por tudo que ainda vamos viver, pelo futuro lindo que estamos construindo juntos.</p>
  <p>Eu te amo com toda a minha existência, Laís. 💖</p>

  <button id="play-button">▶️ Tocar música</button>
</div>

<audio id="music" loop>
  <source src="https://drive.google.com/uc?export=download&id=1IOdCm2ewNLEV9pmfPtMeFXaYV75U6AKT" type="audio/mpeg" />
  Seu navegador não suporta áudio.
</audio>

<script>
  const imageIds = [
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
    "1QZLaCkWeiJMu4e7USNvTIrpEb6ZDU4hh"
  ];

  const track = document.getElementById('background-track');

  // Carrega duas vezes para loop suave
  function loadImages() {
    [...imageIds, ...imageIds].forEach(id => {
      const img = document.createElement('img');
      img.src = `https://drive.google.com/uc?export=download&id=${id}`;
      track.appendChild(img);
    });
  }
  loadImages();

  // Música
  const music = document.getElementById('music');
  const playBtn = document.getElementById('play-button');

  playBtn.addEventListener('click', () => {
    music.play().catch(() => alert('Erro ao tocar a música'));
    playBtn.style.display = 'none';
  });
</script>

</body>
</html>
