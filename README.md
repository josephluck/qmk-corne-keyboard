# Joseph Luck's CRKBD config

The keymap and configuration is available in the `/keyboards/crkbd/keymaps/joseph_luck` directory.

This build has OLED support. It can be turned off in `rules.mk`

### Building firmware

> Assumes you have Docker installed

To build the firmware, run: `util/docker_build.sh crkbd:joseph_luck`

### Flashing the keyboard

Plug the keyboard in via the right half. You shouldn't need the TRRS cable connecting the two halfs, as the master half is the right half, however it wouldn't hurt to do so.

> Note: If you have modified the `config.h` or `rules.mk`, you'll need to flash _both_ halfs of the keyboard.

If you already have this layout flashed (and you haven't removed the reset keys from the keymap), you can plug the keyboard in, and trigger any one of the reset buttons defined in the keymap adjacent to this README. Otherwise you can use the physical reset button between the CRKBD's micro controller and the TRRS jack. A small red LED should appear under the micro controller when the keyboard is in reset mode. Note that the micro controller is only in reset mode for a few seconds, so load up the firmware before pressing the reset button and press flash quickly.

Then to flash the keyboard, use the OSX app `QMK Firmware` and load the generated `crkbd_rev1_common_josephluck.hex` firmware and flash the keyboard.
