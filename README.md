# LUXURY_SL

**En desarrollo:** Blender 3D + CSS + HTML + JavaScript  
**Equipo:** Katya Robuste • Pau Ferrer • Nazar Kishchuk  

---

<details>
<summary><strong>ÍNDICE</strong></summary>

- Introducción  
- Web  
  - Estructura del Sitio Web  
  - Diseño Web  
  - Base de Datos  
- Arduino y Modelo 3D  
  - Programación  
  - Modelo 3D del coche  
- Red  
  - Diagrama de la Red  
  - Mapa Físico  
  - Mapa Lógico  
- Servicios  
  - DNS  
  - DHCP  
  - Apache  
  - Firewall  
  - Copias de Seguridad  
- Bibliografía  

</details>

---

<details>
<summary><strong>INTRODUCCIÓN</strong></summary>

### Briefing

Luxury_SL es un proyecto que combina el diseño 3D de un coche con un sistema físico controlado mediante Arduino ESP32.  
El objetivo es permitir a los usuarios construir, visualizar e interactuar con su propio vehículo tanto en el entorno digital como en el físico.

El proyecto busca integrar tres áreas principales:  
- **Diseño 3D (Blender)**  
- **Programación web (HTML, CSS, JavaScript)**  
- **Electrónica (Arduino ESP32)**  

La finalidad es educativa, promoviendo el aprendizaje de robótica, modelado 3D y programación de forma práctica y visual.

---

### Público Objetivo

Luxury_SL está dirigido a:  
- Estudiantes de ingeniería, robótica o diseño.  
- Aficionados a la electrónica, programación o impresión 3D.  
- Personas interesadas en proyectos “hazlo tú mismo” (DIY).  

El proyecto busca atraer tanto a principiantes como a personas con conocimientos intermedios que deseen aprender mediante la práctica.

---

### Objetivo General

El objetivo de Luxury_SL es integrar la creatividad del diseño 3D, la ingeniería electrónica y la interactividad web para crear una experiencia educativa.  
Busca acercar el aprendizaje de la robótica y la programación de forma visual, práctica y accesible.

---

### Mockup

El mockup del sitio web refleja un estilo moderno y minimalista con colores oscuros y transparencias.  
Incluye un menú lateral, botones suaves y animaciones de desplazamiento.  
El objetivo es mantener una interfaz limpia, profesional y fácil de navegar.

*(Insertar imagen del mockup aquí)*

---

### Tecnologías a Utilizar

| Área | Herramienta / Tecnología | Descripción |
|------|---------------------------|--------------|
| Frontend | HTML5, CSS3, JavaScript | Interfaz del usuario y visualización 3D |
| Backend | PHP / Node.js | Lógica del servidor y conexión con base de datos |
| Base de datos | MySQL | Almacenamiento de usuarios y comentarios |
| Servidor web | Apache | Alojamiento de la página web |
| Modelado 3D | Blender 3D | Creación del modelo del coche |
| Hardware | Arduino ESP32 | Control físico del coche y comunicación Bluetooth |
| Gestión de proyecto | Trello | Organización de tareas |
| Control de versiones | GitHub | Repositorio de código y documentación |
| Diseño | Canva, Miro | Diseño de interfaz y diagramas |
| Red | Visio | Creación del diagrama de red |

---

### Equipo y Herramientas

- **Trello:** Gestión de tareas y roles del equipo.  
- **GitHub:** Control de versiones y almacenamiento del código.  
- **Canva / Miro:** Diseño de interfaz y estructura del sitio.  
- **Visio:** Elaboración del diagrama de red y arquitectura.  
- **Blender 3D:** Modelado y renderizado del coche.  
- **Arduino ESP32:** Control físico del coche y conexión Bluetooth.

---

### Futuras Mejoras

