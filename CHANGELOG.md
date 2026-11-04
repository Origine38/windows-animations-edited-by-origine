# Changelog

## 1.6.21 (Nov 4, 2026)

**New additions compared with the official mod by ReDrag**

- **Genie targeting:** Fixed windows that minimized toward the far-left edge of the taskbar. Dynamic MSAA targeting now follows the appropriate application button.
- **File Explorer acrylic:** Improved transparency-aware Genie captures and reduced traces of the previous application or desktop background, including maximized Explorer windows.
- **Explorer restoration:** Added a fast **75 ms content handoff**, avoiding the problematic full-length Genie restore transition while preserving Genie minimization.
- **Broader closing compatibility:** Extended close detection to all third-party desktop programs tested on the original setup and many Windows utilities, including Explorer, Task Manager, Control Panel, Paint, Notepad, Registry Editor, Disk Cleanup, and Optimize Drives.
- **Confirmation handling:** Preserved normal save/cancel confirmation dialogs and avoided forcing application destruction to trigger an effect.
- **Hosted modern Windows apps:** Added close effects for supported Settings, Calculator, Microsoft Store and other compatible `ApplicationFrameHost.exe` windows.
- **Compatibility:** Kept the original `mmc.exe` exclusion, preserved the original animation effects, GPU/CPU routing and the existing Genie/MSAA engine.
- **Documentation:** Restored ReDrag's English gallery and credits, with four additional demonstration GIF slots.

### Development milestones

- **1.6.4–1.6.7:** Dynamic MSAA taskbar-button targeting and Genie alignment improvements.
- **1.6.8–1.6.9:** Explorer transparency, maximized-window handling, previous-background ghosting and the 75 ms restoration handoff.
- **1.6.11–1.6.14:** Rebased on the author's newer code, expanded close compatibility beyond File Explorer, and introduced diagnostic tooling.
- **1.6.15–1.6.19:** Investigated hosted apps and enabled previously unavailable close animations in many Windows applications.
- **1.6.20–1.6.21:** Compared handoff methods; retained the best tested v1.6.21 configuration despite a small remaining flash in some hosted apps.

### 🔴 Current known issues

- **Brief visual jump:** Settings, Microsoft Store, Calculator, and some similar Windows applications may briefly flicker before their closing animation starts.
- **Explorer restore:** The File Explorer minimize animation is preserved, but the full Genie restore is intentionally replaced by a fast **75 ms restoration handoff** to avoid unresolved acrylic visual artifacts.
- **MMC applications:** Services, Task Scheduler, Event Viewer and other `mmc.exe` consoles have **no custom minimize, restore, or close animation** because the original mod excludes MMC for stability.
- **Application-specific bugs:** Some untested applications may still behave unexpectedly. Add their executable to Windhawk's exclusion list if necessary.

### 🔵 Essential compatibility setting

**Enable “Animate windows hidden to the tray”.** Without this setting, many otherwise supported applications and Windows utilities will not animate when closed.

---

Original developer: **[ReDrag](https://github.com/redrag2105)** · Edited edition: **[Origine38](https://github.com/Origine38)**.
