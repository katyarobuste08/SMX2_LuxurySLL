# LUXURY_SL

<div align="center">

![Logo Luxury_SL](https://i.imgur.com/FG6uNYF.png)

**En desarrollo: Blender 3D + CSS + HTML + JavaScript**  

**Equipo:** Katya Robuste • Pau Ferrer • Nazar Kishchuk

</div>

---

<details>
<summary><strong>ÍNDICE</strong></summary>

- Introducción  
- Arquitectura de Software  
- Tecnologías a Utilizar  
- Red  
  - Diagrama de la Red  
  - Mapa Físico  
  - Mapa Lógico  
- Web  
  - Diseño Web  
  - Mapa de Navegabilidad  
  - Base de Datos  
- Arduino y Modelo 3D  
  - Programación  
  - Modelo 3D del coche  
- Servicios  
  - DNS  
  - DHCP  
  - Apache  
  - Firewall  
  - Copias de Seguridad  
- Conclusiones  
- Bibliografía  

</details>

---

<details>
<summary><strong>BRIEFING LUXURY_SL</strong></summary>

# 🚗 Luxury_SL

**Luxury_SL** es un proyecto innovador que combina el **diseño 3D de un coche** con un **sistema basado en Arduino**, ofreciendo a los usuarios la posibilidad de **construir, visualizar e interactuar** con su propio vehículo tanto en un entorno digital como físico.

---

## 🧩 Descripción del Proyecto

El objetivo de **Luxury_SL** es crear una plataforma web interactiva que guíe al usuario en el **montaje de un coche 3D controlado mediante Arduino ESP32**.  
A través de la web, los usuarios pueden:

- Crear una **cuenta personal** y acceder al contenido exclusivo.  
- Consultar **tutoriales paso a paso** sobre el montaje del coche y la configuración del Arduino.  
- **Visualizar el modelo 3D** del vehículo directamente desde el navegador.  
- **Dejar comentarios o sugerencias** al soporte técnico para resolver dudas o aportar mejoras.  
- **Controlar el coche vía Bluetooth**, con movimientos de:
  - 🔼 Adelante  
  - 🔽 Atrás  
  - ⬅️ Izquierda  
  - ➡️ Derecha  
  - 💡 Encendido y apagado de luces  

---

##  Experiencia Integrada

El proyecto busca ofrecer una **experiencia completa y conectada** entre el mundo digital y el físico:  
- En el **entorno digital**, los usuarios acceden al modelo 3D, tutoriales y comunidad.  
- En el **entorno físico**, pueden construir y controlar el coche real mediante el sistema **Arduino ESP32** y conexión **Bluetooth**.

---

##  Tecnologías Utilizadas

| Área | Herramienta / Tecnología | Descripción |
|------|---------------------------|--------------|
| **Frontend** | HTML5, CSS3, JavaScript | Interfaz de usuario y visualización del modelo 3D |
| **Backend** | PHP / Node.js | Lógica del servidor y conexión con la base de datos |
| **Base de datos** | MySQL | Almacenamiento de usuarios, tutoriales y comentarios |
| **Servidor web** | Apache | Alojamiento de la aplicación web |
| **Modelado 3D** | Blender 3D | Creación del modelo del coche en 3D |
| **Hardware** | Arduino ESP32 | Control físico del coche y comunicación Bluetooth |
| **Gestión de proyecto** | Trello | Organización de tareas y roles del equipo |
| **Control de versiones** | GitHub | Almacenamiento del código y documentación |
| **Diseño y diagramación** | Canva, Miro | Diseño de interfaz y diagrama de navegabilidad |
| **Red y arquitectura** | Visio | Elaboración del diagrama de red del sistema |

---

##  Estructura del Sitio Web

- **Inicio:** Presentación del proyecto.  
- **Quiénes Somos:** Información del equipo desarrollador.  
- **A Quién Va Dirigido:** Público objetivo (estudiantes, aficionados, makers, etc.).  
- **Tutoriales:** Guías y pasos para el montaje y configuración.  
- **Modelo 3D:** Visualizador interactivo del coche.  
- **Contacto / Feedback:** Envío de comentarios y sugerencias.  
- **Login / Registro:** Acceso personalizado para los usuarios.

---

##  Público Objetivo

El proyecto está dirigido a:
- Estudiantes de ingeniería, robótica o diseño.  
- Aficionados a la electrónica, programación o impresión 3D.  
- Personas interesadas en proyectos **“hazlo tú mismo” (DIY)**.  

---

##  Objetivo General

**Luxury_SL** busca integrar la **creatividad del diseño 3D**, la **ingeniería electrónica** y la **interactividad web** en una experiencia educativa única.  
El propósito es acercar el aprendizaje de la robótica y la programación a través de un entorno visual, práctico y accesible.

---

##  Equipo y Herramientas de Desarrollo

- **Trello:** Gestión de tareas y roles.  
- **GitHub:** Control de versiones y documentación.  
- **Canva / Miro:** Diseño de interfaz y estructura del sitio.  
- **Visio:** Diagrama de red y arquitectura.  
- **Blender 3D:** Creación y renderización del coche.  
- **Arduino ESP32:** Control físico del coche vía Bluetooth.  

---

##  Futuras Mejoras

- Integración de sensores adicionales (ultrasonido, infrarrojo, etc.).  
- Control remoto desde la web mediante conexión Wi-Fi.  
- Expansión del sistema de comentarios a un foro interactivo.  
- Implementación de logros y niveles para los usuarios.

---

##  Contacto

Si deseas colaborar o tienes alguna duda, puedes ponerte en contacto con el equipo de desarrollo a través del formulario de la web o enviando tus sugerencias directamente en la sección de **Feedback**.

---

**© 2025 Luxury_SL — Proyecto educativo y tecnológico.**


---

<details>
<summary><strong>WEB</strong></summary>

### Diseño Web

La web utiliza un estilo **oscuro y minimalista** con efecto **glassmorphism**.  
Los paneles tienen transparencia suave, desenfoque de fondo y sombras sutiles para lograr una estética moderna.  

<div align="center">
<img src="https://i.imgur.com/zcfUlYo.png" alt="Mood de colores" width="450"/>
</div>

La navegación es fluida y dinámica, sin recargar la página.  
Incluye notificaciones tipo *toast*, animaciones suaves y un fondo en video que cambia según la sección activa.  

<div align="center">
<img src="https://i.imgur.com/dxfX96U.png" alt="Diseño Web" width="700"/>
</div>

---

<details>
<summary><strong>Base de Datos (Logging)</strong></summary>

El sistema usa **localStorage** para manejar usuarios y comentarios de forma local, rápida y segura, sin necesidad de servidor externo.

<div align="center">
<img src="https://i.imgur.com/ahRo6nr.png" alt="Base de Datos - Logging" width="500"/>
</div>

### Tabla de Usuarios

| Campo          | Ejemplo        | Descripción                                          |
|----------------|----------------|------------------------------------------------------|
| Nombre         | Juan Pérez     | Nombre completo del usuario                          |
| Email          | juanp@gmail.com| Correo electrónico usado para registro y contacto    |
| Fecha Registro | 10/09/2025     | Fecha en la que se creó la cuenta                    |

### Tabla de Comentarios

| Campo         | Ejemplo                                      | Descripción                                      |
|---------------|---------------------------------------------|-------------------------------------------------|
| Id comentario | 001                                         | Identificador único del comentario              |
| Id usuario    | 1                                           | Usuario que realizó el comentario               |
| Mensaje       | Tengo dudas sobre cómo conectar el módulo Bluetooth | Contenido del mensaje del usuario              |
| Fecha         | 2025-10-02                                  | Fecha de creación del comentario                |

</details>
</details>

---

<details>
<summary><strong>ARDUINO Y MODELO 3D</strong></summary>

### Programación Arduino

El control del coche se realiza con un **Arduino ESP32**, que incorpora **Bluetooth integrado** y permite comunicación inalámbrica directa con la web.  
El sistema gestiona movimientos del vehículo (adelante, atrás, izquierda, derecha) y control de luces desde la interfaz digital.  

📺 **Tutorial recomendado:** [YouTube - Facil](https://www.youtube.com/watch?v=03mQrT4lDgM)

<div align="center">
<img src="https://i.imgur.com/rijhOry.png" alt="Arduino ESP32 con Bluetooth" width="400"/>
</div>

---

### Modelo 3D del coche

El modelo 3D fue creado en **Blender** y exportado a **FBX** para su integración en **Three.js / WebGL**.  
Cuenta con 175.000 triángulos y 94.300 vértices, optimizado para navegadores web.  

Permite **rotación, zoom e interacción** directa, sincronizándose con Arduino para reflejar el movimiento del coche físico.

🔗 **Visualiza el modelo 3D:** [Sketchfab Luxury_SL](https://skfb.ly/pCxW9)

</details>

---

<details>
<summary><strong>RED</strong></summary>

### Diagrama de la Red  
### Mapa Físico  
### Mapa Lógico  

</details>

---

<details>
<summary><strong>SERVICIOS</strong></summary>

### DNS  
### DHCP  
### Apache  
### Firewall  
### Copias de Seguridad  

</details>

---

<details>
<summary><strong>CONCLUSIONES</strong></summary>

Luxury_SL ofrece una integración completa entre hardware y software, permitiendo una experiencia inmersiva y educativa donde el usuario aprende sobre programación, diseño 3D y control electrónico.  

</details>

---

<details>
<summary><strong>BIBLIOGRAFÍA</strong></summary>

- [Blender Documentation](https://www.blender.org/)  
- [Three.js Manual](https://threejs.org/docs/)  
- [Arduino ESP32 Reference](https://docs.arduino.cc/hardware/esp32/)  
- [HTML/CSS/JS MDN Docs](https://developer.mozilla.org/)  

</details>

---

<div align="center">

![Banner Luxury_SL](https://i.imgur.com/qPQOsBJ.png)

</div>
