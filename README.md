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

La web **LUXURY_SL** está diseñada con un enfoque oscuro, moderno y minimalista, orientado a transmitir elegancia y tecnología.  
A continuación se presentan las pantallas principales del sitio, ordenadas para reflejar el flujo real de uso: pantalla principal, elementos de acceso (login/registro), navegación, contenido informativo y vistas con el usuario autenticado.

---

#### 1. Pantalla principal (hero)

<div align="center">
<img src="https://i.postimg.cc/50PRHXSb/Captura-de-pantalla-2025-11-04-094043.png" alt="Hero Luxury_SL - Página principal" width="600"/>
</div>

Esta es la pantalla de bienvenida. Muestra el mensaje principal del proyecto y un botón de acción (“Learn More”). Aquí el usuario obtiene la primera impresión visual del proyecto y puede acceder a las funcionalidades del sitio (registro, inicio de sesión o navegar a las secciones principales).

---

#### 2. Barra de acceso rápido (no autenticado)

<div align="center">
<img src="https://i.postimg.cc/rF77CtXq/Captura-de-pantalla-2025-11-04-094021.png" alt="Accesos - Login y Crear Cuenta" width="500"/>
</div>

Estado de usuario no autenticado: presenta los botones **Login** y **Crear Cuenta** en la parte superior, permitiendo al visitante iniciar el proceso de acceso o registro. Es un componente pequeño y persistente que guía al usuario hacia la autenticación.

---

#### 3. Modal: Iniciar sesión

<div align="center">
<img src="https://i.postimg.cc/j5JMjM2s/Captura-de-pantalla-2025-11-04-094233.png" alt="Modal Iniciar Sesión" width="550"/>
</div>

Ventana modal de inicio de sesión con campos para **Email** y **Contraseña**, y un botón **Login**. El diseño es claro y minimalista para facilitar la entrada de credenciales sin distraer al usuario del fondo de la página.

---

#### 4. Modal: Crear cuenta

<div align="center">
<img src="https://i.postimg.cc/YqXYJ1qH/Captura-de-pantalla-2025-11-04-094251.png" alt="Modal Crear Cuenta" width="550"/>
</div>

Formulario de creación de cuenta que solicita **Usuario**, **Email** y **Contraseña** (mínimo 6 caracteres). Al completar este formulario y registrarse correctamente, el usuario podrá iniciar sesión con esas credenciales.

---

#### 5. Menú lateral (navegación)

<div align="center">
<img src="https://i.postimg.cc/CMRgG0Bj/Captura-de-pantalla-2025-11-04-094111.png" alt="Menú lateral - Navegación" width="500"/>
</div>

Menú lateral izquierdo con las secciones principales: **Inicio**, **Sobre Nosotros**, **Contacto** y **Página Oficial**. Permite navegación persistente entre secciones sin recargar la página.

---

#### 6. Sección: Sobre Nosotros

<div align="center">
<img src="https://i.postimg.cc/pT73G9hy/Captura-de-pantalla-2025-11-04-094136.png" alt="Sección Sobre Nosotros" width="600"/>
</div>

Página que explica la propuesta de Luxury_SL: la **fusión entre diseño 3D y tecnología Arduino** para crear vehículos interactivos. Incluye texto descriptivo y un botón **Volver al Inicio** para facilitar la navegación.

---

#### 7. Sección: Contacto

<div align="center">
<img src="https://i.postimg.cc/cCwkFFG2/Captura-de-pantalla-2025-11-04-094208.png" alt="Sección Contacto" width="600"/>
</div>

Panel de contacto dividido en **Contacto General** (email y teléfono) y **Soporte Técnico** (email y horario de atención, lunes–viernes 9:00–18:00). Mantiene la estética oscura y el botón **Volver al Inicio**.

---

#### 8. Sección: Página Oficial (contenidos)

<div align="center">
<img src="https://i.postimg.cc/4xD7gPDP/Captura-de-pantalla-2025-11-04-094404.png" alt="Página Oficial - Modelos/Experiencias/Tutoriales" width="600"/>
</div>

La **Página Oficial** agrupa los bloques de contenido principales: **Modelos 3D de Lujo**, **Experiencia Interactiva** y **Tutoriales Arduino**. Cada bloque ofrece acceso a recursos (modelos, simulaciones y guías) manteniendo coherencia visual.

---

### Observaciones de diseño

- Estética: predominio de negros y grises, tipografía con buena legibilidad y acentos claros para llamadas a la acción.  
- Interacción: navegación sin recarga, modales para autenticación, botones de retorno consistentes.  
- Usabilidad: formularios compactos y directos; menús persistentes y accesibles desde cualquier vista.

---
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
