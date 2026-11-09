# Medidas de Argos

> Cada medida, con la fecha, el instrumento y las condiciones. Si no está aquí, no se ha medido.

## 11 nov · Captura del UART del termómetro ESP32

Instrumento: Argos en protoboard + PulseView. Archivo: `capturas/2026-11-11-uart-termometro.sr`

| Dato | Valor |
|---|---|
| Baudio configurado en el ESP32 | |
| Frecuencia de muestreo usada | |
| Ancho de un bit medido en PulseView (µs) | |
| Baudio calculado a mano a partir del ancho | |
| Error frente al configurado (%) | |
| ¿El texto decodificado coincide con el monitor serie? | |

## 14 nov · Cálculo de la protección

| Dato | Valor | De dónde sale |
|---|---|---|
| Resistencia en serie elegida (Ω) | | |
| Corriente si alguien mete 5 V por error (mA) | | cuenta en la bitácora |
| Capacidad de entrada del GPIO (pF) | | hoja de datos del RP2040, página ___ |
| Frecuencia de corte del RC (MHz) | | |
| Muestreo máximo sin deformar la señal (MHz) | | |

## 27 nov · Pinout de la PCB frente a sigrok-pico

| Canal | GPIO en sigrok-pico | GPIO en mi PCB | ¿Coincide? |
|---|---|---|---|
| D0 | | | |
| D1 | | | |
| D2 | | | |
| D3 | | | |
| D4 | | | |
| D5 | | | |
| D6 | | | |
| D7 | | | |

## 2 dic · Prueba de los 8 canales en la PCB

Señal de prueba: _____ (frecuencia _____). Archivo: `capturas/2026-12-02-8-canales.sr`

| Canal | ¿La ve? | Notas |
|---|---|---|
| D0 | | |
| D1 | | |
| D2 | | |
| D3 | | |
| D4 | | |
| D5 | | |
| D6 | | |
| D7 | | |

## 24 nov y 3 dic · I²C del INA226 de Prometeo

| Dato | Protoboard (24 nov) | PCB (3 dic) |
|---|---|---|
| Frecuencia de SCL medida | | |
| Dirección del INA226 vista | | |
| Registro leído | | |
| Bytes recibidos | | |
| ¿Hay ACK en cada byte? | | |
