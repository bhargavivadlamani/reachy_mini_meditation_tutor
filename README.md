---
title: Reachy Mini Meditation Tutor
emoji: 👋
colorFrom: red
colorTo: blue
sdk: static
pinned: false
short_description: Write your description here
tags:
 - reachy_mini
 - reachy_mini_python_app
---

# Reachy Mini Meditation Tutor

Timed breathing sessions for Reachy Mini (works in simulation or on a real robot).

- Inhale: 5s
- Exhale: 8s
- Sessions: 3 / 5 / 10 minutes
- Optional breathing sound (synthesized, toggle in UI)

## Quickstart (simulation)

### 1) Create a venv and install Reachy Mini + MuJoCo

```bash
mkdir -p ~/reachy_mini_resources
python3 -m venv ~/reachy_mini_resources/.venv
source ~/reachy_mini_resources/.venv/bin/activate
python -m pip install -U pip
python -m pip install "reachy-mini[mujoco]"
```

### 2) Clone this repo

```bash
cd ~/Desktop
git clone https://github.com/suhaasteja/reachy_mini_meditation_tutor.git
```

### 3) Install the app into the same venv (so it shows up in the dashboard)

```bash
source ~/reachy_mini_resources/.venv/bin/activate
pip install -e ~/Desktop/reachy_mini_meditation_tutor
```

### 4) Run the simulation daemon (macOS)

```bash
source ~/reachy_mini_resources/.venv/bin/activate
mjpython -m reachy_mini.daemon.app.main --sim
```

Open:
- http://localhost:8000

### 5) Start the app

In the dashboard:
- Go to **Apps**
- Toggle **reachy_mini_meditation_tutor** on
- Click the **⚙️** icon (opens the app UI)

App UI:
- http://localhost:8042

## Developer notes

See `DEVELOPMENT.md`.