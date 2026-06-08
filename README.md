# Spl1t — ZMK config

Split 6×4 + 4 thumb keys per half, Seeed XIAO nRF52840, by sod1pop.

## Build

GitHub Actions produces `spl1t_dongle`, `spl1t_left`, and `spl1t_right` UF2 files. Flash each controller via double-tap RST -> drag UF2.

- **Board:** `xiao_ble//zmk`
- **Shields:** `spl1t_dongle`, `spl1t_left`, `spl1t_right`
- **ZMK Studio:** enabled on dongle; locking disabled

## Layout

44 keys (positions 0–43). Matrix transform maps 6×4 per half with thumbs on row 3 (columns 2–5 left, 6–9 right in global matrix).

## Flash

1. Download UF2 artifacts from Actions (or build locally with `west build`).
2. Flash `settings_reset` to all three XIAOs before first dongle pairing.
3. Double-tap **RST** on each XIAO -> drag the matching UF2.
4. Plug in the dongle; power both halves. The dongle is BLE central and the left/right halves are peripherals.
5. Connect the host to **Spl1t** over USB or BLE from the dongle.
