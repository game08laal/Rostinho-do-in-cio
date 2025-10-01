<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Robô Fofo</title>
  <style>
    body {
      background: #f0f8ff;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
    }

    .robo {
      width: 60vw;
      height: 70vh;
      background: #0b3d91; /* azul escuro */
      border-radius: 200px; /* quase oval */
      position: relative;
      box-shadow: 0 8px 25px rgba(0,0,0,0.3);
      animation: flutuar 2s ease-in-out infinite; /* movimento mais rápido */
    }

    @keyframes flutuar {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-12px); } /* sobe um pouco mais */
    }

    /* olhos */
    .olho {
      width: 22vh;   /* olhos maiores */
      height: 22vh;
      background: #87cefa; /* azul claro */
      border-radius: 50%;
      position: absolute;
      top: 23%;
      animation: piscar 3s infinite; /* piscar mais rápido */
    }
    .olho.esq { left: 17%; }
    .olho.dir { right: 17%; }

    @keyframes piscar {
      0%, 90%, 100% { transform: scaleY(1); }
      95% { transform: scaleY(0.1); }
    }

    /* sorriso preenchido */
    .boca {
      width: 160px;
      height: 80px;
      background: #87cefa; /* azul claro */
      border-radius: 0 0 120px 120px; /* curva suave */
      position: absolute;
      bottom: 18%;
      left: 50%;
      transform: translateX(-50%);
    }
  </style>
</head>
<body>
  <div class="robo">
    <div class="olho esq"></div>
    <div class="olho dir"></div>
    <div class="boca"></div>
  </div>
</body>
</html>

