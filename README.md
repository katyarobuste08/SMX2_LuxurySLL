<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>SMX2_LuxurySL</title>
<style>
  body {
    margin:0;
    font-family: 'Segoe UI', sans-serif;
    background: #1e1e2f;
    color: #f0f0f0;
    scroll-behavior: smooth;
  }

  /* Layout */
  main { display:flex; padding:2rem; gap:2rem; min-height:100vh; }

  /* Índice lateral */
  nav#indice {
    flex:0 0 220px;
    position: sticky;
    top: 1rem;
    background:#2c2c44;
    padding:1rem;
    border-radius:10px;
  }
  nav#indice h3 {
    color:#ff4c4c;
    text-align:center;
    margin-bottom:1rem;
  }
  nav#indice ul { list-style:none; padding:0; }
  nav#indice li { margin:0.6rem 0; }
  nav#indice a { color:#ff4c4c; text-decoration:none; display:block; padding:0.3rem; border-radius:5px; transition:0.2s; }
  nav#indice a:hover { background:#3c3c58; }

  /* Secciones */
  section.content { flex:1; }
  details {
    background:#2c2c44;
    margin-bottom:1rem;
    padding:0.5rem 1rem;
    border-radius:8px;
    transition: 0.3s;
  }
  details[open] { background:#3c3c58; }
  summary { font-weight:bold; cursor:pointer; font-size:1.1em; }
  details p { margin-top:0.5rem; padding-left:0.5rem; }
</style>
</head>
<body>

<main>
  <!-- Índice -->
  <nav id="indice">
    <h3>Índice</h3>
    <ul>
      <li><a href="#" data-target="explicacion">Explicación</a></li>
      <li><a href="#" data-target="guias">Guías de Uso</a></li>
      <li><a href="#" data-target="diagrama">Diagrama de Red</a></li>
      <li><a href="#" data-target="instalaciones">Instalaciones</a></li>
      <li><a href="#" data-target="backups">BackUps</a></li>
      <li><a href="#" data-target="dns">DNS</a></li>
      <li><a href="#" data-target="firewall">FireWall</a></li>
      <li><a href="#" data-target="blender">Blender</a></li>
      <li><a href="#" data-target="scripts">Scripts</a></li>
      <li><a href="#" data-target="aprendido">Qué hemos Aprendido</a></li>
      <li><a href="#" data-target="incidencias">Incidencias</a></li>
    </ul>
  </nav>

  <!-- Contenido -->
  <section class="content">
    <details id="explicacion"><summary>Explicación</summary><p>Aquí va el contenido de la sección Explicación.</p></details>
    <details id="guias"><summary>Guías de Uso</summary><p>Aquí va el contenido de Guías de Uso.</p></details>
    <details id="diagrama"><summary>Diagrama de Red</summary><p>Aquí va el contenido de Diagrama de Red.</p></details>
    <details id="instalaciones"><summary>Instalaciones</summary><p>Aquí va el contenido de Instalaciones.</p></details>
    <details id="backups"><summary>BackUps</summary><p>Aquí va el contenido de BackUps.</p></details>
    <details id="dns"><summary>DNS</summary><p>Aquí va el contenido de DNS.</p></details>
    <details id="firewall"><summary>FireWall</summary><p>Aquí va el contenido de FireWall.</p></details>
    <details id="blender"><summary>Blender</summary><p>Aquí va el contenido de Blender.</p></details>
    <details id="scripts"><summary>Scripts</summary><p>Aquí va el contenido de Scripts.</p></details>
    <details id="aprendido"><summary>Qué hemos Aprendido</summary><p>Aquí va el contenido de Qué hemos Aprendido.</p></details>
    <details id="incidencias"><summary>Incidencias</summary><p>Aquí va el contenido de Incidencias.</p></details>
  </section>
</main>

<script>
  // Abrir sección al clicar en índice
  const links = document.querySelectorAll('nav#indice a');
  links.forEach(link => {
    link.addEventListener('click', e => {
      e.preventDefault();
      const target = document.getElementById(link.dataset.target);
      document.querySelectorAll('details').forEach(d => d.removeAttribute('open'));
      target.setAttribute('open', true);
      target.scrollIntoView({behavior:'smooth', block:'start'});
    });
  });
</script>

</body>
</html>
