🚀 UF6 – Desarrollo con Arduino y ESP32-S3 WROOM
<p align="center">












</p>
📖 Descripción General del Proyecto

Este repositorio documenta el desarrollo completo de prácticas realizadas en el módulo de Arduino del Ciclo Formativo de Grado Medio SMX.

Se trabaja con la placa ESP32-S3 WROOM, un microcontrolador de 32 bits con conectividad WiFi y Bluetooth, programado mediante Arduino IDE 2.0 utilizando lenguaje C/C++.

El proyecto tiene como finalidad:

Comprender la arquitectura básica de un microcontrolador.

Aprender a configurar y utilizar el entorno Arduino.

Controlar dispositivos electrónicos reales.

Diseñar circuitos funcionales en protoboard.

Aplicar lógica secuencial y condicional.

Integrar hardware y software en sistemas embebidos.

🗂 Índice

Introducción al entorno

Práctica 1 – Blink (LED interno)

Práctica 2 – LED externo

Práctica 3 – Semáforo

Práctica 4 – Botón + LED

Arquitectura del proyecto

Conocimientos adquiridos

Conclusión técnica

🧠 1️⃣ Introducción al Entorno
🔹 ¿Qué es Arduino?

Arduino es una plataforma de hardware y software libre diseñada para facilitar la programación de microcontroladores y el desarrollo de proyectos electrónicos interactivos.

Permite conectar el mundo físico con el mundo digital mediante:

Sensores (entrada)

Actuadores (salida)

Microcontrolador (procesamiento)

🔹 ¿Qué es el ESP32-S3?

El ESP32-S3 WROOM es un microcontrolador avanzado que incluye:

CPU dual core 32 bits

WiFi integrado

Bluetooth

GPIO digitales

Conversores analógico-digitales

Memoria Flash integrada

En estas prácticas utilizamos principalmente los pines GPIO digitales.

🟢 2️⃣ Práctica 1 – Blink (LED Interno)
🎯 Objetivo

Instalar y configurar Arduino IDE.

Subir un programa al microcontrolador.

Controlar un LED integrado.

Comprender la estructura básica de un programa Arduino.

🧰 Material Utilizado
Componente	Función Técnica
ESP32-S3 WROOM	Ejecuta el programa
Cable USB	Alimentación + comunicación
PC con Arduino IDE	Programación y compilación
🔌 Esquema

El LED interno está conectado al GPIO2.

No requiere circuito externo.

💻 Código Completo
#define LED_BUILTIN 2

void setup() {
  pinMode(LED_BUILTIN, OUTPUT);
}

void loop() {
  digitalWrite(LED_BUILTIN, HIGH);
  delay(1000);
  digitalWrite(LED_BUILTIN, LOW);
  delay(1000);
}
🔎 Explicación Técnica Detallada
#define LED_BUILTIN 2

Crea una constante simbólica.
Evita usar números mágicos y mejora la legibilidad del código.

void setup()

Función que se ejecuta una sola vez al iniciar el microcontrolador.

Se utiliza para:

Configurar pines

Inicializar comunicación serial

Configurar variables globales

void loop()

Se ejecuta de forma infinita mientras el microcontrolador esté encendido.

pinMode(pin, OUTPUT)

Configura el pin como salida digital.

digitalWrite(pin, HIGH)

Envía 3.3V al pin → LED encendido.

digitalWrite(pin, LOW)

Envía 0V → LED apagado.

delay(1000)

Pausa el programa durante 1000 milisegundos.

🎥 Evidencias

Video del parpadeo

Captura del IDE compilando correctamente

💡 3️⃣ Práctica 2 – LED Externo
🎯 Objetivo

Montar un circuito físico.

Comprender polaridad del LED.

Utilizar resistencias limitadoras.

Controlar hardware externo.

🧰 Material
Componente	Descripción
LED 3mm	Dispositivo semiconductor emisor de luz
Resistencia 220Ω	Limita la corriente
Protoboard	Permite montaje sin soldar
Jumpers	Conexión eléctrica
⚡ Fundamento Eléctrico

El LED funciona a aproximadamente 2V.
El ESP32 entrega 3.3V.

Sin resistencia, el LED recibiría demasiada corriente y podría dañarse.

🔌 Esquema
GPIO2 ── 220Ω ── LED ── GND
💻 Código

Se reutiliza el código Blink.

La diferencia es que ahora el LED es externo.

🚦 4️⃣ Práctica 3 – Semáforo
🎯 Objetivo

Controlar múltiples salidas digitales.

Crear una secuencia lógica.

Gestionar tiempos diferentes.

Simular sistema real.

🧰 Material
Elemento	Cantidad
LED Rojo	1
LED Amarillo	1
LED Verde	1
Resistencias 220Ω	3
ESP32-S3	1
🔌 Esquema General
GPIO2 → LED Verde
GPIO4 → LED Amarillo
GPIO5 → LED Rojo

Cada LED conectado con resistencia a GND.

💻 Código
#define VERDE 2
#define AMARILLO 4
#define ROJO 5

void setup() {
  pinMode(VERDE, OUTPUT);
  pinMode(AMARILLO, OUTPUT);
  pinMode(ROJO, OUTPUT);
}

void loop() {

  digitalWrite(VERDE, HIGH);
  digitalWrite(AMARILLO, LOW);
  digitalWrite(ROJO, LOW);
  delay(3000);

  digitalWrite(VERDE, LOW);
  digitalWrite(AMARILLO, HIGH);
  delay(1000);

  digitalWrite(AMARILLO, LOW);
  digitalWrite(ROJO, HIGH);
  delay(3000);
}
🧠 Conceptos Aplicados

Estados secuenciales

Lógica estructurada

Sincronización temporal

Organización de múltiples salidas

🔘 5️⃣ Práctica 4 – Botón + LED
🎯 Objetivo

Leer entrada digital.

Aplicar lógica condicional.

Integrar interacción física.

🧰 Material
Componente	Función
Botón	Entrada digital
LED	Salida
Resistencias 10KΩ	Pull-down
Resistencia 220Ω	Protección LED
🔌 Esquema
Botón → GPIO21
LED → GPIO13

Pull-down mantiene el pin en LOW cuando no se presiona.

💻 Código
#define BOTON 21
#define LED 13

void setup() {
  pinMode(BOTON, INPUT);
  pinMode(LED, OUTPUT);
}

void loop() {
  int estado = digitalRead(BOTON);

  if (estado == HIGH) {
    digitalWrite(LED, HIGH);
  } else {
    digitalWrite(LED, LOW);
  }
}
🧠 Conceptos Clave

Entrada digital

Variables

Condicional if

Lógica booleana

Interacción hardware-software
