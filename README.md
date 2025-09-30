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

## 🧩 Add `$HOME/.local/bin` to PATH (if not already)

Run this once to make sure your local binaries are always available in the terminal:

```bash
/bin/bash -c 'os=$(uname -s); s=$(basename "$SHELL"); f=""; if [[ $s == zsh ]]; then f="$HOME/.zprofile"; elif [[ $s == bash && $os == Darwin ]]; then f="$HOME/.bash_profile"; elif [[ $s == bash ]]; then f="$HOME/.bashrc"; else f="$HOME/.profile"; fi; grep -qs ".local/bin" "$f" 2>/dev/null || echo "export PATH=\$HOME/.local/bin:\$PATH" >> "$f"'
```

Then reload your environment:

```bash
exec "$SHELL" -l
```

or simply **restart your terminal**.

---

## 📦 What this does

- Downloads and runs the `update-scripts` installer.  
- Installs `cp-scripts` into:  
  - `$HOME/.local/share/cp-scripts` (the repository)  
  - `$HOME/.local/bin` (symlinks for executables)  
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

No. Everything is installed to `$HOME/.local/` (inside your home directory).  

### What do I need preinstalled?

- **Git** (to clone and update the repo)  
- **Bash** (to run the installer and scripts)  
- Either `curl` or `wget` (for the one-line installer)  

### Where are the scripts installed?

- Repository: `$HOME/.local/share/cp-scripts`  
- Executables (symlinks): `$HOME/.local/bin`  

Make sure `$HOME/.local/bin` is in your `PATH`.  
If not, run the command in the **PATH setup** section above.

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
