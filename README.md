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

<details>
<summary><strong>BRIEFING LUXURY_SL</strong></summary>

Luxury_SL es un proyecto que combina un diseño 3D de un coche con Arduino permitiendo al usuario construir, visualizar e interactuar con su propio coche

Los usuarios podrán crear cuenta, consultar tutoriales para montar el coche, dejar comentarios al soporte técnico y controlar el coche vía Bluetooth incluyendo movimientos hacia adelante, atrás, izquierda y derecha además de controlar las luces

Las entidades clave del sistema incluyen Usuario, Comentarios, Arduino, Diseño 3D, Coche y Herramientas

El proyecto busca ofrecer una web funcional con visualización 3D del coche y control físico del mismo integrando la experiencia digital con la interacción física del hardware

</details>

<details>
<summary><strong>WEB</strong></summary>

#### Diseño Web

La paleta de colores de la web combina un **negro profundo** como fondo principal, un **blanco puro** para textos principales y un **gris claro** para los textos secundarios y elementos de contraste. Los paneles translúcidos aplican una transparencia ligera que permite ver ligeramente el fondo mientras se mantiene la legibilidad, generando el efecto glassmorphism. Las sombras suaves y los detalles minimalistas complementan la estética moderna y elegante del sitio.  

<div align="center">
<img src="https://i.imgur.com/zcfUlYo.png" alt="Mood de colores" width="600"/>
</div>

Esta imagen muestra el **mood visual de los colores**, dando referencia de cómo se aplican los tonos oscuros, claros y las transparencias en toda la interfaz.

---

La web presenta un diseño oscuro moderno y minimalista basado en glassmorphism con fondo negro, texto blanco y detalles en gris claro. Los paneles poseen fondos semitransparentes con desenfoque de seis píxeles aplicado mediante backdrop filter. Se utilizan colores rgba suaves para lograr el efecto translúcido característico del estilo. Las sombras sutiles y las transiciones fluidas en botones y tarjetas aportan profundidad y movimiento a la interfaz.  

La tipografía utilizada es Segoe UI junto con Tahoma, Geneva, Verdana y sans serif garantizando legibilidad y apariencia moderna en cualquier dispositivo. El fondo del sitio está compuesto por un video que se reproduce automáticamente en bucle y sin sonido, adaptándose al tamaño de la pantalla con object-fit cover y contando con imagen alternativa para dispositivos que no reproduzcan video  

La navegación se organiza mediante un menú principal con secciones Inicio, Herramientas, Página Oficial, Contacto y Sobre Nosotros. En Herramientas se encuentran las subcategorías 3D Blender y Arduino. La Página Oficial solo se puede acceder tras iniciar sesión ofreciendo acceso a herramientas personalizadas, área de comentarios y perfil de usuario  

El sistema de usuario es totalmente local usando localStorage para almacenar registro e inicio de sesión de forma rápida y segura. Cada usuario tiene un panel propio para gestionar comentarios, revisar estado y ejecutar acciones sin depender de bases de datos externas. Las secciones cambian dinámicamente sin recargar la página ofreciendo experiencia fluida. Se integran notificaciones tipo toast mostrando confirmaciones o avisos de error. Los videos de fondo cambian según la sección activa creando ambiente visual dinámico  

El diseño incluye animaciones hover suaves que elevan tarjetas y modifican color de botones generando interacción natural. Todo el contenido es responsive adaptándose a móviles, tablets y ordenadores.  

<details>
<summary><strong>Base de Datos</strong></summary>

La base de datos del proyecto se encarga de almacenar la información de los usuarios y sus comentarios de manera local en el navegador usando **localStorage**. Permite mantener registro de usuarios, gestionar sus perfiles y almacenar mensajes de soporte o dudas de forma segura y rápida sin depender de servidores externos. La información se organiza en dos tablas principales: **Usuarios** y **Comentarios**  

### Tabla de Usuarios

Esta tabla guarda los datos básicos de cada usuario registrado, permitiendo identificar y autenticar a cada persona dentro del sistema

| Campo          | Ejemplo        | Descripción                                          |
|----------------|----------------|-----------------------------------------------------|
| Nombre         | Juan Pérez     | Nombre completo del usuario                          |
| Email          | juanp@gmail.com| Correo electrónico usado para registro y contacto   |
| Fecha Registro | 10/09/2025     | Fecha en la que se creó la cuenta                   |

### Tabla de Comentarios

Esta tabla almacena los mensajes enviados por los usuarios al soporte o en áreas de interacción, asociando cada comentario con su autor y fecha de creación  

| Campo         | Ejemplo                                      | Descripción                                      |
|---------------|---------------------------------------------|-------------------------------------------------|
| Id comentario | 001                                         | Identificador único del comentario              |
| Id usuario    | 1                                           | Identificador del usuario que realizó el comentario |
| Mensaje       | Tengo dudas sobre cómo conectar el módulo Bluetooth | Contenido del mensaje del usuario              |
| Fecha         | 2025-10-02                                  | Fecha en la que se creó el comentario          |

Estas tablas permiten mantener organizada la información de los usuarios y sus interacciones, facilitando la gestión de la plataforma y la respuesta del soporte técnico  

</details>
</details>

<details>
<summary><strong>ARDUINO Y MODELO 3D</strong></summary>

### Programación Arduino

Para el control del coche se utiliza Arduino y un módulo Bluetooth que permite mover el vehículo hacia adelante, atrás, izquierda y derecha, así como controlar las luces. La programación se realiza en el IDE de Arduino y se conecta con la web para reflejar los movimientos en tiempo real.  

Tutorial recomendado en YouTube: [YT- Facil](https://www.youtube.com/watch?v=03mQrT4lDgM)

### Modelo 3D del coche

El modelo 3D del coche fue creado en Blender y exportado en formato FBX para su integración en la web mediante Three.js y WebGL. El archivo tiene un tamaño de 6.4 MB y cuenta con 175.000 triángulos y 94.300 vértices, proporcionando una geometría detallada y realista. Se aplicaron 29 materiales diferentes sin texturas PBR, y se crearon capas UV para facilitar texturización futura. El modelo no contiene animaciones ni rigged geometries, lo que permite una visualización ligera y fluida en el navegador.  

Este modelo permite rotación, zoom y exploración interactiva desde la web, y está preparado para sincronizarse con Arduino para reflejar los movimientos y las luces del coche físico. Gracias a estas características, el usuario puede interactuar simultáneamente con el coche digital y el físico, creando una experiencia integrada  

Visualiza el modelo 3D en Sketchfab: [Sketchfab Luxury_SL](https://skfb.ly/pCxW9)

El modelo está escalado y ajustado según Blender 3D, con proporciones correctas para visualización y control físico. Cada material y geometría fue optimizado para rendimiento web, asegurando que la interacción sea fluida incluso en dispositivos con recursos limitados. Esta integración permite que cualquier acción del usuario en la interfaz web se vea reflejada en el coche real a través de Arduino, logrando una experiencia completa de simulación y control  

</details>

<details>
<summary><strong>RED</strong></summary>

### Diagrama de la Red

### Mapa Físico

### Mapa Lógico

</details>

<details>
<summary><strong>SERVICIOS</strong></summary>

### DNS

### DHCP

### Apache

### Firewall

### Copias de Seguridad

</details>

<details>
<summary><strong>CONCLUSIONES</strong></summary>

</details>

<details>
<summary><strong>BIBLIOGRAFÍA</strong></summary>

</details>

---

<div align="center">

![Banner Luxury_SL](https://i.imgur.com/qPQOsBJ.png)

</div>
