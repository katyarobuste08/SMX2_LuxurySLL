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

### Mockup

La página web presenta un diseño **oscuro, moderno y minimalista**, inspirado en el estilo *glassmorphism*, con una experiencia visual limpia y elegante centrada en la marca **LUXURY_SL**.

#### Paleta de colores
- Fondo principal: `#000`
- Texto principal: `#fff`
- Detalles y acentos: `#aaa`
- Efectos translúcidos: `rgba(255,255,255,0.05–0.12)`
- Sombras suaves: `rgba``(255,255,255,0.06)`

#### Tipografía
- `'Segoe UI', Tahoma, Geneva, Verdana, sans-serif`
- Estilo moderno, profesional y legible.
- Tamaños base recomendados:
  `body { font-size: 16px; line-height: 1.6 }`
  `h1 { font-size: 2.25rem }, h2 { 1.75rem }, h3 { 1.25rem }`
- Accesibilidad: respetar contraste WCAG (texto sobre `#000` con `#fff `OK).

#### Estilo visual
- Fondo animado con video. Vídeo `autoplay muted loop` y `object-fit: cover`. Mostrar `image fallback` para dispositivos sin video.
- Glassmorphism: paneles semitransparentes con `backdrop-filter: blur(6px)` y `fondo var(--glass-1/2)`.
- Sombras suaves en tarjetas y botones: `box-shadow: 0 6px 18px rgba(0,0,0,0.6), inset 0 0 6px var(--shadow-soft)`.
- Transiciones fluidas: `transition: transform .25s ease, box-shadow .25s ease, opacity .3s ease`.
- Hover animations: levantar tarjeta `transform: translateY(-6px)` y botón invertir colores (negro → blanco).
- Adaptable para las pantallas de todos los dispositivos.

---

### Mapa de Navegabilidad

**Menú principal:**
- Inicio
- Herramientas  
  3D Blender  
  Arduino  
- Página Oficial *(requiere iniciar sesión)*
- Contacto
- Sobre nosotros

**Página Oficial:**
- Herramientas Oficial  
- 3D Blender Oficial  
- Arduino Oficial  
- Sección de comentarios
- Perfil del usuario (ajustes, comentarios, cerrar sesión)

**Sistema de usuario:**
- Registro / Inicio de sesión (almacenado en `localStorage`)  
- Cierre de sesión  
- Gestión de comentarios personales
- Panel de usuario con estado y acciones rápidas

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

#### Placa Bluetooth
Link
https://www.amazon.es/desarrollo-Binghe-controlador-ESP-WROOM-32-compatible/dp/B0D86JL12Q/ref=sr_1_18_sspa?adgrpid=55614469385&dib=eyJ2IjoiMSJ9.DAHCoAqcD5_clktNk7Amj7fFyit0wnt-gob8L66IwYQmw-uUa8kOz_P-4SF2rOHBmAAGE3hIUrRVSlgfM0IbPJbVMEvowNdUvx6LXTioqYKpDNnhaID0SUAKEQBX84zaWhaLVeIwlPazxsSvTFVzk3tPq3ZDCYbVdYh7cO_Rr48eHKKb81I6s8ZmYxoOSo_BrXEW8qp1M-6Mpb2hYwojzl40NHU6mLT9vGWjVTPz_80xd7Ol1otV2SaTVmkgopd_SQ-mijJ4CGzFoodVd5AjW3ENxpPMhK3AYx7nU0gZylc.7nFnr-vcn8hu-SdyspqroBcY6pFY-ZS2Xpq09qQRNRE&dib_tag=se&hvadid=275345971589&hvdev=c&hvexpln=0&hvlocphy=1005424&hvnetw=g&hvocijid=16473807064755660048--&hvqmt=e&hvrand=16473807064755660048&hvtargid=kwd-308367043101&hydadcr=11829_1842814&keywords=modulo+bluetooth+arduino&mcid=94bc0e5917a23dd8b3d0805a37c0c120&qid=1761034446&sr=8-18-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9tdGY&psc=1

#### Fisica
## Modelo 3D del coche

Visualiza el modelo 3D del proyecto en Sketchfab:
https://skfb.ly/pCxW9

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

<details>
<summary><strong>CONCLUSIONES</strong></summary>

</details>

---

<details>
<summary><strong>BIBLIOGRAFÍA</strong></summary>

</details>

---

<div align="center">

<img src="https://i.imgur.com/qPQOsBJ.png" alt="Banner Luxury_SL" width="700" height="200">

</div>
