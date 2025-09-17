<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <style>
    body {
      margin: 0;
      font-family: Arial, Helvetica, sans-serif;
      background-color: #f5f5f5;
      color: #333;
    }

    /* Portada */
    .cover {
      height: 100vh;
      background: linear-gradient(135deg,#1e1e2f,#3c3c58);
      color: white;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
    }
    .cover h1 {
      font-size: 4em;
      margin: 0;
    }
    .cover h2 {
      font-weight: normal;
      margin-top: 1em;
      font-size: 1.5em;
    }

    /* Índice */
    .index {
      background: white;
      padding: 2rem;
      max-width: 600px;
      margin: 3rem auto;
      border-radius: 12px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.1);
    }
    .index h3 {
      text-align: center;
      margin-top: 0;
      margin-bottom: 1.5rem;
      font-size: 2em;
    }
    .index ul {
      list-style: none;
      padding: 0;
    }
    .index li {
      margin: 0.7rem 0;
    }
    .index a {
      text-decoration: none;
      color: #1e1e2f;
      font-size: 1.2em;
      padding: 0.3rem 0.6rem;
      display: block;
      border-left: 4px solid #1e1e2f;
      transition: all 0.3s ease;
    }
    .index a:hover {
      background-color: #1e1e2f;
      color: white;
      padding-left: 1rem;
    }

    main {
      max-width: 700px;
      margin: 2rem auto;
      padding: 0 1rem;
    }

    details {
      margin-bottom: 1rem;
      background: white;
      border-radius: 8px;
      box-shadow: 0 2px 6px rgba(0,0,0,0.1);
      padding: 0.5rem 1rem;
    }
    summary {
      cursor: pointer;
      font-weight: bold;
      font-size: 1.1em;
      outline: none;
    }
  </style>
</head>
<body>

  <!-- Portada -->
  <section class="cover">
    <h1>SMX2_LuxurySL</h1>
    <h2>Katya Robuste • Pau Ferrer • Nazar Kishchuk</h2>
  </section>

  <!-- Índice bonito -->
  <section class="index">
    <h3>Índice</h3>
    <ul>
      <li><a href="#indice">Índice</a></li>
      <li><a href="#explicacion">Explicación</a></li>
      <li><a href="#guias">Guías de Uso</a></li>
      <li><a href="#diagrama">Diagrama de Red</a></li>
      <li><a href="#instalaciones">Instalaciones</a></li>
      <li><a href="#backups">BackUps</a></li>
      <li><a href="#dns">DNS</a></li>
      <li><a href="#firewall">FireWall</a></li>
      <li><a href="#blender">Blender</a></li>
      <li><a href="#scripts">Scripts</a></li>
      <li><a href="#aprendido">Qué hemos Aprendido</a></li>
      <li><a href="#incidencias">Incidencias</a></li>
    </ul>
  </section>

  <!-- Secciones -->
  <main>
    <details id="indice"><summary>Índice</summary></details>
    <details id="explicacion"><summary>Explicación</summary></details>
    <details id="guias"><summary>Guías de Uso</summary></details>
    <details id="diagrama"><summary>Diagrama de Red</summary></details>
    <details id="instalaciones"><summary>Instalaciones</summary></details>
    <details id="backups"><summary>BackUps</summary></details>
    <details id="dns"><summary>DNS</summary></details>
    <details id="firewall"><summary>FireWall</summary></details>
    <details id="blender"><summary>Blender</summary></details>
    <details id="scripts"><summary>Scripts</summary></details>
    <details id="aprendido"><summary>Qué hemos Aprendido</summary></details>
    <details id="incidencias"><summary>Incidencias</summary></details>
  </main>

</body>
</html>
