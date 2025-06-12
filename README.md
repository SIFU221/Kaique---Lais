<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Carrossel com Fotos e Música</title>
<style>
  body {
    background: #111;
    color: #eee;
    font-family: Arial, sans-serif;
    overflow-x: hidden;
    margin: 0;
    padding: 0;
  }
  .container {
    display: flex;
    align-items: center;
    justify-content: center;
    height: 100vh;
    gap: 20px;
    padding: 20px;
  }
  .carousel {
    width: 200px;
    height: 350px;
    overflow: hidden;
    border-radius: 10px;
    box-shadow: 0 0 15px #222;
    position: relative;
    background: #222;
  }
  .carousel-inner {
    display: flex;
    flex-direction: column;
    animation-timing-function: linear;
    animation-iteration-count: infinite;
  }
  .carousel-left .carousel-inner {
    animation-name: scrollUp;
    animation-duration: 30s;
  }
  .carousel-right .carousel-inner {
    animation-name: scrollDown;
    animation-duration: 30s;
  }
  .carousel img {
    width: 200px;
    height: 350px;
    object-fit: cover;
    display: block;
  }
  .center-text {
    width: 300px;
    text-align: center;
    font-size: 28px;
    font-weight: bold;
    color: #f0a500;
    text-shadow: 1px 1px 6px #000;
  }
  @keyframes scrollUp {
    0% { transform: translateY(0); }
    100% { transform: translateY(calc(-350px * 15)); }
  }
  @keyframes scrollDown {
    0% { transform: translateY(calc(-350px * 15)); }
    100% { transform: translateY(0); }
  }
</style>
</head>
<body>

<div class="container">
  <div class="carousel carousel-left">
    <div class="carousel-inner">
      <!-- 15 imagens do lado esquerdo -->
      <img src="https://drive.google.com/uc?export=download&id=1b4_jjHmz3uvtuJ-ioPT_CWk8UGQFsTZh" alt="Foto 1" />
      <img src="https://drive.google.com/uc?export=download&id=1TECYPXZOjPT_81S8Ln0LBs7-VIGs4vKO" alt="Foto 2" />
      <img src="https://drive.google.com/uc?export=download&id=1vBa7L-JD94slg6Oj37lKVNBHAciGFSpV" alt="Foto 3" />
      <img src="https://drive.google.com/uc?export=download&id=1LE1hU7avGLPktt-43mbScU2VzVghuX1v" alt="Foto 4" />
      <img src="https://drive.google.com/uc?export=download&id=1W5bB8HedOE04oje2491V-ns0MNdDHSXh" alt="Foto 5" />
      <img src="https://drive.google.com/uc?export=download&id=1DN7ild0A5qManalSEOP6eXtWal2bOHzX" alt="Foto 6" />
      <img src="https://drive.google.com/uc?export=download&id=1dnYGFg0YiNHDEgzV9a8GFSwAAbl4YD2u" alt="Foto 7" />
      <img src="https://drive.google.com/uc?export=download&id=1EycDhYHKZjzD057xpZG84TIZ-Vnw9q8e" alt="Foto 8" />
      <img src="https://drive.google.com/uc?export=download&id=15LBdyWxILbUnPzrzcEJLf0ePz_xs8AGR" alt="Foto 9" />
      <img src="https://drive.google.com/uc?export=download&id=1KtPu1pWqby3jsOIB7bQIRT5wuBl7OfOZ" alt="Foto 10" />
      <img src="https://drive.google.com/uc?export=download&id=1UlxOsaTX8BSakrUW6m_Xxt01d8GGB64m" alt="Foto 11" />
      <img src="https://drive.google.com/uc?export=download&id=1Yt0C2NYFwjgnyf9tQSvVtRt_7UhzU0cN" alt="Foto 12" />
      <img src="https://drive.google.com/uc?export=download&id=1yBVoej6KxXHRwiSj5L9_vrso_vB7gJFS" alt="Foto 13" />
      <img src="https://drive.google.com/uc?export=download&id=1WTWiEhPPNdMS_7j_o0j1upBBIHCTpK6t" alt="Foto 14" />
      <img src="https://drive.google.com/uc?export=download&id=1QZLaCkWeiJMu4e7USNvTIrpEb6ZDU4hh" alt="Foto 15" />
    </div>
  </div>

  <div class="center-text">
    Kaique & Laís<br />
    Nosso amor eterno
  </div>

  <div class="carousel carousel-right">
    <div class="carousel-inner">
      <!-- 15 imagens do lado direito -->
      <img src="https://drive.google.com/uc?export=download&id=1ydiXhj1uPNlBegAM6YiZH1tPxLI5JhpI" alt="Foto 16" />
      <img src="https://drive.google.com/uc?export=download&id=1E5LWmtXmoIGv0vEZ1VKiWrAOigxTP6nM" alt="Foto 17" />
      <img src="https://drive.google.com/uc?export=download&id=1XZBFhMqqR5JqHO31thaSBRCqi3sVQ6tN" alt="Foto 18" />
      <img src="https://drive.google.com/uc?export=download&id=1OXHWaHBQX54H_5FKiR6gtZwTR9vDJkLC" alt="Foto 19" />
      <img src="https://drive.google.com/uc?export=download&id=1vHKt_gAJRJOv3VjcrjoaL-rTMm1caf6Y" alt="Foto 20" />
      <img src="https://drive.google.com/uc?export=download&id=1ufnp0c7BJIB4WuWePnmiNjV3DhMkqVmg" alt="Foto 21" />
      <img src="https://drive.google.com/uc?export=download&id=1gj5Y8Q7HnBvU2h2zmlflj1tM3NdNlPL3" alt="Foto 22" />
      <img src="https://drive.google.com/uc?export=download&id=1utWIp_-DxTDnSYGkkx0aVrdhyhfKAIbW" alt="Foto 23" />
      <img src="https://drive.google.com/uc?export=download&id=1cerhBMfN7JXtpyJ2aExqV5YqPRv2ibGo" alt="Foto 24" />
      <img src="https://drive.google.com/uc?export=download&id=1JtXN7D_2vjMhl2BrwKDRiMv4ZwNl9ht1" alt="Foto 25" />
      <img src="https://drive.google.com/uc?export=download&id=1XkEL7kLE3ELmzi-a__e2lgF45iJYjpz9" alt="Foto 26" />
      <img src="https://drive.google.com/uc?export=download&id=1bsyIy-wWIEkZZeRtKs21jsalRYMoewvq" alt="Foto 27" />
      <img src="https://drive.google.com/uc?export=download&id=1ibtGOSzMTsaQPM_HKgAnnEuvt-bJk01I" alt="Foto 28" />
      <img src="https://drive.google.com/uc?export=download&id=1oUSl0UGqN-OZCS7_trn09nMKdQ90h9xH" alt="Foto 29" />
      <img src="https://drive.google.com/uc?export=download&id=1pWHYJXlmec4hZtDkAn2cJu-C_Iq5rwzj" alt="Foto 30" />
    </div>
  </div>
</div>

<!-- Música -->
<audio autoplay loop controls style="position: fixed; bottom: 10px; left: 10px; width: 300px;">
  <source src="https://drive.google.com/uc?export=download&id=1IOdCm2ewNLEV9pmfPtMeFXaYV75U6AKT" type="audio/mpeg" />
  Seu navegador não suporta áudio.
</audio>

</body>
</html>
