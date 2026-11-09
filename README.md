# Argos

> Argos Panóptēs, el gigante de cien ojos. Hera lo puso de guardia porque nunca los cerraba todos a la vez.

Analizador lógico de 8 canales: una Raspberry Pi Pico con el firmware libre [sigrok-pico](https://github.com/pico-coder/sigrok-pico) y PulseView en el PC, sobre una PCB propia con protección de entradas. **La v1 es solo para señales de 3,3 V.** El buffer que acepta 5 V (74LVC245) llega en la v2.

**Metal:** Mineral → objetivo Bronce · **Campaña:** 2026-11 «Forjar el banco» · **EDA:** KiCad 10, con la plantilla [Akmon](https://github.com/BMarquinaProyects/akmon)

<!-- Foto de la placa montada: fotos/argos.jpg (5 dic) -->

## Especificación

| | v1 |
|---|---|
| Canales | 8 |
| Niveles de entrada | 3,3 V. **No admite 5 V** |
| Protección por canal | Resistencia en serie de _____ Ω (calculada el 14 nov, ver MEDIDAS.md) |
| Muestreo máximo útil | _____ MHz (limitado por _____) |
| Firmware | sigrok-pico, versión _____ |
| Software en el PC | PulseView nightly del _____ |
| Placa | 2 capas, _____ × _____ mm, JLCPCB |

## Cómo se usa

1. Flashea sigrok-pico: mantén BOOTSEL, conecta la Pico por USB y arrastra el `.uf2`.
2. Abre PulseView (versión nightly: la 0.4.2 no reconoce sigrok-pico) y elige el controlador de la Pico y su puerto COM.
3. **Une primero las masas** de Argos y del circuito que vas a medir.
4. Conecta las señales a los canales. Solo de 3,3 V.
5. Elige una frecuencia de muestreo de al menos 10 veces la de la señal y añade el decodificador (UART, I²C o SPI).

## Medidas

Resumen de [MEDIDAS.md](MEDIDAS.md). _Se rellena al cerrar la campaña._

## Cómo fabricarla

Los Gerbers de cada pedido están en las releases del repositorio. La BOM está en `hardware/fabricacion/`.

## Lo que aprendí

- Niveles lógicos, y por qué un 74LVC alimentado a 3,3 V acepta 5 V en sus entradas (v2).
- Proteger entradas: resistencia en serie y diodos.
- Muestreo: frecuencia, Nyquist y profundidad de memoria.
- Decodificar UART, I²C y SPI de mis propios montajes.

## Bitácora

[BITACORA.md](BITACORA.md)

## Licencia

Por decidir antes de pasar a Hierro.
