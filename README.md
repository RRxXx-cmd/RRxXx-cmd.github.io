<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Página Interactiva</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: linear-gradient(to right, #74ebd5, #ACB6E5);
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
    }
    .container {
      background-color: white;
      padding: 30px;
      border-radius: 15px;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
      text-align: center;
      max-width: 400px;
    }
    input[type="text"] {
      padding: 10px;
      width: 80%;
      font-size: 16px;
      border: 2px solid #ccc;
      border-radius: 8px;
      margin-bottom: 15px;
    }
    button {
      padding: 10px 20px;
      font-size: 16px;
      background-color: #74ebd5;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      transition: background 0.3s ease;
    }
    button:hover {
      background-color: #56c5d0;
    }
    .message {
      margin-top: 20px;
      font-size: 18px;
      color: #333;
    }
  </style>
</head>
<body>
  <div class="container">
    <h2>¡Bienvenido!</h2>
    <p>Escribe tu nombre para recibir un saludo:</p>
    <input type="text" id="nombre" placeholder="Tu nombre aquí">
    <br>
    <button onclick="saludar()">Saludar</button>
    <div class="message" id="mensaje"></div>
  </div>

  <script>
    function saludar() {
      const nombre = document.getElementById('nombre').value.trim();
      const mensaje = document.getElementById('mensaje');

      if (nombre) {
        mensaje.textContent = `¡Hola, ${nombre}! Gracias por visitar esta página. 😊`;
      } else {
        mensaje.textContent = 'Por favor, ingresa tu nombre primero.';
      }
    }
  </script>
</body>
</html>
