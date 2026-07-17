# 🛡️ ROOMGUARD-X

**X SERIES | PROJECT 1**

*"Detection is the First Line of Defense."*

A real-time person detection and alert system built with Python, YOLOv8, and OpenCV. RoomGuard-X watches your webcam feed, detects when someone enters your room, and instantly alerts you through multiple channels — all wrapped in a professional, custom-branded desktop app.

---

##  Features

- **Real-time person detection** using YOLOv8, accurate in any pose (standing, walking, waving, sitting)
- **Professional HUD interface** — live stats sidebar, targeting-bracket reticles, session uptime, FPS counter, live snapshot preview
- **Dual-theme support** — toggle between dark and light mode on the fly
- **Windowed & fullscreen modes**
- **Multi-channel real-time alerts**:
  - Native Windows toast notifications with photo attached
  - Discord webhook push notifications (with photo + timestamp) straight to your phone
  - Loud audible alarm on detection
- **Continuous recording** — auto-saves timestamped snapshots the entire time someone is in frame
- **Detection logging** — full history saved to a local log file
- **System tray integration** — runs quietly in the background with a custom tray icon and right-click menu
- **Background/headless mode** — run with no visible window, controlled entirely from the tray
- **Branded splash screens** — animated intro/outro with logo fade, scanning line, and loading bar
- **Packaged as a standalone Windows app** (.exe) via PyInstaller

---

## 🖥️ Screenshots

| Launcher : 
<img width="484" height="484" alt="Screenshot 2026-07-17 173624" src="https://github.com/user-attachments/assets/6a7ef582-453c-44a9-824d-9f5558ea7bf5" />

| Detector HUD : <img width="1578" height="873" alt="Screenshot 2026-07-17 173736" src="https://github.com/user-attachments/assets/9f6ff8bb-28c6-439b-b1bf-6fcdbbaf8a62" />

| Splash Screen : <img width="626" height="744" alt="Screenshot 2026-07-17 173751" src="https://github.com/user-attachments/assets/59a33462-47a2-4457-aebf-b4b91057e2fa" />

---

##  Tech Stack

- **Python 3.14**
- **YOLOv8** (via `ultralytics`) — real-time object/person detection
- **OpenCV** — video capture, HUD rendering, image processing
- **Tkinter** — launcher GUI
- **pystray** — system tray integration
- **winotify** — native Windows toast notifications
- **Discord Webhooks** — real-time mobile push alerts
- **PyInstaller** — packaging into a standalone Windows executable

---

## 🚀 Getting Started

### Prerequisites
- Python 3.10+ installed
- A webcam

### Installation

```bash
git clone https://github.com/YOUR-USERNAME/RoomGuard-X.git
cd RoomGuard-X
pip install opencv-python requests ultralytics winotify pystray pillow numpy
```

### Configuration

Open `ROOMGUARD-X.py` and set your own Discord webhook URL (for phone notifications):

```python
DISCORD_WEBHOOK_URL = "your-discord-webhook-url-here"
```

> Don't have one? [Create a Discord webhook](https://support.discord.com/hc/en-us/articles/228383668-Intro-to-Webhooks) in a private server channel — takes under 2 minutes.

### Run it

```bash
python ROOMGUARD-X.py
```

The launcher window will open — click **Start** to begin monitoring.

---

## ⌨️ Controls (while the detector window is open)

| Key | Action |
|---|---|
| `Q` | Quit |
| `F` | Toggle fullscreen |
| `T` | Toggle dark/light theme |

---

## 📦 Building a Standalone .exe

```bash
pip install pyinstaller
pyinstaller --onedir --windowed --icon=roomguardx_logo.png --add-data "roomguardx_logo.png;." --name "ROOMGUARD-X" ROOMGUARD-X.py
```

Your app will be in `dist/ROOMGUARD-X/`. Keep the `.exe` and the `_internal` folder together when moving/sharing it.

---


---

## 📄 License

Personal project — feel free to fork and adapt for your own use.

---

<p align="center"><b>Made by Mr Reix</b></p>
