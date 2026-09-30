> **Language:** [Русский](README.md) · English

# Nvidium (Minecraft 1.21.4 Fabric)

![Java 21](https://img.shields.io/badge/Java-21-blue.svg)
![Minecraft](https://img.shields.io/badge/Minecraft-1.21.4-blue.svg)
![Fabric](https://img.shields.io/badge/Loader-Fabric-blue.svg)
![ModMenu](https://img.shields.io/badge/ModMenu-Supported-blue.svg)
![License](https://img.shields.io/badge/License-LGPL_3.0-blue.svg)

Build and optimization of the **Nvidium** rendering engine for **Minecraft 1.21.4 (Fabric)**.

Source: [GitHub: MCRcortex/nvidium](https://github.com/MCRcortex/nvidium).

---

## About

**Nvidium** is a high-performance alternative rendering engine for **Sodium** that leverages hardware capabilities of modern NVIDIA graphics cards (Turing architecture and newer) to render massive world view distances at exceptional framerates.

---

## Gallery

| Overview | Far Distance Rendering |
|:---:|:---:|
| ![Overview](images/nvidium_overview.webp) | ![Far Distance Rendering](images/nvidium_far_rendering.webp) |
| ![Terrain Rendering](images/nvidium_terrain_rendering.webp) | ![Hermitcraft World](images/nvidium_hermitcraft.webp) |

---

## Features

- Hardware mesh shading chunk geometry pipeline on NVIDIA GPUs.
- Extreme render distances (up to 64+ chunks) with fluid framerates.
- Complete integration with Sodium's video settings menu.
- Full translucency and multi-pass sorting support.

---

## Changes in 1.21.4 Port (byMr712)

- Complete build and adaptation for **Minecraft 1.21.4** (Fabric Loader, Java 21) using official Mojang mappings with Parchment.
- **Fixed translucency rendering**: translucency frame sorting, fixed pass drawing during teleports, corrected sorting quad count.
- **Fixed section sorting**: eliminated integer overflow issues on section IDs during `RenderSection` initialization.
- **Fixed beacon beam rendering**.
- Moved UV coordinates to fragment shader via vertex pulling, optimized fog implementation.

---

## Requirements & Installation

1. Requirements:
   - [Sodium](https://modrinth.com/mod/sodium) 0.6.13
   - NVIDIA GeForce GTX 1600 series GPU or newer (Turing, Ampere, Ada Lovelace, Blackwell)
2. Download `.jar` file and place into your `mods` folder.
3. Launch the game.

---

## Building

1. Requires Java 21 and Fabric Loader for Minecraft 1.21.4.
2. To build the project, run:
   ```bash
   ./gradlew build
   ```
3. The built jar file will be located at `build/libs/nvidium-0.4.1-beta9-1.21.4.jar`.

---

## Credits & License

- Original Author: [MCRcortex](https://github.com/MCRcortex) ([nvidium](https://github.com/MCRcortex/nvidium)).
- Build and adaptation for 1.21.4 by: [Mr712](https://github.com/byMr712).
- Distributed under the [LGPL 3.0 License](LICENSE.txt).