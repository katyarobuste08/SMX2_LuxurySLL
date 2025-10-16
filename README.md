# SMX2_LuxurySL  
**Estado:** En desarrollo | **Tecnologías:** Blender | Arduino | C/C++
## Equipo  

**Katya Robuste • Pau Ferrer • Nazar Kishchuk**

---

<details>
<summary>Briefing</summary>
<div style="margin-left: 20px; padding: 10px 0;">

**SMX2_LuxurySL**

### Descripción  
*SMX2_LuxurySL* es un proyecto donde mezclamos diseño 3D y programación.  
Creamos un coche de lujo en **Blender** y lo conectamos a un **Arduino** para poder moverlo con **Bluetooth** usando un mando.  
El coche puede avanzar, retroceder, girar y encender sus luces.

### Objetivo  
Construir un coche que combine el mundo digital (3D) con el físico (Arduino), mostrando cómo se puede unir el diseño, la electrónica y la programación en un solo proyecto.

### A quién va dirigido  
A estudiantes, profesores y personas curiosas que disfruten de la tecnología, los coches y aprender haciendo cosas prácticas.

### Tecnologías que usamos  
- **Blender 3D:** para diseñar el coche.  
- **Arduino (C/C++):** para controlar el movimiento.  
- **Bluetooth:** para conectar el mando.  
- **HTML / CSS / PHP:** para la web.  
- **MySQL:** para guardar usuarios y comentarios.  

### Lo que entregamos  
- Modelo 3D del coche.  
- Arduino configurado con Bluetooth.  
- Web del proyecto.  
- Base de datos con usuarios y comentarios.  
- Documentación completa.  

</div>
</details>

---

