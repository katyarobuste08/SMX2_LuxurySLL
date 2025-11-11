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

A través de una **interfaz intuitiva**, el usuario puede **crear una cuenta**, acceder a **tutoriales paso a paso**, dejar **comentarios al soporte técnico** y explorar el proyecto de manera interactiva.  

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

<img src="https://i.imgur.com/BqUJceo.jpeg" width="350"/>

</div>

El diseño de **Luxury_SL** busca combinar **elegancia, modernidad y funcionalidad**. Desde la primera impresión, se percibe un enfoque visual cuidado y minimalista, pensado para resaltar la **tecnología y el lujo** que caracterizan el proyecto. La interfaz está diseñada para que el usuario se sumerja en la experiencia sin distracciones innecesarias, concentrándose en los **modelos 3D** y los contenidos educativos.

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
- **Fusión entre virtual y físico:** Cada decisión de diseño refleja la visión del proyecto y su estética tecnológica.  

---

### **Pantallas del Diseño Web**

#### **Dashboard de Inicio**
<img src="https://i.imgur.com/Xhj3vUs.png" width="1000"/>
<p>
Esta pantalla de inicio es la primera impresión que recibe el usuario al entrar a Luxury_SL. Muestra el logotipo, el menú principal y accesos directos a las secciones más importantes, como el modelo 3D, tutoriales y soporte. Su diseño elegante y minimalista transmite lujo y tecnología, invitando al usuario a explorar la plataforma. Se enfoca en la claridad visual y la navegación rápida.
</p>

#### **Iniciar Sesión / Crear Cuenta**
<img src="https://i.imgur.com/xFugChF.png" width="1000"/>
<p>
Pantalla donde los usuarios pueden iniciar sesión si ya poseen una cuenta o crear un nuevo perfil para acceder al contenido exclusivo de Luxury_SL. Esta sección es fundamental para personalizar la experiencia, guardar el progreso del usuario y permitir el acceso a funcionalidades avanzadas, como la interacción con el modelo 3D y los proyectos educativos.
</p>

#### **Objetivos**
<img src="https://i.imgur.com/snpG4OU.png" width="1000"/>
<p>
Esta pantalla muestra la sección principal de la plataforma, con su diseño visual y la organización de los elementos. Permite al usuario visualizar cómo se distribuyen los menús, botones y contenidos dentro del proyecto Luxury_SL. Es una vista conceptual de la interfaz, sin implicar funcionalidades activas.
</p>

#### **Arquitectura Del Proyecto**
<img src="https://i.imgur.com/iM1fOzK.png" width="1000"/>
<p>
La imagen muestra la arquitectura de la plataforma web Luxury_SL, donde el usuario accede desde un navegador para interactuar con el área de usuario, tutoriales y contenido exclusivo. El servidor web gestiona las solicitudes, entrega las páginas y recursos multimedia, y se conecta con la base de datos que almacena perfiles, registros y preferencias. La plataforma cuenta con servicios internos como DNS, DHCP, Firewall y copias de seguridad, garantizando seguridad, conectividad y estabilidad. Toda la información fluye entre usuario, servidor y base de datos de forma segura y organizada
</p>

#### **Flujo De Datos**
<img src="https://i.imgur.com/6NnGtWI.png" width="1000"/>
<p>
el Mapa de Navegación Web de Luxury_SL, visualizando cómo están organizadas y conectadas las diferentes secciones de la plataforma —como Inicio, Usuario, Contenido Educativo, Proyectos y Soporte—, permitiendo al equipo de desarrollo entender de un vistazo la jerarquía y los posibles flujos de acceso dentro del sitio.
</p>

#### **Stack Tecnologico**
<img src="https://i.imgur.com/4gWzAay.png" width="1000"/>
<p>
La imagen muestra el stack tecnológico y los componentes de la plataforma web Luxury_SL, incluyendo todas las secciones y funcionalidades que contiene la web. Se pueden observar elementos como la interfaz de usuario, el área de usuario, los tutoriales y contenido educativo, la gestión de proyectos, la navegación del sitio y los servicios internos que soportan la plataforma. Representa de manera visual todo lo que la web ofrece al usuario final, mostrando cómo se integran los distintos módulos y recursos en una experiencia completa y organizada.
</p>

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

Permite **rotación, zoom e interacción** directa.

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
Desde allí puede interactuar con el modelo 3D, crear o iniciar sesión.  
La comunicación se realiza mediante **HTTPS**, garantizando la seguridad y la integridad de los datos.

---

#### **Servidor Web (Apache)**
El **servidor web** actúa como núcleo del sistema.  
Aloja la **plataforma web**, las **APIs** y los **recursos multimedia** (archivos HTML, CSS, JS, y modelos 3D).  

---

#### **Base de Datos (MySQL / SQLite)**
Almacena información estructurada, incluyendo:
- Datos de usuarios y autenticación.  
- Registros de sesiones y preferencias.  

Permite una recuperación eficiente de datos y mantiene la persistencia del sistema educativo.

---

#### **Arduino ESP32**
El componente **físico principal** del sistema.  
Controla el coche real y envía información al servidor sobre el estado del coche (movimientos, luces, energía, etc.), manteniendo sincronización constante con el modelo 3D digital.

---

#### **Conexión Bluetooth y Comunicación Serial**
El **módulo Bluetooth** del ESP32 establece una comunicación bidireccional.  

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
