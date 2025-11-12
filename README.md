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
  - Diagrama Arduino  
  - Modelo 3D del coche  
- Servicios  
  - DNS  
  - DHCP  
  - Apache  
  - Firewall  
  - Copias de Seguridad  
  - Diagrama de Usuarios y Roles  
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
Pantalla de inicio, con logotipo, menú principal y accesos directos a secciones clave como modelo 3D, tutoriales y soporte. Diseñada para claridad visual y navegación rápida.
</p>

#### **Iniciar Sesión / Crear Cuenta**
<img src="https://i.imgur.com/xFugChF.png" width="1000"/>
<p>
Pantalla donde los usuarios pueden iniciar sesión o crear un perfil. Permite personalizar la experiencia, guardar progreso y acceder a funcionalidades avanzadas, incluyendo interacción con el modelo 3D y proyectos educativos.
</p>

#### **Objetivos**
<img src="https://i.imgur.com/snpG4OU.png" width="1000"/>
<p>
Sección de objetivos de la plataforma, mostrando organización de menús, botones y contenidos. Vista conceptual de la interfaz.
</p>

#### **Arquitectura del Proyecto**
<img src="https://i.imgur.com/iM1fOzK.png" width="1000"/>
<p>
Arquitectura de la plataforma web Luxury_SL, mostrando interacción del usuario con la web, servidor, base de datos y servicios internos. Flujo de información seguro y organizado.
</p>

#### **Flujo de Datos**
<img src="https://i.imgur.com/6NnGtWI.png" width="1000"/>
<p>
Mapa de navegación, mostrando cómo se conectan secciones como Inicio, Usuario, Contenido Educativo, Proyectos y Soporte. Permite entender jerarquía y flujo de acceso.
</p>

#### **Stack Tecnológico**
<img src="https://i.imgur.com/4gWzAay.png" width="1000"/>
<p>
Stack tecnológico de Luxury_SL, mostrando todos los módulos y servicios internos, incluyendo la interfaz, área de usuario, tutoriales, gestión de proyectos y navegación.
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

### Diagrama Arduino

<div align="center">
<img src="https://i.imgur.com/cGVPCzm.png" width="600"/>
</div>

El siguiente diagrama muestra la estructura completa del sistema físico del coche controlado por Arduino ESP32.  
En este esquema se observa cómo cada componente cumple una función específica dentro del conjunto. La **placa ESP32** actúa como el cerebro central del vehículo, procesando las instrucciones enviadas desde la interfaz web a través de la conexión **Bluetooth**.  
Estas órdenes se traducen en movimientos y respuestas físicas del coche, controlando la dirección, la velocidad y las luces de manera inalámbrica y precisa.

El sistema está diseñado para ofrecer una conexión estable y eficiente entre el entorno digital y el hardware físico. Los **motores** son los encargados del desplazamiento del vehículo, mientras que el **driver L298N** o un módulo similar regula la energía que los alimenta. Los **cables jumper** conectan cada elemento eléctrico del circuito, garantizando la comunicación entre la placa, el controlador y las ruedas.

El **chasis**, fabricado generalmente en acrílico o metal ligero, sirve como base estructural para todos los componentes. Además, se incluyen **luces LED** opcionales que permiten simular faros, indicadores o retroalimentación visual del estado del coche.

En conjunto, esta configuración permite que el coche físico responda de forma sincronizada con su modelo 3D en la plataforma web de **Luxury_SL**, logrando una integración total entre el software y el hardware.

---

### Modelo 3D del coche

El modelo 3D representa un **Lamborghini negro** creado completamente desde cero en **Blender**.  
El proceso comenzó con el modelado digital detallado, cuidando cada curva y proporción del vehículo para reflejar el estilo elegante y deportivo de la marca.  
Una vez terminado el diseño, el modelo fue **exportado y preparado para impresión 3D**, lo que permitió fabricar una **versión física del coche** que posteriormente se utilizó para integrar el sistema **Arduino ESP32**.  

De esta manera, el **modelo virtual y el modelo físico** comparten las mismas proporciones y estética, conectando el entorno digital con la realidad tangible.

<div align="center">
  <img src="https://i.imgur.com/IZttiWP.png" width="600"/>
</div>

<div align="center">
  <img src="https://i.imgur.com/bTWoQN3.png" width="600"/>
</div>

El modelo digital conserva los materiales y reflejos característicos de la carrocería negra brillante, con detalles aerodinámicos y acabados de alta calidad.  
En su forma impresa, este Lamborghini se convierte en la base física perfecta para montar los componentes del sistema Arduino, sirviendo como ejemplo de la unión entre **diseño 3D, ingeniería electrónica y fabricación real**.

