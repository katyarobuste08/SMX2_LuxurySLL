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

La web **LUXURY_SL** está diseñada con un enfoque oscuro, moderno y minimalista, orientado a transmitir elegancia y tecnología.  
A continuación se presentan las pantallas principales del sitio, ordenadas para reflejar el flujo real de uso: pantalla principal, elementos de acceso (login/registro), navegación, contenido informativo y vistas con el usuario autenticado.

---

#### 1. Pantalla principal (hero)

<div align="center">
<img src="https://i.postimg.cc/50PRHXSb/Captura-de-pantalla-2025-11-04-094043.png" alt="Hero Luxury_SL - Página principal" width="600"/>
</div>

Esta es la pantalla de bienvenida. Muestra el mensaje principal del proyecto y un botón de acción (“Learn More”). Aquí el usuario obtiene la primera impresión visual del proyecto y puede acceder a las funcionalidades del sitio (registro, inicio de sesión o navegar a las secciones principales).

---

#### 2. Barra de acceso rápido (no autenticado)

<div align="center">
<img src="https://i.postimg.cc/rF77CtXq/Captura-de-pantalla-2025-11-04-094021.png" alt="Accesos - Login y Crear Cuenta" width="500"/>
</div>

Estado de usuario no autenticado: presenta los botones **Login** y **Crear Cuenta** en la parte superior, permitiendo al visitante iniciar el proceso de acceso o registro. Es un componente pequeño y persistente que guía al usuario hacia la autenticación.

---

#### 3. Modal: Iniciar sesión

<div align="center">
<img src="https://i.postimg.cc/j5JMjM2s/Captura-de-pantalla-2025-11-04-094233.png" alt="Modal Iniciar Sesión" width="550"/>
</div>

Ventana modal de inicio de sesión con campos para **Email** y **Contraseña**, y un botón **Login**. El diseño es claro y minimalista para facilitar la entrada de credenciales sin distraer al usuario del fondo de la página.

---

#### 4. Modal: Crear cuenta

<div align="center">
<img src="https://i.postimg.cc/YqXYJ1qH/Captura-de-pantalla-2025-11-04-094251.png" alt="Modal Crear Cuenta" width="550"/>
</div>

Formulario de creación de cuenta que solicita **Usuario**, **Email** y **Contraseña** (mínimo 6 caracteres). Al completar este formulario y registrarse correctamente, el usuario podrá iniciar sesión con esas credenciales.

---

#### 5. Menú lateral (navegación)

<div align="center">
<img src="https://i.postimg.cc/CMRgG0Bj/Captura-de-pantalla-2025-11-04-094111.png" alt="Menú lateral - Navegación" width="500"/>
</div>

Menú lateral izquierdo con las secciones principales: **Inicio**, **Sobre Nosotros**, **Contacto** y **Página Oficial**. Permite navegación persistente entre secciones sin recargar la página.

---

#### 6. Sección: Sobre Nosotros

<div align="center">
<img src="https://i.postimg.cc/pT73G9hy/Captura-de-pantalla-2025-11-04-094136.png" alt="Sección Sobre Nosotros" width="600"/>
</div>

Página que explica la propuesta de Luxury_SL: la **fusión entre diseño 3D y tecnología Arduino** para crear vehículos interactivos. Incluye texto descriptivo y un botón **Volver al Inicio** para facilitar la navegación.

---

#### 7. Sección: Contacto

<div align="center">
<img src="https://i.postimg.cc/cCwkFFG2/Captura-de-pantalla-2025-11-04-094208.png" alt="Sección Contacto" width="600"/>
</div>

Panel de contacto dividido en **Contacto General** (email y teléfono) y **Soporte Técnico** (email y horario de atención, lunes–viernes 9:00–18:00). Mantiene la estética oscura y el botón **Volver al Inicio**.

---

#### 8. Sección: Página Oficial (contenidos)

<div align="center">
<img src="https://i.postimg.cc/4xD7gPDP/Captura-de-pantalla-2025-11-04-094404.png" alt="Página Oficial - Modelos/Experiencias/Tutoriales" width="600"/>
</div>

La **Página Oficial** agrupa los bloques de contenido principales: **Modelos 3D de Lujo**, **Experiencia Interactiva** y **Tutoriales Arduino**. Cada bloque ofrece acceso a recursos (modelos, simulaciones y guías) manteniendo coherencia visual.

---

### Observaciones de diseño

- Estética: predominio de negros y grises, tipografía con buena legibilidad y acentos claros para llamadas a la acción.  
- Interacción: navegación sin recarga, modales para autenticación, botones de retorno consistentes.  
- Usabilidad: formularios compactos y directos; menús persistentes y accesibles desde cualquier vista.

---


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
