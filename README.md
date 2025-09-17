<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
</head>
<body style="margin:0; font-family:'Segoe UI', sans-serif; background:#1e1e2f; color:#f0f0f0; padding:2rem;">

<div style="text-align:center; margin-bottom:2rem;">
  <h1 style="font-size:4em; margin-bottom:0.3em;">SMX2_LuxurySL</h1>
  <h2 style="font-weight: normal; color:#ccc;">Katya Robuste • Pau Ferrer • Nazar Kishchuk</h2>
</div>

<details style="background:#2c2c44; margin-bottom:1rem; padding:0.5rem 1rem; border-radius:8px; transition:0.3s;">
  <summary style="font-weight:bold; cursor:pointer; font-size:1.2em;">Explicación</summary>
  <p style="margin-top:0.5rem; padding-left:0.5rem;">Nuestro proyecto consiste en crear un coche funcional y controlable combinando diseño 3D, con Arduino y programación. La idea es unir Blender, Arduino y un mando para conseguir un vehículo personalizable (luces, controles y más).</p>
</details>

<details style="background:#2c2c44; margin-bottom:1rem; padding:0.5rem 1rem; border-radius:8px; transition:0.3s;">
  <summary style="font-weight:bold; cursor:pointer; font-size:1.2em;">Guías de Uso</summary>
  <p style="margin-top:0.5rem; padding-left:0.5rem;">Instrucciones detalladas sobre cómo usar el coche y el mando interactivo.</p>
</details>

<details style="background:#2c2c44; margin-bottom:1rem; padding:0.5rem 1rem; border-radius:8px; transition:0.3s;">
  <summary style="font-weight:bold; cursor:pointer; font-size:1.2em;">Blender</summary>
  <p style="margin-top:0.5rem; padding-left:0.5rem;">Aquí puedes ver un modelo 3D del coche:</p>
  <!-- Librería model-viewer solo en esta sección -->
  <script type="module" src="https://unpkg.com/@google/model-viewer/dist/model-viewer.min.js"></script>
  <model-viewer src="tu_modelo.glb" alt="Modelo 3D del coche" auto-rotate camera-controls shadow-intensity="1" style="width:100%; height:400px; border-radius:8px; background:#1e1e2f;"></model-viewer>
</details>

<details style="background:#2c2c44; margin-bottom:1rem; padding:0.5rem 1rem; border-radius:8px; transition:0.3s;">
  <summary style="font-weight:bold; cursor:pointer; font-size:1.2em;">Mensajes</summary>
  <div id="chat" style="background:#2c2c44; padding:1rem; border-radius:8px; max-height:200px; overflow-y:auto; margin-top:1rem;"></div>
  <form id="mensaje-form" style="display:flex; gap:0.5rem; margin-top:0.5rem;">
    <input type="text" id="mensaje-input" placeholder="Escribe un mensaje" style="flex:1; padding:0.5rem; border-radius:5px; border:none;">
    <button type="submit" style="padding:0.5rem 1rem; border-radius:5px; border:none; background:#ff4c4c; color:white; cursor:pointer;">Enviar</button>
  </form>
</details>

<details style="background:#2c2c44; margin-bottom:1rem; padding:0.5rem 1rem; border-radius:8px; transition:0.3s;">
  <summary style="font-weight:bold; cursor:pointer; font-size:1.2em;">Incidencias</summary>
  <p style="margin-top:0.5rem; padding-left:0.5rem;">Aquí va el contenido de la sección Incidencias.</p>
</details>

</body>
</html>
