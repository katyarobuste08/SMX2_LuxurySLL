# LUXURY_SL

<div align="center">

![Logo Luxury_SL](https://i.imgur.com/FG6uNYF.png)

**En desarrollo: Blender 3D + CSS + HTML + JavaScript**  

**Equipo:** Katya Robuste •  Nazar Kishchuk

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

<img src="https://i.imgur.com/3uX91yZ.png" width="350"/>

</div>

El diseño de **Luxury_SL** busca combinar **elegancia, modernidad y funcionalidad**. Desde la primera impresión, se percibe un enfoque visual cuidado y minimalista, pensado para resaltar la **tecnología y el lujo** que caracterizan el proyecto. La interfaz está diseñada para que el usuario se sumerja en la experiencia sin distracciones innecesarias, concentrándose en los **modelos 3D**, la interacción con **Arduino** y los contenidos educativos.

---

### Justificación del estilo y los colores

<div align="center">

<img src="https://i.imgur.com/zcfUlYo.png" width="350"/>

</div>

- **Elegancia y sofisticación:** La paleta oscura, basada en negros y grises profundos, transmite sensación de exclusividad, lujo y profesionalidad.  
- **Contraste y claridad:** Los acentos claros proporcionan un contraste visual que facilita la lectura y guía la navegación.  
- **Minimalismo funcional:** Se prioriza la simplicidad visual y la experiencia ágil.  
- **Interactividad intuitiva:** La navegación fluida permite al usuario explorar sin recargas de página.  
- **Experiencia educativa integrada:** Los elementos visuales guían hacia la comprensión de conceptos STEAM.  
- **Fusión entre virtual y físico:** Cada decisión de diseño refleja el control simultáneo del coche real y su modelo digital.  

---

### Pantallas principales del sitio

<div align="center">

<h4>Pantalla de Inicio</h4>
<img src="https://i.postimg.cc/sM0GWm4F/Captura-de-pantalla-2025-11-11-091721.png" width="1000"/>
<p>
La pantalla de inicio da la bienvenida al usuario con el logotipo de Luxury_SL y un diseño minimalista en tonos oscuros con acentos dorados.  
Esta primera vista busca transmitir elegancia y modernidad, presentando el concepto del proyecto y sus principales accesos.  
Su objetivo es generar una experiencia inicial inmersiva que invite al usuario a explorar la plataforma.
</p>

<h4>Menú Principal</h4>
<img src="https://i.postimg.cc/cKggB3Fy/Captura-de-pantalla-2025-11-11-091731.png" width="1000"/>
<p>
Desde el menú principal se accede a todas las secciones clave del sistema: el modelo 3D interactivo, el panel de control, los tutoriales y el soporte técnico.  
El diseño prioriza la navegación simple y directa, con botones visibles y coherentes con la identidad visual del proyecto.  
Cada icono está pensado para guiar intuitivamente al usuario, garantizando una experiencia fluida y profesional.
</p>

<h4>Panel de Control del Coche</h4>
<img src="https://i.postimg.cc/mczzy98K/Captura-de-pantalla-2025-11-11-091742.png" width="1000"/>
<p>
El panel de control permite manejar el vehículo desde el navegador, enviando comandos al Arduino ESP32 mediante conexión Bluetooth.  
Incluye botones para avanzar, retroceder, girar y encender las luces, además de un sistema de retroalimentación visual en tiempo real.  
Esta pantalla demuestra la unión perfecta entre software y hardware, permitiendo al usuario experimentar el control directo sobre un coche físico.
</p>

<h4>Área del Usuario</h4>
<img src="https://i.postimg.cc/v1ggtn3J/Captura-de-pantalla-2025-11-11-091813.png" width="1000"/>
<p>
En el área de usuario se gestionan los perfiles personales, el progreso y los proyectos creados.  
Ofrece una experiencia personalizada, guardando la información de aprendizaje y permitiendo continuar el trabajo desde cualquier dispositivo.  
El diseño está orientado a la comodidad y simplicidad, priorizando la claridad de la información.
</p>

<h4>Mapa de Navegación Web</h4>
<img src="https://i.postimg.cc/bGDD9nmX/Captura-de-pantalla-2025-11-11-091821.png" width="1000"/>
<p>
El mapa de navegación representa la estructura jerárquica del sitio web, mostrando cómo se relacionan las distintas secciones (inicio, usuario, control, tutoriales, comunidad, soporte).  
Facilita la comprensión del flujo de navegación y ayuda a mantener la coherencia visual y funcional del sitio.  
Es una herramienta esencial para el desarrollo front-end y la organización del contenido.
</p>

<h4>Diseño Visual del Proyecto</h4>
<img src="https://i.postimg.cc/Z9BBxNwz/Captura-de-pantalla-2025-11-11-091826.png" width="1000"/>
<p>
En esta pantalla se aprecia la línea estética definitiva de Luxury_SL: tonos oscuros, tipografía moderna y una interfaz limpia.  
Cada elemento visual está pensado para reflejar el equilibrio entre lujo y tecnología.  
El objetivo es mantener la atención del usuario en la interacción con el modelo 3D y los controles del vehículo sin distracciones visuales.
</p>

<h4>Vista General Final</h4>
<img src="https://i.postimg.cc/f3ttfd8h/Captura-de-pantalla-2025-11-11-091830.png" width="1000"/>
<p>
Esta vista reúne todos los elementos de la plataforma en su versión funcional final.  
Se observa la integración completa entre el diseño web, el sistema de control y la visualización 3D.  
Luxury_SL logra unir estética, tecnología y educación en una experiencia digital coherente, elegante y plenamente interactiva.
</p>

</div>

</details>

---

<details>
<summary><strong>ARDUINO Y MODELO 3D</strong></summary>

### Programación Arduino

El control del coche se realiza con un **Arduino ESP32**, que incorpora **Bluetooth integrado** y permite comunicación inalámbrica directa con la web.  
El sistema gestiona movimientos del vehículo (adelante, atrás, izquierda, derecha) y control de luces desde la interfaz digital.  

 **Tutorial recomendado:** [YouTube - Facil](https://www.youtube.com/watch?v=03mQrT4lDgM)

<div align="center">
<img src="https://i.imgur.com/rijhOry.png" width="350"/>
</div>

---

### Modelo 3D del coche

El modelo 3D fue creado en **Blender** y exportado a **FBX** para su integración en **Three.js / WebGL**.  
Cuenta con 175.000 triángulos y 94.300 vértices, optimizado para navegadores web.  

Permite **rotación, zoom e interacción** directa, sincronizándose con Arduino para reflejar el movimiento del coche físico.

 **Visualiza el modelo 3D:** [Sketchfab Luxury_SL](https://skfb.ly/pCxW9)

</details>

---

<details open>
<summary><strong>RED</strong></summary>

### **Arquitectura de la Red – LUXURY_SL**

<div align="center">

![Arquitectura de la Red Luxury_SL](https://i.postimg.cc/fLvzC5Lm/image.png)

</div>

---

### **Explicación de la Arquitectura**

La arquitectura de red de **Luxury_SL** está diseñada para garantizar una **comunicación fluida**, **seguridad de los datos** y **sincronización en tiempo real** entre los componentes **físicos (Arduino ESP32)** y **virtuales (sitio web + modelo 3D)**.  
Cada elemento cumple una función específica dentro del flujo de información, asegurando que tanto el control del coche físico como la visualización 3D respondan de forma coordinada.

---

#### **Cliente / Usuario**
El **usuario final** accede desde un **navegador web** al sitio oficial de **Luxury_SL**.  
Desde allí puede interactuar con el modelo 3D, crear o iniciar sesión, y enviar comandos al coche físico.  
La comunicación se realiza mediante **HTTPS**, garantizando la seguridad y la integridad de los datos.

---

#### **Servidor Web (Apache)**
El **servidor web** actúa como núcleo del sistema.  
Aloja la **plataforma web**, las **APIs** y los **recursos multimedia** (archivos HTML, CSS, JS, y modelos 3D).  
Gestiona peticiones del cliente, procesa autenticación y transmite información entre el entorno digital y el hardware.

---

#### **Base de Datos (MySQL / SQLite)**
Almacena información estructurada, incluyendo:
- Datos de usuarios y autenticación.  
- Registros de sesiones y preferencias.  
- Logs de conexión y actividad con Arduino.  

Permite una recuperación eficiente de datos y mantiene la persistencia del sistema educativo.

---

#### **Arduino ESP32**
El componente **físico principal** del sistema.  
Controla el coche real y recibe órdenes enviadas desde la web mediante **Bluetooth**.  
A su vez, envía información al servidor sobre el estado del coche (movimientos, luces, energía, etc.), manteniendo sincronización constante con el modelo 3D digital.

---

#### **Conexión Bluetooth y Comunicación Serial**
El **módulo Bluetooth** del ESP32 establece una comunicación bidireccional.  
Permite que las acciones del usuario en la interfaz web se traduzcan en movimientos físicos y que la respuesta del hardware se refleje en el modelo 3D.

---

#### **Sincronización Web–Hardware**
El sistema integra un bucle de comunicación:
1. El usuario envía una acción desde la interfaz.  
2. El servidor procesa la solicitud y la envía al ESP32.  
3. El coche físico ejecuta la acción.  
4. El resultado se refleja visualmente en el entorno 3D del navegador.  

De esta manera, **Luxury_SL** logra una experiencia educativa inmersiva y perfectamente coordinada entre el entorno virtual y el físico.

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

**Luxury_SL** ofrece una integración completa entre hardware y software, permitiendo una experiencia inmersiva y educativa donde el usuario aprende sobre **programación**, **diseño 3D** y **control electrónico**.  
El proyecto demuestra el potencial de combinar la ingeniería, el diseño y la educación STEAM en un solo entorno interactivo.

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

<img src="https://i.imgur.com/qPQOsBJ.png" width="350"/>

</div>
