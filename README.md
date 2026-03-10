<div align="center">
  <img src="https://i.imgur.com/FG6uNYF.png" width="220"/>
  <br><br>
  <h1>💎 LUXURY_SL</h1>
  <p><strong>Integración de sistemas, redes, hardware IoT y diseño industrial para el módulo SMX2</strong></p>
  <br>
  <p>Desarrollado por:</p>
  <h3><strong>Katya Robuste</strong> ⬥ <strong>Nazar Kishchuk</strong></h3>
  <p><em>Ciclo: Sistemas Microinformáticos y Redes (SMX2) · Curso 2025–2026</em></p>
  <br>

  ![Ubuntu](https://img.shields.io/badge/Ubuntu_Server-22.04_LTS-E95420?style=for-the-badge&logo=ubuntu&logoColor=white)
  ![Apache](https://img.shields.io/badge/Apache-2.4.x-D22128?style=for-the-badge&logo=apache&logoColor=white)
  ![MySQL](https://img.shields.io/badge/MySQL-8.0.x-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
  ![PHP](https://img.shields.io/badge/PHP-8.1.x-777BB4?style=for-the-badge&logo=php&logoColor=white)
  ![Arduino](https://img.shields.io/badge/Arduino-ESP32-00979D?style=for-the-badge&logo=arduino&logoColor=white)
  ![Blender](https://img.shields.io/badge/Blender-3.6_LTS-F5792A?style=for-the-badge&logo=blender&logoColor=white)

</div>

---

## 📑 1. Índice

| # | Apartado |
| :---: | :--- |
| 1 | [Índice](#-1-índice) |
| 2 | [Introducción — ¿Qué estamos haciendo?](#-2-introducción--qué-estamos-haciendo) |
| 3 | [Briefing de Ideas](#-3-briefing-de-ideas) |
| 4 | [Arquitectura del Software](#-4-arquitectura-del-software) |
| 5 | [Tecnologías a Utilizar](#-5-tecnologías-a-utilizar) |
| 6 | [Red](#-6-red) |
| 7 | [Diagrama de la Red](#-7-diagrama-de-la-red) |
| 8 | [Mapa Físico](#-8-mapa-físico) |
| 9 | [Mapa Lógico](#-9-mapa-lógico) |
| 10 | [Web](#-10-web) |
| 11 | [Diseño](#-11-diseño) |
| 12 | [Mockup](#-12-mockup) |
| 13 | [Mapa de Navegabilidad](#-13-mapa-de-navegabilidad) |
| 14 | [Base de Datos](#-14-base-de-datos) |
| 15 | [Servicios — Visión General](#-15-servicios--visión-general) |
| 16 | [Guía de Servicio — DNS](#-16-guía-de-servicio--dns) |
| 17 | [Guía de Servicio — DHCP](#-17-guía-de-servicio--dhcp) |
| 18 | [Guía de Servicio — Apache](#-18-guía-de-servicio--apache) |
| 19 | [Guía de Servicio — Firewall](#-19-guía-de-servicio--firewall) |
| 20 | [Guía de Servicio — Copias de Seguridad](#-20-guía-de-servicio--copias-de-seguridad) |
| 21 | [Conclusiones](#-21-conclusiones) |
| 22 | [Bibliografía](#-22-bibliografía) |
| 23 | [Guías de Usuario](#-23-guías-de-usuario) |

---

## 🟢 2. Introducción — ¿Qué estamos haciendo?

**Luxury_SL** es un proyecto técnico integral desarrollado como trabajo final del ciclo **SMX2** (Sistemas Microinformáticos y Redes). Construimos un ecosistema completo que integra software, hardware y redes para controlar un vehículo robótico de 4 ruedas mediante una **interfaz web propia**, sin depender de ningún servicio cloud externo.

Todo el sistema funciona sobre infraestructura propia: un servidor Ubuntu que actúa como centro neurálgico de la red, un microcontrolador ESP32 embebido en el vehículo, y un panel web accesible desde cualquier dispositivo de la red local.

### ¿Por qué este proyecto?

La motivación principal es demostrar que se puede construir una solución IoT profesional y funcional partiendo desde cero: diseñando la red, configurando los servidores, programando el hardware y desarrollando la interfaz. No usamos servicios de terceros: **todo lo que ves funciona porque nosotros lo hemos instalado y configurado**.

### Bloques del sistema

| Bloque | Qué es | Para qué sirve |
| :--- | :--- | :--- |
| 🚗 **Vehículo robótico** | Coche 4WD con ESP32 | Ejecutar órdenes de movimiento y enviar telemetría |
| 🌐 **Infraestructura de red** | Ubuntu Server + Pi-hole + Apache | Gestionar toda la comunicación interna de la LAN |
| 🖥️ **Dashboard web** | Panel HTML/CSS/JS + PHP + MySQL | Controlar el vehículo y visualizar datos en tiempo real |

### Flujo general del sistema

```
Usuario (Navegador)
        │
        ▼
  Dashboard Web
  (HTML / CSS / JS)
        │  HTTP / WebSocket
        ▼
  Servidor Apache + PHP
        │  MySQL (consultas)
        ▼
  Base de datos (usuarios, logs)
        │  Wi-Fi (LAN local)
        ▼
  Microcontrolador ESP32
        │  PWM
        ▼
  Motores DC + Sensores
```

1. El usuario accede al dashboard desde el navegador.
2. Apache recibe la petición y PHP valida la sesión y el rol.
3. La orden se reenvía al ESP32 por la red Wi-Fi local.
4. El ESP32 controla los motores y devuelve telemetría al dashboard.

---

## 💡 3. Briefing de Ideas

Antes de definir el proyecto final, se valoraron varias ideas. A continuación se recoge el proceso de selección.

### Ideas Valoradas

| ID | Idea | Descripción breve | Viabilidad |
| :---: | :--- | :--- | :---: |
| A | **Vehículo IoT con control web** | Coche 4WD controlado desde dashboard web propio con infraestructura de red local | ✅ Alta |
| B | Control de domótica por app móvil | Sistema de sensores en casa controlado desde smartphone | ⚠️ Media |
| C | Sistema de inventario con RFID | Lector RFID + base de datos para gestión de stock | ⚠️ Media |
| D | Servidor de archivos en red local | NAS casero con Raspberry Pi y acceso web | ✅ Alta |

### Idea Seleccionada: **Opción A — LUXURY_SL**

Se eligió la opción A por las siguientes razones:

- **Integración máxima de módulos:** cubre redes, servidores, programación, hardware y diseño en un único entregable.
- **Entregable físico tangible:** el vehículo real impreso en 3D hace el proyecto visualmente impactante y demostrable en la presentación final.
- **Infraestructura 100% propia:** se construye todo desde cero (DNS, DHCP, web), lo que obliga a entender cada capa del sistema.
- **Escalabilidad real:** la arquitectura permite añadir sensores, usuarios o nuevas funcionalidades sin rediseñar el sistema.

### Justificación Técnica

El proyecto combina conocimientos de todos los módulos del ciclo SMX2 en un sistema funcional real:

| Módulo del ciclo | Aplicación directa en LUXURY_SL |
| :--- | :--- |
| Redes Locales | Topología LAN, IP estática, DHCP y DNS con Pi-hole |
| Servicios en Red | Apache, PHP, MySQL en Ubuntu Server |
| Sistemas Operativos en Red | Ubuntu Server 22.04, systemctl, UFW |
| Aplicaciones Web | Dashboard completo con login, roles y WebSocket |
| Hardware / Microcontroladores | ESP32, motores DC, PWM, sensores |
| Diseño y Fabricación | Modelado 3D en Blender, impresión y ensamblaje |

### Público Objetivo

| Perfil | Motivo de interés |
| :--- | :--- |
| Alumnos SMX / ASIX | Referencia de integración real de redes + IoT |
| Profesores y evaluadores | Demostración de conocimientos del ciclo |
| Makers y entusiastas IoT | Proyecto de bajo coste con ESP32 y red local propia |
| Pequeñas empresas | Arquitectura IoT local sin dependencia cloud |

---

## 🏗️ 4. Arquitectura del Software

El software del proyecto se organiza en **tres capas** que se comunican entre sí de forma ordenada.

### Diagrama de capas

```
┌──────────────────────────────────────────────┐
│            CAPA DE PRESENTACIÓN              │
│   HTML5 · CSS3 (Dark Gold) · JavaScript      │
│   Fetch API · WebSocket · Leaflet Maps       │
└────────────────────┬─────────────────────────┘
                     │ HTTP / WebSocket
┌────────────────────▼─────────────────────────┐
│               CAPA DE LÓGICA                 │
│   Apache 2.4 · PHP 8.1 · Sesiones y Roles    │
│   API REST interna · Validación de datos      │
└────────────────────┬─────────────────────────┘
                     │ SQL / Wi-Fi
┌────────────────────▼─────────────────────────┐
│           CAPA DE DATOS / HARDWARE           │
│   MySQL 8.0 (usuarios, logs, telemetría)     │
│   ESP32 (servidor HTTP embebido + PWM)        │
└──────────────────────────────────────────────┘
```

### Descripción de cada capa

**Capa de Presentación (Frontend)**

Es lo que ve el usuario en el navegador. Desarrollada con HTML5, CSS3 y JavaScript puro. No usa frameworks pesados para mantener el control total del código. Se comunica con el backend mediante peticiones Fetch (Ajax) y WebSocket para la telemetría en tiempo real.

**Capa de Lógica (Backend)**

Apache actúa como servidor HTTP y PHP gestiona toda la lógica del servidor: autenticación de usuarios, verificación de roles, generación de respuestas JSON y relay de órdenes hacia el ESP32. Es el puente entre el frontend y los datos o el hardware.

**Capa de Datos y Hardware**

MySQL almacena todos los datos persistentes: cuentas de usuario, permisos, historial de conexiones y logs de telemetría. El ESP32, por su parte, actúa como un servidor HTTP embebido que recibe órdenes de movimiento y responde con datos de sensores.

### Comunicación entre componentes

| Origen | Destino | Protocolo | Descripción |
| :--- | :--- | :---: | :--- |
| Navegador | Apache/PHP | HTTP/WS | Órdenes de control y recepción de telemetría |
| PHP | MySQL | SQL | Consultas de usuarios, logs y permisos |
| PHP | ESP32 | HTTP (GET) | Envío de comandos de movimiento |
| ESP32 | PHP | HTTP (GET) | Envío de datos de sensores |
| Pi-hole | Clientes LAN | DNS/DHCP | Resolución de nombres y asignación de IPs |

---

## 🛠️ 5. Tecnologías a Utilizar

### Software

| Tecnología | Versión | Función en el proyecto |
| :--- | :---: | :--- |
| **Ubuntu Server** | 22.04 LTS | Sistema operativo del servidor principal |
| **Apache HTTP Server** | 2.4.x | Servidor web del dashboard |
| **PHP** | 8.1.x | Backend del panel web |
| **MySQL / MariaDB** | 8.0 / 10.6 | Base de datos de usuarios y logs |
| **Pi-hole** | v5.x | Servidor DNS + DHCP centralizado |
| **Arduino IDE** | v2.x | Programación del ESP32 |
| **Blender** | 3.6 LTS | Modelado 3D del chasis |
| **VS Code** | Última estable | Desarrollo web (HTML, CSS, JS) |
| **Netplan** | Incluido en Ubuntu | Configuración de red estática |

### Hardware

| Componente | Cantidad | Función |
| :--- | :---: | :--- |
| Microcontrolador ESP32 | 1 | Cerebro del vehículo (Wi-Fi + PWM) |
| Placa Arduino UNO (ATmega328P) | 1 | Placa de control principal |
| Shield de motores TB6612FNG | 1 | Driver de los 4 motores DC |
| Motores DC con reductora | 4 | Tracción de las ruedas |
| Servo motor | 1 | Orientación del sensor ultrasónico |
| Sensor ultrasónico HC-SR04 | 1 | Detección de obstáculos |
| Sensores de línea TCRT5000 | 3 | Seguimiento de trayectorias |
| Módulo Bluetooth HM-10 | 1 | Control remoto por app móvil |
| Receptor IR | 1 | Control con mando infrarrojo |
| Matriz LED 8×16 | 1 | Visualización de expresiones |
| Ruedas de goma | 4 | Tracción y agarre |
| Portabaterías 18650 / 6×AA | 1 | Alimentación del vehículo |
| Filamento PLA | ~200 g | Piezas del chasis impresas en 3D |

### Librerías Arduino

| Librería | Función | Instalación |
| :--- | :--- | :--- |
| `Servo.h` | Control del servo | Incluida en Arduino IDE |
| `IRremote.h` | Señales IR | Library Manager |
| `HT16K33.h` | Matriz LED I2C | Library Manager → Adafruit HT16K33 |
| `SoftwareSerial.h` | Comunicación BT | Incluida en Arduino IDE |
| `WiFi.h` | Conectividad Wi-Fi ESP32 | Incluida en paquete ESP32 |
| `WebServer.h` | Servidor HTTP en ESP32 | Incluida en paquete ESP32 |

<p align="center">
  <img src="https://e7.pngegg.com/pngimages/146/983/png-clipart-blender-3d-computer-graphics-logo-filehippo-3d-modeling-blenders-3d-computer-graphics-text-thumbnail.png" height="45"/>
  <img src="https://e7.pngegg.com/pngimages/187/112/png-clipart-responsive-web-design-html-computer-icons-css3-world-wide-web-consortium-css-angle-text.png" height="45"/>
  <img src="https://cdn-icons-png.flaticon.com/512/8379/8379454.png" height="45"/>
  <img src="https://toppng.com/uploads/preview/arduino-logo-11563227354ny21akychx.png" height="45"/>
  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRt1MqnFozRoQe9MQK8vlnJQBx7W1MOVYjtig&s" height="45"/>
  <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/27/PHP-logo.svg/1280px-PHP-logo.svg.png" height="45"/>
  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTsHhT0lhtqSDNWxRp-jWjGiqMvYce069W8uA&s" height="45"/>
  <img src="https://upload.wikimedia.org/wikipedia/commons/4/4f/PhpMyAdmin_logo.svg" height="45"/>
  <img src="https://i.imgur.com/2q6VdIQ.png" height="45"/>
</p>

---

## 🌐 6. Red

La red de LUXURY_SL es una **LAN privada** completamente autogestionada. No depende de ningún servicio externo para funcionar: el propio servidor Ubuntu actúa como núcleo de la red, proporcionando DNS, DHCP y los servicios web.

### Topología

La topología elegida es **estrella**, con el servidor Ubuntu como nodo central. Todos los dispositivos se conectan al mismo switch/router, y Pi-hole gestiona las IPs y los nombres de dominio.

### Rangos y direccionamiento

| Elemento | IP / Rango | Descripción |
| :--- | :--- | :--- |
| Servidor Ubuntu (Pi-hole + Apache) | `10.10.10.10` | Nodo central de la red |
| Gateway / Router | `10.10.10.1` | Salida a internet |
| ESP32 (vehículo) | `10.10.10.50` | IP fija asignada por DHCP (reserva) |
| Clientes DHCP | `10.10.10.100 – .200` | Rango dinámico para equipos y móviles |
| Máscara de red | `255.255.255.0 (/24)` | Subred clase C |

### Dominio local

| Nombre de dominio | IP | Servicio |
| :--- | :--- | :--- |
| `luxury.local` | `10.10.10.10` | Dashboard web principal |
| `robot.local` | `10.10.10.50` | Servidor HTTP del ESP32 |
| `pihole.local` | `10.10.10.10` | Panel de administración Pi-hole |

### Configuración de IP estática — Netplan

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

```bash
sudo netplan apply
ip a
ping luxury.local
```

### Protocolos activos

| Protocolo | Capa OSI | Uso |
| :--- | :---: | :--- |
| TCP/IP | 3–4 | Comunicación base de toda la red |
| HTTP | 7 | Comunicación dashboard ↔ servidor |
| WebSocket | 7 | Telemetría en tiempo real |
| DNS | 7 | Resolución de nombres locales |
| DHCP | 7 | Asignación automática de IPs |
| MQTT (opcional) | 7 | Mensajería IoT ligera |

---

## 📊 7. Diagrama de la Red

<p align="center">
  <img src="https://i.imgur.com/WzbjxSQ.png" width="600"/>
</p>

```
                     ┌─────────────────────────────┐
                     │          INTERNET            │
                     └──────────────┬──────────────┘
                                    │
                            ┌───────▼────────┐
                            │ ROUTER/GATEWAY │
                            │  10.10.10.1    │
                            └───────┬────────┘
                                    │
            ┌───────────────────────▼──────────────────────┐
            │                  SWITCH LAN                   │
            └──────┬────────────────┬──────────────┬───────┘
                   │                │              │
       ┌───────────▼──────┐ ┌───────▼──────┐ ┌────▼─────────┐
       │  SERVIDOR UBUNTU │ │    ESP32      │ │  CLIENTES    │
       │  10.10.10.10     │ │  10.10.10.50  │ │  .100–.200   │
       │  Pi-hole DNS+DHCP│ │  Vehículo IoT │ │  PC / móvil  │
       │  Apache + PHP    │ │  HTTP server  │ │  (DHCP)      │
       │  MySQL           │ └───────────────┘ └─────────────┘
       └──────────────────┘
```

El servidor Ubuntu centraliza todos los servicios. Los clientes obtienen su IP del DHCP de Pi-hole y acceden al dashboard escribiendo `luxury.local` en el navegador. El ESP32 se registra con IP reservada y recibe órdenes del servidor PHP.

---

## 🗺️ 8. Mapa Físico

El mapa físico muestra la distribución real de los equipos en el espacio del aula.

```
AULA DE INFORMÁTICA
═══════════════════════════════════════════════════════

  ┌─────────────────┐          ┌──────────────────────┐
  │  PC SERVIDOR    │──cable───│  SWITCH / ROUTER AULA │
  │  Ubuntu 22.04   │          └──────┬───────┬────────┘
  │  VM VirtualBox  │                 │       │
  │  IP: 10.10.10.10│          ┌──────┘       └──────┐
  └─────────────────┘          │                     │
                          ┌────▼─────┐         ┌─────▼──────┐
                          │ PC ALUMNO│         │  MÓVIL /   │
                          │ Cliente  │         │  TABLET    │
                          │ (DHCP)   │         │  (Wi-Fi)   │
                          └──────────┘         └────────────┘

                                       ~~~~ Wi-Fi ~~~~

                                    ┌─────────────────┐
                                    │   VEHÍCULO 4WD  │
                                    │   ESP32         │
                                    │   10.10.10.50   │
                                    └─────────────────┘

Leyenda:
───  Cable Ethernet (RJ-45)
~~~~  Conexión Wi-Fi (2.4 GHz)
```

| Elemento físico | Ubicación | Conexión |
| :--- | :--- | :--- |
| PC servidor (VM Ubuntu) | Mesa del profesor / rack aula | Ethernet |
| Switch/router del aula | Armario de red | — |
| PC alumno (cliente) | Puesto de trabajo | Ethernet o Wi-Fi |
| Vehículo robótico ESP32 | Suelo / mesa de pruebas | Wi-Fi 2.4 GHz |
| Smartphone (cliente móvil) | Mano del operador | Wi-Fi 2.4 GHz |

---

## 🧠 9. Mapa Lógico

El mapa lógico muestra cómo se organizan los servicios y qué IP tiene cada elemento, independientemente de su ubicación física.

```
SUBRED: 10.10.10.0/24
══════════════════════════════════════════════════════════

  SERVIDOR UBUNTU — 10.10.10.10
  ┌────────────────────────────────────────────────────┐
  │  ┌────────────┐  ┌────────────┐  ┌──────────────┐ │
  │  │  Pi-hole   │  │   Apache   │  │    MySQL     │ │
  │  │  DNS :53   │  │  HTTP :80  │  │   SQL :3306  │ │
  │  │  DHCP :67  │  │  HTTPS:443 │  │  (localhost) │ │
  │  └─────┬──────┘  └─────┬──────┘  └──────────────┘ │
  └────────┼───────────────┼────────────────────────────┘
           │               │
    Asigna IPs        Sirve web
    Resuelve DNS      luxury.local
           │               │
  ┌────────▼───────────────▼──────────────────┐
  │            RED LAN  10.10.10.0/24          │
  └───────────┬───────────────────┬────────────┘
              │                   │
  ┌───────────▼────────┐ ┌────────▼───────────┐
  │   ESP32 VEHÍCULO   │ │   CLIENTES DHCP    │
  │   10.10.10.50      │ │   10.10.10.100–200  │
  │   HTTP server :80  │ │   PC / móvil / VM  │
  └────────────────────┘ └────────────────────┘
```

**Tabla de servicios por puerto:**

| IP | Puerto | Protocolo | Servicio |
| :--- | :---: | :---: | :--- |
| 10.10.10.10 | 53 | TCP/UDP | DNS (Pi-hole) |
| 10.10.10.10 | 67/68 | UDP | DHCP (Pi-hole) |
| 10.10.10.10 | 80 | TCP | HTTP (Apache + dashboard) |
| 10.10.10.10 | 443 | TCP | HTTPS (Apache) |
| 10.10.10.50 | 80 | TCP | HTTP (ESP32 servidor embebido) |
| 127.0.0.1 | 3306 | TCP | MySQL (solo localhost) |

---

## 🌍 10. Web

El dashboard web es el **centro de operaciones** de LUXURY_SL. Desde él, el operador controla el vehículo, consulta la telemetría y gestiona los usuarios, todo desde el navegador sin instalar nada en el cliente.

### Funcionalidades del dashboard

| Función | Descripción | Tecnología |
| :--- | :--- | :--- |
| **Control del vehículo** | Botones de dirección y velocidad | JS + Fetch API → PHP → ESP32 |
| **Telemetría en tiempo real** | Velocidad, distancia, estado batería | WebSocket → ESP32 → Dashboard |
| **Sistema de login** | Autenticación con sesiones seguras | PHP sessions + MySQL |
| **Gestión de roles** | Admin / Operador / Invitado | MySQL + PHP |
| **Logs de actividad** | Registro de conexiones y comandos | MySQL + PHP |
| **Mapa de posición** | Seguimiento aproximado por zonas | Leaflet.js |

### Roles y permisos

| Rol | Control vehículo | Ver telemetría | Gestión usuarios | Config. red |
| :--- | :---: | :---: | :---: | :---: |
| **Admin** | ✅ | ✅ | ✅ | ✅ |
| **Operador** | ✅ | ✅ | ❌ | ❌ |
| **Invitado** | ❌ | ✅ | ❌ | ❌ |

### Modos de operación desde la web

| Modo | Descripción |
| :--- | :--- |
| 🚧 Evitación de obstáculos | Modo autónomo con HC-SR04 + servo |
| 🎯 Seguimiento de objetos | Sigue un objeto detectado por ultrasonidos |
| 📡 Control IR | Teledirigido con mando infrarrojo |
| 📱 Control Bluetooth | App móvil iOS/Android (BLE 4.0) |
| ⭕ Confinamiento en círculo | Se mantiene dentro de una zona delimitada |
| 📐 Control por gravedad | Movimiento según inclinación del smartphone |
| 😊 Display emoticones | Expresiones en la matriz LED 8×16 |

---

## 🎨 11. Diseño

El dashboard sigue una estética **"Dark Gold"**: fondos oscuros profundos con acentos dorados, tipografía limpia y elementos con brillo metálico. El objetivo es que el panel transmita precisión técnica y elegancia.

### Paleta de colores

<p align="center">
  <img src="https://i.imgur.com/zcfUlYo_d.png" width="600" />
</p>

| Nombre | Código HEX | Uso |
| :--- | :---: | :--- |
| Fondo principal | `#0D0D0D` | Fondo de página y tarjetas |
| Fondo secundario | `#1A1A1A` | Paneles y sidebar |
| blanco | `#C9A84C` | Títulos, bordes activos, iconos |
| Blanco | `#E8C97E` | Hover, textos de acento |
| Texto principal | `#F0F0F0` | Texto general |
| Texto secundario | `#888888` | Labels, placeholders |
| Alerta / Error | `#E05A5A` | Mensajes de error |
| Éxito / OK | `#5ABA6D` | Confirmaciones |

### Tipografía

| Uso | Fuente | Peso |
| :--- | :--- | :--- |
| Títulos principales | `Orbitron` (Google Fonts) | 700 |
| Texto general | `Inter` (Google Fonts) | 400 / 500 |
| Código y datos técnicos | `JetBrains Mono` | 400 |

### Principios de diseño

- **Consistencia:** todos los componentes siguen el mismo sistema de espaciado y colores.
- **Claridad técnica:** los datos de telemetría se muestran de forma numérica y visual, sin ruido innecesario.
- **Jerarquía visual:** el panel de control del vehículo ocupa la zona central y más prominente.
- **Responsive:** el dashboard se adapta a tablet y móvil para control desde cualquier dispositivo de la LAN.

---

## 📐 12. Mockup

<table>
<tr>
<td align="center">
<strong>Dashboard principal</strong><br>
<img src="https://i.imgur.com/Xhj3vUs.png" width="280"/><br>
<em>Control del vehículo y telemetría en tiempo real</em>
</td>
<td align="center">
<strong>Pantalla de login</strong><br>
<img src="https://i.imgur.com/xFugChF.png" width="280"/><br>
<em>Autenticación segura con gestión de sesiones</em>
</td>
</tr>
<tr>
<td align="center">
<strong>Mapa de logros / hitos</strong><br>
<img src="https://i.imgur.com/snpG4OU.png" width="280"/><br>
<em>Seguimiento del progreso del proyecto</em>
</td>
<td align="center">
<strong>Planos lógicos de red</strong><br>
<img src="https://i.imgur.com/iM1fOzK.png" width="280"/><br>
<em>Visualización de la topología interna</em>
</td>
</tr>
<tr>
<td align="center">
<strong>Panel de comunicaciones</strong><br>
<img src="https://i.imgur.com/6NnGtWI.png" width="280"/><br>
<em>Logs y estado de la conexión ESP32</em>
</td>
<td align="center">
<strong>Stack tecnológico</strong><br>
<img src="https://i.imgur.com/4gWzAay.png" width="280"/><br>
<em>Resumen visual de tecnologías utilizadas</em>
</td>
</tr>
</table>

---

## 🗺️ 13. Mapa de Navegabilidad

```
                 ┌───────────────────┐
                 │   luxury.local    │  (entrada)
                 └─────────┬─────────┘
                           │
                 ┌─────────▼─────────┐
                 │     LOGIN         │
                 │  /index.php       │
                 └─────┬─────┬───────┘
                       │     │
           ┌───────────┘     └──────────────┐
           │                                │
 ┌─────────▼──────────┐          ┌──────────▼───────┐
 │  DASHBOARD ADMIN   │          │ DASHBOARD OPERADOR│
 │  /admin/           │          │ /operator/        │
 └──┬──────┬──────┬───┘          └──────┬────────────┘
    │      │      │                     │
┌───▼──┐ ┌─▼───┐ ┌▼───────┐    ┌───────▼────────────┐
│Users │ │Logs │ │Config. │    │  CONTROL VEHÍCULO  │
│/users│ │/logs│ │/config │    │  /control/         │
└──────┘ └─────┘ └────────┘    └──────┬─────────────┘
                                      │
                               ┌──────▼────────────┐
                               │   TELEMETRÍA       │
                               │   /telemetry/      │
                               │  [todos los roles] │
                               └───────────────────┘

Acceso Invitado:  Login → /guest/ → Solo ver telemetría
```

### Rutas y permisos

| Ruta | Descripción | Roles con acceso |
| :--- | :--- | :--- |
| `/index.php` | Pantalla de login | Todos |
| `/admin/` | Panel de administración | Admin |
| `/admin/users` | Gestión de usuarios | Admin |
| `/admin/logs` | Historial completo | Admin |
| `/admin/config` | Configuración del sistema | Admin |
| `/operator/` | Panel de operador | Admin, Operador |
| `/control/` | Control del vehículo | Admin, Operador |
| `/telemetry/` | Visualización de datos | Todos |
| `/guest/` | Vista de solo lectura | Invitado |

---

## 🗄️ 14. Base de Datos

La base de datos **MySQL** almacena toda la información persistente del sistema: usuarios, roles, sesiones y registros de telemetría.

---

### 🛢️ Herramientas de base de datos utilizadas

<table>
<tr>
<td align="center" width="50%">
  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTsHhT0lhtqSDNWxRp-jWjGiqMvYce069W8uA&s" width="160"/><br><br>
  <strong>MySQL 8.0</strong><br><br>
  <p align="left">
  MySQL es el sistema gestor de base de datos relacional que usamos como almacén central de todos los datos del proyecto. En LUXURY_SL lo hemos utilizado para guardar las cuentas de usuario con sus contraseñas cifradas en bcrypt, los roles de acceso (Admin / Operador / Invitado), el historial de comandos enviados al vehículo, los registros de telemetría del ESP32 (distancia, velocidad, batería) y las sesiones activas del dashboard. El servidor MySQL solo escucha en <code>localhost</code>, nunca expuesto directamente a la LAN, y el usuario de la aplicación (<code>luxury_app</code>) tiene permisos mínimos para reducir la superficie de ataque.
  </p>
</td>
<td align="center" width="50%">
  <img src="https://upload.wikimedia.org/wikipedia/commons/4/4f/PhpMyAdmin_logo.svg" width="200"/><br><br>
  <strong>phpMyAdmin</strong><br><br>
  <p align="left">
  phpMyAdmin es la interfaz web que hemos utilizado durante el desarrollo para gestionar la base de datos de forma visual sin tener que escribir comandos SQL en la terminal. Nos ha permitido crear las tablas del esquema, insertar los primeros registros de prueba, importar y exportar volcados de la base de datos, y verificar que las relaciones entre tablas eran correctas. En producción phpMyAdmin queda deshabilitado o protegido con contraseña y acceso restringido por IP para no exponer la administración de la BD a todos los clientes de la LAN.
  </p>
</td>
</tr>
</table>

---

### Nombre de la base de datos: `luxury_db`

### Esquema de tablas

```sql
-- Tabla de usuarios
CREATE TABLE users (
    id          INT AUTO_INCREMENT PRIMARY KEY,
    username    VARCHAR(50)  NOT NULL UNIQUE,
    password    VARCHAR(255) NOT NULL,  -- hash bcrypt
    role        ENUM('admin','operator','guest') DEFAULT 'guest',
    email       VARCHAR(100),
    created_at  TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    last_login  TIMESTAMP
);

-- Tabla de logs de actividad
CREATE TABLE activity_logs (
    id          INT AUTO_INCREMENT PRIMARY KEY,
    user_id     INT,
    action      VARCHAR(100) NOT NULL,
    ip_origin   VARCHAR(45),
    timestamp   TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    FOREIGN KEY (user_id) REFERENCES users(id)
);

-- Tabla de telemetría del vehículo
CREATE TABLE telemetry (
    id              INT AUTO_INCREMENT PRIMARY KEY,
    distance_cm     FLOAT,
    battery_v       FLOAT,
    speed_pwm       INT,
    direction       VARCHAR(20),
    timestamp       TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

-- Tabla de sesiones activas
CREATE TABLE sessions (
    id          INT AUTO_INCREMENT PRIMARY KEY,
    user_id     INT,
    token       VARCHAR(255) NOT NULL,
    ip_address  VARCHAR(45),
    expires_at  TIMESTAMP,
    FOREIGN KEY (user_id) REFERENCES users(id)
);
```

### Diagrama Entidad-Relación

```
┌──────────────┐       ┌─────────────────┐
│    USERS     │───┐   │  ACTIVITY_LOGS  │
│──────────────│   └──►│─────────────────│
│ id (PK)      │       │ user_id (FK)    │
│ username     │       │ action          │
│ password     │       │ ip_origin       │
│ role         │       │ timestamp       │
│ email        │       └─────────────────┘
│ created_at   │
│ last_login   │───┐   ┌─────────────────┐
└──────────────┘   └──►│    SESSIONS     │
                       │─────────────────│
┌──────────────┐       │ user_id (FK)    │
│  TELEMETRY   │       │ token           │
│──────────────│       │ ip_address      │
│ id (PK)      │       │ expires_at      │
│ distance_cm  │       └─────────────────┘
│ battery_v    │
│ speed_pwm    │
│ direction    │
│ timestamp    │
└──────────────┘
```

### Seguridad de la base de datos

- Contraseñas almacenadas con hash **bcrypt** (nunca en texto plano).
- MySQL solo escucha en `localhost` (127.0.0.1), no expuesto a la LAN.
- Usuario de aplicación `luxury_app` con permisos mínimos (SELECT, INSERT, UPDATE).
- Usuario `root` solo accesible localmente con contraseña fuerte.

---

## 🔌 15. Servicios — Visión General

Una vista rápida de todos los servicios activos en el servidor, su función y cómo se relacionan entre sí dentro de la red.

### Tabla de servicios

| Servicio | ¿Para qué sirve en este proyecto? | Puerto | IP |
| :--- | :--- | :---: | :--- |
| **DNS (Pi-hole)** | Traduce `luxury.local` → `10.10.10.10` | 53 | 10.10.10.10 |
| **DHCP (Pi-hole)** | Da IP automáticamente a cada dispositivo | 67/68 | 10.10.10.10 |
| **Apache + PHP** | Publica el dashboard y gestiona el control del vehículo | 80/443 | 10.10.10.10 |
| **MySQL** | Guarda usuarios, logs y telemetría | 3306 | 127.0.0.1 |
| **Firewall (UFW)** | Bloquea todo el tráfico no autorizado | — | Servidor |
| **Backup (cron)** | Copia automática de BD y configuración | — | Servidor |

### Flujo de servicios vinculado al diagrama de red

```
  Un cliente nuevo se conecta al Wi-Fi del aula
              │
              ▼
  [DHCP] Pi-hole le asigna 10.10.10.XXX automáticamente
              │
              ▼
  El cliente escribe "luxury.local" en el navegador
              │
              ▼
  [DNS] Pi-hole resuelve → 10.10.10.10
              │
              ▼
  [Apache] Recibe la petición HTTP en el puerto 80
              │
              ▼
  [PHP + MySQL] Verifica sesión y responde con el dashboard
              │
              ▼
  El operador pulsa "adelante" en el dashboard
              │
              ▼
  [PHP] Envía HTTP GET a robot.local (10.10.10.50)
              │
              ▼
  [ESP32] Recibe la orden y activa los motores por PWM
              │
  Todo esto protegido por [UFW Firewall] y respaldado por [Backup diario]
```

---

## 🔵 16. Guía de Servicio — DNS

### 16.1 Teoría

**DNS (Domain Name System)** es el sistema que traduce nombres legibles (`luxury.local`) a direcciones IP numéricas (`10.10.10.10`). Sin DNS, los usuarios tendrían que memorizar IPs para acceder a cualquier recurso de la red.

En este proyecto, el DNS lo gestiona **Pi-hole**, que actúa como servidor DNS local para toda la LAN. Además de resolver nombres internos, puede bloquear dominios publicitarios y de seguimiento en toda la red.

| Concepto | Definición |
| :--- | :--- |
| **Registro A** | Asocia un nombre de dominio a una IPv4 |
| **Registro PTR** | Resolución inversa: IP → nombre |
| **DNS upstream** | Servidor externo al que Pi-hole consulta si no conoce la respuesta |
| **DNS local** | Registros personalizados solo visibles dentro de la LAN |
| **TTL** | Tiempo que una respuesta DNS se guarda en caché |

### 16.2 Función dentro de la red

| Pregunta | Respuesta |
| :--- | :--- |
| **¿Qué función cumple?** | Traducir nombres como `luxury.local` a IPs de la LAN |
| **¿A quién da servicio?** | A todos los dispositivos de la red: PCs, móviles, ESP32 |
| **¿Qué problema resuelve?** | Elimina la necesidad de recordar IPs; permite acceder a servicios por nombre |

### 16.3 ¿En qué equipo se instala y qué requisitos necesita?

| Parámetro | Valor |
| :--- | :--- |
| **Equipo** | PC del aula — Máquina Virtual (VirtualBox) |
| **Sistema Operativo** | Ubuntu Server 22.04 LTS (64-bit) |
| **IP del servidor** | `10.10.10.10` (estática, configurada con Netplan) |
| **CPU mínima** | 1 núcleo (recomendado: 2) |
| **RAM mínima** | 512 MB (recomendado: 1 GB) |
| **Disco mínimo** | 5 GB |
| **Dependencias** | `curl`, acceso a internet para la instalación inicial |
| **Red interfaz 1** | Red interna (comunicación con clientes LAN) |
| **Red interfaz 2** | Adaptador puente (acceso a internet para instalación) |

### 16.4 Instalación y configuración

```bash
# Paso 1 — Actualizar el sistema
sudo apt update && sudo apt upgrade -y

# Paso 2 — Instalar Pi-hole
curl -sSL https://install.pi-hole.net | bash

# Paso 3 — Establecer contraseña del panel web
pihole -a -p
```

Durante el instalador seleccionar: interfaz `enp0s8`, DNS upstream `8.8.8.8` / `1.1.1.1`, instalar panel web: Sí, activar logging: Sí.

**Registros DNS locales** — Panel `http://10.10.10.10/admin` → Local DNS → DNS Records:

| Nombre de dominio | IP destino |
| :--- | :--- |
| `luxury.local` | `10.10.10.10` |
| `robot.local` | `10.10.10.50` |
| `pihole.local` | `10.10.10.10` |

### 16.5 Parámetros básicos de configuración

| Parámetro | Valor |
| :--- | :--- |
| **Puerto** | 53 (TCP/UDP) |
| **Archivo de configuración** | `/etc/pihole/setupVars.conf` |
| **Directorio de listas** | `/etc/pihole/` |
| **Logs DNS** | `/var/log/pihole.log` |
| **DNS upstream primario** | `8.8.8.8` |
| **DNS upstream secundario** | `1.1.1.1` |

### 16.6 ¿Cómo verifico que funciona correctamente?

```bash
# Estado del servicio
systemctl status pihole-FTL
# Esperado: active (running)

# Prueba de resolución desde cliente
nslookup luxury.local 10.10.10.10
# Esperado: Address: 10.10.10.10

ping luxury.local
# Esperado: respuesta desde 10.10.10.10

# Log en tiempo real
pihole -t
tail -f /var/log/pihole.log
```

Panel web: `http://10.10.10.10/admin` → Statistics y Query Log

### 16.7 Incidencias técnicas y soluciones

| Problema | Causa probable | Solución |
| :--- | :--- | :--- |
| No resuelve nombres locales | Puerto 53 bloqueado por UFW | `sudo ufw allow 53` |
| Los clientes no usan Pi-hole | El router tiene DNS prioritario | Configurar DNS `10.10.10.10` manualmente en el cliente |
| Pi-hole no arranca | Conflicto con `systemd-resolved` en puerto 53 | `sudo systemctl disable systemd-resolved` |
| La web de Pi-hole no carga | `lighttpd` parado | `sudo systemctl start lighttpd` |

### 16.8 ¿Qué aspectos de seguridad debo revisar?

| Aspecto | Medida implementada |
| :--- | :--- |
| **Firewall** | Solo puerto 53 (TCP/UDP) abierto desde la LAN |
| **Panel de administración** | Protegido con contraseña (`pihole -a -p`) |
| **Permisos de archivos** | `/etc/pihole/` revisado con `ls -la` |
| **Usuario del servicio** | `pihole` (sin privilegios root) |
| **Acceso remoto** | SSH solo desde la LAN |
| **Actualizaciones** | `pihole -up` + `apt update && apt upgrade` periódicamente |

```bash
pihole -up
apt update && apt upgrade
ls -la /etc/pihole/
```

### 16.9 Bibliografía

- Documentación oficial Pi-hole: https://docs.pi-hole.net/
- RFC 1035 (DNS): https://www.rfc-editor.org/rfc/rfc1035
- Tutorial Pi-hole — Wolfgang's Channel: https://youtube.com/@WolfgangsChannel

---

## 🟣 17. Guía de Servicio — DHCP

### 17.1 Teoría

**DHCP (Dynamic Host Configuration Protocol)** asigna configuración de red automáticamente a los dispositivos cliente cuando se conectan: dirección IP, máscara, gateway y servidor DNS.

**Proceso DORA:**

```
Cliente                         Servidor DHCP
   │── DHCPDISCOVER ───────────►│  (¿Hay algún servidor DHCP?)
   │◄─ DHCPOFFER ───────────────│  (Te ofrezco 10.10.10.105)
   │── DHCPREQUEST ─────────────►│  (Acepto esa IP)
   │◄─ DHCPACK ─────────────────│  (Confirmado, es tuya por 24h)
```

| Concepto | Definición |
| :--- | :--- |
| **Lease time** | Tiempo que una IP está reservada para un cliente |
| **Rango DHCP** | Conjunto de IPs disponibles para asignar |
| **Reserva estática** | IP fija siempre asignada a una MAC concreta |
| **Gateway** | IP del router que los clientes usarán para salir a internet |

### 17.2 Función dentro de la red

| Pregunta | Respuesta |
| :--- | :--- |
| **¿Qué función cumple?** | Asignar IP, máscara, gateway y DNS automáticamente a cada dispositivo |
| **¿A quién da servicio?** | A todos los dispositivos de la LAN: PCs, móviles, ESP32 |
| **¿Qué problema resuelve?** | Elimina la configuración manual de red y previene conflictos de IP |

### 17.3 ¿En qué equipo se instala y qué requisitos necesita?

DHCP está integrado en **Pi-hole**. No requiere instalación adicional; se activa desde el panel web.

| Parámetro | Valor |
| :--- | :--- |
| **Equipo** | Mismo servidor Ubuntu que el DNS (`10.10.10.10`) |
| **Sistema Operativo** | Ubuntu Server 22.04 LTS |
| **IP del servidor DHCP** | `10.10.10.10` |
| **Puertos** | 67 (servidor) / 68 (cliente) — UDP |
| **Dependencias** | Pi-hole instalado y funcionando |

> [!IMPORTANT]
> Antes de activar el DHCP de Pi-hole, **desactivar el DHCP del router del aula** para evitar conflictos.

### 17.4 Instalación y configuración

Activar desde: `http://10.10.10.10/admin` → Settings → DHCP

| Parámetro | Valor |
| :--- | :--- |
| Activar DHCP | ✅ Habilitado |
| IP de inicio del rango | `10.10.10.100` |
| IP de fin del rango | `10.10.10.200` |
| Gateway | `10.10.10.1` |
| Tiempo de concesión | `24h` |
| Dominio local | `luxury.local` |

**Reserva de IP estática para el ESP32:**

Settings → DHCP → Static DHCP leases:

```
MAC del ESP32: XX:XX:XX:XX:XX:XX   (ver con Serial.println(WiFi.macAddress()))
IP reservada:  10.10.10.50
Hostname:      robot
```

### 17.5 Parámetros básicos de configuración

| Parámetro | Valor |
| :--- | :--- |
| **Puertos** | 67/68 (UDP) |
| **Archivo de configuración** | `/etc/dnsmasq.d/02-pihole-dhcp.conf` |
| **Log de concesiones** | `/etc/pihole/dhcp.leases` |
| **Rango asignado** | `10.10.10.100` – `10.10.10.200` |

### 17.6 ¿Cómo verifico que funciona correctamente?

```bash
# Ver concesiones activas desde el servidor
cat /etc/pihole/dhcp.leases

# Desde cliente Linux — renovar IP
sudo dhclient -r && sudo dhclient
ip a
# Verificar que la IP está en el rango 10.10.10.100-200

# Pings de comprobación
ping 10.10.10.1
ping 10.10.10.10
ping luxury.local
```

Panel web: `http://10.10.10.10/admin` → Network (muestra todos los clientes con IP, MAC y hostname)

### 17.7 Incidencias técnicas y soluciones

| Problema | Causa probable | Solución |
| :--- | :--- | :--- |
| El cliente no recibe IP | DHCP del router sigue activo | Desactivar DHCP en el router del aula |
| El ESP32 no recibe su IP reservada | MAC no coincide exactamente | Verificar MAC con `Serial.println(WiFi.macAddress())` |
| Conflicto de IPs en la red | Dos dispositivos con la misma IP | Revisar concesiones y ampliar rango si es necesario |
| IP del rango incorrecto | DNS no apuntado a Pi-hole | Configurar manualmente `10.10.10.10` como DNS |

### 17.8 ¿Qué aspectos de seguridad debo revisar?

| Aspecto | Medida implementada |
| :--- | :--- |
| **Firewall** | Puerto 67/68 UDP abierto solo en la interfaz interna |
| **Reservas estáticas** | ESP32 con IP fija para evitar cambios inesperados |
| **Rango limitado** | Solo 101 IPs disponibles, suficiente para el aula |
| **Permisos de archivos** | `/etc/dnsmasq.d/` con permisos revisados |
| **Usuario del servicio** | `pihole` (sin privilegios root) |
| **Actualizaciones** | Incluidas en la actualización general de Pi-hole |

```bash
sudo ufw status verbose | grep 67
```

### 17.9 Bibliografía

- Documentación Pi-hole DHCP: https://docs.pi-hole.net/guides/misc/dhcp/
- RFC 2131 (DHCP): https://www.rfc-editor.org/rfc/rfc2131
- Tutorial Netplan Ubuntu — Christian Lempa: https://youtube.com/@christianlempa

---

## 🔴 18. Guía de Servicio — Apache

### 18.1 Teoría

**Apache HTTP Server** es el servidor web que publica el dashboard de LUXURY_SL. Recibe peticiones HTTP de los navegadores, ejecuta el código PHP del backend y devuelve las respuestas al cliente.

<table>
<tr>
<td align="center" width="50%">
  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRt1MqnFozRoQe9MQK8vlnJQBx7W1MOVYjtig&s" width="180"/><br><br>
  <strong>Apache HTTP Server 2.4</strong><br><br>
  <p align="left">
  Apache es el servidor web que actúa como punto de entrada de todas las peticiones HTTP dentro de la red local. En LUXURY_SL lo hemos configurado con un <strong>Virtual Host</strong> para el dominio <code>luxury.local</code>, apuntando al directorio <code>/var/www/luxury</code> donde residen los archivos del dashboard. Apache recibe la petición del navegador, pasa el control a PHP para que ejecute la lógica del backend (autenticación, consulta a MySQL, relay al ESP32) y devuelve la respuesta HTML/JSON al cliente. También gestiona los logs de acceso y error del sitio, que usamos para monitorizar el tráfico y depurar incidencias.
  </p>
</td>
<td align="center" width="50%">
  <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/27/PHP-logo.svg/1280px-PHP-logo.svg.png" width="180"/><br><br>
  <strong>PHP 8.1</strong><br><br>
  <p align="left">
  PHP es el lenguaje de scripting del servidor que hemos utilizado para toda la lógica del backend del dashboard. En LUXURY_SL, PHP se encarga de validar las credenciales del login comparando contra la tabla <code>users</code> de MySQL, de verificar el rol del usuario en cada petición antes de ejecutar cualquier acción, de construir las respuestas JSON que consume el JavaScript del frontend, y de hacer las peticiones HTTP al servidor embebido del ESP32 para enviarle los comandos de movimiento. PHP corre integrado en Apache a través del módulo <code>libapache2-mod-php</code>, de forma que cada archivo <code>.php</code> del dashboard se ejecuta en el servidor sin que el navegador del cliente vea nunca el código fuente.
  </p>
</td>
</tr>
</table>

| Concepto | Definición |
| :--- | :--- |
| **Virtual Host** | Permite alojar múltiples sitios en un mismo servidor |
| **DocumentRoot** | Directorio del sistema donde están los archivos del sitio |
| **mod_php** | Módulo de Apache que permite ejecutar código PHP |
| **`.htaccess`** | Archivo de configuración a nivel de directorio |
| **access.log / error.log** | Registros de peticiones y errores del servidor |

### 18.2 Función dentro de la red

| Pregunta | Respuesta |
| :--- | :--- |
| **¿Qué función cumple?** | Servir el dashboard web del proyecto a los navegadores de la LAN |
| **¿A quién da servicio?** | A cualquier dispositivo de la LAN que acceda a `luxury.local` |
| **¿Qué problema resuelve?** | Centraliza toda la aplicación web en el servidor; los clientes no instalan nada |

### 18.3 ¿En qué equipo se instala y qué requisitos necesita?

| Parámetro | Valor |
| :--- | :--- |
| **Equipo** | Servidor Ubuntu (`10.10.10.10`) |
| **Sistema Operativo** | Ubuntu Server 22.04 LTS |
| **IP del servidor** | `10.10.10.10` |
| **CPU mínima** | 1 núcleo |
| **RAM recomendada** | 1 GB |
| **Disco mínimo** | 10 GB |
| **Dependencias** | `php`, `libapache2-mod-php`, `php-mysql`, `mysql-server` |

### 18.4 Instalación y configuración

```bash
# Paso 1 — Instalar Apache, PHP y el módulo MySQL
sudo apt update
sudo apt install apache2 php libapache2-mod-php php-mysql -y

# Paso 2 — Instalar MySQL
sudo apt install mysql-server -y
sudo mysql_secure_installation

# Paso 3 — Crear la base de datos del proyecto
sudo mysql -u root -p
```

```sql
CREATE DATABASE luxury_db CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
CREATE USER 'luxury_app'@'localhost' IDENTIFIED BY 'contraseña_segura';
GRANT SELECT, INSERT, UPDATE ON luxury_db.* TO 'luxury_app'@'localhost';
FLUSH PRIVILEGES;
```

**Configuración del Virtual Host:**

```bash
sudo nano /etc/apache2/sites-available/luxury.conf
```

```apache
<VirtualHost *:80>
    ServerName luxury.local
    DocumentRoot /var/www/luxury

    <Directory /var/www/luxury>
        Options -Indexes
        AllowOverride All
        Require all granted
    </Directory>

    ErrorLog ${APACHE_LOG_DIR}/luxury_error.log
    CustomLog ${APACHE_LOG_DIR}/luxury_access.log combined
</VirtualHost>
```

```bash
sudo mkdir -p /var/www/luxury
sudo chown -R www-data:www-data /var/www/luxury
sudo chmod -R 755 /var/www/luxury

sudo a2ensite luxury.conf
sudo a2enmod rewrite
sudo a2dissite 000-default.conf
sudo systemctl reload apache2
```

### 18.5 Parámetros básicos de configuración

| Parámetro | Valor |
| :--- | :--- |
| **Puerto HTTP** | 80 (TCP) |
| **Puerto HTTPS** | 443 (TCP) |
| **DocumentRoot** | `/var/www/luxury` |
| **Configuración principal** | `/etc/apache2/apache2.conf` |
| **Virtual Hosts** | `/etc/apache2/sites-available/` |
| **Log de acceso** | `/var/log/apache2/luxury_access.log` |
| **Log de errores** | `/var/log/apache2/luxury_error.log` |

### 18.6 ¿Cómo verifico que funciona correctamente?

```bash
# Estado del servicio
systemctl status apache2
# Esperado: active (running)

# Prueba desde navegador (cliente LAN)
# http://luxury.local  →  debe cargar el dashboard

# Prueba de PHP
echo "<?php phpinfo(); ?>" | sudo tee /var/www/luxury/info.php
# Abrir http://luxury.local/info.php → si muestra config PHP → correcto
sudo rm /var/www/luxury/info.php  # borrar después

# Logs en tiempo real
tail -f /var/log/apache2/luxury_access.log
tail -f /var/log/apache2/luxury_error.log
```

### 18.7 Incidencias técnicas y soluciones

| Error | Causa | Solución |
| :--- | :--- | :--- |
| **Error 403 Forbidden** | Permisos incorrectos | `sudo chown -R www-data:www-data /var/www/luxury` |
| **Error 404 Not Found** | Virtual Host no activado o ruta errónea | `sudo a2ensite luxury.conf && sudo systemctl reload apache2` |
| **Error 500** | Error en el código PHP | `tail /var/log/apache2/luxury_error.log` |
| **Puerto 80 ocupado** | Otro servicio usa el puerto | `sudo netstat -tulpn \| grep 80` |
| **PHP no ejecuta** | `mod_php` no activo | `sudo a2enmod php8.1 && sudo systemctl restart apache2` |
| **CORS bloqueado** | Navegador bloquea peticiones al ESP32 | `header("Access-Control-Allow-Origin: *");` en PHP |

### 18.8 ¿Qué aspectos de seguridad debo revisar?

| Aspecto | Medida implementada |
| :--- | :--- |
| **Firewall** | Solo puertos 80 y 443 abiertos |
| **Usuario del servicio** | `www-data` (sin privilegios root) |
| **Listado de directorios** | Deshabilitado (`Options -Indexes`) |
| **Versión de Apache oculta** | `ServerTokens Prod` + `ServerSignature Off` |
| **Permisos de archivos** | `755` en directorios, `644` en archivos |
| **PHP seguro** | `expose_php = Off` en `php.ini` |
| **Actualizaciones** | `sudo apt update && sudo apt upgrade` |

```bash
# Aplicar hardening de Apache
sudo nano /etc/apache2/apache2.conf
# ServerTokens Prod
# ServerSignature Off

sudo systemctl restart apache2
```

### 18.9 Bibliografía

- Documentación Apache: https://httpd.apache.org/docs/
- Documentación PHP: https://www.php.net/docs.php
- Tutorial Apache + PHP + MySQL — Traversy Media: https://youtube.com/@TraversyMedia

---

## 🔒 19. Guía de Servicio — Firewall

### 19.1 Teoría

**UFW (Uncomplicated Firewall)** es la herramienta de gestión del firewall en Ubuntu. Controla qué tráfico puede entrar y salir del servidor, bloqueando todo lo que no esté expresamente permitido.

| Concepto | Definición |
| :--- | :--- |
| **Política por defecto** | Lo que ocurre con el tráfico que no coincide con ninguna regla |
| **Regla INBOUND** | Controla quién puede conectarse al servidor |
| **Regla OUTBOUND** | Controla qué conexiones inicia el servidor |
| **Deny / Allow** | Bloquear o permitir tráfico en un puerto |

### 19.2 Función dentro de la red

| Pregunta | Respuesta |
| :--- | :--- |
| **¿Qué función cumple?** | Proteger el servidor bloqueando accesos no autorizados |
| **¿A quién protege?** | Al servidor Ubuntu y a todos los servicios que corren en él |
| **¿Qué problema resuelve?** | Evita que dispositivos no autorizados accedan a MySQL, SSH u otros servicios internos |

### 19.3 ¿En qué equipo se instala y qué requisitos necesita?

UFW está preinstalado en Ubuntu Server. No requiere instalación adicional.

| Parámetro | Valor |
| :--- | :--- |
| **Equipo** | Servidor Ubuntu (`10.10.10.10`) |
| **Sistema Operativo** | Ubuntu Server 22.04 LTS |
| **Dependencias** | Ninguna (viene con Ubuntu) |

### 19.4 Instalación y configuración

```bash
# Paso 1 — Política por defecto: denegar todo
sudo ufw default deny incoming
sudo ufw default allow outgoing

# Paso 2 — Abrir SSH ANTES de activar (importante)
sudo ufw allow ssh

# Paso 3 — Abrir puertos de DNS
sudo ufw allow 53/tcp
sudo ufw allow 53/udp

# Paso 4 — Abrir puertos de DHCP
sudo ufw allow 67/udp
sudo ufw allow 68/udp

# Paso 5 — Abrir HTTP y HTTPS
sudo ufw allow 80/tcp
sudo ufw allow 443/tcp

# Paso 6 — Activar el firewall
sudo ufw enable

# Paso 7 — Verificar
sudo ufw status verbose
```

### 19.5 Parámetros básicos de configuración — Reglas activas

| Puerto | Protocolo | Servicio | Estado |
| :---: | :---: | :--- | :---: |
| 22 | TCP | SSH (administración) | ✅ Abierto |
| 53 | TCP/UDP | DNS (Pi-hole) | ✅ Abierto |
| 67/68 | UDP | DHCP (Pi-hole) | ✅ Abierto |
| 80 | TCP | HTTP (Apache) | ✅ Abierto |
| 443 | TCP | HTTPS (Apache) | ✅ Abierto |
| 3306 | TCP | MySQL | 🔴 Bloqueado |

**Archivos de configuración:**

| Archivo | Descripción |
| :--- | :--- |
| `/etc/ufw/ufw.conf` | Configuración general de UFW |
| `/etc/ufw/rules.before` | Reglas que se aplican antes de las del usuario |
| `/var/log/ufw.log` | Log de conexiones bloqueadas y permitidas |

### 19.6 ¿Cómo verifico que funciona correctamente?

```bash
# Ver estado y reglas activas
sudo ufw status verbose

# Ver reglas numeradas (para poder eliminarlas)
sudo ufw status numbered

# MySQL NO debe ser accesible desde fuera (debe fallar)
# telnet 10.10.10.10 3306  →  Connection refused ✅

# Puerto 80 SÍ debe ser accesible
curl http://10.10.10.10
# Esperado: HTML del dashboard

# Ver log de intentos bloqueados
sudo ufw logging on
tail -f /var/log/ufw.log
```

### 19.7 Incidencias técnicas y soluciones

| Problema | Causa | Solución |
| :--- | :--- | :--- |
| Pérdida de acceso SSH tras activar UFW | Se olvidó abrir el puerto 22 antes de activar | Acceder físicamente: `sudo ufw allow ssh` |
| Pi-hole no resuelve DNS | Puerto 53 bloqueado | `sudo ufw allow 53` |
| Clientes no reciben IP por DHCP | Puerto 67/68 bloqueado | `sudo ufw allow 67/udp && sudo ufw allow 68/udp` |
| Necesito eliminar una regla | Regla incorrecta | `sudo ufw status numbered` → `sudo ufw delete <número>` |

### 19.8 ¿Qué aspectos de seguridad debo revisar?

| Aspecto | Medida implementada |
| :--- | :--- |
| **Política por defecto** | `deny incoming` — todo bloqueado salvo excepciones explícitas |
| **MySQL protegido** | Puerto 3306 solo en `localhost`, nunca expuesto a la LAN |
| **SSH restringido a la LAN** | `ufw allow from 10.10.10.0/24 to any port 22` |
| **Permisos de archivos** | `/etc/ufw/` solo accesible por root |
| **Usuario del servicio** | UFW se ejecuta como root (es el kernel quien filtra) |
| **Logs activos** | `sudo ufw logging on` para registrar intentos bloqueados |
| **Actualizaciones** | UFW se actualiza con `apt update && apt upgrade` |

```bash
# Restringir SSH solo a la LAN
sudo ufw delete allow ssh
sudo ufw allow from 10.10.10.0/24 to any port 22

# Activar logs
sudo ufw logging on
tail -f /var/log/ufw.log
```

### 19.9 Bibliografía

- Guía UFW Ubuntu: https://ubuntu.com/server/docs/security-firewall
- OWASP Secure Web Server: https://owasp.org/
- Ubuntu Server Guide: https://ubuntu.com/server/docs

---

## 💾 20. Guía de Servicio — Copias de Seguridad

### 20.1 Teoría

Las **copias de seguridad (backups)** garantizan que podemos recuperar el sistema en caso de fallo, borrado accidental o corrupción de datos. En este proyecto, perder la base de datos o la configuración de servicios significaría reconfigurarlo todo desde cero.

| Tipo de backup | Descripción | Frecuencia |
| :--- | :--- | :--- |
| **Base de datos** | Volcado completo de `luxury_db` con `mysqldump` | Diario |
| **Configuración** | Archivos de Apache, Pi-hole y Netplan | Semanal |
| **Dashboard** | Archivos del sitio web en `/var/www/luxury` | En cada cambio |

### 20.2 Función dentro de la red

| Pregunta | Respuesta |
| :--- | :--- |
| **¿Qué función cumple?** | Guardar copias de seguridad de datos y configuración para poder restaurar el sistema |
| **¿A quién protege?** | A los datos del proyecto: usuarios, logs, telemetría y configuración de red |
| **¿Qué problema resuelve?** | Permite recuperar el sistema sin perder configuración ni datos en caso de fallo |

### 20.3 ¿En qué equipo se instala y qué requisitos necesita?

Se implementa mediante scripts `bash` y `cron` en el propio servidor. No es un servicio externo.

| Parámetro | Valor |
| :--- | :--- |
| **Equipo** | Servidor Ubuntu (`10.10.10.10`) |
| **Sistema Operativo** | Ubuntu Server 22.04 LTS |
| **Herramientas** | `mysqldump`, `tar`, `cron` |
| **Dependencias** | MySQL client (incluido con MySQL Server) |
| **Directorio de backups** | `/var/backups/luxury/` |

### 20.4 Instalación y configuración

```bash
sudo nano /usr/local/bin/luxury_backup.sh
```

```bash
#!/bin/bash
# Script de backup — LUXURY_SL

DATE=$(date +%Y%m%d_%H%M%S)
BACKUP_DIR="/var/backups/luxury"
DB_USER="luxury_app"
DB_PASS="contraseña_segura"
DB_NAME="luxury_db"

mkdir -p $BACKUP_DIR

# 1. Backup de la base de datos
mysqldump -u $DB_USER -p$DB_PASS $DB_NAME \
  > $BACKUP_DIR/db_${DATE}.sql

# 2. Backup del dashboard web
tar -czf $BACKUP_DIR/web_${DATE}.tar.gz \
  /var/www/luxury/

# 3. Backup de configuraciones de servicios
tar -czf $BACKUP_DIR/config_${DATE}.tar.gz \
  /etc/apache2/sites-available/ \
  /etc/pihole/ \
  /etc/netplan/

# 4. Eliminar backups de más de 7 días
find $BACKUP_DIR -name "*.sql"    -mtime +7 -delete
find $BACKUP_DIR -name "*.tar.gz" -mtime +7 -delete

echo "[$DATE] Backup completado en $BACKUP_DIR"
```

```bash
# Hacer el script ejecutable
sudo chmod +x /usr/local/bin/luxury_backup.sh

# Probar manualmente
sudo /usr/local/bin/luxury_backup.sh
```

**Automatizar con cron (diario a las 2:00 AM):**

```bash
sudo crontab -e
```

```cron
0 2 * * * /usr/local/bin/luxury_backup.sh >> /var/log/luxury_backup.log 2>&1
```

### 20.5 Parámetros básicos de configuración

| Parámetro | Valor |
| :--- | :--- |
| **Directorio de backups** | `/var/backups/luxury/` |
| **Log del backup** | `/var/log/luxury_backup.log` |
| **Retención** | 7 días (backups más antiguos se eliminan automáticamente) |
| **Frecuencia** | Diaria a las 02:00 AM (cron) |
| **Archivos de configuración respaldados** | `/etc/apache2/`, `/etc/pihole/`, `/etc/netplan/` |

### 20.6 ¿Cómo verifico que funciona correctamente?

```bash
# Verificar que los backups se generan
ls -lh /var/backups/luxury/

# Ver el log del backup
cat /var/log/luxury_backup.log

# Verificar integridad del dump MySQL
mysql -u luxury_app -p luxury_db < /var/backups/luxury/db_YYYYMMDD_HHMMSS.sql
# Si no da error → backup válido

# Ver contenido del tar de la web
tar -tzf /var/backups/luxury/web_YYYYMMDD_HHMMSS.tar.gz | head -20
```

**Restauración de la base de datos:**

```bash
mysql -u root -p luxury_db < /var/backups/luxury/db_20250115_020000.sql
```

### 20.7 Incidencias técnicas y soluciones

| Problema | Causa | Solución |
| :--- | :--- | :--- |
| `mysqldump: Access denied` | Credenciales incorrectas en el script | Verificar usuario y contraseña |
| El cron no ejecuta el script | Sin permisos de ejecución | `sudo chmod +x /usr/local/bin/luxury_backup.sh` |
| El directorio se llena | Política de retención no configurada | Añadir `find -mtime +7 -delete` al script |
| Falla el tar de configuración | Ruta incorrecta de algún archivo | Verificar que las rutas existen antes de ejecutar |

### 20.8 ¿Qué aspectos de seguridad debo revisar?

| Aspecto | Medida implementada |
| :--- | :--- |
| **Permisos del directorio** | `chmod 700 /var/backups/luxury` (solo root accede) |
| **Contraseña en el script** | Mover a `/root/.my.cnf` con `chmod 600` |
| **Retención limitada** | Backups eliminados automáticamente tras 7 días |
| **Permisos de archivos** | El script solo lo ejecuta root |
| **Verificación periódica** | Comprobar restauración mensualmente |
| **Actualizaciones** | El script no requiere actualizaciones externas |

```bash
# Método seguro para la contraseña de MySQL
echo "[client]
user=luxury_app
password=contraseña_segura" > /root/.my.cnf
chmod 600 /root/.my.cnf
# Luego en el script usar mysqldump sin flag -p
```

### 20.9 Bibliografía

- Documentación mysqldump: https://dev.mysql.com/doc/refman/8.0/en/mysqldump.html
- Guía cron Ubuntu: https://ubuntu.com/server/docs
- Ubuntu Server Guide: https://ubuntu.com/server/docs

---

## 🏆 21. Conclusiones

El proyecto **LUXURY_SL** ha permitido integrar de forma práctica y profesional todos los bloques del ciclo SMX2 en un único sistema funcional y tangible.

La combinación de ESP32 con infraestructura web propia (DNS, DHCP, Apache, MySQL) ha demostrado ser una arquitectura robusta y escalable, muy superior a soluciones punto a punto como Bluetooth o IR aislados. La implementación de Pi-hole como servidor DNS + DHCP centralizado garantiza una red interna ordenada, segura y automatizada. Apache + PHP completan el ecosistema publicando el dashboard sin necesidad de instalaciones en los clientes.

El proceso también ha evidenciado que integrar sistemas es más complejo que la suma de sus partes: conseguir que DNS, DHCP, Apache, MySQL, el firewall y el hardware físico funcionen de forma coordinada y segura es donde reside el aprendizaje real del ciclo.

**Puntos de mejora futuros:**

- Implementar HTTPS con certificado autofirmado para cifrar el tráfico del dashboard.
- Añadir MQTT como protocolo de telemetría para reducir carga HTTP en el ESP32.
- Incorporar Grafana para visualizar datos históricos de telemetría.
- Implementar autenticación de dos factores (2FA) en el sistema de login.

El modelado 3D del chasis y el ensamblaje físico del vehículo han completado la experiencia, convirtiendo LUXURY_SL en un entregable técnico real, funcional y visualmente impactante.

---

## 📚 22. Bibliografía

### Documentación Oficial

| Recurso | URL |
| :--- | :--- |
| Documentación ESP32 (Espressif) | https://docs.espressif.com/projects/esp-idf/en/latest/ |
| Arduino Language Reference | https://www.arduino.cc/reference/en/ |
| Documentación Pi-hole | https://docs.pi-hole.net/ |
| Apache HTTP Server Docs | https://httpd.apache.org/docs/ |
| MySQL 8.0 Reference Manual | https://dev.mysql.com/doc/refman/8.0/en/ |
| Ubuntu Server Guide | https://ubuntu.com/server/docs |
| Guía oficial del kit 4WD Keyestudio | https://docs.keyestudio.com/projects/KS0470/ |
| Documentación oficial PHP | https://www.php.net/docs.php |

### Estándares y Normas

| Recurso | URL |
| :--- | :--- |
| RFC 1035 — DNS | https://www.rfc-editor.org/rfc/rfc1035 |
| RFC 2131 — DHCP | https://www.rfc-editor.org/rfc/rfc2131 |
| OWASP Secure Web Server Guide | https://owasp.org/ |

### Videotutoriales

| Tema | Canal | URL |
| :--- | :--- | :--- |
| Montaje del coche 4WD | Keyestudio Channel | https://youtube.com/@keyestudio |
| ESP32 + Arduino IDE | Random Nerd Tutorials | https://randomnerdtutorials.com |
| Pi-hole instalación completa | Wolfgang's Channel | https://youtube.com/@WolfgangsChannel |
| Netplan Ubuntu Server | Christian Lempa | https://youtube.com/@christianlempa |
| Blender modelado básico | Blender Guru | https://youtube.com/@blenderguru |
| Dashboard HTML/CSS/JS | Fireship | https://youtube.com/@Fireship |
| Apache + PHP + MySQL | Traversy Media | https://youtube.com/@TraversyMedia |

### Repositorios y Foros

| Recurso | URL |
| :--- | :--- |
| Getting Started with Arduino | https://getting-started-with-arduino.readthedocs.io |
| Random Nerd Tutorials ESP32 | https://randomnerdtutorials.com/esp32/ |
| Stack Exchange Electronics | https://electronics.stackexchange.com |
| Foro de soporte Arduino | https://forum.arduino.cc/ |

---

## 👤 23. Guías de Usuario

Guías orientadas al **usuario final** del sistema: cómo acceder al dashboard, controlar el vehículo, gestionar usuarios y leer la telemetría.

---

### 23.1 Acceso al Dashboard

**¿Qué puedo hacer?** Acceder al panel de control desde cualquier dispositivo conectado a la red del aula.

**Requisitos:** dispositivo conectado a la LAN y navegador web moderno.

**Pasos:**

1. Conectar el dispositivo a la red del aula (cable o Wi-Fi).
2. Abrir el navegador y escribir: `http://luxury.local`
3. Introducir usuario y contraseña en la pantalla de login.
4. Pulsar **Iniciar sesión**.

> Si `luxury.local` no funciona, usar directamente: `http://10.10.10.10`

**Problemas frecuentes:**

| Problema | Solución |
| :--- | :--- |
| La página no carga | Verificar que estás en la misma red LAN que el servidor |
| "Acceso denegado" | Credenciales incorrectas; contactar al Admin |
| El vehículo no responde | Verificar que la luz LED del ESP32 está encendida |

---

### 23.2 Control del Vehículo

**¿Quién puede controlar el vehículo?** Usuarios con rol **Admin** u **Operador**.

**Panel de control** (zona central del dashboard):

| Elemento | Función |
| :--- | :--- |
| ▲ Adelante | El vehículo avanza |
| ▼ Atrás | El vehículo retrocede |
| ◄ Izquierda | Gira a la izquierda |
| ► Derecha | Gira a la derecha |
| ⬛ Stop | Detiene el vehículo inmediatamente |
| Selector de modo | Cambia entre Manual / Autónomo |
| Slider de velocidad | Regula la velocidad (0% – 100%) |

**Modos disponibles:**

| Modo | Descripción | Activación |
| :--- | :--- | :--- |
| Manual | Control directo con botones | Selector → Manual |
| Evitación de obstáculos | El coche esquiva obstáculos solo | Selector → Auto: Obstáculos |
| Seguimiento de línea | Sigue una línea negra en el suelo | Selector → Auto: Línea |
| Confinamiento | Se mantiene dentro de un área | Selector → Auto: Zona |

**Telemetría visible en el panel lateral:**

- Distancia al obstáculo más cercano (cm).
- Nivel de batería (%).
- Velocidad actual (PWM).
- Último comando enviado.
- Latencia de la red (ms).

---

### 23.3 Gestión de Usuarios (Solo Admin)

**Acceder:** Dashboard → Menú lateral → Usuarios

**Crear un nuevo usuario:**

1. Pulsar **+ Nuevo usuario**.
2. Rellenar: nombre de usuario, contraseña y correo.
3. Seleccionar rol: Admin / Operador / Invitado.
4. Pulsar **Guardar**.

**Editar o eliminar un usuario:**

1. Pulsar ✏️ (editar) o 🗑️ (eliminar) junto al usuario en la lista.
2. Confirmar la acción.

> Los usuarios no pueden eliminarse a sí mismos. El Admin principal no puede ser eliminado.

**Resumen de roles:**

| Rol | Qué puede hacer |
| :--- | :--- |
| **Admin** | Todo: control, usuarios, logs, configuración |
| **Operador** | Controlar el vehículo y ver telemetría |
| **Invitado** | Solo ver el dashboard en modo lectura |

---

### 23.4 Consulta de Logs

**¿Quién puede ver los logs?** Admin (todos) y Operador (solo sus acciones).

**Acceder:** Dashboard → Menú lateral → Registros

**Información disponible:**

| Campo | Descripción |
| :--- | :--- |
| Fecha y hora | Cuándo ocurrió la acción |
| Usuario | Quién la realizó |
| Acción | Qué se hizo (login, move_forward, etc.) |
| IP origen | Desde qué dispositivo |

**Filtros:** por usuario, tipo de acción o rango de fechas.

**Exportar:** botón **Exportar CSV** en la esquina superior derecha.

---

<div align="center">
  <br>
  <p>Desarrollado por <strong>Katya Robuste</strong> ⬥ <strong>Nazar Kishchuk</strong></p>
  <p><em>LUXURY_SL — Proyecto Integral SMX2 · 2024–2025</em></p>
  <br>

  ![GitHub](https://img.shields.io/badge/GitHub-SMX2_Project-181717?style=for-the-badge&logo=github&logoColor=white)
  ![Status](https://img.shields.io/badge/Estado-En_Desarrollo-yellow?style=for-the-badge)
  ![License](https://img.shields.io/badge/Licencia-MIT-green?style=for-the-badge)

</div>
