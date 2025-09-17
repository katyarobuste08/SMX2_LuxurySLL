<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<!-- Librería para mostrar modelos 3D -->
<script type="module" src="https://unpkg.com/@google/model-viewer/dist/model-viewer.min.js"></script>
<style>
  body { 
    margin:0; 
    font-family:'Segoe UI', sans-serif; 
    background:#1e1e2f; 
    color:#f0f0f0; 
    padding:2rem; 
  }

  .titulo { 
    text-align:center; 
    margin-bottom:2rem; 
  } 
  .titulo h1 { 
    font-size:4em; 
    margin-bottom:0.3em; 
  } 
  .titulo h2 { 
    font-weight: normal; 
    color:#ccc; 
  }

  details { 
    background:#2c2c44; 
    margin-bottom:1rem; 
    padding:0.5rem 1rem; 
    border-radius:8px; 
    transition:0.3s; 
  } 
  details[open] { 
    background:#3c3c58; 
  } 
  summary { 
    font-weight:bold; 
    cursor:pointer; 
    font-size:1.2em; 
  } 
  details p { 
    margin-top:0.5rem; 
    padding-left:0.5rem; 
  }

  /* Estilo para el chat/mensajes */
  #chat { 
    background:#2c2c44; 
    padding:1rem; 
    border-radius:8px; 
    max-height:200px; 
    overflow-y:auto; 
    margin-top:1rem; 
  } 
  #chat div { 
    margin-bottom:0.5rem; 
    padding:0.3rem 0.5rem; 
    background:#3c3c58; 
    border-radius:5px; 
  } 
  #mensaje-form { 
    display:flex; 
    gap:0.5rem; 
    margin-top:0.5rem; 
  } 
  #mensaje-form input { 
    flex:1; 
    padding:0.5rem; 
    border-radius:5px; 
    border:none; 
  } 
  #mensaje-form button { 
    padding:0.5rem 1rem; 
    border-radius:5px; 
    border:none; 
    background:#ff4c4c; 
    color:white; 
    cursor:pointer; 
  } 
  #mensaje-form button:hover { 
    background:#ff6666; 
  }

  /* Modelo 3D */
  model-viewer { 
    width:100%; 
    height:400px; 
    border-radius:8px; 
    background:#1e1e2f; 
  }
</style>
</head>
<body>

<div class="titulo">
  <h1>SMX2_LuxurySL</h1>
  <h2>Katya Robuste • Pau Ferrer • Nazar Kishchuk</h2>
</div>

<details>
  <summary>Explicación</summary>
  <p>Nuestro proyecto consiste en crear un coche funcional y controlable combinando diseño 3D, con Arduino y programación. La idea es unir Blender, Arduino y un mando para conseguir un vehículo personalizable (luces, controles y más).</p>
</details>

<details>
  <summary>Guías de Uso</summary>
  <p>Instrucciones detalladas sobre cómo usar el coche y el mando interactivo.</p>
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
  <p>Aquí puedes ver un modelo 3D del coche:</p>
  <model-viewer src="tu_modelo.glb" alt="Modelo 3D del coche" auto-rotate camera-controls shadow-intensity="1"></model-viewer>
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
  <summary>Mensajes</summary>
  <div id="chat"></div>
  <form id="mensaje-form">
    <input type="text" id="mensaje-input" placeholder="Escribe un mensaje">
    <button type="submit">Enviar</button>
  </form>
</details>

<details>
  <summary>Incidencias</summary>
  <p>Aquí va el contenido de la sección Incidencias.</p>
</details>

</body>
</html>
