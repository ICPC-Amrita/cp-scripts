# cp-scripts

Utility scripts for competitive programming workflows.  
Provides quick setup, template management, and handy tools for contests.

---

## 🚀 Installation

You can install **cp-scripts** with a single command.  

### Using `curl` (recommended on macOS, most Linux distros)
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/ICPC-Amrita/cp-scripts/main/update-scripts)"
```

### Using `wget` (works on Linux servers/minimal installs)
```bash
/bin/bash -c "$(wget -qO- https://raw.githubusercontent.com/ICPC-Amrita/cp-scripts/main/update-scripts)"
```

---

## 📦 What this does
- Downloads and runs the `update-scripts` installer.  
- Installs `cp-scripts` into:  
  - `~/.local/share/cp-scripts` (the repository)  
  - `~/.local/bin` (symlinks for executables)  
- Adds/upgrades all scripts automatically.  

---

## 🔄 Updating
Once installed, just run:
```bash
update-scripts
```
to fetch the latest version and refresh symlinks.

---

## 📝 Versioning
Each update is tied to a Git commit hash.  
The installer displays:
- Current commit hash (short + full date)  
- Whether your local install is up to date with `origin/main`  

---

## ❓ FAQ

### Do I need sudo?
No. Everything is installed to `~/.local/` (inside your home directory).  

### What do I need preinstalled?
- **Git** (to clone and update the repo)  
- **Bash** (to run the installer and scripts)  
- Either `curl` or `wget` (for the one-line installer)  

### Where are the scripts installed?
- Repository: `~/.local/share/cp-scripts`  
- Executables (symlinks): `~/.local/bin`  

Make sure `~/.local/bin` is in your `PATH` (it usually is by default).  

---

## ⚡ Example
```bash
# Update cp-scripts
update-scripts

# Run a script (example)
run A.cpp
```

---

## 🤝 Contributing
Pull requests and issues are welcome.  
This project is maintained under [ICPC-Amrita](https://github.com/ICPC-Amrita).
