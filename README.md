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

## **Descripción General**

**Luxury_SL** combina un **diseño 3D interactivo** de un coche con un **sistema físico basado en Arduino ESP32**, que permite al usuario **construir, visualizar, personalizar e interactuar** con su propio vehículo desde una **plataforma web**.

A través de una **interfaz intuitiva**, el usuario puede **crear una cuenta**, acceder a **tutoriales paso a paso**, dejar **comentarios al soporte técnico** y **controlar el coche real mediante conexión Bluetooth**, con movimientos como **adelante**, **atrás**, **izquierda**, **derecha** y **control de luces**.  

El **modelo digital** refleja los cambios del **vehículo físico** y viceversa, creando una **experiencia completamente integrada** entre el entorno **virtual (web + 3D)** y el **tangible (coche real controlado por Arduino)**.

---

## **Justificación del Proyecto**

**Luxury_SL** surge de la necesidad de **conectar el aprendizaje práctico con la teoría** a través de un enfoque **interactivo y multidisciplinario**.  
En un contexto donde la **educación tecnológica y la robótica** son fundamentales, el proyecto ofrece una oportunidad única para **desarrollar habilidades** en **programación, diseño 3D y electrónica** de manera conjunta.

Su **justificación** se basa en el valor educativo de **aprender haciendo**: al visualizar el impacto directo de cada acción digital en el objeto físico, el usuario comprende mejor los **principios de la ingeniería**, la **lógica de control** y la **estética del diseño**.  
Además, promueve la **autonomía**, la **resolución de problemas** y la **curiosidad** por descubrir cómo interactúan el **software y el hardware** en tiempo real.

---

## **Objetivos**

El **objetivo principal** de Luxury_SL es **desarrollar una plataforma** que combine el **modelado 3D y la robótica** de manera fluida, permitiendo al usuario **experimentar con un coche inteligente personalizable** tanto en el entorno **virtual** como en el **físico**.

### **Objetivos Específicos**
- Implementar un **sistema de control remoto mediante Bluetooth** que conecte el vehículo digital con su versión real.  
- Ofrecer **recursos educativos**, **guías** y **tutoriales** que acompañen al usuario en el proceso de aprendizaje.  
- Fomentar la **participación y colaboración** dentro de la comunidad.  
- Promover el desarrollo de **competencias STEAM**, impulsando la **creatividad**, la **lógica** y el **pensamiento crítico**.  
- Consolidarse como una **herramienta educativa adaptable** a distintos niveles de conocimiento.

---

## **Público Objetivo**

Luxury_SL está dirigido a:
- **Estudiantes y profesores** interesados en robótica, diseño 3D y programación.  
- **Centros educativos** que buscan incorporar proyectos innovadores STEAM.  
- **Aficionados a la electrónica y la creatividad digital**.  
- Personas **curiosas y autodidactas** que deseen construir sus propios proyectos tecnológicos.  

El proyecto resulta especialmente atractivo para quienes disfrutan de **transformar ideas digitales en objetos reales**, conectando el **diseño visual con la ingeniería electrónica** en una experiencia completa y motivadora.

---

## **Tecnologías Utilizadas**

- **Blender 3D** — Modelado y visualización 3D interactiva.  
- **HTML + CSS + JavaScript** — Interfaz web y conexión con el entorno virtual.  
- **Arduino ESP32** — Control físico del vehículo mediante Bluetooth.  
- **Plataforma Web** — Interacción y gestión de usuarios.  

---

## **Licencia**

Este proyecto es de uso **educativo y experimental**, enfocado en la **innovación tecnológica** y el **aprendizaje práctico**.

</details>

---

<details>
<summary><strong>WEB</strong></summary>

### Mockup Conceptual de la Web Luxury_SL

<div align="center">

