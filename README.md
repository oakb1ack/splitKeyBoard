# Split keyboard

A 42-key split keyboard with a KiCad PCB and ZMK firmware for two XIAO
nRF52840 controllers. The left half connects to the host; the right half
connects to the left over Bluetooth.

![Keyboard layout showing switch references](docs/layout.svg)

- [PCB and schematics](src/pcb/README.md)
- [Firmware and keymap](src/firmware/README.md)

## License

Project files are available under the [MIT License](LICENSE). The included
parts from [marbastlib](src/pcb/marbastlib-main/LICENSE),
[Seeed OPL](src/pcb/OPL_Kicad_Library-master/LICENSE), and
[mouse-bite.pretty](src/pcb/mouse-bite.pretty/LICENSE) retain their own licenses.
