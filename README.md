# 🎵 SanPlayer (SBP Editor) v0.1

![Version](https://img.shields.io/badge/version-0.1-blue.svg)
![Platform](https://img.shields.io/badge/platform-Windows%20(WPF)-lightgrey.svg)
![License](https://img.shields.io/badge/license-Open%20Source-green.svg)

**SanPlayer** is a custom, feature-rich rhythm game player and chart editor written in C# (WPF). It is specifically designed to replicate and map **BeatUp** style charts (similar to Audition / CDIU). 

With a seamless blend of charting tools and a highly authentic gameplay renderer, SanPlayer allows you to create, edit, and play beat-maps with absolute sub-pixel precision.


## This is the v0.1 Pre-Release to find more information about the newest release please also read the ![v0.3 Release](https://github.com/bishpop/SBP-BeatUp-Editor-and-Player/releases/tag/v0.3).
---

## ✨ Key Features

* **Live Split-View Charting:** Edit your charts in real-time while watching the Autoplay render your gameplay and hit-bursts instantly in the split-screen game view!
* **3 Display Modes:** 
  * 🎮 **Game Mode:** Pure gameplay experience with authentic hit-bursts, combos, and UI scaling.
  * 📝 **Editor Mode:** A powerful timeline canvas to place, copy, paste, and mirror notes.
  * 🎛️ **Split View:** Charting timeline and live gameplay side-by-side.
* **Custom Backgrounds:** Easily swap backgrounds directly from the top menu. Just drop your favorite `.png`, `.jpg`, or `.bmp` files into the `assets/background` folder!
* **Authentic Mechanics:** Fully replicates 6-Key + Spacebar gameplay, including the iconic "Finish Move" (Lane 7) ease-out animations and combo gauge systems.
* **Extensive File Support:**
  * Import/Export: `.slk` (SYLK) and `.ssc` (StepMania) chart files.
  * Audio: Import standard `.ogg` music files.
  * Native: Save and load your full workspace using custom `.san` project files.
* **Smooth Rendering:** Anti-flutter sub-pixel rendering for arrows (`a18`-`a98`) ensures butter-smooth animations even during heavy mouse movement.

---

## 🕹️ Controls & Keybinds

### Global Transport (Audio)
| Key | Action |
| :--- | :--- |
| `Space` | **Play** (Only if paused) |
| `P` | **Pause** |
| `K` | **Stop** (Rewinds to start/editor position) |
| `Up / Down` | Seek forward / backward in timeline |

### Gameplay & Charting (Standard Mode)
| Key | Action (Lane) |
| :--- | :--- |
| `1` / `2` / `3` | Left Arrows (Top, Mid, Bottom) |
| `4` / `5` / `6` | Right Arrows (Top, Mid, Bottom) |
| `S` | Spacebar (Normal) |
| `F` | Spacebar (Finish Move) |

### Gameplay & Charting (Numpad Mode `74196305`)
| Key | Action (Lane) |
| :--- | :--- |
| `Num 7` / `4` / `1` | Left Arrows (Top, Mid, Bottom) |
| `Num 9` / `6` / `3` | Right Arrows (Top, Mid, Bottom) |
| `Num 0` | Spacebar (Normal) |
| `Num 5` | Spacebar (Finish Move) |

---

## 📂 Project Structure & Assets

To run SanPlayer correctly, ensure the `assets` folder is placed in the output directory (e.g., `bin/Debug/assets/`).

```text
SanPlayer/
├── Core/               # GameState, BeatEngine and Math logic
├── Rendering/          # GameRenderer (WPF Canvas) & Editor Canvas
├── Services/           # Audio playback logic
├── assets/
│   ├── arrows/         # a18-a98 base arrows, l0-l5 glows, arrow_explode
│   ├── background/     # Drop custom .png/.jpg/.bmp backgrounds here
│   ├── bars/           # spacebar, blackbars, fn (Finish Move)
│   ├── game/           # Gameplay UI (combos, cups, gauges)
│   ├── sounds/         # beat.wav, space_bar.wav
```

---

## 🚀 Installation & Build

1. Clone the repository:
   ```bash
   git clone [https://github.com/bishpop/SBP-BeatUp-Editor-and-Player.git](https://github.com/bishpop/SBP-BeatUp-Editor-and-Player.git)
   ```
2. Open the `.sln` file in **Visual Studio** (2019/2022).
3. Ensure `.NET Framework` (WPF) is installed via the Visual Studio Installer.
4. Restore NuGet packages (if applicable).
5. Press `F5` to build and run the project.

*(Note: If you add new background images to the `assets/background` folder, restart the application to load them into the menu).*

---

## 👨‍💻 About

**SanPlayer - SBP v0.1**  
Free and Open-Source software.  
Made with ❤️ by **Sanya**.