![Mockup Conceptual Luxury_SL](https://i.imgur.com/3uX91yZ.png)

</div>

El diseño de **Luxury_SL** busca combinar **elegancia, modernidad y funcionalidad**. Desde la primera impresión, se percibe un enfoque visual cuidado y minimalista, pensado para resaltar la **tecnología y el lujo** que caracterizan el proyecto. La interfaz está diseñada para que el usuario se sumerja en la experiencia sin distracciones innecesarias, concentrándose en los **modelos 3D**, la interacción con **Arduino** y los contenidos educativos.

---

### Justificación del estilo y los colores

- **Elegancia y sofisticación:** La paleta oscura, basada en negros y grises profundos, transmite sensación de exclusividad, lujo y profesionalidad. Este enfoque visual ayuda a que la atención del usuario se centre en los elementos interactivos y en los detalles del coche 3D.  
- **Contraste y claridad:** Los acentos claros, como botones, iconos y textos destacados, proporcionan un contraste visual que facilita la lectura y guía la navegación de manera intuitiva.  
- **Minimalismo funcional:** Se prioriza la simplicidad y la limpieza visual. Los menús, botones y modales aparecen solo cuando son necesarios, evitando la sobrecarga de información y ofreciendo una experiencia ágil.  
- **Interactividad intuitiva:** La navegación sin recarga, los menús laterales persistentes y los modales de inicio de sesión o creación de cuenta permiten que el usuario explore el sitio de forma fluida, promoviendo la **exploración educativa** y la interacción directa con los recursos.  
- **Experiencia educativa integrada:** Los elementos visuales y la organización de la información están orientados a guiar al usuario hacia la comprensión de conceptos STEAM. La jerarquía visual destaca las secciones principales —como **tutoriales Arduino**, **modelos 3D interactivos** y **guías de aprendizaje**— permitiendo que la educación y la experiencia tecnológica convivan de forma natural.  
- **Fusión entre virtual y físico:** Cada decisión de diseño busca reflejar la filosofía del proyecto: **el usuario controla un coche físico mientras observa su equivalente digital**. El diseño elegante y oscuro sirve como un “marco” que resalta la innovación tecnológica y crea un ambiente inmersivo para la interacción entre hardware y software.  

---

### Pantallas principales del sitio

#### 1. Pantalla principal (hero)

<div align="center">
<img src="https://i.postimg.cc/50PRHXSb/Captura-de-pantalla-2025-11-04-094043.png" alt="Hero Luxury_SL - Página principal" width="600"/>
</div>

La pantalla de bienvenida muestra el mensaje principal del proyecto y un botón de acción (“Learn More”), ofreciendo la primera impresión visual y acceso a funcionalidades principales.

#### 2. Barra de acceso rápido (no autenticado)

<div align="center">
<img src="https://i.postimg.cc/rF77CtXq/Captura-de-pantalla-2025-11-04-094021.png" alt="Accesos - Login y Crear Cuenta" width="500"/>
</div>

Presenta los botones **Login** y **Crear Cuenta**, permitiendo al visitante iniciar el proceso de acceso o registro de manera rápida y accesible.

#### 3. Modal: Iniciar sesión

<div align="center">
<img src="https://i.postimg.cc/j5JMjM2s/Captura-de-pantalla-2025-11-04-094233.png" alt="Modal Iniciar Sesión" width="550"/>
</div>

Ventana modal de inicio de sesión con campos para **Email** y **Contraseña**, con diseño claro y minimalista para facilitar la entrada de credenciales.

#### 4. Modal: Crear cuenta

<div align="center">
<img src="https://i.postimg.cc/YqXYJ1qH/Captura-de-pantalla-2025-11-04-094251.png" alt="Modal Crear Cuenta" width="550"/>
</div>

Formulario de creación de cuenta que solicita **Usuario**, **Email** y **Contraseña**. Al registrarse, el usuario podrá iniciar sesión con esas credenciales.

#### 5. Menú lateral (navegación)

<div align="center">
<img src="https://i.postimg.cc/CMRgG0Bj/Captura-de-pantalla-2025-11-04-094111.png" alt="Menú lateral - Navegación" width="500"/>
</div>

Menú lateral izquierdo con las secciones principales: **Inicio**, **Sobre Nosotros**, **Contacto** y **Página Oficial**, permitiendo navegación persistente sin recargar la página.

#### 6. Sección: Sobre Nosotros

<div align="center">
<img src="https://i.postimg.cc/pT73G9hy/Captura-de-pantalla-2025-11-04-094136.png" alt="Sección Sobre Nosotros" width="600"/>
</div>

Explica la propuesta de Luxury_SL: la **fusión entre diseño 3D y tecnología Arduino** para crear vehículos interactivos, con texto descriptivo y un botón de retorno al inicio.

#### 7. Sección: Contacto

<div align="center">
<img src="https://i.postimg.cc/cCwkFFG2/Captura-de-pantalla-2025-11-04-094208.png" alt="Sección Contacto" width="600"/>
</div>

Panel de contacto dividido en **Contacto General** y **Soporte Técnico**, manteniendo estética oscura y botones consistentes.

#### 8. Sección: Página Oficial (contenidos)

<div align="center">
<img src="https://i.postimg.cc/4xD7gPDP/Captura-de-pantalla-2025-11-04-094404.png" alt="Página Oficial - Modelos/Experiencias/Tutoriales" width="600"/>
</div>

Agrupa los bloques principales: **Modelos 3D de Lujo**, **Experiencia Interactiva** y **Tutoriales Arduino**, manteniendo coherencia visual y fácil acceso a recursos.

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
