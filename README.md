# LUXURY_SL

<div align="center">

![Logo Luxury_SL](https://i.imgur.com/FG6uNYF.png)

**Proyecto Integrado: Web + Arduino + Modelo 3D**  
**Desarrollado por:** Katya Robuste · Nazar Kishchuk  

### Herramientas utilizadas
<div align="center">
<img src="https://e7.pngegg.com/pngimages/146/983/png-clipart-blender-3d-computer-graphics-logo-filehippo-3d-modeling-blenders-3d-computer-graphics-text-thumbnail.png" width="40" style="margin:0 10px"/> 
<img src="https://e7.pngegg.com/pngimages/187/112/png-clipart-responsive-web-design-html-computer-icons-css3-world-wide-web-consortium-css-angle-text.png" width="40" style="margin:0 10px"/> 
<img src="https://pngdownload.io/wp-content/uploads/2023/12/CSS-Logo-PNG-Symbol-for-Web-Development-Transparent-jpg.webp" width="40" style="margin:0 10px"/> 
<img src="https://cdn-icons-png.flaticon.com/512/8379/8379454.png" width="40" style="margin:0 10px"/> 
<img src="https://toppng.com/uploads/preview/arduino-logo-11563227354ny21akychx.png" width="40" style="margin:0 10px"/> 
<img src="https://img.favpng.com/25/15/12/logo-apache-http-server-apache-software-foundation-computer-servers-web-server-png-favpng-ebJ1wHvFsydhrpp6V0xFN5NBQ.jpg" width="40" style="margin:0 10px"/> 
<img src="https://e7.pngegg.com/pngimages/617/252/png-clipart-mysql-workbench-computer-icons-logo-database-server-blue-text.png" width="40" style="margin:0 10px"/>
</div>

</div>

---

<!-- ÍNDICE -->
<details>
<summary><strong>Índice</strong></summary>

1. Introducción  
2. Web  
3. Arduino y Modelo 3D  
4. Red  
5. Servicios  
6. Conclusiones  
7. Bibliografía  

</details>

---

<!-- INTRODUCCIÓN -->
<details>
<summary><strong>Introducción</strong></summary>

### Justificación del Proyecto
Luxury_SL surge de la necesidad de **conectar el aprendizaje práctico con la teoría** mediante un enfoque interactivo y multidisciplinario.  
El proyecto permite comprender los principios de **ingeniería, lógica de control y diseño**, fomentando **autonomía, resolución de problemas y curiosidad técnica**.  

La experiencia combina **software y hardware**, ofreciendo un entorno educativo único que integra programación, diseño 3D y control electrónico en tiempo real.

### Objetivos

#### Objetivo Principal
Desarrollar una plataforma que combine **modelado 3D y robótica**, permitiendo al usuario experimentar con un coche inteligente tanto en el entorno **virtual** como **físico**.

#### Objetivos Específicos
- Implementar un sistema **Bluetooth** que conecte el coche físico con la plataforma web.  
- Ofrecer **recursos educativos, guías y tutoriales** interactivos.  
- Fomentar la **participación y colaboración** dentro de la comunidad.  
- Promover competencias **STEAM**, incluyendo creatividad, lógica y pensamiento crítico.  
- Consolidar la herramienta como adaptable a distintos niveles de conocimiento.

### Público Objetivo
Luxury_SL está dirigido a:  
- Estudiantes y profesores interesados en robótica, diseño 3D y programación.  
- Centros educativos que buscan proyectos innovadores en STEAM.  
- Aficionados a la electrónica y la creatividad digital.  
- Personas autodidactas que deseen transformar ideas digitales en objetos reales.  

### Tecnologías Utilizadas
| Tecnología | Uso Principal |
|------------|---------------|
| Blender 3D | Modelado y visualización 3D interactiva |
| HTML | Estructura web |
| CSS | Estilos y diseño visual |
| JavaScript | Interactividad web |
| Arduino ESP32 | Control físico mediante Bluetooth |
| Apache | Servidor web y APIs |
| MySQL | Base de datos y gestión de información |

</details>

---

<!-- WEB -->
<details>
<summary><strong>Web</strong></summary>

### Justificación del Estilo y Colores
Luxury_SL utiliza una paleta de colores cuidadosamente seleccionada para transmitir **lujo, elegancia y profesionalidad**.  
Los tonos oscuros (negro y gris) aportan sensación de exclusividad.  
Los acentos claros mejoran la legibilidad y la navegación.  
El diseño minimalista garantiza una experiencia **ágil y sin distracciones**, reflejando la fusión entre **entorno virtual y físico**.

<div align="center">
<img src="https://i.imgur.com/zcfUlYo_d.png" width="400"/>
<br><i>Paleta de colores utilizada en el diseño web de Luxury_SL.</i>
</div>

### Pantallas del Diseño Web
<div align="center">
<table>
<tr>
<td align="center"><img src="https://i.imgur.com/Xhj3vUs.png" width="400"/><br><i>Dashboard de Inicio</i></td>
<td align="center"><img src="https://i.imgur.com/xFugChF.png" width="400"/><br><i>Iniciar Sesión / Crear Cuenta</i></td>
</tr>
<tr>
<td align="center"><img src="https://i.imgur.com/snpG4OU.png" width="400"/><br><i>Objetivos</i></td>
<td align="center"><img src="https://i.imgur.com/iM1fOzK.png" width="400"/><br><i>Arquitectura del Proyecto</i></td>
</tr>
<tr>
<td align="center"><img src="https://i.imgur.com/6NnGtWI.png" width="400"/><br><i>Flujo de Datos</i></td>
<td align="center"><img src="https://i.imgur.com/4gWzAay.png" width="400"/><br><i>Stack Tecnológico</i></td>
</tr>
</table>
</div>

### Diagrama de Gantt
Aquí se muestra la planificación temporal completa del proyecto Luxury_SL.  

[Descargar Gantt.xlsx](./Gantt.xlsx)

</details>

---

<!-- ARDUINO Y MODELO 3D -->
<details>
<summary><strong>Arduino y Modelo 3D</strong></summary>

### Programación Arduino
El control del coche se realiza mediante **Arduino ESP32** con **Bluetooth integrado**, gestionando movimientos y luces desde la web.  

**Tutorial recomendado:** [YouTube - Facil](https://www.youtube.com/watch?v=03mQrT4lDgM)

<div align="center">
<img src="https://i.imgur.com/rijhOry.png" width="450"/>
<br><i>Esquema básico de control y conexión de Arduino ESP32.</i>
</div>

### Diagrama Arduino
<div align="center">
<img src="https://i.imgur.com/cGVPCzm.png" width="500"/>
<br><i>Componentes: placa ESP32, 4 ruedas + motores, driver L298N, cables y chasis. Sincronización en tiempo real con la web.</i>
</div>

### Modelo 3D del Coche
<div align="center">
<img src="https://i.imgur.com/IZttiWP.png" width="400"/>  
<img src="https://i.imgur.com/bTWoQN3.png" width="400"/>
<br><i>Lamborghini negro creado en Blender 3D e impreso para integrarse con Arduino. Permite interacción y visualización en tiempo real.</i>
</div>

**Visualiza el modelo 3D:** [Sketchfab Luxury_SL](https://skfb.ly/pCxW9)

</details>

---

<!-- RED -->
<details>
<summary><strong>Red</strong></summary>

### Explicación de la arquitectura de red
La arquitectura de red de Luxury_SL permite **comunicaciones seguras y sincronización en tiempo real** entre la plataforma web, la base de datos y el Arduino ESP32.  
Se asegura que las órdenes del usuario lleguen correctamente al coche físico y que la visualización 3D se actualice sin retrasos, manteniendo coherencia entre lo virtual y lo real.

### Sincronización Web-Hardware
1. Usuario envía acción desde la web.  
2. Servidor procesa y envía al ESP32.  
3. Coche físico ejecuta la acción.  
4. Modelo 3D se actualiza visualmente.

### Arquitectura Detallada
- **Cliente / Usuario:** Navegador web, interacción con modelo 3D, HTTPS seguro.  
- **Servidor Web (Apache):** Aloja plataforma web, APIs y multimedia.  
- **Base de Datos (MySQL/SQLite):** Datos de usuarios, sesiones y preferencias.  
- **Arduino ESP32:** Control del coche real y sincronización con modelo 3D.  
- **Bluetooth / Comunicación Serial:** Comunicación bidireccional para sincronización.

<div align="center">
<img src="https://i.imgur.com/WzbjxSQ.png" width="450"/>
<br><i>Arquitectura de red: comunicación segura y sincronización entre web, servidor y Arduino ESP32.</i>
<br><i>Mini explicación: La red asegura que cada acción del usuario se refleje simultáneamente en el coche físico y en la representación 3D.</i>
</div>

</details>

---

<!-- SERVICIOS -->
<details>
<summary><strong>Servicios</strong></summary>

### Explicación de los servicios
Los servicios implementados en Luxury_SL garantizan **conectividad, seguridad y sincronización**:  
- **DNS:** Facilita la conexión mediante nombres de dominio, permitiendo que el ESP32 se conecte automáticamente.  
- **DHCP:** Asigna IPs únicas y evita conflictos, asegurando que los comandos lleguen correctamente.  
- **Apache:** Procesa acciones de la web y sincroniza el modelo 3D con el coche físico.  
- **Firewall:** Protege la plataforma y controla accesos externos.  
- **Copias de Seguridad:** Mantiene la información restaurable y sincronizada.

| Servicio | Uso | Explicación / Beneficio |
|----------|-----|------------------------|
| DNS | Acceso mediante nombre de dominio | Permite acceso fácil y que ESP32 se conecte automáticamente. Traduce nombre a dirección correcta, comunicación en tiempo real. |
| DHCP | Asigna IPs automáticas | Garantiza IP única sin conflictos. Comandos llegan correctamente al servidor y al coche físico. |
| Apache | Aloja web y APIs | Procesa acciones, sincroniza modelo 3D y coche físico. |
| Firewall | Protección | Controla permisos, evitando interferencias externas. |
| Copias de Seguridad | Guardado de datos | Permite restaurar información y mantener sincronización entre web y coche físico. |

### Explicación del diagrama de usuarios y roles
Los roles definen **permisos y niveles de interacción** dentro de Luxury_SL:  
- **Estudiantes:** Uso básico, control del coche y modelo 3D.  
- **Docentes:** Supervisión y guía del aprendizaje.  
- **Administradores:** Control completo de servicios, usuarios y datos.  
- **Visitantes:** Acceso limitado a información pública.

<div align="center">
<img src="https://i.imgur.com/r03QN0i.png" width="450"/>
<br><i>Roles: estudiantes, docentes, administradores y visitantes interactuando con los servicios.</i>
</div>

</details>

---

<!-- CONCLUSIONES -->
<details>
<summary><strong>Conclusiones</strong></summary>

Luxury_SL integra **hardware y software** para ofrecer una experiencia educativa inmersiva.  
Permite aprender sobre **programación, diseño 3D y control electrónico**, combinando **ingeniería, diseño y educación STEAM** en un solo entorno interactivo.

</details>

---

<!-- BIBLIOGRAFÍA -->
<details>
<summary><strong>Bibliografía</strong></summary>

- [Blender Documentation](https://www.blender.org/)  
- [Three.js Manual](https://threejs.org/docs/)  
- [Arduino ESP32 Reference](https://docs.arduino.cc/hardware/esp32/)  
- [HTML/CSS/JS MDN Docs](https://developer.mozilla.org/)

<div align="center">
<img src="https://i.imgur.com/qPQOsBJ.png" width="400"/>
<br><i>Inspiración y referencias visuales del proyecto.</i>
</div>

</details>
