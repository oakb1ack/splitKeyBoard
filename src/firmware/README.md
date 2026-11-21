# ZMK firmware

This directory is reserved for the keyboard's ZMK configuration and custom
shield. No firmware has been configured or built yet.

The PCB design references a XIAO nRF52840. If that is the controller used,
the current ZMK board target is `xiao_ble//zmk`.

Follow the [new keyboard shield guide](https://zmk.dev/docs/hardware-integration/new-shield)
to create a ZMK module in this directory. Define the split halves, matrix pins,
diode direction, physical layout, and keymap from the actual PCB wiring. See
the [local toolchain guide](https://zmk.dev/docs/development/local-toolchain/setup)
to build and flash each half.

For local builds, point `ZMK_CONFIG` at the absolute path to this directory's
`config` folder and `ZMK_EXTRA_MODULES` at the absolute path to this directory
when it contains the module's `zephyr/module.yml`. See the
[build instructions](https://zmk.dev/docs/development/local-toolchain/build-flash).
