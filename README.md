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

| 🟢 [**1. INTRODUCCIÓN**](#-1-introducción) | 🔵 [**2. TECNOLOGÍAS Y HERRAMIENTAS**](#-2-tecnologías-y-herramientas) |
| :--- | :--- |
| Visión, objetivos y despliegue SMX2. | Software, Firmware y Herramientas. |
| 🟡 [**3. WEB**](#-3-web) | 🔴 [**4. ARDUINO & 3D**](#-4-arduino--modelo-3d) |
| UX Premium, APIs y Telemetría. | ESP32, Motores y Modelado Industrial. |
| 🟣 [**5. ARQUITECTURA & RED**](#-5-arquitectura--red) | 🟠 [**6. SERVICIOS & ROLES**](#-6-servicios--roles) |
| Latencia, Protocolos y Conectividad. | DNS, DHCP, Netplan y Seguridad. |
| 🟤 [**7. PRUEBAS REALIZADAS**](#-7-pruebas-realizadas) | ⚫ [**8. CONCLUSIONES**](#-8-conclusiones) |
| Ping, Latencia y Control Remoto. | Integración final y aprendizajes. |

</div>

---

<details>
<summary><h2>✨ 1. Introducción</h2></summary>

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

</details>

---

<details>
<summary><h2>🛠️ 2. Tecnologías y Herramientas</h2></summary>

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

</details>

---

<details>
<summary><h2>🌐 3. Web</h2></summary>

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

</details>

---

<details>
<summary><h2>🤖 4. Arduino & Modelo 3D</h2></summary>

### Electrónica y Conectividad

El cerebro del coche es el **ESP32**, que maneja comunicación con el servidor web y controla motores mediante **PWM** para regular velocidad y dirección.

**Esquema eléctrico:**

<p align="center">
<img src="https://i.imgur.com/rijhOry.png" width="400"/>
</p>

---

### Lista de Materiales (BOM)

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

<p align="center">
<img src="https://i.imgur.com/cGVPCzm.png" width="400"/>
</p>

---

### Especificaciones Técnicas del Hardware

| Parámetro | Valor |
| :--- | :--- |
| Tensión de operación (lógica) | 5V DC |
| Tensión de alimentación (motores) | 6 – 9V DC |
| Corriente máxima por motor | ~250 mA |
| Velocidad máxima aproximada | ~0.8 m/s |
| Alcance sensor ultrasónico | 2 cm – 400 cm |
| Dimensiones del chasis | ~28 × 21 × 12 cm |
| Peso aproximado (sin baterías) | ~500 g |

---

### Proceso de Ensamblaje

El montaje se divide en **6 pasos** diferenciados, sin necesidad de soldadura.

#### 🔩 Step 1 — Montaje de motores en PCB inferior

1. Insertar los **4 motores DC** en los soportes de aluminio.
2. Fijar cada soporte a la base PCB con tornillos M3 y tuercas.
3. Conectar las **ruedas** a cada eje de motor.
4. Instalar el **portabaterías** en el espacio designado del chasis inferior.

> ⚠️ Verificar la orientación de cada motor: los del lado izquierdo giran en sentido contrario a los del derecho para asegurar la tracción correcta.

#### 💡 Step 2 — Instalación de la matriz LED 8×16

1. Colocar el módulo **LED 8×16** en la parte frontal del chasis.
2. Fijarlo con 4 tornillos M3×6.
3. Pasar el cable de datos por el interior del chasis hacia la placa superior.

#### 🔄 Step 3 — Plataforma del servo (soporte del ultrasonidos)

1. Montar la **plataforma giratoria** con 4 tornillos M1.2×4.
2. Insertar el **servo motor** y fijarlo con tornillos M2×4.
3. Instalar el **HC-SR04** en la plataforma giratoria.
4. Organizar el cableado con bridas de plástico para evitar enredos.

#### 🔋 Step 4 — Cierre de la estructura y portapilas

1. Conectar el portabaterías al circuito de alimentación.
2. Asegurarse de que el **interruptor de encendido** quede accesible.
3. Verificar que todos los cables del nivel inferior queden ordenados.

#### 🖥️ Step 5 — Montaje de la placa de control (PCB superior)

1. Apilar la **Motor Driver Shield** sobre la placa de control.
2. Fijar el conjunto al chasis superior con pilares de cobre y tornillos M3.
3. Conectar los **4 motores** a las salidas del driver (M1, M2, M3, M4).
4. Conectar la **alimentación** del portabaterías a la shield.

#### 🔌 Step 6 — Conexión de sensores y módulos

| Módulo | Puerto / Pin en shield |
| :--- | :--- |
| Sensor ultrasónico HC-SR04 | Trig: D12 / Echo: D13 |
| Servo motor | D10 (PWM) |
| Módulo Bluetooth HM-10 | RX-TX (Serial) |
| Receptor IR | D9 |
| Sensores de línea (×3) | A0, A1, A2 |
| Matriz LED 8×16 | SDA / SCL (I2C) |

> ⚠️ **Importante:** Cargar el sketch de Arduino **antes** de conectar el módulo Bluetooth HM-10, ya que comparte el puerto serie y bloquea la comunicación con el IDE.

---

### Modos de Operación del Vehículo

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

### Programación — Arduino IDE

- **Entorno:** Arduino IDE v1.8.x o superior
- **Lenguaje:** C/C++ estándar para AVR
- **Librerías necesarias:**
  - `Servo.h` — control del servo
  - `IRremote.h` — receptor infrarrojo
  - `HT16K33.h` — matriz LED I2C
  - `SoftwareSerial.h` — comunicación BT

**Proyectos de aprendizaje progresivos incluidos (17 en total):**

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

</details>

---

<details>
<summary><h2>🏗️ 5. Arquitectura & Red</h2></summary>

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

</details>

---

<details>
<summary><h2>🔐 6. Servicios & Roles</h2></summary>

### DNS Local y DHCP

**DNS**
- Traduce nombres de dominio a IP.
- Facilita acceso a servicios web internos.
- Implementación: Pi-hole en Ubuntu Server.

**DHCP**
- Asigna IP automáticamente a clientes.
- Reduce errores y simplifica integración de nuevos dispositivos.

---

### Instalación y Configuración de Pi-hole (DNS + DHCP)

Pi-hole actúa como servidor DNS y DHCP centralizado de la red interna del proyecto.

#### Requisitos previos

- Ubuntu Server 64-bit instalado y actualizado.
- IP estática configurada en el servidor (ver Netplan más abajo).
- Acceso a internet durante la instalación.

#### Paso 1 — Actualizar el sistema

```bash
sudo apt update && sudo apt upgrade -y
```

#### Paso 2 — Instalar Pi-hole

```bash
curl -sSL https://install.pi-hole.net | bash
```

Durante el asistente de instalación:

| Opción | Valor recomendado |
| :--- | :--- |
| Interface de red | `enp0s8` (la interna, IP estática) |
| Upstream DNS | `8.8.8.8` (Google) o `1.1.1.1` (Cloudflare) |
| Instalar admin web | ✅ Sí |
| Instalar lighttpd | ✅ Sí |
| Habilitar query logging | ✅ Sí |

#### Paso 3 — Establecer contraseña del panel web

```bash
pihole -a -p
```

#### Paso 4 — Activar el servidor DHCP en Pi-hole

1. Acceder al panel web: `http://10.10.10.10/admin`
2. Ir a **Settings → DHCP**
3. Activar **DHCP server enabled**
4. Configurar rango de IPs:

| Parámetro | Valor |
| :--- | :--- |
| IP de inicio | `10.10.10.100` |
| IP de fin | `10.10.10.200` |
| Gateway | `10.10.10.1` |
| Tiempo de concesión | 24h |

> ⚠️ Si el router ya tiene DHCP activo, desactivarlo primero para evitar conflictos.

#### Paso 5 — Añadir registros DNS locales

En **Settings → DNS → Local DNS Records**, añadir:

| Nombre de dominio | IP |
| :--- | :--- |
| `luxury.local` | `10.10.10.10` |
| `robot.local` | `10.10.10.50` (IP del ESP32) |

---

### Netplan y configuración de red

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

Aplicar cambios:

```bash
sudo netplan apply
```

Verificar:

```bash
ip a
ping luxury.local
```

---

### Roles y Permisos de Usuario

| Rol | Permisos |
| :--- | :--- |
| **Admin** | Control total: usuarios, logs, configuración de red |
| **Operador** | Control del vehículo y visualización de telemetría |
| **Invitado** | Solo visualización del dashboard (modo lectura) |

Los roles se gestionan desde la base de datos **MySQL** conectada al backend **Apache + PHP**.

</details>

---

<details>
<summary><h2>🧪 7. Pruebas Realizadas</h2></summary>

- **Ping y latencia:** Medición de tiempos de respuesta en la red local.
- **Control remoto:** Verificación de respuesta del ESP32 ante órdenes del dashboard.
- **Seguimiento de línea:** Pruebas físicas con el sensor de trayectoria.
- **Evitación de obstáculos:** Validación del HC-SR04 en entornos reales.
- **Carga de la web:** Test de sesiones concurrentes en Apache.

</details>

---

<details>
<summary><h2>🏆 8. Conclusiones</h2></summary>

El proyecto **Luxury_SL** ha permitido integrar de forma práctica y profesional todos los bloques del ciclo SMX2: redes, hardware embebido, servicios de servidor y diseño físico. La combinación de ESP32 con infraestructura web propia (DNS, DHCP, Apache, MySQL) ha demostrado ser una arquitectura robusta y escalable, muy superior a soluciones punto a punto como Bluetooth o IR aislados.

El modelado 3D del chasis y el ensamblaje físico del vehículo han completado la experiencia, haciendo del proyecto un entregable técnico real y funcional.

</details>

---

<div align="center">
  <p>Desarrollado por <strong>Katya Robuste</strong> ⬥ <strong>Nazar Kishchuk</strong></p>
  <p><em>LUXURY_SL — Proyecto Integral SMX2</em></p>
</div>
