# QMK/VIA Firmware (for BlackPill)

There is a separate binary for standard layout and ortholinear.  For VIA, you will need to sideload the associated `*via.json` file until it's officially supported.

https://github.com/dcpedit/qmk_firmware/tree/modmmm/keyboards/dcpedit/modmmm

# Vial Firmware (for BlackPill)

https://get.vial.today

The bin file in this directory was compiled for the SMT32F114 Blackpill.  You can view the sourcecode in my fork:

https://github.com/dcpedit/vial-qmk-dev/tree/vial/keyboards/dcpedit/modmmm

# ZMK Firmware (for PillBug)

You can view the sourcecode in my fork:

https://github.com/dcpedit/zmk/tree/dcpedit/app/boards/shields/modmmm

Build command

```
west build -b pillbug -- -DSHIELD=modmmm
```
