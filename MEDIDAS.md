# Medidas de Draupnir

> Cada medida, con la fecha, el instrumento y las condiciones. Si no está aquí, no se ha medido.

## 12 nov · Captura del UART del termómetro ESP32

Instrumento: Draupnir en protoboard + PulseView, con 1 kΩ en serie en el canal D2. Archivo: `capturas/2026-11-12-uart-termometro.sr`

| Dato | Valor |
|---|---|
| Baudio configurado en el ESP32 | |
| Frecuencia de muestreo usada | |
| Ancho de un bit medido en PulseView (µs) | |
| Baudio calculado a mano a partir del ancho | |
| Error frente al configurado (%) | |
| ¿El texto decodificado coincide con el monitor serie? | |

## 12 nov · Cálculo de la resistencia en serie (decisiones 1 y 2 de la guía)

| Dato | Valor | De dónde sale |
|---|---|---|
| Tensión máxima absoluta en un GPIO (V) | | hoja de datos del RP2040, tabla 622, pág. 614 |
| ¿Hay diodo del GPIO a la alimentación? | | hoja del RP2040, tabla 614, pág. 612; hoja de la Pico, apartado 4.2 |
| Tensión en el pin si alguien mete 5 V, con la resistencia puesta (V) | | cuenta en la bitácora |
| Resistencia en serie elegida (Ω) | | |
| Corriente si un GPIO en salida choca con la señal (mA) | | 3,3 V / R |
| Capacidad de entrada supuesta (pF) | | **hipótesis**: la hoja de datos no la da. Se comprueba el 3 dic |
| Frecuencia de corte del RC (MHz) | | 1 / (2π·R·C) |
| Tiempo de subida, 2,2·R·C (ns) | | |
| Muestreo recomendado con 8 canales (Msps) | | guía de usuario de sigrok-pico |
| Señal más rápida que se ve bien, a 10 muestras por periodo (MHz) | | |

## 18 nov · Pinout de la PCB frente a sigrok-pico (paso 5.2 de la guía)

sigrok-pico numera sus canales como los GPIO: D2 es GP2. Se rellena resaltando cada red en la placa: es el paso 5.2 de la guía.

| Canal | GPIO en sigrok-pico | Pin de J1 en mi PCB | Resistencia | Pin de la Pico en mi PCB | ¿Coincide? |
|---|---|---|---|---|---|
| D2 | GP2 | | | | |
| D3 | GP3 | | | | |
| D4 | GP4 | | | | |
| D5 | GP5 | | | | |
| D6 | GP6 | | | | |
| D7 | GP7 | | | | |
| D8 | GP8 | | | | |
| D9 | GP9 | | | | |

## 2 dic · Prueba de los 8 canales en la PCB

Señal de prueba: _____ (frecuencia _____). Archivo: `capturas/2026-12-02-8-canales.sr`

| Canal | ¿La ve? | Notas |
|---|---|---|
| D2 | | |
| D3 | | |
| D4 | | |
| D5 | | |
| D6 | | |
| D7 | | |
| D8 | | |
| D9 | | |

## 3 dic · Límite útil (paso 7.5 de la guía)

Onda cuadrada de la otra Pico. Se sube la frecuencia hasta que el ciclo de trabajo capturado sale del 45–55 %.

| Dato | Valor |
|---|---|
| Frecuencia de muestreo usada (Msps) | |
| Frecuencia más alta capturada bien (MHz) | |
| ¿Qué lo limita: el muestreo o el filtro RC? | |
| Capacidad de entrada que sale de ahí (pF), frente a la hipótesis | |

## 3 dic · I²C del INA226 de Narthex (en protoboard)

| Dato | Con Draupnir en su PCB (3 dic) | Repetido con Narthex en su PCB (dic) |
|---|---|---|
| Frecuencia de SCL medida | | |
| Dirección del INA226 vista | | |
| Registro leído | | |
| Bytes recibidos | | |
| ¿Hay ACK en cada byte? | | |
