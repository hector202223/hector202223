<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Visualizador HTML</title>
  <style>
    body {
      font-family: sans-serif;
      margin: 2rem;
      background: #f9f9f9;
    }

    h1 {
      text-align: center;
      margin-bottom: 1rem;
    }

    textarea {
      width: 100%;
      height: 200px;
      font-family: monospace;
      font-size: 1rem;
      padding: 1rem;
      border: 1px solid #ccc;
      border-radius: 6px;
      resize: vertical;
    }

    button {
      display: block;
      margin: 1rem auto;
      padding: 0.75rem 1.5rem;
      font-size: 1rem;
      border: none;
      background: #007acc;
      color: white;
      border-radius: 6px;
      cursor: pointer;
    }

    iframe {
      width: 100%;
      height: 300px;
      border: 1px solid #ccc;
      border-radius: 6px;
      margin-top: 1rem;
      background: white;
    }
  </style>
</head>
<body>
  <h1>🧪 Visualizador de HTML</h1>

  <textarea id="editor" placeholder="Escribí tu código HTML aquí..."></textarea>
  <button onclick="verHTML()">Ver HTML</button>

  <iframe id="preview"></iframe>

  <script>
    function verHTML() {
      const html = document.getElementById("editor").value;
      const iframe = document.getElementById("preview");
      iframe.srcdoc = html;
    }
  </script>
</body>
</html>
