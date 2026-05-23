# Camera Login Valid Checker v3.0 - Advanced Camera Scanner & Brute Force Tool

<div align="center">

![Visitors](https://api.visitorbadge.io/api/visitors?path=https%3A%2F%2Fgithub.com%2Fjustcloneit%2FSMVirusCamera&label=Visitors&countColor=%23263759&style=flat)
![GitHub Views](https://komarev.com/ghpvc/?username=justcloneit&label=Profile%20Views&color=0e75b6&style=flat)
[![GitHub Stars](https://img.shields.io/github/stars/justcloneit/SMVirusCamera?style=social)](https://github.com/justcloneit/SMVirusCamera)
[![GitHub Forks](https://img.shields.io/github/forks/justcloneit/SMVirusCamera?style=social)](https://github.com/justcloneit/SMVirusCamera)

![Python Version](https://img.shields.io/badge/python-3.7%2B-blue?style=flat&logo=python)
![Termux Support](https://img.shields.io/badge/Termux-Compatible-green?style=flat&logo=android)
![Platform](https://img.shields.io/badge/platform-Linux%20%7C%20Windows%20%7C%20Android-lightgrey?style=flat)
![License](https://img.shields.io/badge/license-MIT-green?style=flat)
![Countries](https://img.shields.io/badge/countries-44-brightgreen?style=flat)
![One Click](https://img.shields.io/badge/operation-one--click-orange?style=flat)

### 🎯 Real-Time Visitor Counter - See Who's Visiting! 👆

</div>
Advanced Python CLI network device scanner supporting 243+ countries across all 5 RIR regions (APNIC, RIPE, ARIN, LACNIC, AFRINIC). Auto-fetches IP ranges from any regional registry, detects IP Cameras, NVR/DVR, Routers, and other network devices with geolocation, and saves results to files. Includes Telegram integration for real-time alerts and result file sharing.

## 🆕 What's New in V3.0?

Upgrading from [V2](https://github.com/justcloneit/W8CameraHackV2)? Here's what's new:

**How to Run**
Run via the "Run Camera Scanner V3" workflow which executes python SMVirusCamera.py.

**Main Menu (Options 1-13):**

1. **Random Camera Scan — select country, detect devices across 5 RIR regions**
2. **Login Check from Saved TXT File — brute-force credentials against found cameras**
3. **IP Range Scan — scan a specific CIDR/IP range manually**
4. **View All Valid Camera — display validated login results**
5. **Send Result File to Telegram — manually push any result file to Telegram**
6. **Merge & Deduplicate Result Files and CCTV Found Files**
7. **Password Analysis (Aggregator) — stats on cracked passwords**
8. **Credential Success Stats — per-credential success rates**
9. **Exit**
10. **Help & Feature Reference**
11. **NVR Channel Splitter — split multi-channel NVR streams**
12. **Extra Tools — RTSP Brute Force, Heatmap, QR Code, CVE checker, Diff, CSV export…**
13. **RTSP Path Tester & File Viewer — 5-item submenu (see below):**
# **Option 13 — RTSP Path Tester & File Viewer**
**Submenu with five modes, all with Telegram integration and result-file send:**

-	Mode	Description:
1. **Single	Test one camera manually; auto-probes all brand paths; Basic + Digest auth**
2. **Batch	Read cameras from ValidCamera file(s); comma/dash file selection; live progress bar; resume/save support**
3. **View	Inspect RTSP result files — live/dead counts + URL table**
4. **M3U	Build a VLC-ready .m3u playlist from RTSP_Tested.txt**
5. **Quick Re-Test	Re-ping every URL in RTSP_Tested.txt; mark dead entries, remove them, write RTSP_Dead.txt; sends updated files to Telegram**
- **After every operation the result file (RTSP_Tested.txt / RTSP_Tested.m3u / RTSP_Dead.txt) is sent automatically to Telegram.**


### 🔐 Login Validation Features

- ✅ **HIK Vision Camera Support** - ISAPI Digest Authentication
- ✅ **Dahua/Anjhua Camera Support** - HTTP API & RTSP validation
- ✅ **Multi-Threaded Brute Force** - Fast credential testing
- ✅ **Default Credentials Database** - Common admin passwords included

## Key Features

### 🌍 Country Support
- **243 Country Support across 5 RIR regions (APNIC, RIPE, ARIN, LACNIC, AFRINIC)**

- **Expanded Device Detection: Hikvision, Dahua/Anjhua, NVR, DVR, ONVIF, Axis, Foscam, Reolink, Amcrest, Uniview, Tiandy, XMeye, Router (MikroTik/TP-Link/RouterOS)**

- **Device Model Extraction: Parses HTTP Server header for device model info**

- **Telegram Integration: Scan start/stop notifications, result file sending after every operation, valid password alerts, emergency backup on crash; multi-bot/channel config supported**

- **Resume Scan: Saves progress to scan_progress.json; prompts to continue or start fresh**

- **RTSP Path Tester (Option 13): Manual single probe, batch from ValidCamera files, live progress bar, save/resume, Quick Re-Test (re-ping + dead removal), M3U export, Telegram auto-send**

- **Preferred Admin Injector: Plants a configured admin account on confirmed devices via ISAPI / Dahua CGI / generic CGI; saves to PreferredAdmin_Accounts.txt**

- **Memory Pressure Monitor: Auto-pauses scan when RAM ≥ 85 %, resumes below 70 %**

- **Duplicate Removal: Automatically removes duplicate IP entries from result files after scan**

- **IP Geolocation: Shows city, region, country, postal code, ISP**

- **Auto IP Range Fetch: Downloads latest allocations from any of the 5 RIR registries**

- **Multi-Threaded Scanning: Up to 300 concurrent threads (matching original proven engine)**

- **Advanced Login Validator: Brute-force with Digest/Basic authentication (Hikvision & Dahua); credential list from credentials.txt**

- **Emergency Backup: Saves progress on crash/exit via Telegram and scan_progress.json**

- **Console Overlap Fix: Uses ANSI escape codes for clean progress output**

- **Main Menu Loop: Returns to menu after each operation instead of exiting**

- **4G/5G Mobile Camera Finder: Built-in carrier CIDR ranges for 20+ countries**

- **ISP Diversity Reporter: Tracks ISP sightings across scan sessions**

- **Auto Dashboard: Live scan stats dashboard with CVE/config/RTSP counts**

- **CVE Checker: Checks detected devices against known vulnerability patterns**

- **Heatmap / QR / CSV export: Extra tools in Option 12 submenu**

- 🌐 **Auto-Fetch IP Ranges** - **Automatically downloads from 5 RIR regions (APNIC, RIPE, ARIN, LACNIC, AFRINIC) database if file missing**

**RIR Registry URLs:**
- **APNIC (Asia-Pacific)**: ftp.apnic.net
- **RIPE NCC (Europe/Middle East/Central Asia)**: ftp.ripe.net
- **ARIN (North America/Caribbean)**: ftp.arin.net
- **LACNIC (Latin America/Caribbean)**: ftp.lacnic.net
- **AFRINIC (Africa)**: ftp.afrinic.net


**Telegram Config Format**
```bash
{
  "bot_token": "",
  "chat_id": "",
  "enabled": false,
  "send_realtime": true,
  "send_summary": true
}
```

- **📲 Telegram Integration (Automatic)**
- Auto-send after every operation — no y/n prompt, files are delivered immediately when Telegram is enabled
- Scan start/stop notifications
- Camera detection alerts (batched to prevent API flooding)
- Valid credential alerts with full camera details
- RTSP URL delivery after single, batch, M3U, and re-test operations
- Emergency crash handler — sends error details and backup files on unexpected exit
- Multi-destination support (multiple bot tokens/chat IDs)
- Rate-limited (0.5s minimum interval) with 429 retry handling


#⚡ **Performance**
- 300 concurrent threads for maximum scan speed
- 0.15s port scan timeout for ultra-fast detection
- Parallel port scanning per IP
- Submit-all-per-range with as_completed (no chunking/cancellation bugs)
- Bounded Telegram queue (max 500 messages) to prevent memory overflow

#🔧 **Advanced Tools**:

- **NVR Channel Splitter** — splits multi-channel NVR RTSP streams into individual URLs
- **CVE Scanner** — tests for known camera firmware vulnerabilities
- **Batch Country Scan** — scan multiple countries sequentially with one command
- **Live Dashboard **— real-time scan progress monitoring
- **Config Downloader** — download device configs from exposed endpoints
- **Export Results **— export to CSV and JSON
- **Single IP Brute Force** — targeted credential testing on one IP
- **Resume Scan** — saves progress to scan_progress.json, prompts to continue or restart
- **Duplicate Removal** — automatically removes duplicate IPs from result files after scan.

#🔒 **Windows EXE Build**:
Two build scripts included:
- **build_exe.py** — standard Wine + PyInstaller build, produces standalone Windows .exe
- **build_custom_bootloader.py** — AV-bypass build: compiles PyInstaller bootloader from source using MinGW cross-compiler for a unique binary signature

## Installation

### Quick Install (Recommended)

#### For Termux (Android)

```bash
# Update packages
pkg update && pkg upgrade

# Install required packages
pkg install python git

# Clone repository
git clone https://github.com/justcloneit/SMVirusCamera
cd SMVirusCamera

# Install Python dependencies
pip install requests colorama urllib3
```

## Run Tool

```bash
python SMVirusCamera.py
```
 

#### For Desktop (Windows/Linux/Mac)

```bash
# Clone the repository
git clone https://github.com/justcloneit/SMVirusCamera
cd SMVirusCamera

# Install dependencies
pip install requests colorama urllib3
```

### Manual Installation

#### For Termux (Android)

```bash
# Update packages
pkg update && pkg upgrade

# Install required packages
pkg install python git

# Clone repository
git clone https://github.com/justcloneit/SMVirusCamera
cd SMVirusCamera

# Install Python dependencies
pip install requests colorama urllib3

# Optional: For better colors (if colorama install fails, the script works without it)
pip install colorama
```

#### For Desktop (Windows/Linux/Mac)

```bash
# Clone repository
git clone https://github.com/justcloneit/SMVirusCamera
cd SMVirusCamera

# Install Python dependencies
pip install requests colorama urllib3
```

## Usage

Run the script:
```bash
python SMVirusCamera.py
```