**Visualiza el modelo 3D:** [Sketchfab Luxury_SL](https://skfb.ly/pCxW9)

</details>

---

<details>
<summary><strong>RED</strong></summary>

### **Arquitectura de la Red – LUXURY_SL**

<div align="center">
<img src="https://i.imgur.com/WzbjxSQ.png" width="800"/>
</div>

La arquitectura de red de **Luxury_SL** está diseñada para garantizar una **comunicación fluida**, **seguridad de los datos** y **sincronización en tiempo real** entre los componentes **físicos (Arduino ESP32)** y **virtuales (sitio web + modelo 3D)**.  
Cada elemento cumple una función específica dentro del flujo de información, asegurando que tanto el control del coche físico como la visualización 3D respondan de forma coordinada.

#### **Cliente / Usuario**  
El usuario final accede desde un navegador web al sitio oficial de **Luxury_SL**.  
Desde allí puede interactuar con el modelo 3D, crear o iniciar sesión.  
La comunicación se realiza mediante **HTTPS**, garantizando la seguridad y la integridad de los datos.

#### **Servidor Web (Apache)**  
El servidor web actúa como núcleo del sistema.  
Aloja la **plataforma web**, las **APIs** y los **recursos multimedia** (archivos HTML, CSS, JS, y modelos 3D).

#### **Base de Datos (MySQL / SQLite)**  
Almacena información estructurada, incluyendo:  
- Datos de usuarios y autenticación.  
- Registros de sesiones y preferencias.

Permite una recuperación eficiente de datos y mantiene la persistencia del sistema educativo.

#### **Arduino ESP32**  
Controla el coche real y envía información al servidor sobre el estado del coche (movimientos, luces, energía, etc.), manteniendo sincronización constante con el modelo 3D digital.

#### **Conexión Bluetooth y Comunicación Serial**  
El módulo Bluetooth del ESP32 establece una comunicación bidireccional.

#### **Sincronización Web–Hardware**  
1. El usuario envía una acción desde la interfaz.  
2. El servidor procesa la solicitud y la envía al ESP32.  
3. El coche físico ejecuta la acción.  
4. El resultado se refleja visualmente en el entorno 3D del navegador.

</details>

---

<details>
<summary><strong>SERVICIOS</strong></summary>

### **Servicios de Luxury_SL – Para qué los usaremos y cómo te benefician**

Cada servicio cumple una función crítica para que la plataforma funcione de manera **fluida, segura y educativa**. Te explicaré **para qué lo usamos** primero y luego una **explicación completa**, como si yo te guiara.

---

### **1. DNS (Domain Name System)**  

**Para qué lo usaremos:**  
Para que los usuarios puedan acceder a Luxury_SL escribiendo un nombre fácil de recordar y que el ESP32 se conecte automáticamente al servidor.

**Explicación:**  
El DNS traduce el nombre de la web a la dirección correcta. Esto permite que accedas rápido y que tus acciones (mover el coche, encender luces) se reflejen en tiempo real en el coche físico y el modelo 3D. Todo funciona sin que tengas que preocuparte por direcciones IP.

---

### **2. DHCP**  

**Para qué lo usaremos:**  
Para asignar automáticamente direcciones IP únicas a todos los dispositivos que se conecten a la red.

**Explicación:**  
Con DHCP, tu ordenador, móvil o el ESP32 reciben una IP sin conflictos, permitiendo que los comandos lleguen correctamente al servidor y al coche físico. Esto garantiza que la experiencia sea fluida y sin interrupciones.

---

### **3. Apache**  

**Para qué lo usaremos:**  
Para alojar la web, entregar los contenidos, manejar APIs y sincronizar la interacción con la base de datos y el ESP32.

**Explicación:**  
Apache procesa todas tus acciones en la web y las envía al ESP32 usando C++. Guarda tus proyectos y progreso, manteniendo todo sincronizado con el modelo 3D y el coche físico.

---

### **4. Firewall**  

**Para qué lo usaremos:**  
Para proteger la plataforma y el hardware de accesos no autorizados.

**Explicación:**  
Controla qué usuarios pueden hacer qué acciones, asegurando que nadie externo interfiera con tus proyectos.

---

### **5. Copias de Seguridad**  

**Para qué lo usaremos:**  
Para guardar toda la información de usuarios, proyectos y tutoriales.

**Explicación:**  
Permiten restaurar datos si algo falla y mantener la sincronización entre acciones web y coche físico.

---

### **6. Diagrama de Usuarios y Roles**  

**Para qué lo usaremos:**  
Para mostrar cómo interactúan los diferentes roles con los servicios y cómo todo está conectado.

<div align="center">
<img src="https://i.imgur.com/r03QN0i.png" width="600"/>
</div>

**Explicación:**  
- Estudiantes usan la web para mover el coche y seguir tutoriales.  
- Docentes supervisan y guían.  
- Administradores gestionan servicios, seguridad y copias de seguridad.  
- Visitantes exploran contenido público.

Los servicios aseguran que la experiencia sea **fluida, segura y educativa**, reflejando tus acciones en el modelo 3D y el coche físico.

</details>

---

<details>
<summary><strong>CONCLUSIONES</strong></summary>

**Luxury_SL** integra hardware y software para ofrecer una experiencia educativa inmersiva. Permite aprender sobre **programación, diseño 3D y control electrónico**, demostrando el potencial de combinar ingeniería, diseño y educación STEAM en un solo entorno interactivo.

</details>

---

<details>
<summary><strong>BIBLIOGRAFÍA</strong></summary>

- [Blender Documentation](https://www.blender.org/)  
- [Three.js Manual](https://threejs.org/docs/)  
- [Arduino ESP32 Reference](https://docs.arduino.cc/hardware/esp32/)  
- [HTML/CSS/JS MDN Docs](https://developer.mozilla.org/)  

</details>

<div align="center">
<img src="https://i.imgur.com/qPQOsBJ.png" width="350"/>
</div>
