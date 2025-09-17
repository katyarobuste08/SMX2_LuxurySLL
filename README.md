<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
</head>
<body>

  <!-- Portada -->
  <section style="display:flex;flex-direction:column;justify-content:center;align-items:center;
                  height:100vh;background:linear-gradient(135deg,#1e1e2f,#3c3c58);
                  color:white;text-align:center;">
    <h1 style="font-size:4em;margin:0;">SMX2_LuxurySL</h1>
    <h2 style="font-weight:normal;margin-top:1em;">Katya Robuste • Pau Ferrer • Nazar Kishchuk</h2>
  </section>

  <!-- Índice -->
  <main style="padding:2rem;">
    <details id="indice">
      <summary>Índice</summary>
      <ul style="margin-top:1rem;list-style:none;padding-left:0;line-height:1.8;">
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
    </details>

    <!-- Secciones reales -->
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

  </main>

  <script>
    function openSection(id) {
      // Cierra todas las secciones
      document.querySelectorAll('details').forEach(d => d.removeAttribute('open'));
      // Abre la sección clicada
      document.getElementById(id).setAttribute('open', true);
      // Hace scroll suave hasta la sección
      document.getElementById(id).scrollIntoView({ behavior: 'smooth' });
    }
  </script>

</body>
</html>
