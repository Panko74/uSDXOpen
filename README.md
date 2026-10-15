# uSDXOpen

## About this fork (Panko74)

This fork modifies **`usdxREDCORNERS_CW.ino`** (firmware version 4.00d) for the uSDX "Red Corners" model. All other `.ino` files are unchanged from the GW8RDI upstream.

**What changed**
- Restored the full CW functionality, including the **Iambic keyer** (Iambic A, Iambic B and Single modes).
- Enabled `KEYER`, `KEY_CLICK` (key-click envelope shaping) and the 700 Hz CW filter.

**What was removed**
- The **CAT interface** is disabled (`CAT`, `CAT_EXT`, `CAT_STREAMING`, `CAT_FAST` and related options are commented out) to free program memory on the ATmega328P.

**Why**
The ATmega328P has limited flash/RAM and CAT uses a large amount of memory, so enabling CW (especially the Iambic keyer) forces a trade-off. This build favours CW.

**Flashing**
- Use only `usdxREDCORNERS_CW.ino` for the Red Corners model.
- **Before flashing**, edit the `MY_CALLSIGN` (currently a `XXXXX` placeholder) and `MY_NAME` (currently `NAME`) fields in `usdxREDCORNERS_CW.ino` to your own callsign and name.
- Upload via **Arduino as ISP** (menu: *Sketch → Upload Using Programmer*), not via serial bootloader.

## Credits

This project is based on [GW8RDI/uSDXOpen](https://github.com/GW8RDI/uSDXOpen), which in turn is branched from [threeme3/usdx](https://github.com/threeme3/usdx).

Credits: Guido PE1NNZ, Dan Tayloe N7VE, DL2MAN, Rob GW8RDI and many others.

## License

MIT — see the [LICENSE](LICENSE) file. Use of this firmware is at your own risk; no warranty is provided.
