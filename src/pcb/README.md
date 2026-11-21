# PCB

Open [pcb.kicad_pro](pcb.kicad_pro) in KiCad 10. The PCB is panelized as two
halves with breakaway tabs.

These renders show a local PCB revision whose source changes are not yet committed:

![PCB front](../../docs/pcb-front.png)
![PCB back](../../docs/pcb-back.png)

## Schematic

The [root schematic](pcb.kicad_sch) contains left and right sheets. Preview the
[left](../../docs/schematic-left.svg) or [right](../../docs/schematic-right.svg)
half at full size.

![Left-half schematic](../../docs/schematic-left.svg)

## Before ordering

The saved [Gerbers](Gerber-Files/) and [DRC report](DRC.rpt) are older exports.
The current board has unresolved DRC findings. Run electrical and design-rule
checks, review the results, and regenerate the Gerbers before fabrication.
