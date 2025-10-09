# SMX2_LuxurySL

## Equipo
**Katya Robuste • Pau Ferrer • Nazar Kishchuk**

---

## Logo
![Logo Luxury_SL](https://i.imgur.com/BqUJceo.jpeg)  

---

## 1. Descripción general del proyecto web

Nuestro proyecto tiene varias aplicaciones que utilizaremos, como **Blender** y **C/C++** para el Arduino.  
El nombre "Luxury_SL" refleja una empresa de lujo centrada en coches de alta gama.  

**Propósito de la web:**  
Mostraremos un modelo de coche en **3D** y un **motor controlado con Arduino**, usando un mando para manipular movimientos y efectos especiales como luces.  
Los usuarios podrán controlar:  
- Movimientos: adelante, atrás, izquierda, derecha  
- Cambiar luces del coche  

**Funcionalidades principales para los usuarios:**  
- Crear cuenta (nombre, apellidos, correo electrónico, contraseña)  
- Dejar comentarios y contactar con soporte técnico  

**Objetivo:** Entender el contexto general del proyecto para identificar qué tipo de datos necesitamos guardar.

---

## 2. Identificación de entidades principales

**Elementos importantes que necesitan almacenarse:**  
- Usuarios  
- Herramientas utilizadas para el coche  
- Arduino  
- Diseño 3D (Blender)  
- Coche  
- Comentarios de usuarios al soporte técnico  

**Acceso a la web:**  
- Explicación y pasos para que los usuarios puedan montar el coche con Arduino

**Tablas sugeridas y motivo de guardado:**

| Tabla       | Tema de información                           | Motivo de guardado |
|------------|-----------------------------------------------|------------------|
| Usuarios    | Datos de usuarios                             | Para gestionar cuentas y comentarios |
| Comentarios | Comentarios de usuarios al soporte técnico   | Para soporte y seguimiento de dudas |
| Herramientas | Detalles de herramientas y componentes      | Para documentar el montaje del coche |
| Arduino     | Información sobre el Arduino                 | Para conocer el modelo y fecha de compra |
| Diseño 3D   | Datos de diseño Blender                      | Para relacionarlo con los coches creados |
| Coche       | Información de cada coche                    | Para saber qué diseño y Arduino usa cada coche |

**Objetivo:** Detectar los objetos clave del proyecto que se convertirán en tablas de la base de datos.

---

## 3. Datos que se deben guardar de cada entidad

### Herramientas
- Nombre de la herramienta (varchar)  
- Descripción (text)  
- Cantidad necesaria (int)  

### Arduino
- Id Arduino (varchar)  
- Modelo (varchar)  
- Descripción del modelo (text)  
- Fecha de compra (date)  

### Diseño 3D (Blender)
- Id diseño (varchar)  
- Nombre del diseño (varchar)  
- Archivo Blender (varchar)  
- Descripción (text)  
- Fecha creación (date)  

### Coche
- Id coche (varchar)  
- Id diseño (varchar)  
- Id Arduino (varchar)  
- Estado actual (varchar)  
- Configuración/Detalles (text)  

### Comentarios
- Id comentario (varchar)  
- Id usuario (varchar)  
- Mensaje (text)  
- Fecha comentario (date)  

**Objetivo:** Comprender los campos o columnas que tendrá cada tabla y el tipo de información que contienen.

---

## 4. Relaciones entre entidades

| Relación         | Descripción |
|-----------------|------------|
| Usuarios - Comentarios | Un usuario puede hacer muchos comentarios. Cada comentario pertenece a un solo usuario. |
| Diseño 3D - Coche     | Un diseño 3D puede usarse en muchos coches. Cada coche tiene un solo diseño. |
| Arduino - Coche       | Un modelo de Arduino puede usarse en muchos coches. Cada coche tiene un Arduino asignado. |
| Herramientas - Coche  | Un coche puede usar muchas herramientas y una herramienta puede usarse en muchos coches. |

**Objetivo:** Entender cómo los datos se conectan entre sí, esencial para el diseño de tablas con claves foráneas.

---

## 5. Ejemplo de datos (simulación)

### Comentarios
| Id comentario | Id usuario | Mensaje | Fecha comentario |
|---------------|------------|---------|----------------|
| 001           | 1          | Tengo dudas sobre cómo conectar el módulo Bluetooth | 2025-10-02 |

### Arduino
| Id Arduino | Modelo      | Descripción de modelo                | Fecha de compra |
|------------|------------|------------------------------------|----------------|
| A001       | Arduino UNO | Microcontrolador base del coche (ATmega328) | 2025-10-02 |

**Objetivo:** Comprobar si los datos que se han pensado tienen sentido y si falta algo importante.

---

## 6. Reflexiones, dificultades y dudas

- **Partes más difíciles de definir:**  
  Identificar todas las relaciones entre entidades y decidir qué atributos son realmente necesarios.  

- **Incertidumbres:**  
  La gestión exacta de la configuración del coche y cómo relacionarla con las herramientas usadas.  

- **Preguntas:**  
  ¿Es necesario guardar el historial de cambios de configuración del coche, o solo la configuración actual?  

**Objetivo:** Fomentar la reflexión y detectar posibles dudas para mejorar el diseño de la base de datos.
