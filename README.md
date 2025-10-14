# SMX2_LuxurySL
**Estado:** En desarrollo | **Tecnologías:** Blender | Arduino | C/C++

---

## Equipo
**Katya Robuste • Pau Ferrer • Nazar Kishchuk**

---

## Logo
![Logo Luxury_SL](https://i.imgur.com/BqUJceo.jpeg)

---

## Descripción general del proyecto

### *Aplicaciones utilizadas*
- **Blender3d:** Modelado 3D  
- **C/C++ (Arduino):** Control de hardware  

### *Propósito*
Presentar un **coche de lujo en 3D**, controlado con Arduino mediante un mando Bluetooth, con **efectos visuales realistas y control de movimiento**.

### *Funcionalidades para usuarios*

| Funcionalidad | Descripción |
|---------------|-------------|
| Movimiento    | Adelante, atrás, izquierda, derecha |
| Luces         | Cambiar luces del coche |
| Crear cuenta  | Registrar nombre, apellidos, correo y contraseña |
| Comentarios   | Contactar con soporte técnico |

### *Objetivo*
Definir qué **datos necesitamos almacenar** en la base de datos de usuarios y coches.

---

## Entidades principales

| Entidad      | Descripción |
|--------------|-------------|
| Usuarios     | Datos de los usuarios registrados |
| Comentarios  | Mensajes enviados al soporte técnico |
| Herramientas | Componentes y herramientas usadas en el coche |
| Arduino      | Información del microcontrolador |
| Diseño 3D    | Modelos 3D creados en Blender |
| Coche        | Datos generales y configuración de cada coche |

---

## Atributos de cada entidad

| Entidad      | Atributos |
|--------------|-----------|
| Usuarios     | Id, Nombre, Apellidos, Email, Contraseña, Fecha de registro |
| Comentarios  | Id comentario, Id usuario, Mensaje, Fecha |
| Herramientas | Nombre, Descripción, Cantidad |
| Arduino      | Id Arduino, Modelo, Descripción, Fecha de compra |
| Diseño 3D    | Id diseño, Nombre, Archivo Blender, Descripción, Fecha creación |
| Coche        | Id coche, Id diseño, Id Arduino, Estado, Configuración/Detalles |

---

## Relaciones entre entidades (ERD simplificado)

- Usuarios → tiene → Comentarios  
- Diseño 3D → pertenece a → Coche ← usa → Arduino  
- Herramientas ↔ relacionadas con ↔ Coche

---
