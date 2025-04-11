<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8" />
    <title>Asistente Turístico Navia</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <style>
      body {
        font-family: sans-serif;
        padding: 2rem;
        text-align: center;
      }
    </style>
  </head>
  <body>
    <h1>Asistente Turístico de Navia</h1>
    <p>Habla con nuestro chatbot para descubrir todo lo que puedes hacer en Navia.</p>

    <script>
      var vapiInstance = null;
      const assistant = "269eb90b-5f6e-481a-baad-64f04302a198"; // ← pon aquí tu bot ID
      const apiKey = "9e1bf0e5-3c4f-4b4f-a659-73391058a4ed";   // ← pon aquí tu API key
      const buttonConfig = {};       // puedes personalizar esto

      (function (d, t) {
        var g = document.createElement(t),
          s = d.getElementsByTagName(t)[0];
        g.src =
          "https://cdn.jsdelivr.net/gh/VapiAI/html-script-tag@latest/dist/assets/index.js";
        g.defer = true;
        g.async = true;
        s.parentNode.insertBefore(g, s);

        g.onload = function () {
          vapiInstance = window.vapiSDK.run({
            apiKey: apiKey,
            assistant: assistant,
            config: buttonConfig,
          });
        };
      })(document, "script");
    </script>
  </body>
</html>
