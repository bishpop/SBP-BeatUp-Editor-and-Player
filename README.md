<div align="center">
<img src="https://capsule-render.vercel.app/api?type=waving&color=1A1825&height=200&section=header&text=SanPlayer&fontSize=70&fontColor=E0AF68&animation=fadeIn&fontAlignY=35&desc=BeatUp%20Chart%20Editor&descAlignY=68&descSize=18" />

![Platform](https://img.shields.io/badge/Platform-Windows-blue?style=for-the-badge)
![Framework](https://img.shields.io/badge/Framework-WPF%20%2F%20.NET-512BD4?style=for-the-badge)
![License](https://img.shields.io/badge/License-Open%20Source-green?style=for-the-badge)
![Version](https://img.shields.io/badge/Version-v0.3-orange?style=for-the-badge)

<br>

**San BeatUp Player** (SBP) is a modern, open-source rhythm game engine and advanced chart editor, explicitly built for **6-Key / BeatUp** style mechanics (Numpad 741 / 963 + Space + Finish). 

Whether you want to play existing charts, create your own from scratch, or convert between different game formats, SanPlayer provides a seamless, high-performance solution with a beautifully designed Glassmorphism UI.

<br>

![San BeatUp Player Preview](https://raw.githubusercontent.com/bishpop/bishpop/main/assets/san_player.png)

</div>

---

## ✨ Features at a Glance

* 🎮 **Dynamic Dual View:** Seamlessly switch between **Game Mode** (to play), **Editor Mode** (DAW-style tracker), or **Split View** to chart and playtest simultaneously.
* 🚀 **High-Performance Engine:** Powered by a 1000Hz custom game loop with dynamic WPF rendering. It runs at a smooth 60 FPS in the editor (to save CPU) and automatically unlocks uncapped FPS during playback.
* 📝 **Advanced Charting Tools:** 
  * Real-time Numpad-charting or mouse placement.
  * Box-selection, Copy & Paste.
  * Horizontal Mirroring (Left <-> Right) & Vertical Mirroring.
  * Smart Randomization tools.
* 🔄 **Bulletproof Undo & Redo:** A 100-step history cache allows you to undo (`Ctrl+Z`) and redo (`Ctrl+Y`) any modification instantly.
* 📊 **Live Stats Analysis:** A beautiful floating Glassmorphism window provides real-time chart analysis (Density, Rapid Ticks, L/R Patterns, Stair Patterns, and a calculated Difficulty Level).
* 🛡️ **Auto-Save & Crash Handler:** Never lose a chart again. The app silently saves your project every 2 minutes. If the worst happens, a custom crash handler catches the error and keeps your data safe.
* 🎵 **Built-in Auto-Updater:** The app checks the GitHub API on startup and notifies you automatically when a new version is available.

---

## 🛠️ Supported File Formats

SanPlayer acts as a bridge between different rhythm game engines:

* **`.san` (SanPlayer Project):** The native workspace format. It saves your audio path, BPM, offset, chart data, and your **Creditor Watermark** in a single compressed file.
* **`.slk` (SYLK Format):** Import and Export charts for standard BeatUp engines. (Automatically embeds your Creditor name as a watermark!).
* **`.ssc` (StepMania Format):** Import and export `dance-bu` style StepMania charts. Audio files are automatically copied, and offsets/BPMs are formatted with high precision.
* **`.ogg` (Audio):** The universally supported audio format for playback.

---

## 🚀 Getting Started (Workflow Guide)

### 1. Installation
1. Download the latest release from the [Releases page](https://github.com/bishpop/SBP-BeatUp-Editor-and-Player/releases).
2. Unzip the folder. Make sure the `assets` folder is kept in the same directory as the `AuditionPlayer.exe`.
3. Launch the application.

### 2. Setting up a new Chart
1. Click **File -> Import .ogg Audio** and select your song.
2. Enter the **BPM** of the song when prompted.
3. On the top menu, enter your **Creditor** name (this will be used as a watermark when exporting).
4. *(Optional)* Adjust the **Audio Offset** (default is `0.7` sec).

### 3. The Charting Process
1. Switch to **Editor Mode** or **Split View** via the top menu.
2. Choose your **Snap Settings** (Right-Click the grid):
   * **Red Line:** 1/4 Beat
   * **Blue Line:** 1/8 Beat
   * **Yellow Line:** 1/16 Beat
3. Enable **Autoplay / Numpad Charting** if you want to record notes live using your keyboard while the music plays.
4. Hit **Play** (`Space`) and start mapping!

### 4. Saving & Exporting
* **Always save your progress** via `File -> Save Project (.san)`. This allows you to close the app and resume perfectly later.
* Once your chart is finished, use `File -> Export .ssc` (for StepMania) or `File -> Export .slk`.

---

## ⌨️ Controls & Keybinds

### Gameplay & Live Numpad Charting
| Action | Keybind |
| :--- | :--- |
| **Left Lanes (7, 4, 1)** | `Numpad 7`, `Numpad 4`, `Numpad 1` (or `Home`, `Left`, `End`) |
| **Right Lanes (9, 6, 3)** | `Numpad 9`, `Numpad 6`, `Numpad 3` (or `PgUp`, `Right`, `PgDn`) |
| **Spacebar (SP)** | `Space`, `Numpad 0`, or `Insert` |
| **Finish (F)** | `Numpad 5`, `Enter`, or `Clear` |

### Chart Editor Shortcuts
| Shortcut | Action |
| :--- | :--- |
| `Left Click` | Place or Delete a note at the cursor |
| `Ctrl` + `Left Click (Drag)` | Box Selection (select multiple notes) |
| `Ctrl` + `Left Click` | Select or Deselect an individual note |
| `Right Click` | Open Context Menu (Settings, Snapping, Randomize) |
| `Ctrl` + `Scroll Wheel` | Zoom in / Zoom out of the timeline |
| `Scroll Wheel` | Scroll up / down the timeline |
| `Up` / `Down` Arrow | Seek timeline forward/backward by current Snap step |
| `Space` / `P` | Play / Pause |
| `K` | Stop (Returns to Beat 0) |

### Advanced Editor Hotkeys
| Shortcut | Action |
| :--- | :--- |
| `Ctrl` + `Z` | Undo last action |
| `Ctrl` + `Y` | Redo last action |
| `Ctrl` + `C` | Copy selected notes |
| `Ctrl` + `V` | Paste copied notes at the current playhead |
| `Ctrl` + `A` | Select all notes in the chart |
| `Delete` | Delete all selected notes |
| `Ctrl` + `W` | Mirror horizontally (Left <-> Right) |
| `Ctrl` + `E` | Mirror vertically (7<->4, 9<->6, etc.) |

---

## 🔧 Building from Source

If you want to modify or compile SanPlayer yourself:
1. Clone the repository:
   ```bash
   git clone https://github.com/bishpop/SBP-BeatUp-Editor-and-Player.git
   ```
2. Open the solution `(.sln)` in **Visual Studio 2022**.
3. Ensure you have the .NET desktop development (WPF) workload installed.
4. Build the solution (Target: x86)

---

### 👨‍💻About & Credits
Developed and mainted by [Sabya (bishpop)](https://github.com/bishpop).
Built to solve real workflow problems for charting nerds and rhythm game enthusiasts playing Audition.

If you find a bug or have a feature request, feel free to open an **Issue** or submit a **Pull Request**.

<div align="center">
<i>© 2026 Sanya — All rights reserved.</i>
</div>
