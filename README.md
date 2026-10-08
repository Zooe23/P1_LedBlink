Práctica de Control de LEDs en Raspberry Pi (BCM vs BOARD)
Este repositorio contiene scripts en Python diseñados para controlar un LED conectado a una Raspberry Pi utilizando la librería RPi.GPIO, demostrando las dos formas principales de numeración de pines disponibles: BCM (Broadcom SOC channel) y BOARD (numeración física de la placa).

🚀 Tecnologías y Hardware Utilizado
Hardware: Raspberry Pi (cualquier modelo con pines GPIO de 40 pines)
Componente: LED y resistencia de protección (aprox. 220Ω - 330Ω)
Lenguaje: Python 3
Librería GPIO: RPi.GPIO
Control de Versiones: Git & GitHub
📌 Descripción de los Programas
El repositorio incluye dos implementaciones prácticas:

Modo BCM (control_bcm.py):

Utiliza la numeración lógica del procesador Broadcom.
Conecta el LED al GPIO 18 (que corresponde físicamente al Pin 12).
Ejecuta un bucle infinito (while True) de parpadeo continuo (encendido y apagado cada 1 segundo) hasta que el usuario lo interrumpe manualmente con Ctrl+C.
Modo BOARD (control_board.py):

Utiliza la numeración física de los pines de la placa.
Conecta directamente al Pin físico 12 (equivalente al GPIO 18).
Ejecuta un patrón de control estructurado por ciclos limitados (10 iteraciones de parpadeos rápidos con pausas largas).
🛠️ Conexión de Hardware
Ánodo (Pata larga del LED): Conectado a través de la resistencia hacia el Pin 12 (GPIO 18).
Cátodo (Pata corta del LED): Conectado a cualquier pin de GND (Tierras físicas, por ejemplo, el pin 6 o 14) de la Raspberry Pi.
