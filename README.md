# Split keyboard ZMK firmware

This configuration targets two XIAO nRF52840 controllers over Bluetooth. The
left half is central and connects to the host; the right half is peripheral.
The 42 bindings in `config/splitkeyboard.keymap` are deliberately `&none`.
Replace them with your own bindings. Each group of five follows the schematic's
matrix rows; the final two bindings are the outer switches SW63 and SW84.
Switch references in the keymap identify the physical positions.

To edit visually, open [Keymap Editor](https://nickcoutsos.github.io/keymap-editor/),
connect your GitHub account, and select this repository. The root-level
`config/splitkeyboard.json` describes the PCB layout for the editor.

The shield is under `config/boards/shields/splitkeyboard` so ZMK and the keymap editor can find it.
The PCB netlist connects columns 0–4 to XIAO D1–D5 and rows 0–4 to D10–D6;
the diode cathodes connect to the row nets. The shield assumes the PCB matches
the schematic. Battery sensing and ZMK Studio are not configured.

Push changes to build both halves in GitHub Actions and download the left and right firmware
artifacts from the completed run. Flash the matching left and right UF2 files
to their controllers. No key will do anything until you write the keymap.

For a local ZMK workspace, build from its `zmk/app` directory using an absolute
path to this repository's `config` directory:

```sh
west build -p -b seeeduino_xiao_ble -d build/left -- -DSHIELD=splitkeyboard_left -DZMK_CONFIG=/absolute/path/to/splitKeyBoard/config
west build -p -b seeeduino_xiao_ble -d build/right -- -DSHIELD=splitkeyboard_right -DZMK_CONFIG=/absolute/path/to/splitKeyBoard/config
```

The config is pinned to ZMK v0.3; use the matching ZMK revision locally. See
the [ZMK shield guide](https://zmk.dev/docs/hardware-integration/new-shield)
and [build guide](https://zmk.dev/docs/development/local-toolchain/build-flash).
