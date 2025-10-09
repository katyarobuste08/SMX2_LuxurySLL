# SMX2_LuxurySL

![Estado](https://img.shields.io/badge/Estado-En%20desarrollo-orange)
![Tecnologías](https://img.shields.io/badge/Tecnologías-Blender%20|%20Arduino%20|%20C/C++-blue)

## Equipo
Katya Robuste • Pau Ferrer • Nazar Kishchuk

## Logo
![Logo Luxury_SL](https://i.imgur.com/BqUJceo.jpeg)

---

## 1. Descripción general del proyecto

**Aplicaciones utilizadas:**  
- Blender (modelo 3D)  
- C/C++ (Arduino)  

**Propósito:**  
Mostrar un coche de lujo en 3D controlado con Arduino usando un mando Bluetooth, con efectos visuales y control de movimiento.

**Funcionalidades para usuarios:**

| Funcionalidad | Descripción |
|---------------|------------|
| Movimiento    | Adelante, atrás, izquierda, derecha |
| Luces         | Cambiar luces del coche |
| Crear cuenta  | Registrar nombre, apellidos, correo y contraseña |
| Comentarios   | Contactar con soporte técnico |

**Objetivo:**  
Identificar qué tipo de datos necesitamos almacenar en la base de datos.

---

## 2. Entidades principales

| Entidad       | Descripción |
|---------------|------------|
| Usuarios      | Datos de los usuarios |
| Comentarios   | Mensajes enviados al soporte técnico |
| Herramientas  | Componentes y herramientas usadas en el coche |
| Arduino       | Información del microcontrolador usado |
| Diseño 3D     | Modelos en Blender para los coches |
| Coche         | Datos generales y configuración de cada coche |

---

## 3. Atributos de cada entidad

| Entidad       | Atributos |
|---------------|-----------|
| Usuarios      | Id, Nombre, Apellidos, Email, Contraseña, Fecha de registro |
| Comentarios   | Id comentario, Id usuario, Mensaje, Fecha |
| Herramientas  | Nombre, Descripción, Cantidad |
| Arduino       | Id Arduino, Modelo, Descripción, Fecha de compra |
| Diseño 3D     | Id diseño, Nombre, Archivo Blender, Descripción, Fecha creación |
| Coche         | Id coche, Id diseño, Id Arduino, Estado, Configuración/Detalles |

---

