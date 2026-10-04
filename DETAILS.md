# inder-dinamic-fpga

🇬🇧 English (below) · [🇪🇸 Español](#español)

FPGA recreation of the **Inder / Dinamic** TMS34010 arcade board (1990-92), built on the **JTFRAME**
framework (GPLv3). MiSTer target.

> ℹ️ Independent project — **NOT** an official jotego core. Built on his GPLv3 JTFRAME framework.

## Games

One `.rbf` runs all three games; each `.mra` selects the game (and its video mode).

| Game | Year | Video | Status |
|---|---|---|---|
| Hammer Boy | 1990 | 4 bpp, 324×200 | playable |
| Mega Phoenix | 1991 | 8 bpp, 338×246 | playable |
| YoYo Spell (prototype) | 1992 | 8 bpp, 338×288 | playable |
| After the War | 1991 | 4 bpp | **coming soon** (waiting for the ROM to be released) |

Hardware: **MC68000** main CPU + **TMS34010** graphics processor (512 KB VRAM, Bt478-style RAMDAC) +
**PIC16C54** (inputs / DIP switches) + Inder sound board (**Z80** + CTC + DACs).

**Status: W.I.P.** — all three games boot and are playable on MiSTer over HDMI. The optional 15 kHz CRT mode
has not been tested on hardware yet.

## Install

Copy the contents of [`_Arcade/`](_Arcade/) to the `_Arcade/` folder of your MiSTer SD card
(`.rbf` into `_Arcade/cores/`).

## ROMs

**Not included** (copyrighted material). Everyone provides the original ROMs of their own board for each
game. The `.mra` describes how to assemble them (MAME set names: `hamboy`, `megaphx`, `yoyospel`); every
ROM is loaded at runtime, so the `.rbf` carries no copyrighted data.

## Credits

- **JTFRAME** — the GPLv3 framework this core is built on
- **TMS34010_sv** (Kevin Coleman, MIT) — TMS34010 core, adapted for this board
- **fx68k** (Jorge Cwik, GPLv3) — MC68000 core
- **T80** (Daniel Wallner) — Z80 core
- **MiSTer CRT Adjust** (rmonic79, GPLv3) — CRT geometry adjustment
- **MAME** — hardware reference (`misc/megaphx.cpp`, `shared/inder_vid.cpp`, `shared/inder_sb.cpp`)

## Acknowledgements

- To **Sorgelig** and the whole **MiSTer FPGA** project and community.
- To the **MAME community**, for the preservation and reverse-engineering work without which this core
  would not be possible.
- And to **Anthropic**, for **Claude**.

## License

**GPLv3** (see [`LICENSE`](LICENSE)) — required by the JTFRAME dependency.

---

## Español

🇪🇸 Español · [🇬🇧 English ↑](#inder-dinamic-fpga)

Recreación en FPGA de la placa arcade con TMS34010 de **Inder / Dinamic** (1990-92), construida sobre el
framework **JTFRAME** (GPLv3). Objetivo MiSTer.

> ℹ️ Proyecto independiente — **NO** es un core oficial de jotego. Construido sobre su framework
> JTFRAME (GPLv3).

## Juegos

Un solo `.rbf` ejecuta los tres juegos; cada `.mra` elige el juego (y su modo de vídeo).

| Juego | Año | Vídeo | Estado |
|---|---|---|---|
| Hammer Boy | 1990 | 4 bpp, 324×200 | jugable |
| Mega Phoenix | 1991 | 8 bpp, 338×246 | jugable |
| YoYo Spell (prototipo) | 1992 | 8 bpp, 338×288 | jugable |
| After the War | 1991 | 4 bpp | **próximamente** (a la espera de que se libere la ROM) |

Hardware: CPU principal **MC68000** + procesador gráfico **TMS34010** (512 KB de VRAM, RAMDAC tipo Bt478) +
**PIC16C54** (entradas / DIP switches) + placa de sonido de Inder (**Z80** + CTC + DACs).

**Estado: W.I.P.** — los tres juegos arrancan y son jugables en MiSTer por HDMI. El modo opcional CRT de
15 kHz aún no se ha probado en hardware.

## Instalación

Copiar el contenido de [`_Arcade/`](_Arcade/) a la carpeta `_Arcade/` de la SD de la MiSTer
(el `.rbf` en `_Arcade/cores/`).

## ROMs

**No se incluyen** (material con copyright). Cada cual aporta las ROMs originales de su propia placa
para cada juego. El `.mra` describe cómo ensamblarlas (sets de MAME: `hamboy`, `megaphx`, `yoyospel`);
cada ROM se carga en runtime, así que el `.rbf` no lleva ningún dato con copyright.

## Créditos

- **JTFRAME** — el framework GPLv3 sobre el que se construye este core
- **TMS34010_sv** (Kevin Coleman, MIT) — núcleo TMS34010, adaptado a esta placa
- **fx68k** (Jorge Cwik, GPLv3) — núcleo MC68000
- **T80** (Daniel Wallner) — núcleo Z80
- **MiSTer CRT Adjust** (rmonic79, GPLv3) — ajuste de geometría CRT
- **MAME** — referencia de hardware (`misc/megaphx.cpp`, `shared/inder_vid.cpp`, `shared/inder_sb.cpp`)

## Agradecimientos

- A **Sorgelig** y todo el proyecto y comunidad **MiSTer FPGA**.
- A la **comunidad MAME**, por el trabajo de preservación e ingeniería inversa sin el cual este core no
  sería posible.
- Y a **Anthropic**, por **Claude**.

## Licencia

**GPLv3** (ver [`LICENSE`](LICENSE)) — obligado por la dependencia JTFRAME.
