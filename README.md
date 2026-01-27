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

| 🟢 [**1. INTRODUCCIÓN**](#introducción) | 🔵 [**2. TECNOLOGÍAS Y HERRAMIENTAS**](#tecnologías-y-herramientas) |
| :--- | :--- |
| Visión, objetivos y despliegue SMX2. | Software, Firmware y Herramientas. |
| 🟡 [**3. WEB**](#web) | 🔴 [**4. ARDUINO & 3D**](#arduino--modelo-3d) |
| UX Premium, APIs y Telemetría. | ESP32, Motores y Modelado Industrial. |
| 🟣 [**5. ARQUITECTURA & RED**](#arquitectura--red) | 🟠 [**6. SERVICIOS & ROLES**](#servicios--roles) |
| Latencia, Protocolos y Conectividad. | DNS, DHCP, Netplan y Seguridad. |
| 🟤 [**7. PRUEBAS REALIZADAS**](#pruebas-realizadas) | ⚫ [**8. CONCLUSIONES**](#conclusiones) |
| Ping, Latencia y Control Remoto. | Integración final y aprendizajes. |

</div>

---

## ✨ 1. Introducción

**Luxury_SL** es un proyecto técnico integral desarrollado como ejercicio final del ciclo **SMX2** (Sistemas Microinformáticos y Redes).  

Su objetivo principal es crear un **ecosistema que integre software, hardware y redes** para controlar un vehículo robótico mediante una interfaz web, aplicando de forma práctica todos los conocimientos adquiridos en el módulo.  

### Objetivos

- Desarrollar un **panel web de control** robusto y seguro.
- Implementar un **microcontrolador ESP32** que gestione motores y sensores.
- Configurar la **infraestructura de red** para garantizar baja latencia y conectividad estable.
- Integrar **servicios como DNS y DHCP** para la gestión centralizada de la red interna.
- Aplicar **diseño industrial y fabricación 3D** para construir el chasis del vehículo.

### Beneficios del proyecto

- Aprendizaje práctico en entornos **IoT y redes internas**.
- Integración de múltiples tecnologías en un **proyecto funcional y profesional**.
- Documentación y control de accesos para usuarios con distintos roles.
- Experiencia en **simulación y prototipado digital**, así como pruebas físicas.

---

## 🛠️ 2. Tecnologías y Herramientas

| Tecnología | Aplicación en SMX2 | Función específica |
| :---: | :--- | :--- |
| **Blender 3D** | Diseño de Chasis | Modelado y optimización de piezas para impresión 3D |
| **HTML5 / CSS3** | Panel de Control | Estructura y diseño visual de la interfaz de usuario |
| **JavaScript** | Lógica Frontend | Comunicación asíncrona con Fetch API y WebSocket |
| **Arduino ESP32** | Microcontrolador | Gestión de hardware y conectividad de red |
| **Apache** | Servidor Web | Hosting de la plataforma y gestión de tráfico HTTP |
| **MySQL** | Base de Datos | Almacenamiento de perfiles, permisos y registros |
| **Pi-hole** | Servidor DNS/DHCP | Gestión centralizada de DNS local y asignación automática de IP |
| **Ubuntu Server 64-bit** | Sistema Operativo | Entorno de servidor para servicios de red y base de datos |

<p align="center">
  <img src="https://e7.pngegg.com/pngimages/146/983/png-clipart-blender-3d-computer-graphics-logo-filehippo-3d-modeling-blenders-3d-computer-graphics-text-thumbnail.png" height="45"/>
  <img src="https://e7.pngegg.com/pngimages/187/112/png-clipart-responsive-web-design-html-computer-icons-css3-world-wide-web-consortium-css-angle-text.png" height="45"/>
  <img src="https://pngdownload.io/wp-content/uploads/2023/12/CSS-Logo-PNG-Symbol-for-Web-Development-Transparent-jpg.webp" height="45"/>
  <img src="https://cdn-icons-png.flaticon.com/512/8379/8379454.png" height="45"/>
  <img src="https://toppng.com/uploads/preview/arduino-logo-11563227354ny21akychx.png" height="45"/>
  <img src="https://img.favpng.com/25/15/12/logo-apache-http-server-apache-software-foundation-computer-servers-web-server-png-favpng-ebJ1wHvFsydhrpp6V0xFN5NBQ.jpg" height="45"/>
  <img src="https://e7.pngegg.com/pngimages/617/252/png-clipart-mysql-workbench-computer-icons-logo-database-server-blue-text.png" height="45"/>
  <img src="https://i.imgur.com/2q6VdIQ.png" height="45"/>
</p>

### Descripción de herramientas principales

- **Blender 3D:** Se utilizó para modelar el chasis, optimizando el peso y la estructura para impresión 3D. Cada componente fue probado virtualmente antes de imprimir.  
- **HTML, CSS y JavaScript:** Construcción del dashboard web, gestión de órdenes al ESP32 y visualización de telemetría.  
- **ESP32:** Microcontrolador con Wi-Fi integrado, utilizado para recibir órdenes del servidor y controlar motores mediante PWM.  
- **Apache + MySQL:** Backend de la aplicación web, gestión de usuarios, roles y registros de actividad.  
- **Pi-hole:** Servidor interno que proporciona DNS local, además de DHCP para automatizar la asignación de direcciones IP a todos los clientes de la red.  

---

## 🌐 3. Web

La web de **Luxury_SL** funciona como **centro de control del vehículo**. Se diseñó con estética **"Dark Gold"**, combinando estilo moderno con claridad técnica.  

**Paleta de colores:**
<p align="center">
  <img src="https://i.imgur.com/zcfUlYo_d.png" width="600" />
</p>

### Dashboard Principal

- Visualización en tiempo real de la posición y velocidad del vehículo.  
- Panel de logs de órdenes ejecutadas y usuarios conectados.  

<table>
<tr>
<td align="center">
<strong>Dashboard</strong><br>
<img src="https://i.imgur.com/Xhj3vUs.png" width="220"/><br>
<span style="color:gray;">Estado del vehículo en tiempo real</span>
</td>
<td align="center">
<strong>Acceso de Usuario</strong><br>
<img src="https://i.imgur.com/xFugChF.png" width="220"/><br>
<span style="color:gray;">Gestión de sesiones seguras</span>
</td>
<td align="center">
<strong>Mapa de Logros</strong><br>
<img src="https://i.imgur.com/snpG4OU.png" width="220"/><br>
<span style="color:gray;">Seguimiento de tareas y hitos del proyecto</span>
</td>
</tr>
<tr>
<td align="center">
<strong>Planos Lógicos</strong><br>
<img src="https://i.imgur.com/iM1fOzK.png" width="220"/>
</td>
<td align="center">
<strong>Comunicación</strong><br>
<img src="https://i.imgur.com/6NnGtWI.png" width="220"/>
</td>
<td align="center">
<strong>Tecnologías</strong><br>
<img src="https://i.imgur.com/4gWzAay.png" width="220"/>
</td>
</tr>
</table>

**Funcionalidades Clave:**

- Control remoto del vehículo mediante botones en la web.  
- Visualización de logs de conexión y telemetría.  
- Integración de mapas para seguimiento de posición.  

---

## 🤖 4. Arduino & Modelo 3D

### Electrónica y Conectividad

El cerebro del coche es el **ESP32**, que maneja comunicación con el servidor web y controla motores mediante **PWM** para regular velocidad y dirección.  

**Esquema eléctrico:**

<p align="center">
<img src="https://i.imgur.com/rijhOry.png" width="400"/>
</p>

**Componentes principales:**

<p align="center">
<img src="https://i.imgur.com/cGVPCzm.png" width="400"/>
</p>

### Diseño y Fabricación 3D

- **Prototipo digital:** Optimización de piezas y verificación de encajes.  
- **Modelo físico:** Impresión 3D y ensamblaje final.  

<table>
<tr>
<td align="center">
<strong>Prototipo digital</strong><br>
<img src="https://i.imgur.com/IZttiWP.png" width="245"/>
</td>
<td align="center">
<strong>Modelo físico</strong><br>
<img src="https://i.imgur.com/bTWoQN3.png" width="245"/>
</td>
</tr>
</table>

> [!IMPORTANT]  
> Explora el modelo 3D: [Sketchfab Luxury_SL](https://skfb.ly/pCxW9)  

---

## 🏗️ 5. Arquitectura & Red

### Flujo de datos

1. Usuario envía orden desde web.  
2. Apache + PHP procesan solicitud y validan usuario.  
3. Servidor transmite datos al ESP32 por Wi-Fi.  
4. ESP32 ejecuta órdenes en motores y sensores.  

**Diagrama de red:**

<p align="center">
<img src="https://i.imgur.com/WzbjxSQ.png" width="550"/>
</p>

### Protocolos y Latencia

- **HTTP/HTTPS** para comunicación web.  
- **TCP/IP** en la red local.  
- **MQTT opcional** para telemetría.  
- Latencia medida < 100ms entre orden y ejecución.  

---

## 🔐 6. Servicios & Roles

### DNS Local y DHCP

**DNS**  
- Traduce nombres de dominio a IP.  
- Facilita acceso a servicios web internos.  
- Implementación: Pi-hole en Ubuntu Server.

**DHCP**  
- Asigna IP automáticamente a clientes.  
- Reduce errores y simplifica integración de nuevos dispositivos.  

**Netplan y configuración de red**

```yaml
network:
  version: 2
  renderer: networkd
  ethernets:
    enp0s8:
      dhcp4: no
      addresses: [10.10.10.10/24]
      gateway4: 10.10.10.1
      nameservers:
          addresses: [10.10.10.10, 8.8.8.8]
    enp0s3:
      dhcp4: yes

