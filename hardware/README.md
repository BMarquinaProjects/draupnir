# hardware

Aquí va el proyecto de Draupnir. Se crea en el paso 0.2 de la guía, con el nombre `draupnir` y dentro de esta carpeta. Hay una guía por herramienta, `guia-kicad.html` y `guia-altium.html`: se elige una y no se cambia a mitad.

| Si es en KiCad 10 | Si es en Altium Designer 26 | Qué es |
|---|---|---|
| `draupnir\draupnir.kicad_pro` | `Draupnir\Draupnir.PrjPcb` | El proyecto |
| `draupnir\draupnir.kicad_sch` | `Draupnir\Draupnir.SchDoc` | El esquema |
| `draupnir\draupnir.kicad_pcb` | `Draupnir\Draupnir.PcbDoc` | La placa |
| `fabricacion\gerbers\` | `Draupnir\Project Outputs for Draupnir\` | Donde la herramienta escribe los Gerbers y los taladros. Git lo ignora |

En las dos:

| Archivo | Qué es |
|---|---|
| `fabricacion\draupnir-v1.0-gerbers.zip` | Lo que se envía a JLCPCB. Git lo ignora; se publica como release |
| `fabricacion\draupnir-v1.0-bom.csv` | La lista de piezas. Sí va a git |

- Las piezas propias no están aquí: salen de Akmon. En KiCad, de `FORJA\akmon\biblioteca\forja.pretty`; en Altium, de `FORJA\akmon\altium\Forja.SchLib` y `Forja.PcbLib`. El esquema y la placa guardan una copia de cada pieza, así que el proyecto se abre aunque falte Akmon.
- Cada pedido se etiqueta en git (`v1.0`, `v1.1`…) y se publica como release con su zip.
