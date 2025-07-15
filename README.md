<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <title>Contador de Dias de Namoro</title>
  <style>
    body {
      background-color: #ffe6f0;
      font-family: Arial, sans-serif;
      text-align: center;
      padding: 50px;
      color: #333;
    }

    h1 {
      font-size: 2.5em;
      margin-bottom: 10px;
    }

    .contador {
      font-size: 2em;
      font-weight: bold;
      margin-top: 20px;
    }

    .emoji {
      font-size: 1.5em;
    }
  </style>
</head>
<body>
  <h1>💖 Contador de Dias de Namoro 💖</h1>
  <div class="contador" id="contador"></div>

  <script>
    const dataInicio = new Date("2025-01-11T00:00:00");
    
    function atualizarContador() {
      const agora = new Date();
      const diffMs = agora - dataInicio;
      
      const dias = Math.floor(diffMs / (1000 * 60 * 60 * 24));
      const horas = agora.getHours();
      const minutos = agora.getMinutes();
      const segundos = agora.getSeconds();
      
      document.getElementById("contador").innerHTML =
        `Estamos juntos há <span class="emoji">💕</span> ${dias} dias, ${horas}h ${minutos}min ${segundos}s <span class="emoji">💕</span>`;
    }

    atualizarContador();
    setInterval(atualizarContador, 1000);
  </script>
</body>
</html>
