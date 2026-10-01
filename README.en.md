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

## Changes in Build (byMr712)

- **Fixed OpenGL state leaks on reconnect**: resolved black entities, black REI GUI items, and player model translucency bugs on server reconnect or world reload (added proper cleanup and reset of texture slots, samplers, UBO ranges, and shader programs).
- **Blaze3D cache synchronization**: replaced direct `glBindTextureUnit` calls with `GlStateManager` to prevent texture slot desynchronization with the game engine.
- **Pipeline state cleanup**: ensured all active shader programs (`glUseProgram(0)`) and buffers are cleanly unbound after rendering passes and on pipeline destruction (`RenderPipeline.delete()`).
- **Build script**: added `build.bat` quick build script.

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
3. The built jar file will be located at `build/libs/Nvidium-1.21.4-byMr712.jar`.

---

## Credits & License

- Original Author: [MCRcortex](https://github.com/MCRcortex) ([nvidium](https://github.com/MCRcortex/nvidium)).
- Port to 1.21.4: [drouarb](https://github.com/drouarb) ([Shays-Forks/nvidium](https://github.com/Shays-Forks/nvidium/tree/1.21.4)).
- Fixes and build: [Mr712](https://github.com/byMr712).
- Distributed under the [LGPL 3.0 License](LICENSE.txt).