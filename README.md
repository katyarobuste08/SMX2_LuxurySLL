# SMX2_LuxurySL  
**Estado:** En desarrollo | **Tecnologías:** Blender | Arduino | C/C++
## Equipo  

**Katya Robuste • Pau Ferrer • Nazar Kishchuk**

---

<details>
<summary>Briefing</summary>


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

## Logo  
![Logo Luxury_SL](https://i.imgur.com/BqUJceo.jpeg)

---

<details>
<summary> Índice del Proyecto SMX2_LuxurySL</summary>

**1. Introducción**  
 Qué estamos creando y por qué

**2. Cómo Surgió la Idea**  
 Motivación y objetivos iniciales

**3. Cómo Funciona el Sistema**  
 Interacción entre 3D, Arduino y web

**4. Herramientas y Materiales**  
 Software, hardware y componentes

**5. Conexiones del Proyecto**  
 Flujo de información entre dispositivos

**6. Esquema de Red**  
 Organización de servidores y servicios

**7. Parte Física**  
 Componentes reales: coche, Arduino y Bluetooth

**8. Parte Lógica**  
 Flujo de datos y procesamiento de comandos

**9. La Web del Proyecto**  
 Registro, control y visualización

**10. Diseño Visual**  
 Estilo, colores y presentación

**11. Prototipo (Mockup)**  
 Bocetos y diseño responsive

**12. Navegación Web**  
 Flujo de usuario desde inicio hasta soporte

**13. Servicios del Sistema**  
 Servidores, bases de datos y backups

**14. DNS y Red**  
 Configuración de nombres y conectividad

**15. IPs Automáticas (DHCP)**  
 Asignación de direcciones a dispositivos

**16. Servidor Web (Apache)**  
 Gestión de peticiones y contenido web

**17. Seguridad (Firewall)**  
 Protección de la red y reglas de acceso

**18. Copias de Seguridad**  
 Backups periódicos del proyecto

**19. Conclusiones**  
 Aprendizajes y resultados del proyecto

**20. Bibliografía**  
 Recursos consultados y documentación

**21. Base de Datos del Proyecto**  
 Entidades, relaciones y datos guardados

</details>

---

<details>
<summary> Introducción y Contenido Completo</summary>

# 1. Introducción  

Estamos creando un coche de lujo en 3D que se puede controlar con un mando Bluetooth gracias a Arduino.  
El proyecto mezcla diseño, programación y electrónica para aprender cómo se conectan el mundo físico y el digital.

---

# 2. Cómo Surgió la Idea  

Queríamos hacer algo original que uniera creatividad y tecnología.  
Así nació la idea de **un coche 3D realista que también se mueve en la vida real** usando sensores y Bluetooth.

---

# 3. Cómo Funciona el Sistema  

El proyecto se divide en tres partes:  
- **Diseño 3D:** se crea el coche en Blender.  
- **Control físico:** Arduino recibe los comandos por Bluetooth y mueve el coche.  
- **Web:** donde los usuarios pueden registrarse, ver el proyecto y dejar comentarios.

---

# 4. Herramientas y Materiales  

- Blender 3D  
- Arduino UNO  
- Módulo Bluetooth HC-05  
- LEDs para luces  
- Baterías recargables  
- Cables y protoboard  
- HTML, CSS, PHP, MySQL para la web  

---

# 5. Conexiones del Proyecto  

El mando se conecta por Bluetooth al Arduino, el Arduino controla los motores del coche y la web muestra toda la información del sistema y los comentarios de los usuarios.

---

# 6. Esquema de Red  

Incluye:  
- Firewall (PFSense)  
- Servidor web (Apache)  
- Base de datos (MySQL)  
- Servidor DNS y DHCP  
- Sistema de copias de seguridad  

---

# 7. Parte Física  

Contiene los componentes reales: el coche, el Arduino, los motores, el módulo Bluetooth y el mando.

---

# 8. Parte Lógica  

Explica cómo la información pasa del mando Bluetooth al Arduino, luego a los motores, y finalmente se registra en la web.  
También incluye cómo el sistema interpreta los comandos y los transforma en acciones físicas.

---

# 9. La Web del Proyecto  

La web muestra el coche, permite registrarse, iniciar sesión, ver actualizaciones y dejar comentarios sobre el proyecto.

---

# 10. Diseño Visual  

Colores: **negro, blanco y gris**, estilo elegante y moderno.  
El vídeo del coche es el elemento principal.

---

# 11. Prototipo (Mockup)  

Incluye bocetos del diseño de la web, las páginas principales y cómo se verán las secciones desde distintos dispositivos.

---

# 12. Navegación Web  

Inicio → Registro/Login → Página del coche → Comentarios → Soporte  

---

# 13. Servicios del Sistema  

- Apache (servidor web)  
- MySQL (base de datos)  
- DNS y DHCP  
- TrueNAS (backups automáticos)

---

# 14. DNS y Red

Configuración de red y nombres de dominio para acceder fácilmente al proyecto desde la red local.

---

# 15. IPs Automáticas (DHCP)

Sistema que asigna direcciones IP automáticamente a los dispositivos conectados al proyecto.

---

# 16. Servidor Web (Apache)

Servidor que permite alojar la página del proyecto y mostrar la información en la red.

---

# 17. Seguridad (Firewall)

Protege el sistema de accesos no deseados mediante reglas configuradas en PFSense.

---

# 18. Copias de Seguridad

Las copias se realizan con **TrueNAS**, asegurando que los datos del proyecto no se pierdan.

---

# 19. Conclusiones

Este proyecto une diseño, programación y electrónica en algo visual y útil.  
Aprendimos a conectar hardware con software y a trabajar en equipo.  

---

# 20. Bibliografía

- Manual de Blender  
- Guías de Arduino y Bluetooth  
- Documentación de PFSense y Apache  
- Tutoriales de HTML, CSS, PHP y MySQL  

---

# 21. Base de Datos del Proyecto

## Qué se puede hacer en la web  
- Crear cuenta (nombre, apellidos, correo, contraseña)  
- Enviar comentarios al soporte técnico  

## Entidades principales  
- Usuarios  
- Comentarios  
- Herramientas  
- Arduino  
- Diseño 3D  
- Coche  

</details>

---

<details>
<summary> Datos Guardados y Relacionados</summary>

## Datos guardados  

| Entidad     | Atributos |
|--------------|------------|
| Usuarios     | Id, Nombre, Apellidos, Email, Contraseña, Fecha de registro |
| Comentarios  | Id comentario, Id usuario, Mensaje, Fecha |
| Herramientas | Nombre, Descripción, Cantidad |
| Arduino      | Id Arduino, Modelo, Descripción, Fecha de compra |
| Diseño 3D    | Id diseño, Nombre diseño, Archivo Blender, Descripción, Fecha creación |
| Coche        | Id coche, Id diseño, Id Arduino, Estado, Configuración |

## Relaciones  
- Un usuario puede hacer varios comentarios.  
- Un diseño 3D puede usarse en varios coches.  
- Un Arduino puede controlar varios coches.  

## Ejemplo de datos  

| Entidad | Ejemplo |
|----------|----------|
| Usuario | Juan Pérez, (juanp@gmail.com) , 10/09/2025 |
| Comentario | Duda con Bluetooth, 02/10/2025 |
| Arduino | Modelo: Arduino UNO, 02/10/2025 |

## Dificultades y reflexiones  

Durante el desarrollo tuvimos que aprender a conectar hardware y software, sincronizar el diseño 3D con el sistema real y coordinar el trabajo en equipo para que todo funcionara de forma estable y visualmente atractiva.

</details>
