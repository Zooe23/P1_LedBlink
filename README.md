# ⚡ Práctica de Control de LEDs en Raspberry Pi
> *Diferencias entre numeración BCM y BOARD mediante RPi.GPIO*

---

## 📌 Descripción General

Este proyecto contiene scripts en **Python** diseñados para controlar un LED conectado a una **Raspberry Pi** utilizando la librería `RPi.GPIO`. El objetivo principal es demostrar y comparar las dos formas principales de numeración de pines:

* **BCM:** Broadcom SOC channel (numeración lógica).
* **BOARD:** Numeración física de los pines de la placa.

---

## 🚀 Tecnologías y Hardware

| Categoría | Detalle |
| :--- | :--- |
| **Hardware** | Raspberry Pi *(cualquier modelo con GPIO de 40 pines)* |
| **Componentes** | 1x LED y 1x Resistencia de protección ($220\Omega$ - $330\Omega$) |
| **Lenguaje** | Python 3 |
| **Librería** | `RPi.GPIO` |
| **Control de Versiones** | Git & GitHub |

---

## 📂 Archivos del Repositorio

### 1. `control_bcm.py` — Modo BCM
* Usa la numeración **lógica** del procesador.
* LED conectado al **GPIO 18** *(Pin físico 12)*.
* Ejecuta un bucle infinito (`while True`) con parpadeo de 1 segundo hasta presionar `Ctrl + C`.

### 2. `control_board.py` — Modo BOARD
* Usa la numeración **física** de la placa.
* LED conectado directamente al **Pin físico 12** *(GPIO 18)*.
* Realiza un ciclo controlado de **10 iteraciones** de parpadeo rápido con pausas largas.

---

## 🔌 Conexión del Hardware

* **Ánodo** *(Patita larga del LED)* $\rightarrow$ Resistencia $\rightarrow$ **Pin 12 (GPIO 18)**.
* **Cátodo** *(Patita corta del LED)* $\rightarrow$ **GND** *(Ej. Pin 6 o Pin 14)*.

---

## 💻 Ejecución

```bash
# Ejecutar versión BCM
python3 control_bcm.py

# Ejecutar versión BOARD
python3 control_board.py
