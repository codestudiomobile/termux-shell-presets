# CodeStudio Termux Shell Presets

Core shell configurations and interactive workspace orchestration layers for CodeStudio Mobile IDE. This repository manages path initialization, environment state safety checks, and seamless runtime terminal restarts.

## 📦 What's Inside?
* **`bash.bashrc`**: Core environment bootstrap. Configures localized paths (`$PREFIX/bin`), switches raw Android pathing to accessible shortcuts, manages terminal verification routines, and builds the custom dynamic prompt.
* **`restart-terminal.sh`**: A utility script mapped to broadcast an internal Android restart intent command, refreshing your shell workspace variables instantly without manual application closure.

---

## 🚀 Quick Setup & Installation

To pull these components directly into your application environment, follow these steps inside the Termux terminal wrapper:

### Register Core Shell Rules
Download and overwrite your terminal's main initialization file:
```bash
curl -fsSL [https://raw.githubusercontent.com/codestudiomobile/termux-shell-presets/main/bash.bashrc](https://raw.githubusercontent.com/codestudiomobile/termux-shell-presets/main/bash.bashrc) -o $PREFIX/etc/bash.bashrc
