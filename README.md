# 💎 LUXURY_SL — Documento de Presentación del Proyecto
> **Integración de sistemas, redes, hardware IoT y diseño industrial para el módulo de SMX2.**

<div align="center">
  <img src="https://i.imgur.com/FG6uNYF.png" width="220"/>
  <br>
  <h1><strong>LUXURY_SL</strong></h1>
  <p>Desarrollado por:</p>
  <h3><strong>Katya Robuste</strong> ⬥ <strong>Nazar Kishchuk</strong></h3>
  <p><em>Ciclo: Sistemas Microinformáticos y Redes (SMX2) · Curso 2024–2025</em></p>
</div>

---

## 📑 Índice

<div align="center">

| | Apartado |
| :---: | :--- |
| 🟢 | [**1. Presentación de la Idea**](#-1-presentación-de-la-idea) |
| 🔵 | [**2. Objetivos del Proyecto**](#-2-objetivos-del-proyecto) |
| 🟡 | [**3. Requisitos Técnicos**](#-3-requisitos-técnicos) |
| 🔴 | [**4. Metodología de Trabajo**](#-4-metodología-de-trabajo) |
| 🟣 | [**5. Recursos Disponibles**](#-5-recursos-disponibles) |
| 🟠 | [**6. Desafíos y Soluciones Previstas**](#-6-desafíos-y-soluciones-previstas) |

</div>

---

<details>
<summary><h2>🟢 1. Presentación de la Idea</h2></summary>

**Luxury_SL** es un proyecto técnico integral desarrollado como ejercicio final del ciclo **SMX2** (Sistemas Microinformáticos y Redes). Su propósito es construir un ecosistema funcional que integre software, hardware y redes para controlar un vehículo robótico de 4 ruedas mediante una **interfaz web propia**.

El proyecto combina tres grandes bloques tecnológicos que trabajan de forma coordinada:

- 🚗 **Vehículo robótico físico:** un coche de 4 ruedas motrices montado sobre chasis diseñado en Blender e impreso en 3D, controlado por un microcontrolador **ESP32** con Wi-Fi integrado.
- 🌐 **Infraestructura de red local:** servidor Ubuntu con Apache, MySQL, Pi-hole (DNS + DHCP) y conectividad Wi-Fi para gestionar todos los dispositivos de la red interna.
- 🖥️ **Interfaz web de control:** panel dashboard con estética "Dark Gold" que permite controlar el vehículo en tiempo real, visualizar telemetría y gestionar usuarios por roles.

### Flujo de funcionamiento

```
Usuario (Navegador)
        │
        ▼
Dashboard Web (HTML/CSS/JS)
        │  HTTP / WebSocket
        ▼
Servidor Apache + PHP + MySQL
        │  Wi-Fi (LAN local)
        ▼
Microcontrolador ESP32
        │  PWM
        ▼
Motores DC + Sensores (Vehículo)
```

1. El usuario accede al dashboard web desde su navegador.
2. El servidor Apache + PHP recibe la orden, valida el usuario y la reenvía.
3. El ESP32 recibe la instrucción por Wi-Fi y controla los motores mediante PWM.
4. El vehículo ejecuta el movimiento y los datos de telemetría vuelven al dashboard en tiempo real.

---

### 🌐 Interfaz Web — Dashboard

La web funciona como **centro de control del vehículo**, diseñada con estética **"Dark Gold"** combinando estilo moderno con claridad técnica.

**Paleta de colores:**
<p align="center">
  <img src="https://i.imgur.com/zcfUlYo_d.png" width="600" />
</p>

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

**Funcionalidades clave:**
- Control remoto del vehículo mediante botones en la web.
- Visualización de logs de conexión y telemetría en tiempo real.
- Integración de mapas para seguimiento de posición.

---

### 🤖 Hardware — Vehículo Robótico

El cerebro del coche es el **ESP32**, que maneja la comunicación con el servidor web y controla los motores mediante **PWM** para regular velocidad y dirección.

**Esquema eléctrico:**
<p align="center">
<img src="https://i.imgur.com/rijhOry.png" width="400"/>
</p>

**Componentes principales:**
<p align="center">
<img src="https://i.imgur.com/cGVPCzm.png" width="400"/>
</p>

---

### 🏗️ Arquitectura de Red

**Diagrama de red:**
<p align="center">
<img src="https://i.imgur.com/WzbjxSQ.png" width="550"/>
</p>

**Protocolos utilizados:**
- **HTTP/HTTPS** para comunicación web.
- **TCP/IP** en la red local.
- **MQTT opcional** para telemetría.
- Latencia medida **< 100ms** entre orden y ejecución.

---

### 🖨️ Diseño y Fabricación 3D

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
> Explora el modelo 3D interactivo: [Sketchfab Luxury_SL](https://skfb.ly/pCxW9)

</details>

---

<details>
<summary><h2>🔵 2. Objetivos del Proyecto</h2></summary>

### Objetivo General

Diseñar, construir y desplegar un sistema IoT completo que integre hardware embebido, infraestructura de red y una interfaz web funcional, aplicando los conocimientos adquiridos a lo largo del ciclo SMX2.

### Objetivos Específicos

- Desarrollar un **panel web de control** robusto, seguro y con autenticación por roles.
- Implementar un **microcontrolador ESP32** capaz de gestionar motores, sensores y conectividad Wi-Fi.
- Configurar una **infraestructura de red local** con DNS, DHCP y servidor web propio.
- Aplicar **diseño industrial** mediante modelado 3D (Blender) y fabricación por impresión 3D.
- Integrar servicios de **base de datos** (MySQL) para la gestión de usuarios y registros de actividad.

### Beneficios del proyecto

- Aprendizaje práctico en entornos **IoT y redes internas**.
- Integración de múltiples tecnologías en un **proyecto funcional y profesional**.
- Documentación y control de accesos para usuarios con distintos roles.
- Experiencia en **simulación y prototipado digital**, así como pruebas físicas reales.

### Habilidades que se Desarrollan

| Área | Habilidad Específica |
| :--- | :--- |
| **Redes** | Configuración de DNS, DHCP, Netplan, Wi-Fi y topología LAN |
| **Servidores** | Instalación y gestión de Apache, MySQL y Pi-hole en Ubuntu Server |
| **Programación** | Desarrollo web (HTML, CSS, JS) y firmware para ESP32 (Arduino IDE) |
| **Hardware IoT** | Integración de sensores, motores DC, PWM y comunicación serie |
| **Diseño 3D** | Modelado en Blender, optimización para impresión y ensamblaje físico |
| **Seguridad** | Gestión de roles, sesiones y control de acceso en aplicación web |

</details>

---

<details>
<summary><h2>🟡 3. Requisitos Técnicos</h2></summary>

### 3.1 Tecnologías y Herramientas

| Tecnología | Aplicación en SMX2 | Función específica |
| :---: | :--- | :--- |
| **Blender 3D** | Diseño de Chasis | Modelado y optimización de piezas para impresión 3D |
| **HTML5 / CSS3** | Panel de Control | Estructura y diseño visual de la interfaz de usuario |
| **JavaScript** | Lógica Frontend | Comunicación asíncrona con Fetch API y WebSocket |
| **Arduino ESP32** | Microcontrolador | Gestión de hardware y conectividad de red |
| **Apache** | Servidor Web | Hosting de la plataforma y gestión de tráfico HTTP |
| **MySQL** | Base de Datos | Almacenamiento de perfiles, permisos y registros |
| **Pi-hole** | Servidor DNS/DHCP | Gestión centralizada de DNS local y asignación de IP |
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

---

### 3.2 Componentes de Hardware (BOM)

#### Placa de Control Principal

| Componente | Modelo / Detalles |
| :--- | :--- |
| **Placa de control** | Compatible Arduino UNO |
| **Microcontrolador** | ATmega328P |
| **Conversor USB-UART** | CP2102 |
| **Pines digitales I/O** | 14 (6 con PWM) |
| **Entradas analógicas** | 6 |
| **Velocidad de reloj** | 16 MHz (cristal externo) |
| **Shield de motores** | Driver TB6612FNG / 8833 (doble puente H) |

#### Motores y Actuadores

| Componente | Cantidad | Función |
| :--- | :---: | :--- |
| Motor DC metálico con reductora | 4 | Tracción de las 4 ruedas |
| Servo motor | 1 | Orientación del sensor ultrasónico |
| Ruedas de goma | 4 | Tracción y agarre |

#### Sensores y Módulos

| Módulo | Cantidad | Función |
| :--- | :---: | :--- |
| Sensor de seguimiento de línea | 3 | Detección de trayectorias blanco/negro |
| Sensor ultrasónico HC-SR04 | 1 | Detección de obstáculos y distancia |
| Módulo Bluetooth HM-10 (BLE 4.0) | 1 | Control remoto vía app móvil |
| Receptor IR | 1 | Control con mando infrarrojo |
| Módulo matriz LED 8×16 | 1 | Visualización de expresiones/emoticones |

#### Alimentación y Estructura

| Componente | Detalles |
| :--- | :--- |
| Portabaterías | Para 2× baterías 18650 o 6× pilas AA |
| Tensión de operación | 7.4V (18650) / 9V (AA) |

| Componente | Material |
| :--- | :--- |
| Chasis base (PCB inferior) | PCB multicapa + soporte aluminio |
| Plataforma servo | ABS negro |
| Tornillería | Acero + pilares de cobre |
| Soporte motores | Aleación de aluminio |

---

### 3.3 Especificaciones Técnicas del Hardware

| Parámetro | Valor |
| :--- | :--- |
| Tensión de operación (lógica) | 5V DC |
| Tensión de alimentación (motores) | 6 – 9V DC |
| Corriente máxima por motor | ~250 mA |
| Velocidad máxima aproximada | ~0.8 m/s |
| Alcance sensor ultrasónico | 2 cm – 400 cm |
| Alcance Bluetooth (BLE 4.0) | ~10 m en espacio abierto |
| Dimensiones del chasis | ~28 × 21 × 12 cm |
| Peso aproximado (sin baterías) | ~500 g |

---

### 3.4 Software — Versiones y Entornos

| Software | Versión Recomendada | Uso en el Proyecto |
| :--- | :--- | :--- |
| **Arduino IDE** | v1.8.19 o v2.x | Programación del ESP32 y placas Arduino |
| **Ubuntu Server** | 22.04 LTS (64-bit) | Sistema operativo del servidor |
| **Apache HTTP Server** | 2.4.x | Servidor web para el dashboard |
| **MySQL / MariaDB** | 8.0.x / 10.6.x | Base de datos de usuarios y logs |
| **Pi-hole** | v5.x (última estable) | Servidor DNS y DHCP local |
| **Blender** | 3.6 LTS o 4.x | Modelado 3D del chasis |
| **VS Code** | Última estable | Desarrollo web (HTML, CSS, JS) |
| **PHP** | 8.1.x | Backend del panel web |

---

### 3.5 Librerías Arduino Necesarias

| Librería | Función | Cómo Instalarla |
| :--- | :--- | :--- |
| `Servo.h` | Control del servo motor | Incluida en Arduino IDE |
| `IRremote.h` | Decodificación de señales IR | Library Manager → "IRremote" |
| `HT16K33.h` | Comunicación I2C matriz LED | Library Manager → "Adafruit HT16K33" |
| `SoftwareSerial.h` | Comunicación con módulo BT | Incluida en Arduino IDE |
| `WiFi.h` | Conectividad Wi-Fi del ESP32 | Incluida en paquete ESP32 |
| `WebServer.h` | Servidor HTTP ligero en ESP32 | Incluida en paquete ESP32 |

---

### 3.6 Materiales y Recursos Adicionales

| Material | Cantidad Estimada | Dónde Obtenerlo |
| :--- | :---: | :--- |
| Filamento PLA (impresión 3D) | ~200g | Tiendas de impresión 3D / Amazon |
| Tornillos M3, M2, M1.2 | Kit surtido | Ferretería / Amazon |
| Pilares de cobre M3 | 8–12 unidades | Ferretería / Tiendas electrónica |
| Bridas de plástico (cable ties) | 10–20 unidades | Ferretería / Todo a 100 |
| Cable USB tipo A-B | 1 unidad | Incluido en el kit / Amazon |
| Protoboard + cables dupont | 1 set | Tienda electrónica / AliExpress |
| Cinta aislante negra | 1 rollo | Ferretería / Todo a 100 |
| Baterías 18650 o pilas AA | 2 o 6 unidades | Ferretería / Supermercado |

---

### 3.7 Configuración de Red — Netplan

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
```

Aplicar y verificar:

```bash
sudo netplan apply
ip a
ping luxury.local
```

---

### 3.8 Modos de Operación del Vehículo

| Modo | Descripción |
| :--- | :--- |
| 🚧 **Evitación de obstáculos** | Detecta y esquiva objetos mediante HC-SR04 + servo |
| 🎯 **Seguimiento de objetos** | Sigue un objeto en movimiento detectado por ultrasonidos |
| 📡 **Control IR** | Teledirigido con mando infrarrojo incluido |
| 📱 **Control Bluetooth** | App móvil para iOS y Android (BLE 4.0) |
| ⭕ **Confinamiento en círculo** | El vehículo se mantiene dentro de una zona delimitada |
| 📐 **Control por gravedad** | Movimiento según la inclinación del smartphone |
| 😊 **Display de emoticones** | Muestra expresiones en la matriz LED 8×16 |

---

### 3.9 Roles y Permisos de Usuario

| Rol | Permisos |
| :--- | :--- |
| **Admin** | Control total: usuarios, logs, configuración de red |
| **Operador** | Control del vehículo y visualización de telemetría |
| **Invitado** | Solo visualización del dashboard (modo lectura) |

Los roles se gestionan desde la base de datos **MySQL** conectada al backend **Apache + PHP**.

</details>

---

<details>
<summary><h2>🔴 4. Metodología de Trabajo</h2></summary>

El proyecto se divide en **5 fases de implementación progresiva**. Cada fase tiene tareas concretas que permiten validar el sistema por bloques antes de la integración final.

---

### 🗓️ Fase 1 — Diseño y Planificación `Semana 1–2`

- [ ] Definir arquitectura completa del sistema (red, servidor, hardware, web).
- [ ] Diseñar el chasis del vehículo en Blender 3D.
- [ ] Preparar el diagrama de red y topología LAN.
- [ ] Crear la lista de materiales (BOM) completa.
- [ ] Dividir el trabajo entre los integrantes del equipo.

---

### 🌐 Fase 2 — Infraestructura de Red `Semana 2–3`

- [ ] Instalar Ubuntu Server 22.04 en la máquina virtual o física.
- [ ] Configurar IP estática con Netplan.
- [ ] Instalar y configurar Pi-hole como servidor DNS y DHCP.
- [ ] Instalar Apache y PHP para el servidor web.
- [ ] Instalar y configurar MySQL con las tablas de usuarios y logs.
- [ ] Verificar conectividad completa de la red local.

**Instalación de Pi-hole:**

```bash
# Paso 1 — Actualizar el sistema
sudo apt update && sudo apt upgrade -y

# Paso 2 — Instalar Pi-hole
curl -sSL https://install.pi-hole.net | bash

# Paso 3 — Establecer contraseña del panel web
pihole -a -p
```

Configuración DHCP en el panel web `http://10.10.10.10/admin`:

| Parámetro | Valor |
| :--- | :--- |
| IP de inicio | `10.10.10.100` |
| IP de fin | `10.10.10.200` |
| Gateway | `10.10.10.1` |
| Tiempo de concesión | 24h |

Registros DNS locales a añadir:

| Nombre de dominio | IP |
| :--- | :--- |
| `luxury.local` | `10.10.10.10` |
| `robot.local` | `10.10.10.50` (IP del ESP32) |

---

### 🤖 Fase 3 — Hardware y Firmware `Semana 3–4`

- [ ] Imprimir el chasis en 3D y ensamblar la estructura del vehículo.
- [ ] Montar los 4 motores, servo y sensores sobre el chasis.
- [ ] Conectar la placa Arduino + shield de motores.
- [ ] Programar el ESP32: control de motores, lectura de sensores y servidor HTTP.
- [ ] Probar cada sensor de forma individual (ultrasónico, línea, IR).
- [ ] Validar el control básico del vehículo por consola serie.

**Pasos de ensamblaje:**

| Step | Acción |
| :---: | :--- |
| 🔩 1 | Insertar los 4 motores DC en los soportes de aluminio y fijar al chasis inferior |
| 💡 2 | Instalar la matriz LED 8×16 en la parte frontal con tornillos M3×6 |
| 🔄 3 | Montar la plataforma del servo con el HC-SR04 encima |
| 🔋 4 | Conectar portabaterías y verificar el interruptor de encendido |
| 🖥️ 5 | Apilar la Motor Driver Shield sobre la placa de control y conectar motores |
| 🔌 6 | Conectar todos los sensores y módulos según la tabla de pines |

**Tabla de pines:**

| Módulo | Pin en shield |
| :--- | :--- |
| Sensor ultrasónico HC-SR04 | Trig: D12 / Echo: D13 |
| Servo motor | D10 (PWM) |
| Módulo Bluetooth HM-10 | RX-TX (Serial) |
| Receptor IR | D9 |
| Sensores de línea (×3) | A0, A1, A2 |
| Matriz LED 8×16 | SDA / SCL (I2C) |

**Proyectos de aprendizaje Arduino (17 en total):**

```
Proyecto 01 → LED blink básico
Proyecto 02 → Control PWM de LED
Proyecto 03 → Control de motores DC
Proyecto 04 → Sensor ultrasónico HC-SR04
Proyecto 05 → Servo motor
Proyecto 06 → Receptor infrarrojo
Proyecto 07 → Módulo Bluetooth HM-10
Proyecto 08 → Matriz LED 8x16
Proyecto 09 → Sensores de seguimiento de línea
Proyecto 10 → Evitación de obstáculos
Proyecto 11 → Seguimiento de objetos
Proyecto 12 → Seguimiento de línea
Proyecto 13 → Control IR del coche
Proyecto 14 → Control BT del coche
Proyecto 15 → Control por gravedad (BT)
Proyecto 16 → Confinamiento en círculo (BT)
Proyecto 17 → Robot multi-función completo
```

---

### 🖥️ Fase 4 — Desarrollo Web `Semana 4–5`

- [ ] Diseñar el dashboard con estética Dark Gold (HTML + CSS).
- [ ] Implementar el sistema de login y gestión de roles.
- [ ] Desarrollar la lógica de control (JavaScript + Fetch API / WebSocket).
- [ ] Integrar el backend PHP para comunicar el dashboard con el ESP32.
- [ ] Implementar el sistema de logs en tiempo real.

---

### ✅ Fase 5 — Integración, Pruebas y Documentación `Semana 5–6`

- [ ] Integrar todos los módulos del sistema.
- [ ] Realizar pruebas de latencia (ping, control remoto).
- [ ] Validar la seguridad del acceso web (roles, sesiones).
- [ ] Documentar el proyecto completo (README GitHub + memoria técnica).
- [ ] Preparar la presentación final del proyecto.

**Pruebas realizadas:**
- **Ping y latencia:** Medición de tiempos de respuesta en la red local.
- **Control remoto:** Verificación de respuesta del ESP32 ante órdenes del dashboard.
- **Seguimiento de línea:** Pruebas físicas con el sensor de trayectoria.
- **Evitación de obstáculos:** Validación del HC-SR04 en entornos reales.
- **Carga de la web:** Test de sesiones concurrentes en Apache.

</details>

---

<details>
<summary><h2>🟣 5. Recursos Disponibles</h2></summary>

### 📚 Documentación Oficial

| Recurso | Enlace |
| :--- | :--- |
| Documentación ESP32 | https://docs.espressif.com/projects/esp-idf/en/latest/ |
| Arduino Reference | https://www.arduino.cc/reference/en/ |
| Documentación Pi-hole | https://docs.pi-hole.net/ |
| Apache HTTP Server Docs | https://httpd.apache.org/docs/ |
| MySQL 8.0 Reference | https://dev.mysql.com/doc/refman/8.0/en/ |
| Ubuntu Server Guide | https://ubuntu.com/server/docs |
| Guía oficial del kit 4WD | https://docs.keyestudio.com/projects/KS0470/ |

---

### 🎥 Videotutoriales Recomendados

| Tema | Canal | Enlace |
| :--- | :--- | :--- |
| Montaje del coche 4WD | Keyestudio Channel | [youtube.com/@keyestudio](https://youtube.com/@keyestudio) |
| ESP32 + Arduino IDE setup | Random Nerd Tutorials | [randomnerdtutorials.com](https://randomnerdtutorials.com) |
| Pi-hole instalación completa | Wolfgang's Channel | [youtube.com/@WolfgangsChannel](https://youtube.com/@WolfgangsChannel) |
| Netplan Ubuntu Server | Christian Lempa | [youtube.com/@christianlempa](https://youtube.com/@christianlempa) |
| Blender modelado básico | Blender Guru | [youtube.com/@blenderguru](https://youtube.com/@blenderguru) |
| Dashboard HTML/CSS/JS | Fireship | [youtube.com/@Fireship](https://youtube.com/@Fireship) |
| Apache + PHP + MySQL | Traversy Media | [youtube.com/@TraversyMedia](https://youtube.com/@TraversyMedia) |

---

### 💻 Repositorios y Recursos de Código

| Recurso | Enlace |
| :--- | :--- |
| Repositorio GitHub del proyecto | *(URL interna del equipo)* |
| Getting Started with Arduino | https://getting-started-with-arduino.readthedocs.io |
| Random Nerd Tutorials ESP32 | https://randomnerdtutorials.com/esp32/ |
| Stack Exchange Electronics | https://electronics.stackexchange.com |
| Foro de soporte Arduino (ES) | https://forum.arduino.cc/ |

</details>

---

<details>
<summary><h2>🟠 6. Desafíos y Soluciones Previstas</h2></summary>

Basándonos en la documentación oficial del kit y en la experiencia de la comunidad Arduino, hemos identificado los principales problemas que pueden surgir durante el desarrollo del proyecto, junto con las estrategias para resolverlos.

---

### ⚡ Hardware y Electrónica

<details>
<summary><strong>▶ Módulo Bluetooth bloquea la subida de código</strong></summary>

**Problema:** El HM-10 comparte el puerto serie (RX/TX) con el Arduino IDE. Si está conectado, falla la carga del sketch.

**Solución:** Retirar siempre el módulo Bluetooth **antes** de cargar cualquier sketch. Reconectarlo solo después de la subida exitosa.

</details>

<details>
<summary><strong>▶ Driver CP2102 no reconocido por el sistema operativo</strong></summary>

**Problema:** Algunos sistemas operativos no instalan automáticamente el driver del chip CP2102.

**Solución:** Descargar e instalar el driver CP2102 manualmente desde la página de Silicon Labs. Verificar el puerto COM en el Administrador de Dispositivos.

</details>

<details>
<summary><strong>▶ El servo no vuelve a 90° al inicio</strong></summary>

**Problema:** Si no se inicializa el servo, el sensor ultrasónico puede quedar girado y dar lecturas erróneas desde el arranque.

**Solución:** Añadir en el `setup()` del sketch una instrucción explícita para centrar el servo:

```cpp
void setup() {
  myServo.attach(10);
  myServo.write(90); // Centrar el servo al inicio
}
```

</details>

<details>
<summary><strong>▶ Motores de velocidad asimétrica</strong></summary>

**Problema:** Los 4 motores DC pueden tener pequeñas diferencias de fabricación que provocan que el coche no vaya completamente recto.

**Solución:** Calibrar los valores de PWM de cada motor individualmente en el código hasta conseguir movimiento recto estable.

</details>

<details>
<summary><strong>▶ Película protectora olvidada en el chasis</strong></summary>

**Problema:** El chasis viene con una película plástica protectora que puede generar cortocircuitos si no se retira.

**Solución:** ⚠️ Retirar **siempre** la película plástica de todas las piezas del chasis **antes** de instalar cualquier componente electrónico.

</details>

---

### 📡 Sensores y Lecturas

<details>
<summary><strong>▶ Sensor de línea falla bajo luz solar directa</strong></summary>

**Problema:** El TCRT5000 es sensible a la luz ambiental. En exteriores o con luz solar directa, da lecturas incorrectas.

**Solución:** Probar siempre en entornos con luz controlada. Ajustar el potenciómetro de sensibilidad antes de cada sesión.

</details>

---

### 🌐 Red e Infraestructura

<details>
<summary><strong>▶ Conflicto DHCP entre Pi-hole y el router</strong></summary>

**Problema:** Si el router ya tiene DHCP activo, puede haber conflicto de IPs con Pi-hole, causando fallos de conectividad en toda la red.

**Solución:** Desactivar el DHCP del router **antes** de activar Pi-hole. Documentar el rango de IPs asignado para evitar solapamientos.

</details>

<details>
<summary><strong>▶ Latencia alta o pérdida de paquetes Wi-Fi</strong></summary>

**Problema:** Si el ESP32 y el servidor están en redes distintas o hay interferencias, la latencia puede superar los 200ms.

**Solución:** Asegurar que el ESP32 y el servidor estén en la misma LAN local. Usar banda de 2.4GHz para mayor alcance.

</details>

---

### 🖥️ Desarrollo Web e Integración

<details>
<summary><strong>▶ Integración web + ESP32: CORS y timeout</strong></summary>

**Problema:** El dashboard web puede bloquearse por políticas CORS al intentar comunicarse directamente con el ESP32.

**Solución:** Añadir cabeceras CORS en el servidor HTTP del ESP32 o usar Apache como proxy intermedio.

```cpp
server.sendHeader("Access-Control-Allow-Origin", "*");
```

</details>

<details>
<summary><strong>▶ Pérdida de datos de telemetría en tiempo real</strong></summary>

**Problema:** El uso de polling HTTP puede saturar el ESP32 con muchas peticiones simultáneas y provocar reinicios.

**Solución:** Implementar WebSocket para telemetría en tiempo real. Limitar la frecuencia de actualización del dashboard a 200–500ms.

</details>

---

### 🛡️ Estrategia General de Resolución de Problemas

- **Trabajar por bloques:** validar cada componente de forma individual antes de integrar.
- **Monitor serie:** usar el monitor serie del Arduino IDE para depurar el firmware en tiempo real.
- **Documentar errores:** mantener un registro en GitHub Issues para resolver problemas de forma colaborativa.
- **Entorno controlado:** realizar pruebas sin luz solar directa y con red estable antes de las demos finales.
- **Comunidad:** consultar el foro oficial de Arduino y la documentación del kit ante cualquier duda de hardware.

</details>

---

## 🏆 Conclusiones

El proyecto **Luxury_SL** ha permitido integrar de forma práctica y profesional todos los bloques del ciclo SMX2: redes, hardware embebido, servicios de servidor y diseño físico. La combinación de ESP32 con infraestructura web propia (DNS, DHCP, Apache, MySQL) ha demostrado ser una arquitectura robusta y escalable, muy superior a soluciones punto a punto como Bluetooth o IR aislados.

El modelado 3D del chasis y el ensamblaje físico del vehículo han completado la experiencia, haciendo del proyecto un entregable técnico real y funcional.

---

<div align="center">
  <p>Desarrollado por <strong>Katya Robuste</strong> ⬥ <strong>Nazar Kishchuk</strong></p>
  <p><em>LUXURY_SL — Proyecto Integral SMX2 · 2024–2025</em></p>
</div>
