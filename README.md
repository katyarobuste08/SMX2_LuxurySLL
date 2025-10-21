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

**Luxury_SL** combina un diseño 3D de un coche con un sistema Arduino que permite al usuario **construir, visualizar e interactuar** con su propio vehículo.  

Los usuarios pueden crear cuenta, consultar tutoriales, dejar comentarios al soporte y **controlar el coche vía Bluetooth** (movimientos: adelante, atrás, izquierda, derecha y luces).  

El proyecto busca una experiencia integrada entre el entorno **digital (web + 3D)** y el **físico (coche real controlado por Arduino ESP32)**.

</details>

---

<details>
<summary><strong>WEB</strong></summary>

### Diseño Web

La web utiliza un estilo **oscuro y minimalista** con efecto **glassmorphism**.  
Los paneles tienen transparencia suave, desenfoque de fondo y sombras sutiles para lograr una estética moderna.  

<div align="center">
<img src="https://i.imgur.com/zcfUlYo.png" alt="Mood de colores" width="450"/>
</div>

La navegación es fluida y dinámica, sin recargar la página.  
Incluye notificaciones tipo *toast*, animaciones suaves y un fondo en video que cambia según la sección activa.  

<div align="center">
<img src="https://i.imgur.com/dxfX96U.png" alt="Diseño Web" width="700"/>
</div>

---

<details>
<summary><strong>Base de Datos (Logging)</strong></summary>

El sistema usa **localStorage** para manejar usuarios y comentarios de forma local, rápida y segura, sin necesidad de servidor externo.

<div align="center">
<img src="https://i.imgur.com/ahRo6nr.png" alt="Base de Datos - Logging" width="500"/>
</div>

### Tabla de Usuarios

| Campo          | Ejemplo        | Descripción                                          |
|----------------|----------------|------------------------------------------------------|
| Nombre         | Juan Pérez     | Nombre completo del usuario                          |
| Email          | juanp@gmail.com| Correo electrónico usado para registro y contacto    |
| Fecha Registro | 10/09/2025     | Fecha en la que se creó la cuenta                    |

### Tabla de Comentarios

| Campo         | Ejemplo                                      | Descripción                                      |
|---------------|---------------------------------------------|-------------------------------------------------|
| Id comentario | 001                                         | Identificador único del comentario              |
| Id usuario    | 1                                           | Usuario que realizó el comentario               |
| Mensaje       | Tengo dudas sobre cómo conectar el módulo Bluetooth | Contenido del mensaje del usuario              |
| Fecha         | 2025-10-02                                  | Fecha de creación del comentario                |

</details>
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
