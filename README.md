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

  /* Portada */
  .portada {
    height:100vh;
    display:flex;
    flex-direction:column;
    justify-content:center;
    align-items:center;
    text-align:center;
    background: linear-gradient(135deg,#1e1e2f,#3c3c58);
  }
  .portada h1 { font-size:4em; margin-bottom:0.3em; }
  .portada h2 { font-weight: normal; color: #ccc; }

  /* Layout */
  main { display:flex; padding:2rem; gap:2rem; }

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

<section class="portada">
  <h1>SMX2_LuxurySL</h1>
  <h2>Katya Robuste • Pau Ferrer • Nazar Kishchuk</h2>
</section>

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
    <details id="explicacion"><summary>Explicación</summary><p>Aquí va el texto de la sección Explicación.</p></details>
    <details id="guias"><summary>Guías de Uso</summary><p>Aquí va el texto de la sección Guías de Uso.</p></details>
    <details id="diagrama"><summary>Diagrama de Red</summary><p>Aquí va el texto de la sección Diagrama de Red.</p></details>
    <details id="instalaciones"><summary>Instalaciones</summary><p>Aquí va el texto de la sección Instalaciones.</p></details>
    <details id="backups"><summary>BackUps</summary><p>Aquí va el texto de la sección BackUps.</p></details>
    <details id="dns"><summary>DNS</summary><p>Aquí va el texto de la sección DNS.</p></details>
    <details id="firewall"><summary>FireWall</summary><p>Aquí va el texto de la sección FireWall.</p></details>
    <details id="blender"><summary>Blender</summary><p>Aquí va el texto de la sección Blender.</p></details>
    <details id="scripts"><summary>Scripts</summary><p>Aquí va el texto de la sección Scripts.</p></details>
    <details id="aprendido"><summary>Qué hemos Aprendido</summary><p>Aquí va el texto de la sección Qué hemos Aprendido.</p></details>
    <details id="incidencias"><summary>Incidencias</summary><p>Aquí va el texto de la sección Incidencias.</p></details>
  </section>
</main>

<script>
  // Función que abre la sección y hace scroll
  const links = document.querySelectorAll('nav#indice a');
  links.forEach(link => {
    link.addEventListener('click', e => {
      e.preventDefault();
      const target = document.getElementById(link.dataset.target);

      // Cerrar todas
      document.querySelectorAll('details').forEach(d => d.removeAttribute('open'));
      
      // Abrir la sección deseada
      target.setAttribute('open', true);

      // Scroll suave
      target.scrollIntoView({behavior: 'smooth', block:'start'});
    });
  });
</script>

</body>
</html>
