# Lotus 58 ZMK Configuration

[![Build Status](https://github.com/darshkpatel/zmk-config/actions/workflows/build.yml/badge.svg)](https://github.com/darshkpatel/zmk-config/actions/workflows/build.yml)

This repository contains my custom ZMK firmware configuration for the Lotus 58 split keyboard. The Lotus 58 is an open-source split keyboard design that offers elegant minimalism and endless customization possibilities.

[Read more about it in my blog](https://darshkpatel.com/blog/lotus-58-build)

## Keyboard Specifications

- **Base**: Custom modified Lotus 58 PCB
- **Switches**: Gateron Baby Kangaroo (MX Compatible)
- **Keycaps**: XDA Profile blanks
- **Controller**: Raspberry Pi RP2040

## Layout Features

### Base Layer
- Standard QWERTY layout with full number row
- Auto-shift enabled for all alphanumeric keys
- Media controls (Play/Pause) on thumb clusters
- Navigation keys (Up/Down) on thumb clusters
```
,-----------------------------------.                ,-----------------------------------.
| ESC |  1 |  2 |  3 |  4 |  5 |    |                |  6 |  7 |  8 |  9 |  0 |  - | ESC |
|-----+----+----+----+----+----|    |                |----+----+----+----+----+----+-----|
| Tab |  Q |  W |  E |  R |  T |    |                |  Y |  U |  I |  O |  P |  [ | Tab |
|-----+----+----+----+----+----|    |                |----+----+----+----+----+----+-----|
|Caps |  A |  S |  D |  F |  G |Play|                |Play|  H |  J |  K |  L |  ; |  '  |
|-----+----+----+----+----+----+----|                |----+----+----+----+----+----+-----|
|Ctrl |  Z |  X |  C |  V |  B |Dn|Up|               |Up|Dn|  N |  M |  , |  . |  / |Ctrl|
`-------------------------------+----+----.    .----+----+-------------------------------'
                        |Alt|Lower|GUI|Space|    |Enter|Bksp|Raise|Alt|
                        `-------------------'    '-------------------'
```

### Lower Layer
- Special characters and symbols
- Media controls (Previous, Next, Volume)
- Navigation keys (Arrow keys)
- Parentheses and brackets
```
,-----------------------------------.                ,-----------------------------------.
|Boot |    |    |    |    |    |    |                |    |    |    |    |    |    |Boot |
|-----+----+----+----+----+----|    |                |----+----+----+----+----+----+-----|
|     |    |    |    | (  | )  |    |                | #  |Prev|VolD|VolU|Next|    |     |
|-----+----+----+----+----+----|    |                |----+----+----+----+----+----+-----|
|     |    |    |    | [  | ]  |    |                | &  |Left|Down| Up |Rght|    |     |
|-----+----+----+----+----+----+----|                |----+----+----+----+----+----+-----|
|     |    |  * |  ` |  \ |  = |    |                | $  |    |    |    |    |    |     |
`-------------------------------+----+----.    .----+----+-------------------------------'
                        |   |    |   |     |    |    |    |    |   |
                        `-------------------'    '-------------------'
```

### Raise Layer
- Function keys (F1-F10)
- Bluetooth profile selection (5 profiles)
- USB/BLE output toggling
- Numpad layout
- System controls (Reset, Bootloader)
```
,-----------------------------------.                ,-----------------------------------.
|Boot | F1 | F2 | F3 | F4 | F5 |    |                | F6 |  7 |  8 |  9 |F10 |Boot|Boot |
|-----+----+----+----+----+----|    |                |----+----+----+----+----+----+-----|
|Rst  |BT0 |BT1 |BT2 |BT3 |BT4 |    |                |    |  4 |  5 |  6 |    |Rst |     |
|-----+----+----+----+----+----|    |                |----+----+----+----+----+----+-----|
|     |USB |BLE |Tog |    |    |    |                |    |  1 |  2 |  3 |    |    |     |
|-----+----+----+----+----+----+----|                |----+----+----+----+----+----+-----|
|     |Clr |    |    |    |    |    |                |    |  0 |  . |  : |  - |    |     |
`-------------------------------+----+----.    .----+----+-------------------------------'
                        |   |    |   |     |    |    |    |    |   |
                        `-------------------'    '-------------------'
```

## Special Features

- **Auto Shift**: Hold any key slightly longer to capitalize it
- **Grave Escape**: Escape key doubles as backtick when used with modifiers
- **OLED Display**: Shows current layer, battery status and paired device
- **Bluetooth**: Support to easily switch between paired devices
- **Rotary Encoders**: Volume control on both halves

## Building and Flashing

1. Clone this repository
2. Follow the [ZMK build guide](https://zmk.dev/docs/development/setup)
3. Build and flash the firmware to your keyboard
