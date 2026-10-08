# RX 580 SPI vBIOS Dumps

This repository contains full SPI flash (vBIOS) dumps from **XFX Radeon RX 580** graphics cards, dumped by me using the [AMDVBFlash](https://github.com/aryan-nikzad/amdvbflash) utility.

It also contains a **Gigabyte RX 580** dump. The Gigabyte ROM has also been tested as a usable ROM for an XFX RX 580 in the context of the RX 580 vBIOS loader project.

## What these files are

These are hardware SPI-flash dumps made from physical RX 580 cards. They are provided primarily as reference and compatibility candidates for low-level recovery and testing, including use with:

- [RX 580 vBIOS Loader GUI](https://github.com/aryan-nikzad/rx580_vbios_loader_GUI)
- Other RX 580 / Polaris recovery and initialization work

A full SPI dump may contain data outside the normal visible vBIOS image. Do not assume that every dump is universally compatible with every RX 580.

Before using a ROM on a different card, verify the GPU model, board, VRAM size, memory configuration, subsystem information, and other hardware details.

## Using these ROMs with RX 580 vBIOS Loader

The [RX 580 vBIOS Loader GUI](https://github.com/aryan-nikzad/rx580_vbios_loader_GUI) can use the ROMs in this repository.

You can either download individual ROM files or download the repository's **`vbioses/`** folder and place it directly in the project root of the loader, next to `install_linux.sh`.

For example:

```text
rx580_vbios_loader_GUI/
├── vbioses/
│   ├── your_xfx_dump.rom
│   ├── your_gigabyte_dump.rom
│   └── ...
├── install_linux.sh
└── ...
```

Then build/install the loader as described in the loader repository's README.

## Important

**Keep your own original SPI dump whenever possible.** Your own card's dump is the best starting point for recovery.

A ROM that works on one RX 580 is not automatically safe or compatible with another RX 580. Low-level GPU initialization can hang or damage the card's configuration if an incompatible firmware image is used.

These files are provided **as-is**. Use them at your own risk.

## Source of the dumps

The dumps were made by me from physical RX 580 cards using:

- AMDVBFlash: https://github.com/aryan-nikzad/amdvbflash

No vendor firmware was downloaded and re-uploaded from an online ROM database as the source of these particular dumps.

## Copyright / licensing notice

These files are **vendor firmware / vBIOS dumps**. I am not claiming ownership of the original firmware contained in these files, and this repository does **not** grant a new copyright license to AMD, XFX, Gigabyte, or any other rights holder's firmware.

The repository's `LICENSE` file is therefore a **repository permission notice**, not a license for the underlying vendor firmware.

The files are currently made available for users who need them for legitimate testing, recovery, research, and compatibility purposes.

If the copyright owner or other relevant rights holder requests that this repository or any of its files be removed, I will remove the requested repository/files.

## Disclaimer

I make no guarantee that any dump is suitable for a particular GPU. Check the hardware identifiers and compatibility before using a ROM for initialization or flashing.

**Do not flash these files to a GPU unless you understand the risks and have a recovery method available.**
