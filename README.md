<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>SMX2_LuxurySL</title>
  <style>
    /* Tipografía y colores base */
    body {
      margin: 0;
      font-family: "Segoe UI", Roboto, sans-serif;
      background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
      color: #eee;
      line-height: 1.6;
    }

    h1, h2 {
      margin: 0;
    }

    /* Cabecera */
    .header {
      text-align: center;
      padding: 3rem 1rem;
    }

    .header h1 {
      font-size: 3.5rem;
      font-weight: 700;
      letter-spacing: 1px;
      background: linear-gradient(90deg,#00f0ff,#00aaff);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }

    .header img {
      max-width: 220px;
      width: 80%;
      height: auto;
      margin: 1.5rem 0;
      border-radius: 1rem;
      box-shadow: 0 8px 20px rgba(0,0,0,0.5);
    }

    .header h2 {
      color: #bbb;
      font-weight: 400;
      font-size: 1.2rem;
    }

    /* Secciones details */
    details {
      background: rgba(255,255,255,0.05);
      border-radius: 12px;
      margin: 1rem auto;
      max-width: 900px;
      padding: 1rem 1.2rem;
      box-shadow: 0 4px 15px rgba(0,0,0,0.3);
      transition: transform 0.2s ease, background 0.3s ease;
    }

    details:hover {
      transform: translateY(-3px);
      background: rgba(255,255,255,0.08);
    }

    summary {
      cursor: pointer;
      font-size: 1.3rem;
      font-weight: 600;
      outline: none;
    }

    details[open] summary {
      color: #00f0ff;
    }

    details p {
      margin-top: 0.8rem;
      font-size: 1rem;
    }

    /* Texto azul eléctrico en la primera sección */
    .explicacion-texto {
      color: #00f0ff;
    }

    /* Animación suave al abrir */
    details[open] p {
      animation: fadein 0.4s ease;
    }
    @keyframes fadein {
      from { opacity: 0; transform: translateY(-5px); }
      to   { opacity: 1; transform: translateY(0); }
    }

    /* Responsive */
    @media (max-width: 600px) {
      .header h1 { font-size: 2.4rem; }
      summary { font-size: 1.1rem; }
    }
  </style>
</head>
<body>

  <div class="header">
    <h1>SMX2_LuxurySL</h1>
    <img src="https://i.imgur.com/YePpr4D.png" alt="Logo Luxury_SL">
    <h2>Katya Robuste • Pau Ferrer • Nazar Kishchuk</h2>
  </div>

  <details open>
    <summary>Explicación</summary>
    <p class="explicacion-texto">
      Hola, Somos el grupo de SMX2_LuxurySL. Nuestro proyecto tiene varias apps que usaremos,
      ya como Blender y c/c++ (un tipo de script de arduino).
      El nombre que hemos escogido es el nombre donde muestra una empresa de lujo,
      pero de coches de lujo. Mostraremos el modelo de un coche en 3D y con un motor
      de arduino que irá con un mando controlado donde tendrás varios efectos especiales (aún falta).
    </p>
  </details>

  <details>
    <summary>Guías de Uso</summary>
    <p>Aquí va el contenido de la sección Guías de Uso.</p>
  </details>

  <details>
    <summary>Diagrama de Red</summary>
    <p>Aquí va el contenido de la sección Diagrama de Red.</p>
  </details>

  <details>
    <summary>Instalaciones</summary>
    <p>Aquí va el contenido de la sección Instalaciones.</p>
  </details>

  <details>
    <summary>BackUps</summary>
    <p>Aquí va el contenido de la sección BackUps.</p>
  </details>

  <details>
    <summary>DNS</summary>
    <p>Aquí va el contenido de la sección DNS.</p>
  </details>

  <details>
    <summary>FireWall</summary>
    <p>Aquí va el contenido de la sección FireWall.</p>
  </details>

  <details>
    <summary>Blender</summary>
    <p>Aquí va el contenido de la sección Blender.</p>
  </details>

  <details>
    <summary>Scripts</summary>
    <p>Aquí va el contenido de la sección Scripts.</p>
  </details>

  <details>
    <summary>Qué hemos Aprendido</summary>
    <p>Aquí va el contenido de la sección Qué hemos Aprendido.</p>
  </details>

  <details>
    <summary>Incidencias</summary>
    <p>Aquí va el contenido de la sección Incidencias.</p>
  </details>

</body>
</html>
