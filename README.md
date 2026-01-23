# 💎 LUXURY_SL: Proyecto Integral SMX2
> **Integración de sistemas, redes, hardware IoT y diseño industrial para el módulo de SMX2.**

<div align="center">
  <img src="https://i.imgur.com/FG6uNYF.png" width="220"/>
  <br>
  <h1><strong>LUXURY_SL</strong></h1>
  <p>Desarrollado por:</p>
  <h3><strong>Katya Robuste</strong> ⬥ <strong>Nazar Kishchuk</strong></h3>
  <br>
</div>

---

## 📑 Índice

<div align="center">

| 🟢 **1. INTRODUCCIÓN** | 🔵 **2. TECNOLOGÍAS** |
| :--- | :--- |
| Visión, objetivos y despliegue SMX2. | Software, Firmware y Herramientas. |
| 🟡 **3. WEB** | 🔴 **4. ARDUINO & 3D** |
| UX Premium, APIs y Telemetría. | ESP32, Motores y Modelado Industrial. |
| 🟣 **5. ARQUITECTURA & RED** | 🟠 **6. SERVICIOS & ROLES** |
| Latencia, Protocolos y Conectividad. | RBAC, Firewalls y Servicios de Red. |

</div>


---

<details id="introducción" open>
<summary><strong>✨ 1. Introducción</strong></summary>

**Luxury_SL** es un proyecto técnico diseñado para aplicar de forma práctica las competencias del ciclo de **SMX2** (Sistemas Microinformáticos y Redes). El objetivo central es la creación de un ecosistema donde la administración de servidores, el montaje de hardware y la configuración de redes convergen en un vehículo robótico controlado mediante una interfaz web.

En este proyecto, se han trabajado los siguientes pilares fundamentales:

* **Gestión de Sistemas y Servicios:** Se ha configurado una infraestructura de servidor capaz de procesar peticiones en tiempo real y gestionar bases de datos para el control de usuarios.
* **Redes y Conectividad:** Implementación de protocolos de comunicación inalámbrica para unir el panel de control web con el hardware físico (ESP32).
* **Montaje de Hardware:** Ensamblaje de componentes electrónicos, gestión de energía mediante baterías y construcción del chasis mediante fabricación aditiva.
* **Optimización de Recursos:** Aplicación de técnicas para reducir la latencia de red y asegurar una respuesta inmediata del coche ante las órdenes del usuario.

Este trabajo demuestra la capacidad de integrar múltiples tecnologías de sistemas y redes en un entorno real y funcional.

</details>

---

<details id="tecnologías-y-herramientas">
<summary><strong>🛠️ 2. Tecnologías y Herramientas</strong></summary>



| Tecnología | Aplicación en SMX2 | Función Específica |
| :---: | :--- | :--- |
| **Blender 3D** | Diseño de Chasis. | Modelado y optimización de piezas para impresión 3D. |
| **HTML5 / CSS3** | Panel de Control. | Estructura y diseño visual de la interfaz de usuario. |
| **JavaScript** | Lógica Frontend. | Comunicación asíncrona mediante Fetch API. |
| **Arduino ESP32** | Microcontrolador. | Gestión de hardware y conectividad de red. |
| **Apache** | Servidor Web. | Hosting de la plataforma y gestión de tráfico HTTP. |
| **MySQL** | Base de Datos. | Almacenamiento de perfiles, permisos y registros. |

<p align="center">
  <img src="https://e7.pngegg.com/pngimages/146/983/png-clipart-blender-3d-computer-graphics-logo-filehippo-3d-modeling-blenders-3d-computer-graphics-text-thumbnail.png" height="45"/>
  <img src="https://e7.pngegg.com/pngimages/187/112/png-clipart-responsive-web-design-html-computer-icons-css3-world-wide-web-consortium-css-angle-text.png" height="45"/>
  <img src="https://pngdownload.io/wp-content/uploads/2023/12/CSS-Logo-PNG-Symbol-for-Web-Development-Transparent-jpg.webp" height="45"/>
  <img src="https://cdn-icons-png.flaticon.com/512/8379/8379454.png" height="45"/>
  <img src="https://toppng.com/uploads/preview/arduino-logo-11563227354ny21akychx.png" height="45"/>
  <img src="https://img.favpng.com/25/15/12/logo-apache-http-server-apache-software-foundation-computer-servers-web-server-png-favpng-ebJ1wHvFsydhrpp6V0xFN5NBQ.jpg" height="45"/>
  <img src="https://e7.pngegg.com/pngimages/617/252/png-clipart-mysql-workbench-computer-icons-logo-database-server-blue-text.png" height="45"/>
</p>

</details>

---

<details id="web">
<summary><strong>🌐 3. Web</strong></summary>

La web de **Luxury_SL** es la consola central del administrador. Se ha diseñado una interfaz con estética "Dark Gold" para facilitar la visualización en entornos de trabajo técnicos y reducir la carga visual.

**Paleta de colores principal:**
<p align="center">
  <img src="https://i.imgur.com/zcfUlYo_d.png" width="600" />
</p>

### Mosaico de Interfaces de Control:

