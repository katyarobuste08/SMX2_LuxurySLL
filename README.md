# LUXURY_SL

<div align="center">
  <img src="https://i.imgur.com/FG6uNYF.png" width="160"/>
  <h2><strong>Proyecto Integrado: Web + Arduino + Modelo 3D</strong></h2>
  <h3>Desarrollado por: <strong>Katya Robuste</strong> · <strong>Nazar Kishchuk</strong></h3>
</div>

---

## Índice

1. [Introducción](#introducción)
2. [Tecnologías y Herramientas](#tecnologías-y-herramientas)
3. [Web](#web)
4. [Arduino & Modelo 3D](#arduino-y-modelo-3d)
5. [Arquitectura y Red](#arquitectura-y-red)
6. [Servicios & Roles](#servicios-y-roles)
7. [Conclusiones](#conclusiones)
8. [Bibliografía](#bibliografía)

---

<details>
<summary><strong>Introducción</strong></summary>

**Luxury_SL** une la **teoría y la práctica** en educación STEAM (robótica, diseño 3D, web, electrónica).
El objetivo es crear una experiencia que motive el aprendizaje autónomo y creativo, con herramientas modernas que unen programación, control, diseño y hardware real.
La plataforma es colaborativa y multidisciplinar: combina recursos, retos y control en tiempo real, adaptable a todos los niveles.

**¿Para quién está pensado?**  
- **Estudiantes, docentes y centros educativos**
- **Aficionados y autodidactas** tecnológicos

</details>

---

<details>
<summary><strong>Tecnologías y Herramientas</strong></summary>

**Luxury_SL usa tecnologías robustas para una experiencia fluida:**  
Las herramientas seleccionadas permiten la integración desde el modelado 3D hasta el control físico y la gestión web segura.

| Tecnología    | Propósito                                         |
|:-------------:|:-------------------------------------------------|
| **Blender 3D**    | **Modelado y visualización 3D interactiva**            |
| **HTML**          | **Estructura de la web**                              |
| **CSS**           | **Diseño visual y estilos**                           |
| **JavaScript**    | **Interactividad web**                                |
| **Arduino ESP32** | **Control físico y comunicación Bluetooth**           |
| **Apache**        | **Servidor de APIs/web y multimedia**                 |
| **MySQL/SQLite**  | **Gestión de base de datos e información**            |

<p align="center">
  <img src="https://e7.pngegg.com/pngimages/146/983/png-clipart-blender-3d-computer-graphics-logo-filehippo-3d-modeling-blenders-3d-computer-graphics-text-thumbnail.png" height="40"/>
  <img src="https://e7.pngegg.com/pngimages/187/112/png-clipart-responsive-web-design-html-computer-icons-css3-world-wide-web-consortium-css-angle-text.png" height="40"/>
  <img src="https://pngdownload.io/wp-content/uploads/2023/12/CSS-Logo-PNG-Symbol-for-Web-Development-Transparent-jpg.webp" height="40"/>
  <img src="https://cdn-icons-png.flaticon.com/512/8379/8379454.png" height="40"/>
  <img src="https://toppng.com/uploads/preview/arduino-logo-11563227354ny21akychx.png" height="40"/>
  <img src="https://img.favpng.com/25/15/12/logo-apache-http-server-apache-software-foundation-computer-servers-web-server-png-favpng-ebJ1wHvFsydhrpp6V0xFN5NBQ.jpg" height="40"/>
  <img src="https://e7.pngegg.com/pngimages/617/252/png-clipart-mysql-workbench-computer-icons-logo-database-server-blue-text.png" height="40"/>
</p>

</details>

---

<details>
<summary><strong>Web</strong></summary>

**Luxury_SL web:**  
Diseño minimalista y elegante, transmite profesionalidad. Navegación clara, interactiva y accesible para usuarios de todos los perfiles.

**Paleta de colores principal:**  
<p align="center">
  <img src="https://i.imgur.com/zcfUlYo_d.png" width="600" />
</p>
<p align="center" style="font-size:16px;">
  <strong>Paleta Luxury_SL:</strong> Negros y dorados para un estilo premium y una lectura cómoda.
</p>

---

### <strong>Vistas principales (en mosaico):</strong>

Cada pantalla tiene un objetivo educativo y práctico. El mosaico permite comparar y navegar visualmente de forma rápida.

<table>
  <tr>
    <td align="center">
      <strong>Dashboard principal</strong><br>
      <img src="https://i.imgur.com/Xhj3vUs.png" width="220"/><br>
      <span style="color:gray; font-size:13px;">
        <strong>Centro de todo:</strong> Accesos, estado y bienvenida del usuario.
      </span>
    </td>
    <td align="center">
      <strong>Login / Registro</strong><br>
      <img src="https://i.imgur.com/xFugChF.png" width="220"/><br>
      <span style="color:gray; font-size:13px;">
        <strong>Seguridad avanzada:</strong> Registro individual y grupal.
      </span>
    </td>
    <td align="center">
      <strong>Objetivos guiados</strong><br>
      <img src="https://i.imgur.com/snpG4OU.png" width="220"/><br>
      <span style="color:gray; font-size:13px;">
        <strong>Progreso STEAM:</strong> Visualiza y marca tus logros.
      </span>
    </td>
  </tr>
  <tr>
    <td align="center">
      <strong>Arquitectura del proyecto</strong><br>
      <img src="https://i.imgur.com/iM1fOzK.png" width="220"/><br>
      <span style="color:gray; font-size:13px;">
        <strong>Diagrama global:</strong> Descubre la estructura completa.
      </span>
    </td>
    <td align="center">
      <strong>Flujo de datos</strong><br>
      <img src="https://i.imgur.com/6NnGtWI.png" width="220"/><br>
      <span style="color:gray; font-size:13px;">
        <strong>Comunicación total:</strong> Señales y comandos del sistema.
      </span>
    </td>
    <td align="center">
      <strong>Stack tecnológico</strong><br>
      <img src="https://i.imgur.com/4gWzAay.png" width="220"/><br>
      <span style="color:gray; font-size:13px;">
        <strong>La base técnica:</strong> Tecnologías que hacen posible Luxury_SL.
      </span>
    </td>
  </tr>
</table>

---

<p><strong>Descargar el plan de Gantt:</strong> <a href="./Gantt.xlsx">Gantt.xlsx</a></p>

</details>

---

<details>
<summary><strong>Arduino y Modelo 3D</strong></summary>

**Coche inteligente controlado por Arduino ESP32:**  
Permite controlar el modelo físico desde la web en tiempo real. El montaje y programación están documentados y son fáciles de seguir y ampliar.

**Modelo 3D propio en Blender:**  
Visualizable y printable, integra diseño, tecnología y creatividad. Sirve tanto en el entorno digital como físico.

### <strong>Mosaico visual Arduino y conexiones:</strong>

<table>
  <tr>
    <td align="center" style="vertical-align:top;">
      <strong>Esquema básico de control</strong><br>
      <span style="color:#b88922; font-weight:bold; font-size:15px;">
        El corazón del proyecto: conecta la placa ESP32 a motores y luces.<br/>
        ¡Aprende electrónica práctica!
      </span><br>
      <img src="https://i.imgur.com/rijhOry.png" width="245"/><br>
      <span style="color:gray; font-size:13px;">
        <strong>Diagrama funcional:</strong> Conexiones elementales, base para prototipar y experimentar.
      </span>
    </td>
    <td align="center" style="vertical-align:top;">
      <strong>Componentes conectados</strong><br>
      <span style="color:#b88922; font-weight:bold; font-size:15px;">
        Todo listo para ensamblar:<br/>
        motores, driver, placa y chasis para tu primer coche robótico.
      </span><br>
      <img src="https://i.imgur.com/cGVPCzm.png" width="245"/><br>
      <span style="color:gray; font-size:13px;">
        <strong>Vista de hardware:</strong> Elementos reales y su integración con el software.
      </span>
    </td>
  </tr>
</table>

<p><strong>Tutorial rápido y visual:</strong> <a href="https://www.youtube.com/watch?v=03mQrT4lDgM" target="_blank">Arduino Fácil</a></p>

---

### <strong>Mosaico modelo Lamborghini 3D</strong>

<table>
  <tr>
    <td align="center" style="vertical-align:top;">
      <strong>Diseño digital</strong><br>
      <span style="color:#b88922; font-weight:bold; font-size:15px;">
        Edita, visualiza y exporta tu propio coche en Blender.<br/>
        ¡Dale personalidad digital a tu prototipo!
      </span><br>
      <img src="https://i.imgur.com/IZttiWP.png" width="245"/><br>
      <span style="color:gray; font-size:13px;">
        <strong>Modelo virtual:</strong> Personalizable, ideal para creatividad y aprendizaje.
      </span>
    </td>
    <td align="center" style="vertical-align:top;">
      <strong>Impresión física</strong><br>
      <span style="color:#b88922; font-weight:bold; font-size:15px;">
        Lleva el 3D al mundo real.<br/>
        Imprime este Lamborghini e intégralo con Arduino.
      </span><br>
      <img src="https://i.imgur.com/bTWoQN3.png" width="245"/><br>
      <span style="color:gray; font-size:13px;">
        <strong>Resultado físico:</strong> La fusión de impresión, diseño, y robótica educativa.
      </span>
    </td>
  </tr>
</table>

<p><strong>Modelo 3D interactivo:</strong> <a href="https://skfb.ly/pCxW9" target="_blank">Sketchfab Luxury_SL</a></p>

</details>

---

<details>
<summary><strong>Arquitectura y Red</strong></summary>

**Luxury_SL presenta una arquitectura robusta y segura:**  
Permite sincronización total y actualización instantánea entre web y hardware. Todos los comandos y datos pasan por un flujo seguro y eficiente.

- **Cliente/Usuario:** Navegador, control web (HTTPS)
- **Servidor Apache:** Aloja web, APIs, multimedia
- **Base de Datos:** Usuarios, sesiones, historial
- **Arduino ESP32:** Comunicación física con Bluetooth
- **Firewall y backups** garantizan la seguridad total

<p align="center">
  <img src="https://i.imgur.com/WzbjxSQ.png" width="500"/>
</p>
<p align="center" style="font-size:15px; font-weight:bold;">
  Sistema de conexión y sincronización: cada acción se refleja al instante en el coche y en la representación digital de la web.
</p>

</details>

---

<details>
<summary><strong>Servicios & Roles</strong></summary>

**Servicios clave para seguridad, gestión y administración:**

| Servicio   | Uso y Beneficio                                         |
|:----------:|:-------------------------------------------------------|
| **DNS**    | Acceso por nombre, conecta automáticamente el ESP32     |
| **DHCP**   | IPs únicas, circulación de comandos sin conflictos      |
| **Apache** | Web, APIs y sincronización                              |
| **Firewall**| Protección y control de acceso externo                 |
| **Backup** | Copias y restauración para seguridad de la plataforma   |

**Roles por permisos:**

| Rol           | Permisos principales                                  |
|:-------------:|:-----------------------------------------------------|
| **Estudiante**    | Control del coche, progreso didáctico                   |
| **Docente**       | Supervisión, guía y configuración didáctica             |
| **Administrador** | Gestión total y administración del sistema              |
| **Visitante**     | Acceso solo a la información pública                    |

<p align="center">
  <img src="https://i.imgur.com/r03QN0i.png" width="650"/>
</p>
<p align="center" style="font-size:15px; font-weight:bold;">
  Explicación visual: <br>
  <span style="color:#b88922;">Cada usuario accede a los servicios y áreas del sistema según su rango y permisos, garantizando control, seguridad y personalización total.</span>
</p>

</details>

---

<details>
<summary><strong>Conclusiones</strong></summary>

**Luxury_SL fusiona tecnología, creatividad y educación.**
Brinda acceso real y digital para aprender, crear y experimentar. El usuario maneja el ciclo completo: **diseñar, programar, ensamblar y controlar** su propio coche robótico, promoviendo aprendizaje multidisciplinar y autonomía.

</details>

---

<details>
<summary><strong>Bibliografía</strong></summary>

- [Blender Documentation](https://www.blender.org/)
- [Three.js Manual](https://threejs.org/docs/)
- [Arduino ESP32 Reference](https://docs.arduino.cc/hardware/esp32/)
- [HTML/CSS/JS MDN Docs](https://developer.mozilla.org/)

<p align="center">
  <img src="https://i.imgur.com/qPQOsBJ.png" width="400"/>
  <br><i>Inspiraciones visuales y técnicas empleadas en Luxury_SL.</i>
</p>
</details>
