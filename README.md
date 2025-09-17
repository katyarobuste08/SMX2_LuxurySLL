<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>SMX2_LuxurySL</title>
  <style>
    /* Reset básico */
    * { margin:0; padding:0; box-sizing:border-box; font-family: 'Segoe UI', sans-serif; }

    body {
      background-color: #1e1e2f;
      color: #f0f0f0;
      line-height: 1.6;
      scroll-behavior: smooth;
    }

    a { text-decoration: none; color: #ff4c4c; transition: 0.3s; }
    a:hover { color: #ffa0a0; }

    /* Portada */
    .portada {
      display:flex;
      flex-direction:column;
      justify-content:center;
      align-items:center;
      height:100vh;
      background: linear-gradient(135deg,#1e1e2f,#3c3c58);
      text-align:center;
    }
    .portada h1 {
      font-size:4em;
      margin-bottom: 0.5em;
    }
    .portada h2 {
      font-weight: normal;
      font-size:1.5em;
      color:#ccc;
    }

    /* Layout principal */
    main {
      display: flex;
      padding: 2rem;
      gap: 2rem;
    }

    /* Índice lateral */
    nav#indice {
      flex:0 0 200px;
      background:#2c2c44;
      padding:1rem;
      border-radius:10px;
      position: sticky;
      top: 1rem;
      height: fit-content;
    }
    nav#indice h3 {
      margin-bottom:1rem;
      color:#ff4c4c;
      font-size:1.2em;
      text-align:center;
    }
    nav#indice ul { list-style:none; }
    nav#indice li { margin:0.7rem 0; }
    nav#indice li a { display:block; padding:0.3rem 0.5rem; border-radius:5px; }
    nav#indice li a:hover { background:#3c3c58; }

    /* Contenido de secciones */
    section.content {
      flex:1;
    }
    details {
      background:#2c2c44;
      margin-bottom:1rem;
      padding:0.5rem 1rem;
      border-radius:8px;
      transition: 0.3s;
    }
    details[open] {
      background:#3c3c58;
    }
    summary {
      font-weight:bold;
      font-size:1.1em;
      cursor:pointer;
      outline:none;
    }
    details p {
      margin-top:0.5rem;
      padding-left:0.5rem;
    }
  </style>
</head>
<body>

  <!-- Portada -->
  <section class="portada">
    <h1>SMX2_LuxurySL</h1>
    <h2>Katya Robuste • Pau Ferrer • Nazar Kishchuk</h2>
  </section>

  <!-- Layout principal: índice + contenido -->
  <main>
    <!-- Índice lateral -->
    <nav id="indice">
      <h3>Índice</h3>
      <ul>
        <li><a href="#explicacion" onclick="openSection('explicacion')">Explicación</a></li>
        <li><a href="#guias" onclick="openSection('guias')">Guías de Uso</a></li>
        <li><a href="#diagrama" onclick="openSection('diagrama')">Diagrama de Red</a></li>
        <li><a href="#instalaciones" onclick="openSection('instalaciones')">Instalaciones</a></li>
        <li><a href="#backups" onclick="openSection('backups')">BackUps</a></li>
        <li><a href="#dns" onclick="openSection('dns')">DNS</a></li>
        <li><a href="#firewall" onclick="openSection('firewall')">FireWall</a></li>
        <li><a href="#blender" onclick="openSection('blender')">Blender</a></li>
        <li><a href="#scripts" onclick="openSection('scripts')">Scripts</a></li>
        <li><a href="#aprendido" onclick="openSection('aprendido')">Qué hemos Aprendido</a></li>
        <li><a href="#incidencias" onclick="openSection('incidencias')">Incidencias</a></li>
      </ul>
    </nav>

    <!-- Contenido -->
    <section class="content">
      <details id="explicacion"><summary>Explicación</summary>
        <p>Aquí va el texto de la sección Explicación.</p>
      </details>

      <details id="guias"><summary>Guías de Uso</summary>
        <p>Aquí va el texto de la sección Guías de Uso.</p>
      </details>

      <details id="diagrama"><summary>Diagrama de Red</summary>
        <p>Aquí va el texto de la sección Diagrama de Red.</p>
      </details>

      <details id="instalaciones"><summary>Instalaciones</summary>
        <p>Aquí va el texto de la sección Instalaciones.</p>
      </details>

      <details id="backups"><summary>BackUps</summary>
        <p>Aquí va el texto de la sección BackUps.</p>
      </details>

      <details id="dns"><summary>DNS</summary>
        <p>Aquí va el texto de la sección DNS.</p>
      </details>

      <details id="firewall"><summary>FireWall</summary>
        <p>Aquí va el texto de la sección FireWall.</p>
      </details>

      <details id="blender"><summary>Blender</summary>
        <p>Aquí va el texto de la sección Blender.</p>
      </details>

      <details id="scripts"><summary>Scripts</summary>
        <p>Aquí va el texto de la sección Scripts.</p>
      </details>

      <details id="aprendido"><summary>Qué hemos Aprendido</summary>
        <p>Aquí va el texto de la sección Qué hemos Aprendido.</p>
      </details>

      <details id="incidencias"><summary>Incidencias</summary>
        <p>Aquí va el texto de la sección Incidencias.</p>
      </details>
    </section>
  </main>

  <script>
    function openSection(id) {
      // Cierra todas las secciones
      document.querySelectorAll('details').forEach(d => d.removeAttribute('open'));
      // Abre la sección clicada
      const section = document.getElementById(id);
      section.setAttribute('open', true);
      // Scroll suave
      section.scrollIntoView({ behavior: 'smooth', block: 'start' });
    }
  </script>

</body>
</html>