- Incorporación de sensores adicionales como ultrasonido o infrarrojo.  
- Control remoto del coche desde la web mediante conexión Wi-Fi.  
- Creación de un foro interactivo para usuarios.  
- Implementación de logros o niveles para gamificar el aprendizaje.  
- Exportación del modelo 3D con texturas y colores personalizados.  

</details>

---

<details>
<summary><strong>WEB</strong></summary>

### Estructura del Sitio Web

El sitio web está compuesto por diferentes secciones que organizan el contenido y las funciones del proyecto:

- **Inicio:** Presentación del proyecto.  
- **Quiénes Somos:** Información sobre el equipo desarrollador.  
- **A Quién Va Dirigido:** Explica el público objetivo.  
- **Tutoriales:** Guías detalladas para el montaje y programación del coche.  
- **Modelo 3D:** Visualizador interactivo del coche creado en Blender.  
- **Contacto / Feedback:** Espacio para dudas o sugerencias.  
- **Login / Registro:** Acceso personalizado para los usuarios.

---

### Diseño Web

El diseño utiliza un estilo oscuro y minimalista con efecto de transparencia.  
Los paneles presentan desenfoque de fondo y sombras suaves para lograr una estética moderna.  
La navegación es fluida y dinámica, con animaciones suaves y notificaciones tipo "toast".

---

### Base de Datos

El sistema emplea almacenamiento local (localStorage) para gestionar usuarios y comentarios de forma rápida y sencilla.

**Tabla de Usuarios**

| Campo | Ejemplo | Descripción |
|--------|----------|-------------|
| Nombre | Juan Pérez | Nombre del usuario |
| Email | juanp@gmail.com | Correo electrónico del usuario |
| Fecha Registro | 10/09/2025 | Fecha de creación de la cuenta |

**Tabla de Comentarios**

| Campo | Ejemplo | Descripción |
|--------|----------|-------------|
| Id comentario | 001 | Identificador del comentario |
| Id usuario | 1 | Usuario que realizó el comentario |
| Mensaje | Duda sobre el módulo Bluetooth | Contenido del comentario |
| Fecha | 2025-10-02 | Fecha de publicación |

</details>

---

<details>
<summary><strong>ARDUINO Y MODELO 3D</strong></summary>

### Programación

El coche utiliza un Arduino ESP32 con Bluetooth integrado, lo que permite el control inalámbrico desde la web.  
Gestiona los movimientos del vehículo (adelante, atrás, izquierda, derecha) y el encendido de luces.

---

### Modelo 3D del Coche

El modelo fue creado en Blender y exportado a formato FBX para su integración en Three.js.  
Cuenta con aproximadamente 175.000 triángulos y 94.300 vértices.  
Permite rotación, zoom e interacción sincronizada con los movimientos del coche físico.

</details>

---

<details>
<summary><strong>RED</strong></summary>

### Diagrama de la Red
Muestra la relación entre los dispositivos: cliente, servidor web y sistema Arduino.

### Mapa Físico
Representa la disposición física de los equipos y su conexión.

### Mapa Lógico
Expone el flujo de datos y la estructura de comunicación entre los distintos componentes del sistema.

</details>

---

<details>
<summary><strong>SERVICIOS</strong></summary>

### DNS
Servicio encargado de traducir nombres de dominio a direcciones IP.

### DHCP
Proporciona direcciones IP automáticas a los dispositivos conectados.

### Apache
Servidor web encargado de alojar y servir la página de Luxury_SL.

### Firewall
Sistema de protección que controla el tráfico de red para mantener la seguridad.

### Copias de Seguridad
Implementación de copias periódicas de datos y configuraciones del proyecto.

</details>

---

<details>
<summary><strong>BIBLIOGRAFÍA</strong></summary>

- Documentación oficial de Blender  
- Manual de Three.js  
- Referencia técnica del Arduino ESP32  
- Documentación de HTML, CSS y JavaScript en MDN  

</details>

---

© 2025 Luxury_SL — Proyecto educativo y tecnológico.
