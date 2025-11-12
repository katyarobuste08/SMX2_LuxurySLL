# 🚗 LUXURY_SL

<div align="center">

![Logo Luxury_SL](https://i.imgur.com/FG6uNYF.png)

**Proyecto Integrado: Web + Arduino + Modelo 3D**  
**Desarrollado por:** Katya Robuste · Nazar Kishchuk  
**Herramientas:** Blender 3D · HTML · CSS · JavaScript · Arduino ESP32

</div>

---

## 📑 Índice

- 📖 Introducción  
  - Justificación  
  - Objetivos  
  - Público Objetivo  
  - Tecnologías Utilizadas  
- 💻 Web  
  - Justificación del Estilo y Colores  
  - Pantallas del Diseño Web  
- 🔧 Arduino y Modelo 3D  
  - Programación Arduino  
  - Diagrama Arduino  
  - Modelo 3D del Coche  
- 🌐 Red  
  - Sincronización Web-Hardware  
- 🧩 Servicios  
- 🧾 Conclusiones  
- 📚 Bibliografía  

---

<details>
<summary><strong>📖 Introducción</strong></summary>

### 💡 Justificación del Proyecto
Luxury_SL surge de la necesidad de **conectar el aprendizaje práctico con la teoría** mediante un enfoque interactivo y multidisciplinario.  
El proyecto permite comprender los principios de **ingeniería, lógica de control y diseño**, fomentando **autonomía, resolución de problemas y curiosidad técnica**.  

La experiencia combina **software y hardware**, ofreciendo un entorno educativo único que integra programación, diseño 3D y control electrónico en tiempo real.

---

### 🎯 Objetivos

#### Objetivo Principal
Desarrollar una plataforma que combine **modelado 3D y robótica**, permitiendo al usuario experimentar con un coche inteligente tanto en el entorno **virtual** como **físico**.

#### Objetivos Específicos
- Implementar un sistema **Bluetooth** que conecte el coche físico con la plataforma web.  
- Ofrecer **recursos educativos, guías y tutoriales** interactivos.  
- Fomentar la **participación y colaboración** dentro de la comunidad.  
- Promover competencias **STEAM**, incluyendo creatividad, lógica y pensamiento crítico.  
- Consolidar la herramienta como adaptable a distintos niveles de conocimiento.

---

### 🧑‍🎓 Público Objetivo
Luxury_SL está dirigido a:  
- Estudiantes y profesores interesados en robótica, diseño 3D y programación.  
- Centros educativos que buscan proyectos innovadores en STEAM.  
- Aficionados a la electrónica y la creatividad digital.  
- Personas autodidactas que deseen transformar ideas digitales en objetos reales.  

---

### 🛠️ Tecnologías Utilizadas
| Tecnología | Uso Principal |
|------------|---------------|
| 🧱 Blender 3D | Modelado y visualización 3D interactiva |
| 💻 HTML + CSS + JS | Interfaz web y conexión virtual |
| ⚙️ Arduino ESP32 | Control físico mediante Bluetooth |
| 🌍 Apache + MySQL | Gestión de base de datos y comunicación web |

</details>

<details>
<summary><strong>💻 Web</strong></summary>

### 🎨 Justificación del Estilo y Colores
<div align="center" style="display:flex; justify-content:flex-start; align-items:center;">
<div style="width:50%; padding-right:20px; text-align:justify;">
Luxury_SL utiliza una paleta de colores cuidadosamente seleccionada para transmitir **lujo, elegancia y profesionalidad**.  
Los tonos oscuros (negro y gris) aportan sensación de exclusividad.  
Los acentos claros mejoran la legibilidad y la navegación.  
El diseño minimalista garantiza una experiencia **ágil y sin distracciones**, reflejando la fusión entre **entorno virtual y físico**.
</div>
<div style="width:45%;">
<img src="https://i.imgur.com/zcfUlYo.png" width="80%"/>
</div>
</div>

---

### 🖼️ Pantallas del Diseño Web

<div align="center">
<table>
<tr>
<td align="center"><img src="https://i.imgur.com/Xhj3vUs.png" width="450"/><br><i>Dashboard de Inicio: pantalla principal con logotipo y accesos a secciones.</i></td>
<td align="center"><img src="https://i.imgur.com/xFugChF.png" width="450"/><br><i>Iniciar Sesión / Crear Cuenta: personalización de la experiencia de usuario.</i></td>
</tr>
<tr>
<td align="center"><img src="https://i.imgur.com/snpG4OU.png" width="450"/><br><i>Objetivos: organización clara de menús, botones y contenido educativo.</i></td>
<td align="center"><img src="https://i.imgur.com/iM1fOzK.png" width="450"/><br><i>Arquitectura del Proyecto: interacción entre usuario, servidor y base de datos.</i></td>
</tr>
<tr>
<td align="center"><img src="https://i.imgur.com/6NnGtWI.png" width="450"/><br><i>Flujo de Datos: navegación interna entre secciones y módulos de la web.</i></td>
<td align="center"><img src="https://i.imgur.com/4gWzAay.png" width="450"/><br><i>Stack Tecnológico: todos los módulos y servicios que componen la plataforma.</i></td>
</tr>
</table>
</div>

</details>

<details>
<summary><strong>🔧 Arduino y Modelo 3D</strong></summary>

### 💡 Programación Arduino
El control del coche se realiza mediante **Arduino ESP32** con **Bluetooth integrado**, gestionando movimientos y luces desde la web.  

**Tutorial recomendado:** [YouTube - Facil](https://www.youtube.com/watch?v=03mQrT4lDgM)

<div align="center">
<img src="https://i.imgur.com/rijhOry.png" width="500"/>
<br><i>Esquema básico de control y conexión de Arduino ESP32.</i>
</div>

---

### ⚙️ Diagrama Arduino
<div align="center">
<img src="https://i.imgur.com/cGVPCzm.png" width="600"/>
<br><i>Componentes: placa ESP32, 4 ruedas + motores, driver L298N, cables y chasis. Sincronización en tiempo real con la web.</i>
</div>

---

### 🏎️ Modelo 3D del Coche
<div align="center">
<img src="https://i.imgur.com/IZttiWP.png" width="450"/>  
<img src="https://i.imgur.com/bTWoQN3.png" width="450"/>
<br><i>Lamborghini negro creado en Blender 3D e impreso para integrarse con Arduino. Permite interacción y visualización en tiempo real.</i>
</div>

**Visualiza el modelo 3D:** [Sketchfab Luxury_SL](https://skfb.ly/pCxW9)

</details>

<details>
<summary><strong>🌐 Red</strong></summary>

<div align="center">
<img src="https://i.imgur.com/WzbjxSQ.png" width="800"/>
<br><i>Arquitectura de red: comunicación segura y sincronización entre web, servidor y Arduino ESP32.</i>
</div>

### 🔗 Sincronización Web-Hardware
1. Usuario envía acción desde la web.  
2. Servidor procesa y envía al ESP32.  
3. Coche físico ejecuta la acción.  
4. Modelo 3D se actualiza visualmente.

</details>

<details>
<summary><strong>🧩 Servicios</strong></summary>

| Servicio | Función | Beneficio |
|----------|--------|-----------|
| 🌍 DNS | Traduce dominio web | Acceso rápido y seguro |
| 💻 DHCP | Asigna IPs automáticas | Conexión sin conflictos |
| 🧠 Apache | Aloja la web y APIs | Sincronización fluida |
| 🔒 Firewall | Protege el sistema | Seguridad ante accesos externos |
| 💾 Backups | Guarda datos y progreso | Recuperación ante fallos |

### 👥 Diagrama de Usuarios y Roles
<div align="center">
<img src="https://i.imgur.com/r03QN0i.png" width="600"/>
<br><i>Roles: estudiantes, docentes, administradores y visitantes interactuando con los servicios.</i>
</div>

</details>

<details>
<summary><strong>🧾 Conclusiones</strong></summary>

Luxury_SL integra **hardware y software** para ofrecer una experiencia educativa inmersiva.  
Permite aprender sobre **programación, diseño 3D y control electrónico**, combinando **ingeniería, diseño y educación STEAM** en un solo entorno interactivo.

</details>

<details>
<summary><strong>📚 Bibliografía</strong></summary>

- [Blender Documentation](https://www.blender.org/)  
- [Three.js Manual](https://threejs.org/docs/)  
- [Arduino ESP32 Reference](https://docs.arduino.cc/hardware/esp32/)  
- [HTML/CSS/JS MDN Docs](https://developer.mozilla.org/)

<div align="center">
<img src="https://i.imgur.com/qPQOsBJ.png" width="400"/>
<br><i>Inspiración y referencias visuales del proyecto.</i>
</div>

</details>

