<div align="center">

# LUXURY_SL

<img src="https://i.imgur.com/FG6uNYF.png" alt="Logo Luxury_SL" width="400" height="400">

**En desarrollo: Blender 3D + CSS + HTML + JavaScript**  

**Equipo:** Katya Robuste • Pau Ferrer • Nazar Kishchuk

</div>

---

<details>
<summary><strong>ÍNDICE</strong></summary>

#### **INTRODUCCIÓN**

#### **ARQUITECTURA DE SOFTWARE**

#### **TECNOLOGÍAS A UTILIZAR**

#### **RED**
• **Diagrama de la Red**  
• **Mapa Físico**  
• **Mapa Lógico**  

#### **WEB**
• **Diseño Web**  
• **Mapa de Navegabilidad**  
• **Usuarios y Comentarios**  

#### **ARDUINO**
• **Programación**  
• **Electrónica**  

#### **SERVICIOS**
• **DNS**  
• **DHCP**  
• **Apache**  
• **Firewall**  
• **Copias de Seguridad**  

#### **CONCLUSIONES**

#### **BIBLIOGRAFÍA**

</details>

---

<details>
<summary><strong>BRIEFING LUXURY_SL</strong></summary>

**Luxury_SL** es un proyecto que combina un **diseño 3D de un coche** con **Arduino**, permitiendo al usuario **construir, visualizar e interactuar** con su propio coche.  

Los usuarios podrán **crear cuenta**, **consultar tutoriales** para montar el coche, **dejar comentarios** al soporte técnico y **controlar el coche vía Bluetooth**, incluyendo movimientos (adelante, atrás, izquierda, derecha) y luces.  

Las **entidades clave** del sistema incluyen **Usuario, Comentarios, Arduino, Diseño 3D, Coche y Herramientas**.  

El proyecto busca ofrecer una **web funcional**, con **visualización 3D del coche** y **control físico** del mismo, integrando la experiencia digital con la interacción física del hardware.  

</details>

---

<details>
<summary><strong>WEB</strong></summary>

### Diseño

La página web presenta un diseño **oscuro, moderno y minimalista**, inspirado en el estilo *glassmorphism*, con una experiencia visual limpia y elegante centrada en la marca **LUXURY_SL**.

#### Paleta de colores
- Fondo principal: `#000`
- Texto principal: `#fff`
- Detalles y acentos: `#aaa`
- Efectos translúcidos: `rgba(255,255,255,0.05–0.12)`

#### Tipografía
- `'Segoe UI', Tahoma, Geneva, Verdana, sans-serif`
- Estilo moderno, profesional y legible.

#### Estilo visual
- Fondo animado con video
- Efectos de desenfoque y transparencia (*glassmorphism*)
- Sombras suaves y transiciones fluidas
- Tarjetas y botones con animaciones al pasar el cursor
- Diseño adaptable a diferentes tamaños de pantalla

---

### Mapa de Navegabilidad

**Menú principal:**
- Herramientas  
- 3D Blender  
- Arduino  
- Página Oficial *(requiere iniciar sesión)*  

**Página Oficial:**
- Herramientas Oficial  
- 3D Blender Oficial  
- Arduino Oficial  
- Sección de comentarios  

**Sistema de usuario:**
- Registro / Inicio de sesión (almacenado en `localStorage`)  
- Cierre de sesión  
- Gestión de comentarios personales  

---

### Funcionalidades

- Sistema de login y registro local sin backend  
- Persistencia de datos mediante `localStorage`  
- Comentarios con control por usuario  
- Cambio dinámico de secciones sin recargar la página  
- Notificaciones tipo “toast” (mensajes flotantes)  
- Videos de fondo que cambian según la sección activa  

---

### Tecnologías utilizadas

- **HTML5:** estructura y contenido  
- **CSS3:** estilos, animaciones y efectos visuales  
- **JavaScript (ES6):** manejo de usuarios, navegación y comentarios  
- **LocalStorage:** almacenamiento local de usuarios y comentarios  

---

### Usuarios
| Campo          | Ejemplo              |
|----------------|--------------------|
| Nombre         | Juan Pérez          |
| Email          | juanp@gmail.com     |
| Fecha Registro | 10/09/2025          |

### Comentarios
| Campo         | Ejemplo                                      |
|---------------|---------------------------------------------|
| Id comentario | 001                                         |
| Id usuario    | 1                                           |
| Mensaje       | Tengo dudas sobre cómo conectar el módulo Bluetooth |
| Fecha         | 2025-10-02                                  |

</details>

---

<details>
<summary><strong>ARDUINO</strong></summary>

#### Programación
Tutorial YT- Facil
https://www.youtube.com/watch?v=03mQrT4lDgM

#### Fisica
## Modelo 3D del coche

Visualiza el modelo 3D del proyecto en Sketchfab:

[![Modelo 3D Luxury_SL](./4bb6ce32-ae7d-42a5-a500-93917e898b58.png)](https://skfb.ly/pBrxp)

#### Proporciones
### Proporciones y Detalles Técnicos del Modelo

| Propiedad                | Valor                                           |
|---------------------------|------------------------------------------------|
| Formato                   | FBX                                            |
| Tamaño del archivo        | 6.4 MB (descargable: 6 MB)                     |
| Geometría                 | 175.000 triángulos, 94.300 vértices           |
| Materiales                | 29 (sin texturas PBR)                          |
| UV Layers                 | Sí                                             |
| Colores por vértice       | No                                             |
| Animaciones               | 0                                              |
| Rigged geometries         | No                                             |
| Morph geometries          | 0                                              |
| Escala / Transformaciones | Ajustes aplicados según Blender 3D             |
| Uso en proyecto           | Visualización 3D e interacción física con Arduino |

### Funcionalidad del Modelo 3D
- Integración web mediante **Blender + Three.js / WebGL** para visualización interactiva.  
- Permite rotación, zoom y exploración dinámica desde el navegador.  
- Conexión con Arduino para reflejar movimientos y luces del coche físico.

</details>

---

<details>
<summary><strong>RED</strong></summary>

#### Diagrama de la Red

#### Mapa Físico

#### Mapa Lógico

</details>

---

<details>
<summary><strong>SERVICIOS</strong></summary>

#### DNS

#### DHCP

#### Apache

#### Firewall

#### Copias de Seguridad

</details>

---

<div align="center">

<img src="https://i.imgur.com/qPQOsBJ.png" alt="Banner Luxury_SL" width="700" height="200">

</div>