![Logo Luxury_SL](https://i.imgur.com/BqUJceo.jpeg)

---

<details>
<summary>Índice del Proyecto SMX2_LuxurySL</summary>
<div style="margin-left: 20px; padding: 10px 0;">

## **1. Índice**  
## **2. Introducción - ¿qué estamos haciendo?**  
## **3. Briefing de ideas**  
## **4. Arquitectura del software**  
## **5. Tecnologías a utilizar**  
## **6. Red**  
## **7. Web**  
## **8. Servicios**  
## **9. Conclusiones**  
## **10. Bibliografía**

</div>
</details>

---

<details>
<summary>Introducción y Contenido Completo</summary>
<div style="margin-left: 20px; padding: 10px 0;">

<details>
<summary> **Introducción**</summary>
<div style="margin-left: 20px; padding: 10px 0;">

Estamos creando un coche de lujo en 3D que se puede controlar con un mando Bluetooth gracias a Arduino.  
El proyecto mezcla diseño, programación y electrónica para aprender cómo se conectan el mundo físico y el digital.

</div>
</details>

---

<details>
<summary> **Cómo Surgió la Idea**</summary>
<div style="margin-left: 20px; padding: 10px 0;">

Queríamos hacer algo original que uniera creatividad y tecnología.  
Así nació la idea de **un coche 3D realista que también se mueve en la vida real** usando sensores y Bluetooth.

</div>
</details>

---

<details>
<summary> **Cómo Funciona el Sistema**</summary>
<div style="margin-left: 20px; padding: 10px 0;">

El proyecto se divide en tres partes:  
- **Diseño 3D:** se crea el coche en Blender.  
- **Control físico:** Arduino recibe los comandos por Bluetooth y mueve el coche.  
- **Web:** donde los usuarios pueden registrarse, ver el proyecto y dejar comentarios.

</div>
</details>

---

<details>
<summary> **Herramientas y Materiales**</summary>
<div style="margin-left: 20px; padding: 10px 0;">

- Blender 3D  
- Arduino UNO  
- Módulo Bluetooth HC-05  
- LEDs para luces  
- Baterías recargables  
- Cables y protoboard  
- HTML, CSS, PHP, MySQL para la web  

</div>
</details>

---

<details>
<summary> **Conexiones del Proyecto**</summary>
<div style="margin-left: 20px; padding: 10px 0;">

El mando se conecta por Bluetooth al Arduino, el Arduino controla los motores del coche y la web muestra toda la información del sistema y los comentarios de los usuarios.

</div>
</details>

---

<details>
<summary> **Esquema de Red**</summary>
<div style="margin-left: 20px; padding: 10px 0;">

Incluye:  
- Firewall (PFSense)  
- Servidor web (Apache)  
- Base de datos (MySQL)  
- Servidor DNS y DHCP  
- Sistema de copias de seguridad  

</div>
</details>

---

<details>
<summary> **Parte Física**</summary>
<div style="margin-left: 20px; padding: 10px 0;">

Contiene los componentes reales: el coche, el Arduino, los motores, el módulo Bluetooth y el mando.

</div>
</details>

---

<details>
<summary> **Parte Lógica**</summary>
<div style="margin-left: 20px; padding: 10px 0;">

Explica cómo la información pasa del mando Bluetooth al Arduino, luego a los motores, y finalmente se registra en la web.  
También incluye cómo el sistema interpreta los comandos y los transforma en acciones físicas.

</div>
</details>

---

<details>
<summary> **La Web del Proyecto**</summary>
<div style="margin-left: 20px; padding: 10px 0;">

La web muestra el coche, permite registrarse, iniciar sesión, ver actualizaciones y dejar comentarios sobre el proyecto.

</div>
</details>

---

<details>
<summary> **Diseño Visual**</summary>
<div style="margin-left: 20px; padding: 10px 0;">

Colores: **negro, blanco y gris**, estilo elegante y moderno.  
El vídeo del coche es el elemento principal.

</div>
</details>

---

<details>
<summary> **Prototipo (Mockup)**</summary>
<div style="margin-left: 20px; padding: 10px 0;">

Incluye bocetos del diseño de la web, las páginas principales y cómo se verán las secciones desde distintos dispositivos.

</div>
</details>

---

<details>
<summary> **Navegación Web**</summary>
<div style="margin-left: 20px; padding: 10px 0;">

Inicio → Registro/Login → Página del coche → Comentarios → Soporte  

</div>
</details>

---

<details>
<summary> **Servicios del Sistema**</summary>
<div style="margin-left: 20px; padding: 10px 0;">

- Apache (servidor web)  
- MySQL (base de datos)  
- DNS y DHCP  
- TrueNAS (backups automáticos)

</div>
</details>

---

<details>
<summary> **DNS y Red**</summary>
<div style="margin-left: 20px; padding: 10px 0;">

Configuración de red y nombres de dominio para acceder fácilmente al proyecto desde la red local.

</div>
</details>

---

<details>
<summary> **IPs Automáticas (DHCP)**</summary>
<div style="margin-left: 20px; padding: 10px 0;">

Sistema que asigna direcciones IP automáticamente a los dispositivos conectados al proyecto.

</div>
</details>

---

<details>
<summary> **Servidor Web (Apache)**</summary>
<div style="margin-left: 20px; padding: 10px 0;">

Servidor que permite alojar la página del proyecto y mostrar la información en la red.

</div>
</details>

---

<details>
<summary> **Seguridad (Firewall)**</summary>
<div style="margin-left: 20px; padding: 10px 0;">

Protege el sistema de accesos no deseados mediante reglas configuradas en PFSense.

</div>
</details>

---

<details>
<summary> **Copias de Seguridad**</summary>
<div style="margin-left: 20px; padding: 10px 0;">

Las copias se realizan con **TrueNAS**, asegurando que los datos del proyecto no se pierdan.

</div>
</details>

---

<details>
<summary> **Conclusiones**</summary>
<div style="margin-left: 20px; padding: 10px 0;">

Este proyecto une diseño, programación y electrónica en algo visual y útil.  
Aprendimos a conectar hardware con software y a trabajar en equipo.  

</div>
</details>

---

<details>
<summary> **Bibliografía**</summary>
<div style="margin-left: 20px; padding: 10px 0;">

- Manual de Blender  
- Guías de Arduino y Bluetooth  
- Documentación de PFSense y Apache  
- Tutoriales de HTML, CSS, PHP y MySQL  

</div>
</details>

---

<details>
<summary> **Base de Datos del Proyecto**</summary>
<div style="margin-left: 20px; padding: 10px 0;">

### Qué se puede hacer en la web  
- Crear cuenta (nombre, apellidos, correo, contraseña)  
- Enviar comentarios al soporte técnico  

### Entidades principales  
- Usuarios  
- Comentarios  
- Herramientas  
- Arduino  
- Diseño 3D  
- Coche  

</div>
</details>

---

<details>
<summary> **Datos guardados**</summary>
<div style="margin-left: 20px; padding: 10px 0;">

| Entidad     | Atributos |
|--------------|------------|
| Usuarios     | Id, Nombre, Apellidos, Email, Contraseña, Fecha de registro |
| Comentarios  | Id comentario, Id usuario, Mensaje, Fecha |
| Herramientas | Nombre, Descripción, Cantidad |
| Arduino      | Id Arduino, Modelo, Descripción, Fecha de compra |
| Diseño 3D    | Id diseño, Nombre diseño, Archivo Blender, Descripción, Fecha creación |
| Coche        | Id coche, Id diseño, Id Arduino, Estado, Configuración |

### Relaciones  
- Un usuario puede hacer varios comentarios.  
- Un diseño 3D puede usarse en varios coches.  
- Un Arduino puede controlar varios coches.  

### Ejemplo de datos  

| Entidad | Ejemplo |
|----------|----------|
| Usuario | Juan Pérez, (juanp@gmail.com) , 10/09/2025 |
| Comentario | Duda con Bluetooth, 02/10/2025 |
| Arduino | Modelo: Arduino UNO, 02/10/2025 |

### Dificultades y reflexiones  

Durante el desarrollo tuvimos que aprender a conectar hardware y software, sincronizar el diseño 3D con el sistema real y coordinar el trabajo en equipo para que todo funcionara de forma estable y visualmente atractiva.

</div>
</details>

</div>
</details>

