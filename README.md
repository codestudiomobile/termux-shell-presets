# CodeStudio Termux Shell Presets

Core shell configurations and interactive workspace orchestration layers for CodeStudio Mobile IDE. This repository manages path initialization, environment state safety checks, and seamless runtime terminal restarts.

## 📦 What's Inside?
* **`bash.bashrc`**: Core environment bootstrap. Configures localized paths (`$PREFIX/bin`), switches raw Android pathing to accessible shortcuts, manages terminal verification routines, and builds the custom dynamic prompt.
* **`restart-terminal.sh`**: A utility script mapped to broadcast an internal Android restart intent command, refreshing your shell workspace variables instantly without manual application closure.

---

## 🚀 Quick Setup & Installation

To pull these components directly into your application environment, follow these steps inside the Termux terminal wrapper:

### 1. Register Core Shell Rules
Download and overwrite your terminal's main initialization file:
```bash
curl -fsSL [https://raw.githubusercontent.com/codestudiomobile/termux-shell-presets/main/bash.bashrc](https://raw.githubusercontent.com/codestudiomobile/termux-shell-presets/main/bash.bashrc) -o $PREFIX/etc/bash.bashrc

```

### 2. Add System Command Shortcuts

Download the terminal environment restarter tool directly into your execution folder and mark it executable:

```bash
curl -fsSL [https://raw.githubusercontent.com/codestudiomobile/termux-shell-presets/main/restart-terminal.sh](https://raw.githubusercontent.com/codestudiomobile/termux-shell-presets/main/restart-terminal.sh) -o $PREFIX/bin/restart-terminal
chmod +x $PREFIX/bin/restart-terminal

```

---

## 💡 How to Use

### 📁 Dynamic IDE Project Mapping

When launching a workspace project inside CodeStudio, declare the `OPENED_FOLDER` environment variable. The core profile automatically translates complex, restrictive Android system storage layouts into cleaner virtual shortcuts:

```bash
export OPENED_FOLDER="/storage/emulated/0/MyProject"
source $PREFIX/etc/bash.bashrc

```

### 🔄 Instant Shell Environments Reboot

If environment variables change or configuration adjustments lock your workflow sessions, reload the layout seamlessly using:

```bash
restart-terminal

```

```
