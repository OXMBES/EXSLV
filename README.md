📱 EXSLV — Advanced Android Pentesting Framework

<div align="center">

```
              ⠀⠀⣰⣆⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀
  ⠀⠀⠀⠀⠀⠀⢀⣠⣤⠞⢹⡏⠳⣤⣄⡀⠀⠀⠀⠀⠀
  ⠰⣤⣀⠀⢀⡴⣫⣴⡇⠀⢸⡇⠀⠈⢦⣝⢦⡀⠀⣀⣤⠆
  ⠀⢷⠀⠉⠛⠾⣿⣿⡇⠀⢸⡇⠀⢀⠀⠙⠷⠛⠉⠀⡾⠀
  ⠀⠘⡄⠀⢠⡀⠀⢿⡇⠀⢸⡇⠀⠈⠉⠀⣀⡄⠀⢠⠃⠀
  ⠀⠀⢳⡀⠀⣷⠀⠘⡇⠀⢸⡇⡀⢤⣶⣿⠟⠀⢀⡞⠀⠀
  ⠀⠀⠈⣟⣦⠸⡆⠀⠁⠀⢸⡏⠀⢸⠿⠁⠀⣴⣻⠁⠀
  ⠀⠀⠀⠹⣌⢷⣿⡀⠀⠀⢸⡇⠀⠈⠀⣠⡾⣡⠏⠀⠀⠀
  ⠀⠀⠀⠀⠈⠳⣝⠣⡄⠀⢸⡇⠀⢠⠜⣫⠞⠁
  ⠀⠀⠀⠀⠀⠀⠈⠙⠛⢦⣸⡇⡴⠛⠋⠁⠀
  ⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠹⠏⠀⠀⠀⠀⠀
```

v3.0.0 — Advanced Android Pentesting Framework

https://img.shields.io/badge/Python-3.9%2B-blue?style=for-the-badge&logo=python
https://img.shields.io/badge/Termux-Compatible-green?style=for-the-badge&logo=android
https://img.shields.io/badge/License-MIT-red?style=for-the-badge
https://img.shields.io/badge/Author-Aceng--Hunter404-purple?style=for-the-badge&logo=youtube

</div>

---

⚠️ LEGAL DISCLAIMER

PENTING! EXSLV dirancang HANYA untuk penetration testing yang sah dengan izin tertulis. Penggunaan terhadap sistem yang tidak Anda miliki atau tidak memiliki izin eksplisit adalah ILEGAL dan dapat mengakibatkan tuntutan pidana. Penulis tidak bertanggung jawab atas penyalahgunaan!

---

📖 DAFTAR ISI

· Overview
· Fitur
· Struktur Project
· Dependencies
· Instalasi
· Cara Penggunaan
· Mode CLI
· Module Reference
· Screenshots
· FAQ
· Roadmap
· Contributing
· Author & Credits
· License

---

🔍 OVERVIEW

EXSLV adalah framework pentesting Android komprehensif yang mengintegrasikan analisa APK statis, eksploitasi dinamis via ADB, pemindaian jaringan, pemetaan kerentanan, pembuatan payload, dan generasi laporan profesional — semua berjalan di Termux tanpa root.

EXSLV menggabungkan 7 modul inti dengan 17+ fungsi ke dalam satu antarmuka Rich UI interaktif, mendukung mode menu interaktif maupun command line untuk otomatisasi.

---

🚀 FITUR

🔎 APK Static Analyzer

· Hash file (MD5, SHA1, SHA256)
· Dekompilasi manifest Android
· Deteksi 30+ permission berbahaya
· Pemindaian komponen exported
· Deteksi 11 pola hardcoded secrets (API keys, tokens, private keys)
· Ekstraksi URL & IP embedded
· Deteksi obfuscation
· Pemeriksaan backup & debuggable flag

📱 Device Manager (ADB)

· Informasi device 30+ properti
· Keamanan assessment otomatis (root, SELinux, patch expiry)
· Package manager (list, filter, info detail)
· Screenshot capture & screen recording
· Logcat capture dengan deteksi rahasia otomatis
· ADB WiFi connect & auto WiFi bridge
· Interactive ADB shell
· File transfer (pull/push)

🌐 Network Scanner

· Port scanning multithreaded (100 workers, 65535 ports)
· 24 common port service identification
· Risk assessment per port
· WiFi information extraction
· Host discovery (ping sweep)
· SSL pinning detection via logcat
· MitM proxy setup guide

🚨 Vulnerability Scanner

· Pemetaan CVE berdasarkan versi Android (KitKat → 14)
· Root detection komprehensif (su binary + Magisk)
· Pemeriksaan SELinux status
· Insecure storage scanning
· Developer options & encryption check
· Package-specific assessment

💥 Exploit Engine

