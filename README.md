# Holani-retro
[Libretro](https://www.libretro.com/) implementation of [Holani](https://github.com/LLeny/holani), a cycle-stepped Atari Lynx emulator.

#### Supported libretro features
* Save/load states
* [RetroArch cheats](https://docs.libretro.com/guides/cheat-codes/)

## Build
You will need [Rust and its package manager Cargo](https://www.rust-lang.org/). 

```
git clone https://github.com/LLeny/holani-retro.git
```

Build the libretro core with:

```
cargo build --release
```

The core will be in the `target/release/` directory.

## Run
To use the core you will need a [libretro frontend](https://www.libretro.com/index.php/powered-by-libretro/).

[RetroArch](https://www.retroarch.com/) is the official frontend.
With retroarch you can use the previsouly built core from the command line with:

#### Linux
```
retroarch --libretro target/release/libholani.so <cartridge.lnx>
```

#### Windows
[Microsoft Visual C++ 2015 Redistributable](https://www.microsoft.com/en-us/download/details.aspx?id=52685) is required.

## Embedded ROM
Holani uses the [Free Lynx Boot Rom](http://lynxdev.atari.org). If you encouter issues booting your cartridge try copying the original Lynx firmware *lynxboot.img* into Retroarch's "system" folder.
