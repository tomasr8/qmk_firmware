# IDA Macropad QMK Configuration

A minimal QMK configuration for the 3-key IDA macropad.

## Hardware

- Microcontroller: Pro Micro (ATmega32U4)
- Keys: 3
- Matrix: 2x2 (with one position unused)

## Pinout

- F4 → Column 1
- F5 → Column 2
- F6 → Row 1
- F7 → Row 2

## Building

Copy this folder to your QMK installation at `keyboards/ida/`, then:

```bash
qmk compile -kb ida -km default
```

## Flashing

```bash
qmk flash -kb ida -km default
```

Then reset your Pro Micro (usually by shorting RST to GND twice quickly).

## Customizing

Edit `keymaps/default/keymap.c` to change the key assignments. The default layout is:

```
[ A ] [ B ]
[ C ]
```

You can use any QMK keycodes - see https://docs.qmk.fm/keycodes
