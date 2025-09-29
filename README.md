<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Página Gamer Interactiva</title>
  <style>
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      margin: 0;
      background-color: #1a1a1d;
      color: #f5f5f5;
      display: flex;
      flex-direction: column;
      min-height: 100vh;
    }

    .container {
      flex: 1;
      display: flex;
      justify-content: center;
      align-items: center;
      padding: 40px 20px;
    }

    .box {
      background-color: #2d2d30;
      padding: 30px;
      border-radius: 15px;
      box-shadow: 0 0 15px #0ff;
      text-align: center;
      width: 100%;
      max-width: 400px;
    }

    h1 {
      color: #0ff;
      margin-bottom: 15px;
    }

    input[type="text"] {
      padding: 10px;
      width: 90%;
      font-size: 16px;
      border-radius: 8px;
      border: 2px solid #0ff;
      background-color: #1a1a1d;
      color: #f5f5f5;
      margin-bottom: 15px;
    }

    button {
      padding: 10px 20px;
      font-size: 16px;
      background-color: #0ff;
      color: #1a1a1d;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      transition: background 0.3s ease;
    }

    button:hover {
      background-color: #00cccc;
    }

    .message {
      margin-top: 20px;
      font-size: 18px;
      color: #0ff;
    }

    footer {
      background-color: #111;
      color: #ccc;
      text-align: center;
      padding: 20px 10px;
      font-size: 14px;
      border-top: 2px solid #0ff;
    }

    footer p {
      margin: 5px 0;
    }

    .footer-icons {
      margin-top: 10px;
    }

    .footer-icons span {
      margin: 0 8px;
      font-size: 18px;
    }
  </style>
</head>
<body>

  <div class="container">
    <div class="box">
      <h1>🎮 Mundo Gamer 🎮</h1>
      <p>Escribe tu nombre para empezar la aventura:</p>
      <input type="text" id="nombre" placeholder="Tu nombre gamer...">
      <br>
      <button onclick="saludar()">¡Jugar!</button>
      <div class="message" id="mensaje"></div>
    </div>
  </div>

  <footer>
    <p>🌟 Página creada para gamers como tú 🌟</p>
    <p>&copy; 2025 Mundo Gamer. Todos los derechos reservados.</p>
    <div class="footer-icons">
      <span>🕹️</span>
      <span>👾</span>
      <span>🎧</span>
      <span>💻</span>
    </div>
  </footer>

  <script>
    function saludar() {
      const nombre = document.getElementById('nombre').value.trim();
      const mensaje = document.getElementById('mensaje');

      if (nombre) {
        mensaje.textContent = `¡Bienvenido, ${nombre}! Prepárate para la misión. 🚀`;
      } else {
        mensaje.textContent = '⚠️ Ingresa tu nombre para comenzar tu aventura.';
      }
    }
  </script>

</body>
</html>