· Launch exported activities
· Broadcast receiver injection
· Content provider data extraction
· Deep link fuzzer (30 path default)
· Frida injection guide
· Reverse shell payload dropper
· SQLite database extraction
· Lock screen bypass (PIN brute)
· Developer options enabler

🎯 Payload Generator

· msfvenom APK generation (4 payload types)
· Intent payload generator
· Reverse shell one-liners (6 methods)
· ADB exploitation script generator
· Payload obfuscation (base64 & hex)

📋 Report Generator

· HTML report dengan styling cyberpunk
· JSON structured report
· CLI summary table
· Remediation recommendations
· CVE links ke NVD database

⚡ Auto Dependency Checker

· Pengecekan 10 Python packages
· Pengecekan 10 system tools
· Auto-install missing dependencies
· Progress bar interaktif
· Critical dependency blocking

---

📦 DEPENDENCIES

Wajib (Critical)

Package Version Fungsi
Python 3.9+ Runtime
ADB 1.0.41+ Android Debug Bridge
Git 2.x+ Version control
Rich 13.x+ Terminal UI
Requests 2.x+ HTTP library
Colorama 0.4.x+ Terminal colors
BeautifulSoup4 4.x+ HTML/XML parser

Optional (Enhancement)

Package Fungsi
Nmap Advanced port scanning
scrcpy Screen mirroring
Apktool APK decompilation
JADX DEX to Java
Frida Dynamic instrumentation
msfvenom Payload generation
androguard Deep APK analysis

---

💻 INSTALASI

One-Line Setup

```bash
pkg update -y && pkg upgrade -y && pkg install git python python-pip -y && git clone https://github.com/OXMBES/Xxx ~/EXSLV && cd ~/EXSLV && python3 requirements_checker.py && python3 main.py
```

Manual Setup

```bash
# 1. Update Termux
pkg update -y && pkg upgrade -y

# 2. Install dependencies dasar
pkg install git python python-pip android-tools -y

# 3. Clone repository
git clone https://github.com/OXMBES/Xxx ~/EXSLV

# 4. Masuk folder
cd ~/EXSLV

# 5. Jalankan auto dependency checker
python3 requirements_checker.py

# 6. Jalankan EXSLV
python3 main.py
```

Setup Modules Manual (Jika dari source code)

```bash
# Buat struktur folder
mkdir -p ~/EXSLV/modules ~/EXSLV/output ~/EXSLV/payloads

# Download / copy semua file .py ke folder yang sesuai
# (requirements_checker.py, main.py, modules/*.py)

# Install dependencies
pip install rich requests colorama beautifulsoup4 python-nmap

# Jalankan
cd ~/EXSLV
python3 main.py
```

---

🎮 CARA PENGGUNAAN

Mode Interaktif (Default)

```bash
python3 main.py
```

Navigasi menu:

```
1  → Device Manager       9  → Auto ADB WiFi Connect
2  → APK Analyzer         10 → Screenshot Capture
3  → Network Scanner      11 → Package Manager
4  → Vulnerability Scan   12 → Logcat Analyzer
5  → Exploit Engine       13 → SSL Pinning Check
6  → Payload Generator    14 → File Transfer
7  → Report Generator     15 → Interactive Shell
8  → ADB WiFi Connect     16 → Remote Control
                           17 → About
                           0  → Exit
```

---

⚡ MODE CLI

Untuk scripting dan otomatisasi:

```bash
# List devices
python3 main.py --devices

# Device info
python3 main.py --device ABC123 --info

# APK analysis
python3 main.py --apk app.apk --report html

# Vulnerability scan
python3 main.py --device ABC123 --vuln-scan --pkg com.target.app

# Port scan
python3 main.py --target 192.168.1.1 --port-scan

# Generate payload
python3 main.py --payload reverse_tcp --lhost 10.0.0.1 --lport 4444

# Deep link exploit
python3 main.py --device ABC123 --exploit deep-link --pkg com.app --scheme myapp

# WiFi ADB
python3 main.py --device ABC123 --adb-wifi

# Screenshot
python3 main.py --device ABC123 --screenshot

# Full workflow example
python3 main.py --device ABC123 --info --vuln-scan --port-scan --report html
```

---

📚 MODULE REFERENCE

ADB Manager (adb_manager.py)

Fungsi Deskripsi
list_devices() List device terhubung dengan detail
device_info(id) 30+ properti device
list_packages(id, filter) Enumerasi package terinstall
take_screenshot(id) Screenshot + pull otomatis
capture_logcat(id, lines) Logcat dengan secret detection
enable_adb_wifi(id, port) Aktifkan ADB TCP
auto_adb_wifi_connect(id) Auto bridge USB → WiFi

APK Analyzer (apk_analyzer.py)

