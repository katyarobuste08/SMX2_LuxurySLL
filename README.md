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


##  Jerarquía Visual

Los colores utilizados  en la web ↔ Blanco, Negro y Gris, con un video al fondo del coche que hemos escogido para el logo 

El color principal del fondo es el negro. Transmite elegancia, lujo y exclusividad. Además, hace que los elementos claros resalten con fuerza.
El gris se  usa como color intermedio en botones y fondos secundarios. Aporta equilibrio visual y suaviza el contraste entre el blanco y el negro.
El blanco se aplica al texto y algunos detalles, aportando claridad, limpieza y legibilidad.

## Equilibrio Visual

 El video  del coche ocupa la parte central superior, atrayendo la atención principal.
 Debajo se encuentran los botones (HERRAMIENTAS, 3D BLENDER, ARDUINO), pocicionado  de forma equilibrada y con igual tamaño, lo que aporta orden y coherencia.
 En la parte superior derecha se muestra la información del usuario conectado, creando un contraste con la zona izquierda vacía, lo que equilibra la composición general.



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
Definir qué **datos necesitamos almacenar** en la base de datos de usuarios y del coche.

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
- Colores ↔ Blanco, Negro y Gris

---
