# 🔍 Python Nmap Port Scanner

A simple Python-based port scanner that automates **Nmap** scans using the `python-nmap` library.  
This project is intended for **learning and educational purposes** and demonstrates how to integrate a system security tool with Python.

---

## ✨ Features

- Run Nmap scans directly from Python
- Supports fast, balanced, and deep scan modes
- Displays open ports grouped by protocol
- Uses the real Nmap engine (not a reimplementation)
- Works inside a Python virtual environment

---

## 🛠️ Requirements

- Python 3.9+
- Nmap (installed system-wide)
- `python-nmap` library

On Kali Linux:

```bash
sudo apt update
sudo apt install nmap python3-venv
```

📦 Installation
Clone the repository:

```bash
git clone https://github.com/your-username/PyNmapScanner.git
cd portscanner
```

Create and activate a virtual environment:

```bash
python3 -m venv venv
source venv/bin/activate
```

Install dependencies:

```bash
pip install python-nmap
```

🚀 Usage
Edit the target and scan options in portscanner.py:

```python
Copier le code
target = "45.33.32.156"
options = "-T4 -F"
```

Run the scanner:

```bash
python portscanner.py
```

For scan modes that require elevated privileges:

```bash
sudo $(which python) portscanner.py
```

---

## 🎯 Target & IP Address Disclaimer

### ⚠️ Important Notice

The example IP address used in this project is not a random target.

The IP address is taken from the official Nmap documentation and learning resources

It is provided by Nmap specifically for testing and educational purposes

It is used here only as an example to demonstrate how the tool works

You should never scan systems you do not own or have explicit authorization to test.

### ⏱️ Scan Modes & Duration

This tool relies on Nmap, so scan duration depends on the selected options.

Mode Options Description Speed
Fast -T4 -F Scans common ports only ⚡ Fast
Balanced -sV -T4 -p 1-1000 Version detection on common ports ⏳ Medium
Deep -sV -sC Version detection + default NSE scripts 🐢 Slow

### ⚠️ Deep scans can take 10+ minutes, especially:

When scanning remote hosts

When running inside a virtual machine

When executing NSE scripts

This is expected behavior and not a bug.

---

## 📁 Project Structure

```text
portscanner/
├── portscanner.py
├── venv/
└── README.md
```

---

## ⚠️ Legal Disclaimer

This project is intended for educational purposes only.

Unauthorized port scanning may be illegal.
Only scan systems that you own or have explicit permission to test.

The author assumes no responsibility for misuse of this tool.

---

## 📚 What I Learned

Managing Python virtual environments

Integrating system tools with Python

Understanding Nmap scan trade-offs

Debugging environment and permission issues

Basic penetration testing workflow

---

## 🧩 Future Improvements

Live scan progress output

Export results to JSON or XML

Command-line arguments instead of hardcoded values

Automated staged scanning (fast → deep)
