# SOMA Smart Shades documentation

Unofficial reference for making custom bridges or integrations.

## Commands

- [Older V2 model](V2.md)
- [New V3 model](V3.md)

## Finding devices

Manufacturer data company id for devices is `0x0370` or 880 in decimal (Wazombi Labs OÜ). V2 devices have "S" as name, V3 devices do not have a name.

### Manufacturer advertising data bytes array

- Byte 0 - version
    - V3 devices have `0x10` or larger

#### v2 devices

- Byte 1 - ?
- Byte 2 - current position
- Byte 3 - target position
- Bytes 4+ - ASCII device name, ends with `30 20 [20...]`

#### v3 devices

- Byte 1 - current position
- Byte 2 - battery level

Example V3 device 100% open and battery at 50%: `10 00 32`.

## Useful tools

For debugging or learning different command responses you can use

- Android app [nRF Connect for Mobile](https://play.google.com/store/apps/details?id=no.nordicsemi.android.mcp&hl=en)

Other helpful software

- [Apktool](https://apktool.org/)
- [pyxamstore](https://github.com/jakev/pyxamstore/)
- [dotPeek](https://www.jetbrains.com/decompiler/)