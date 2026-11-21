# PCB

Open [pcb.kicad_pro](pcb.kicad_pro) in KiCad 10. The two halves are joined by
breakaway tabs in a panel about 244 × 103 mm.

The 42 switches use 19.05 mm pitch. The five main columns stagger by up to
3 mm between neighbors. The controllers and switch footprints are on the back.

![PCB front](../../docs/pcb-front.png)
![PCB back](../../docs/pcb-back.png)

## Schematic

The [root schematic](pcb.kicad_sch) contains left and right sheets. Preview the
[left](../../docs/schematic-left.svg) or [right](../../docs/schematic-right.svg)
half at full size.

Each half has its own XIAO controller, switch matrix, battery sensing circuit,
and local ground net. The halves communicate wirelessly after separation.

![Left-half schematic](../../docs/schematic-left.svg)

## Before ordering

The [Gerbers and drill files](Gerber-Files/) and [ZIP archive](Gerber-Files.zip)
were exported for this layout. The saved [DRC report](DRC.rpt) reports no
violations, unconnected pads, or schematic parity issues under the project's
enabled checks. It also lists checks that are disabled.

Physical keycap fit, case fit, and typing feel still need a prototype.
