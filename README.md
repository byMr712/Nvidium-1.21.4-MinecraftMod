> **Language:** Русский · [English](README.en.md)

# Nvidium (Minecraft 1.21.4 Fabric)

![Java 21](https://img.shields.io/badge/Java-21-blue.svg)
![Minecraft](https://img.shields.io/badge/Minecraft-1.21.4-blue.svg)
![Fabric](https://img.shields.io/badge/Loader-Fabric-blue.svg)
![ModMenu](https://img.shields.io/badge/ModMenu-Supported-blue.svg)
![License](https://img.shields.io/badge/License-LGPL_3.0-blue.svg)

Сборка и оптимизация движка рендеринга **Nvidium** для **Minecraft 1.21.4 (Fabric)**.

Источник: [GitHub: MCRcortex/nvidium](https://github.com/MCRcortex/nvidium).

---

## О моде

**Nvidium** — альтернативный высокопроизводительный движок рендеринга для **Sodium**, использующий аппаратные возможности видеокарт NVIDIA (архитектура Turing и новее) для отрисовки огромных дистанций мира при сверхвысоком FPS.

---

## Галерея

| Обзор рендеринга | Дальняя прорисовка |
|:---:|:---:|
| ![Обзор рендеринга](images/nvidium_overview.webp) | ![Дальняя прорисовка](images/nvidium_far_rendering.webp) |
| ![Рендеринг ландшафта](images/nvidium_terrain_rendering.webp) | ![Hermitcraft мир](images/nvidium_hermitcraft.webp) |

---

## Возможности

- Аппаратный mesh shading рендеринг геометрии чанков на видеокартах NVIDIA.
- Экстремально высокая дальность прорисовки (до 64+ чанков) с плавным фреймрейтом.
- Полная интеграция с графическими настройками Sodium.
- Поддержка полупрозрачных блоков и многослойной сортировки.

---

## Что изменено в порте для 1.21.4 (byMr712)

- Полная сборка и адаптация под **Minecraft 1.21.4** (Fabric Loader, Java 21) на официальных маппингах Mojang с Parchment.
- **Исправлен полупрозрачный рендер**: сортировка кадров translucency, устранена отрисовка проходов при телепортации, исправлен подсчёт квадов сортировки.
- **Исправлена сортировка секций**: устранены целочисленные переполнения идентификаторов секций при инициализации `RenderSection`.
- **Исправлен рендер лучей маяков (beacons)**.
- UV перенесены во фрагментный шейдер через vertex pulling, оптимизирована реализация тумана.

---

## Требования и установка

1. Требования:
   - [Sodium](https://modrinth.com/mod/sodium) 0.6.13
   - Видеокарта NVIDIA GeForce GTX 1600 серии или новее (архитектура Turing, Ampere, Ada Lovelace, Blackwell)
2. Скачайте `.jar` файл и поместите в папку `mods`.
3. Запустите игру.

---

## Сборка

1. Требуется Java 21 и Fabric Loader для Minecraft 1.21.4.
2. Для сборки выполните:
   ```bash
   ./gradlew build
   ```
3. Собранный файл находится в `build/libs/nvidium-0.4.1-beta9-1.21.4.jar`.

---

## Авторы и лицензия

- Оригинальный автор: [MCRcortex](https://github.com/MCRcortex) ([nvidium](https://github.com/MCRcortex/nvidium)).
- Сборка и адаптация для 1.21.4: [Mr712](https://github.com/byMr712).
- Распространяется под лицензией [LGPL 3.0](LICENSE.txt).