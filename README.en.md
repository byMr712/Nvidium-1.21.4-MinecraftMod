> **Language:** [Русский](README.md) · English

# Nvidium (Minecraft 1.21.4 Fabric Port)

Port and update of the **Nvidium** mod for **Minecraft 1.21.4 (Fabric)** by **byMr712**.

Source: [GitHub: MCRcortex/nvidium](https://github.com/MCRcortex/nvidium).

---

## About the Mod

**Nvidium** is an alternate rendering engine for **Sodium** that uses NVIDIA hardware features (Turing architecture and newer) to render large amounts of world geometry at very high framerates.

### Requirements:
- Minecraft 1.21.4 (Fabric Loader)
- Sodium 0.6.13
- NVIDIA GeForce GTX 1600 series or newer GPU (Turing+ architecture)

---

## Changes in 1.21.4 Port (byMr712)

- Full build and adaptation for Minecraft 1.21.4 (Fabric Loader, Java 21) on official Mojang mappings with Parchment.
- Fixed translucent rendering: translucency pass sorting, fixed pass rendering during teleportation, fixed sorting quad counts.
- Fixed section sorting and integer overflow of section IDs during RenderSection initialization.
- Fixed beacon rendering.
- UVs moved to the fragment shader via vertex pulling, alternative fog implementation.
- Version: **0.4.1-beta9-1.21.4**.

---

## Build & Installation

1. Requires **Java 21** and **Fabric Loader** for Minecraft 1.21.4.
2. To build from source, run:
   ```bash
   ./gradlew build
   ```
3. The resulting mod jar is located at `build/libs/nvidium-0.4.1-beta9-1.21.4.jar`.

---

## License

Licensed under the **LGPL-3.0**. See the [LICENSE.txt](LICENSE.txt) file for details.