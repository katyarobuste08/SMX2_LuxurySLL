# SMX2_LuxurySL  
**Estado:** En desarrollo | **Tecnologías:** Blender | Arduino | C/C++

## Equipo  
**Katya Robuste • Pau Ferrer • Nazar Kishchuk**

---

<details>
<summary> **Briefing**</summary>

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

</details>

---

![Logo Luxury_SL](https://i.imgur.com/BqUJceo.jpeg)

---

<details>
<summary> **Índice del Proyecto SMX2_LuxurySL**</summary>

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

</details>

---

<details>
<summary> **Introducción y Contenido Completo**</summary>

<details>
<summary> **Introducción**</summary>

Estamos creando un coche de lujo en 3D que se puede controlar con un mando Bluetooth gracias a Arduino.  
El proyecto mezcla diseño, programación y electrónica para aprender cómo se conectan el mundo físico y el digital.

</details>

---

<details>
<summary> **Cómo Surgió la Idea**</summary>

Queríamos hacer algo original que uniera creatividad y tecnología.  
Así nació la idea de **un coche 3D realista que también se mueve en la vida real** usando sensores y Bluetooth.

</details>

---

<details>
<summary> **Cómo Funciona el Sistema**</summary>

El proyecto se divide en tres partes:  
- **Diseño 3D:** se crea el coche en Blender.  
- **Control físico:** Arduino recibe los comandos por Bluetooth y mueve el coche.  
- **Web:** donde los usuarios pueden registrarse, ver el proyecto y dejar comentarios.

</details>

---

<details>
<summary> **Herramientas y Materiales**</summary>

- Blender 3D  
- Arduino UNO  
- Módulo Bluetooth HC-05  
- LEDs para luces  
- Baterías recargables  
- Cables y protoboard  
- HTML, CSS, PHP, MySQL para la web  

</details>

---

<details>
<summary> **Conexiones del Proyecto**</summary>

El mando se conecta por Bluetooth al Arduino, el Arduino controla los motores del coche y la web muestra toda la información del sistema y los comentarios de los usuarios.

</details>

---

<details>
<summary> **Esquema de Red**</summary>

Incluye:  
- Firewall (PFSense)  
- Servidor web (Apache)  
- Base de datos (MySQL)  
- Servidor DNS y DHCP  
- Sistema de copias de seguridad  

</details>

---

<details>
<summary> **Parte Física**</summary>

Contiene los componentes reales: el coche, el Arduino, los motores, el módulo Bluetooth y el mando.

</details>

---

<details>
<summary> **Parte Lógica**</summary>

Explica cómo la información pasa del mando Bluetooth al Arduino, luego a los motores, y finalmente se registra en la web.  
También incluye cómo el sistema interpreta los comandos y los transforma en acciones físicas.

</details>

---

<details>
<summary> **La Web del Proyecto**</summary>

La web muestra el coche, permite registrarse, iniciar sesión, ver actualizaciones y dejar comentarios sobre el proyecto.

</details>

---

<details>
<summary> **Diseño Visual**</summary>

Colores: **negro, blanco y gris**, estilo elegante y moderno.  
El vídeo del coche es el elemento principal.

</details>

---

<details>
<summary> **Prototipo (Mockup)**</summary>

Incluye bocetos del diseño de la web, las páginas principales y cómo se verán las secciones desde distintos dispositivos.

</details>

---

<details>
<summary> **Navegación Web**</summary>

Inicio → Registro/Login → Página del coche → Comentarios → Soporte  

</details>

---

<details>
<summary> **Servicios del Sistema**</summary>

- Apache (servidor web)  
- MySQL (base de datos)  
- DNS y DHCP  
- TrueNAS (backups automáticos)

</details>

---

<details>
<summary> **DNS y Red**</summary>

Configuración de red y nombres de dominio para acceder fácilmente al proyecto desde la red local.

</details>

---

<details>
<summary> **IPs Automáticas (DHCP)**</summary>

Sistema que asigna direcciones IP automáticamente a los dispositivos conectados al proyecto.

</details>

---

<details>
<summary> **Servidor Web (Apache)**</summary>

Servidor que permite alojar la página del proyecto y mostrar la información en la red.

</details>

---

<details>
<summary> **Seguridad (Firewall)**</summary>

Protege el sistema de accesos no deseados mediante reglas configuradas en PFSense.

</details>

---

<details>
<summary> **Copias de Seguridad**</summary>

Las copias se realizan con **TrueNAS**, asegurando que los datos del proyecto no se pierdan.

</details>

---

<details>
<summary> **Conclusiones**</summary>

Este proyecto une diseño, programación y electrónica en algo visual y útil.  
Aprendimos a conectar hardware con software y a trabajar en equipo.  

</details>

---

<details>
<summary> **Bibliografía**</summary>

- Manual de Blender  
- Guías de Arduino y Bluetooth  
- Documentación de PFSense y Apache  
- Tutoriales de HTML, CSS, PHP y MySQL  

</details>

---

<details>
<summary> **Base de Datos del Proyecto**</summary>

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

</details>

---

<details>
<summary> **Datos Guardados y Relacionados**</summary>

###  Datos guardados  

| Entidad     | Atributos |
|--------------|------------|
| Usuarios     | Id, Nombre, Apellidos, Email, Contraseña, Fecha de registro |
| Comentarios  | Id comentario, Id usuario, Mensaje, Fecha |
| Herramientas | Nombre, Descripción, Cantidad |
| Arduino      | Id Arduino, Modelo, Descripción, Fecha de compra |
| Diseño 3D    | Id diseño, Nombre diseño, Archivo Blender, Descripción, Fecha creación |
| Coche        | Id coche, Id diseño, Id Arduino, Estado, Configuración |

---

###  Relaciones  
- Un usuario puede hacer varios comentarios.  
- Un diseño 3D puede usarse en varios coches.  
- Un Arduino puede controlar varios coches.  

---

###  Ejemplo de datos  

| Entidad | Ejemplo |
|----------|----------|
| Usuario | Juan Pérez, (juanp@gmail.com), 10/09/2025 |
| Comentario | Duda con Bluetooth, 02/10/2025 |
| Arduino | Modelo: Arduino UNO, 02/10/2025 |

---

###  Dificultades y reflexiones  

Durante el desarrollo tuvimos que aprender a conectar hardware y software, sincronizar el diseño 3D con el sistema real y coordinar el trabajo en equipo para que todo funcionara de forma estable y visualmente atractiva.

</details>

</details>