Fungsi Deskripsi
analyze_apk(path) Full static analysis
30+ dangerous permissions Deteksi permission berbahaya
11 secret patterns API keys, tokens, private keys
URL/IP extraction Endpoint discovery

Network Scanner (network_scanner.py)

Fungsi Deskripsi
port_scan(host, ports) Multithreaded port scan
get_wifi_info(id) WiFi detail extraction
discover_devices(subnet) Host discovery
check_ssl_pinning(id, pkg) SSL pinning detection

Vulnerability Scanner (vulnerability_scanner.py)

Fungsi Deskripsi
check_root_status(id) Root detection 10+ paths
check_android_version_cves(id) CVE mapping (KK→14)
full_vulnerability_scan(id, pkg) Comprehensive assessment

Exploit Engine (exploit_engine.py)

Fungsi Deskripsi
launch_exported_activity(id, pkg, act) Intent injection
deep_link_fuzzer(id, pkg, scheme) 30 path fuzzing
shell_payload_dropper(id, lhost, lport) Reverse shell deploy
bypass_lock_screen(id) PIN brute force

Payload Generator (payload_generator.py)

Fungsi Deskripsi
generate_msfvenom_apk(lhost, lport, type) APK payload
generate_reverse_shell_commands(lhost, lport) 6 one-liners
obfuscate_payload(cmd, method) base64/hex encoding

Report Generator (report_generator.py)

Fungsi Deskripsi
generate_html_report(data, output) Cyberpunk HTML
generate_json_report(data, output) Structured JSON
print_summary_table(data) CLI summary

---

📸 SCREENSHOTS

Main Menu


<div align="center">

![EXSLV Banner](https://files.catbox.moe/x4fre3.jpg)

**v3.0.0 — Advanced Android Pentesting Framework**

</div>


APK Analysis Output

```
══════════ APK ANALYSIS RESULTS ══════════
📱 App Info: Package: com.example.app | SDK: 21-33
⚠ Dangerous Permissions: 5 ditemukan
🔑 Hardcoded Secrets: 1 ditemukan (CRITICAL)
🌐 Embedded URLs: 15 ditemukan
🚨 Vulnerabilities: 2 ditemukan
```

---

❓ FAQ

Q: Apakah butuh root?

A: Tidak. EXSLV dirancang untuk Termux non-root. Beberapa fitur exploit engine membutuhkan target yang sudah di-root.

Q: Kenapa ADB tidak terdeteksi?

A: Jalankan pkg install android-tools -y, lalu adb kill-server && adb start-server.

Q: Kenapa scrcpy tidak bisa install?

A: scrcpy adalah optional. Fitur core EXSLV tidak bergantung padanya. Untuk screen mirror, jalankan scrcpy dari laptop/PC.

Q: Bagaimana cara connect device via WiFi?

A:

1. Colok USB dulu
2. adb tcpip 5555
3. Cabut USB
4. adb connect IP_DEVICE:5555
5. Atau gunakan menu 9 (Auto ADB WiFi Connect) di EXSLV

Q: APK Analyzer tidak membaca manifest?

A: APK mungkin di-obfuscate atau berupa bundle (.apks). Ekstrak dulu dengan bundletool atau unzip.

Q: Port scan gagal?

A: Pastikan target bisa dijangkau (ping target). Gunakan mode host untuk scan eksternal.

---

🗺️ ROADMAP

· v3.1 — Metasploit integration
· v3.2 — Web GUI dashboard
· v3.3 — Frida automation scripts
· v3.4 — Cloud sync reports
· v3.5 — AI-powered vulnerability assessment
· v4.0 — Cross-platform desktop version

---

🤝 CONTRIBUTING

Kontribusi sangat diterima!

1. Fork repository
2. Buat branch fitur (git checkout -b feature/nama-fitur)
3. Commit perubahan (git commit -m 'feat: tambah fitur baru')
4. Push ke branch (git push origin feature/nama-fitur)
5. Buka Pull Request

Guidelines:

· Gunakan type hints
· Tambahkan docstrings
· Update README jika perlu
· Test di Termux non-root

---

👤 AUTHOR & CREDITS

<div align="center">

 
Author Aceng-Hunter404
YouTube @Aceng-Hunter404
GitHub OXMBES
Version v3.0.0
Year 2026

</div>

Special Thanks

· Almighty God -- Gives reason and life 
· Rich Library — Textualize/rich
· Androguard — APK analysis engine
· Termux Community — Android terminal emulator

---

📄 LICENSE

```
MIT License

Copyright (c) 2026 Aceng-Hunter404

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

<div align="center">

⚠️ FOR AUTHORIZED PENETRATION TESTING USE ONLY ⚠️

Made with ❤️ by Aceng-Hunter404 | © 2026 

</div>
