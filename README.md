# SMX2_LuxurySL  
**Estado:** En desarrollo | **Tecnologías:** Blender | Arduino | C/C++

---

## Sobre el Proyecto

### Nombre del Proyecto  
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

---

## Equipo  
**Katya Robuste • Pau Ferrer • Nazar Kishchuk**

---

## Logo  
![Logo Luxury_SL](https://i.imgur.com/BqUJceo.jpeg)

---

# Índice del Proyecto

### 1. Introducción  
Qué estamos creando y por qué lo hacemos.  

### 2. Cómo Surgió la Idea  
De dónde vino la inspiración y los objetivos iniciales.  

### 3. Cómo Funciona el Sistema  
Explicación sencilla de cómo se conectan las partes del proyecto.  

### 4. Herramientas y Materiales  
Todo lo que usamos: software, hardware y componentes.  

### 5. Conexiones del Proyecto  
Cómo se comunican el coche, el mando y la web.  

### 6. Esquema de Red  
Resumen de cómo se organiza la red del sistema.  

### 7. Parte Física  
Los componentes reales: coche, Arduino, Bluetooth y mando.  

### 8. Parte Lógica  
Cómo fluye la información entre las partes.  

### 9. La Web del Proyecto  
Qué se puede hacer en la web y cómo se usa.  

### 10. Diseño Visual  
Colores, estilo y aspecto general.  

### 11. Prototipo (Mockup)  
Bocetos y vista previa del diseño final.  

### 12. Navegación Web  
Cómo se mueven los usuarios por la página.  

### 13. Servicios del Sistema   

### 14. DNS y Red   

### 15. IPs Automáticas (DHCP)  

### 16. Servidor Web (Apache)  

### 17. Seguridad (Firewall)   

### 18. Copias de Seguridad  

### 19. Conclusiones  .  

### 20. Bibliografía  

### 21. Base de Datos del Proyecto  

---

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


---

# 9. La Web del Proyecto  


---

# 10. Diseño Visual  

Colores: **negro, blanco y gris**, estilo elegante y moderno.  
El vídeo del coche es el elemento principal.

---

# 11. Prototipo (Mockup)  

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


---

# 15. IPs Automáticas (DHCP)  


---

# 16. Servidor Web (Apache)  


---

# 17. Seguridad (Firewall)  

---

# 18. Copias de Seguridad  


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