<table>
  <tr>
    <td align="center">
      <strong>Dashboard Principal</strong><br>
      <img src="https://i.imgur.com/Xhj3vUs.png" width="220"/><br>
      <span style="color:gray; font-size:13px;">Monitorización del estado del vehículo.</span>
    </td>
    <td align="center">
      <strong>Acceso de Usuario</strong><br>
      <img src="https://i.imgur.com/xFugChF.png" width="220"/><br>
      <span style="color:gray; font-size:13px;">Gestión de sesiones seguras.</span>
    </td>
    <td align="center">
      <strong>Mapa de Logros</strong><br>
      <img src="https://i.imgur.com/snpG4OU.png" width="220"/><br>
      <span style="color:gray; font-size:13px;">Seguimiento de tareas del proyecto.</span>
    </td>
  </tr>
  <tr>
    <td align="center">
      <strong>Planos Lógicos</strong><br>
      <img src="https://i.imgur.com/iM1fOzK.png" width="220"/><br>
    </td>
    <td align="center">
      <strong>Comunicación</strong><br>
      <img src="https://i.imgur.com/6NnGtWI.png" width="220"/><br>
    </td>
    <td align="center">
      <strong>Tecnologías</strong><br>
      <img src="https://i.imgur.com/4gWzAay.png" width="220"/><br>
    </td>
  </tr>
</table>

</details>

---

<details id="arduino-y-modelo-3d">
<summary><strong>🤖 4. Arduino & Modelo 3D</strong></summary>

### ⚡ Electrónica y Conectividad
El cerebro del coche es el **ESP32**. Este chip permite manejar la comunicación con el servidor web mientras controla los motores mediante señales **PWM** (Modulación por ancho de pulsos), lo que permite regular la velocidad con precisión.



<table>
  <tr>
    <td align="center">
      <strong>Esquema Eléctrico</strong><br>
      <img src="https://i.imgur.com/rijhOry.png" width="245"/><br>
    </td>
    <td align="center">
      <strong>Componentes</strong><br>
      <img src="https://i.imgur.com/cGVPCzm.png" width="245"/><br>
    </td>
  </tr>
</table>

### 🎨 Diseño y Fabricación 3D
<table>
  <tr>
    <td align="center">
      <strong>Prototipado Digital</strong><br>
      <img src="https://i.imgur.com/IZttiWP.png" width="245"/><br>
    </td>
    <td align="center">
      <strong>Modelo Físico</strong><br>
      <img src="https://i.imgur.com/bTWoQN3.png" width="245"/><br>
    </td>
  </tr>
</table>

> [!IMPORTANT]
> **Explora el modelo 3D:** [Sketchfab Luxury_SL](https://skfb.ly/pCxW9).  

</details>

---

<details id="arquitectura-y-red">
<summary><strong>🏗️ 5. Arquitectura & Red</strong></summary>

La red de **Luxury_SL** se ha configurado para garantizar que las órdenes del usuario lleguen al hardware de forma inmediata.

### Flujo de Datos del Sistema:
1.  **Capa de Aplicación:** El usuario envía una orden desde la web (p. ej., "Mover Adelante").
2.  **Procesamiento del Servidor:** Apache y PHP reciben la orden, verifican la autenticidad del usuario y registran la actividad en MySQL.
3.  **Transmisión:** El servidor se comunica con el **ESP32** utilizando una conexión de red inalámbrica estable.
4.  **Hardware:** El microcontrolador recibe los datos, los procesa y activa los motores mediante el driver de potencia.



<p align="center">
  <img src="https://i.imgur.com/WzbjxSQ.png" width="550" style="border-radius:10px;"/>
</p>

</details>

---

<details id="servicios-y-roles">
<summary><strong>🔐 6. Servicios & Roles</strong></summary>

La base de este proyecto de **SMX2** es la correcta configuración de los servicios que permiten la conectividad y seguridad de la red.

### 🛠️ Servicios Desplegados:
* **DNS Local:** Configuración para acceder a la web mediante `luxury.sl`, evitando el uso de IPs.
* **DHCP:** Gestión de direcciones IP para que los dispositivos se conecten automáticamente a la red.
* **Servicio de Base de Datos:** Gestión centralizada de la información mediante MySQL.
* **Seguridad:** Configuración de reglas para asegurar que solo usuarios autenticados puedan operar el hardware.

### 👤 Gestión de Roles:
| Rol | Permisos | Función |
| :--- | :--- | :--- |
| **Administrador** | Total | Gestión del servidor, redes y bases de datos. |
| **Docente** | Supervisión | Monitorización de logs y estado del sistema. |
| **Estudiante** | Operación | Control del hardware y visualización de datos. |
| **Visitante** | Lectura | Visualización de documentación e información pública. |

<p align="center">
  <img src="https://i.imgur.com/r03QN0i.png" width="650"/>
</p>

</details>

---

<details id="conclusiones">
<summary><strong>🚀 7. Conclusiones</strong></summary>

**Luxury_SL** es la culminación de un proceso de aprendizaje técnico que integra redes, hardware y software. Este proyecto demuestra que el control de dispositivos remotos es posible mediante una infraestructura bien configurada, segura y eficiente, aplicando los conocimientos clave del ciclo de SMX2.

</details>

---

<details id="bibliografía">
<summary><strong>📚 8. Bibliografía</strong></summary>

- [Documentación Apache HTTP](https://httpd.apache.org/)
- [Referencia ESP32 Arduino](https://docs.arduino.cc/hardware/esp32/)
- [Manual de Blender](https://www.blender.org/)
- [MDN Web Docs](https://developer.mozilla.org/)

<p align="center">
  <img src="https://i.imgur.com/qPQOsBJ.png" width="450"/>
</p>
</details>

---

<div align="center">
  <strong>LUXURY_SL - Proyecto Final SMX2</strong>
</div>
