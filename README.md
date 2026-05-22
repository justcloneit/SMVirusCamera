# Camera Login Valid Checker v3.0 - Advanced Camera Scanner & Brute Force Tool

<div align="center">

![Visitors](https://api.visitorbadge.io/api/visitors?path=https%3A%2F%2Fgithub.com%2FW8SOJIB%2FW8CameraHackV3&label=Visitors&countColor=%23263759&style=flat)
![GitHub Views](https://komarev.com/ghpvc/?username=W8SOJIB&label=Profile%20Views&color=0e75b6&style=flat)
[![GitHub Stars](https://img.shields.io/github/stars/W8SOJIB/W8CameraHackV3?style=social)](https://github.com/W8SOJIB/W8CameraHackV3)
[![GitHub Forks](https://img.shields.io/github/forks/W8SOJIB/W8CameraHackV3?style=social)](https://github.com/W8SOJIB/W8CameraHackV3)

![Python Version](https://img.shields.io/badge/python-3.7%2B-blue?style=flat&logo=python)
![Termux Support](https://img.shields.io/badge/Termux-Compatible-green?style=flat&logo=android)
![Platform](https://img.shields.io/badge/platform-Linux%20%7C%20Windows%20%7C%20Android-lightgrey?style=flat)
![License](https://img.shields.io/badge/license-MIT-green?style=flat)
![Countries](https://img.shields.io/badge/countries-44-brightgreen?style=flat)
![One Click](https://img.shields.io/badge/operation-one--click-orange?style=flat)
A powerful multi-phase camera scanner and device validator supporting 243 countries across all 5 global RIR registries. Detects IP cameras, NVR/DVR systems, ONVIF devices, and routers — then validates credentials, probes RTSP streams, tests CVEs, and delivers results directly to Telegram automatically.

Features
🌍 Country & IP Range Support
243 Countries across all 5 RIR regions:
APNIC — Asia-Pacific (44 countries)
RIPE NCC — Europe, Middle East, Central Asia
ARIN — North America, Caribbean
LACNIC — Latin America, Caribbean
AFRINIC — Africa
Auto-fetches latest IP allocations directly from each registry's FTP server
No manual IP file management needed
📹 Device Detection & Login Validation
Multi-Brand Detection: Hikvision, Dahua/Anjhua, NVR, DVR, ONVIF, Axis, Foscam, Reolink, Amcrest, Uniview, Tiandy, and more
Device Model Extraction from HTTP Server headers
Brute-Force Login Validator with Digest/Basic authentication (Hikvision ISAPI & Dahua HTTP API)
Custom Credentials loaded from credentials.txt (username:password per line)
Credential Stats Dashboard — per-credential success tracking with daily and dated breakdowns
📡 RTSP Path Tester (Option 13) — 5 Modes
Single — probe one camera IP manually with live path-by-path output; auto-sends best URL + file to Telegram
Batch — test all cameras from one or more ValidCamera files in parallel; multi-file select with comma/range syntax (1,3, 2-4); auto-sends summary + RTSP_Tested.txt to Telegram
View — browse and inspect any RTSP result file; bulk-merge selected URLs into RTSP_Tested.txt; send files to Telegram
M3U — generate a VLC-ready .m3u playlist from any combination of RTSP/ValidCamera files with proper #EXTINF entries; auto-sends playlist to Telegram
Quick Re-Test — re-pings every URL in RTSP_Tested.txt (or any RTSP file), removes dead/unreachable URLs, saves the cleaned file atomically, and auto-sends updated file to Telegram
📲 Telegram Integration (Automatic)
Auto-send after every operation — no y/n prompt, files are delivered immediately when Telegram is enabled
Scan start/stop notifications
Camera detection alerts (batched to prevent API flooding)
Valid credential alerts with full camera details
RTSP URL delivery after single, batch, M3U, and re-test operations
Emergency crash handler — sends error details and backup files on unexpected exit
Multi-destination support (multiple bot tokens/chat IDs)
Rate-limited (0.5s minimum interval) with 429 retry handling
⚡ Performance
300 concurrent threads for maximum scan speed
0.15s port scan timeout for ultra-fast detection
Parallel port scanning per IP
Submit-all-per-range with as_completed (no chunking/cancellation bugs)
Bounded Telegram queue (max 500 messages) to prevent memory overflow
🔧 Advanced Tools
NVR Channel Splitter — splits multi-channel NVR RTSP streams into individual URLs
CVE Scanner — tests for known camera firmware vulnerabilities
Batch Country Scan — scan multiple countries sequentially with one command
Live Dashboard — real-time scan progress monitoring
Config Downloader — download device configs from exposed endpoints
Export Results — export to CSV and JSON
Single IP Brute Force — targeted credential testing on one IP
Resume Scan — saves progress to scan_progress.json, prompts to continue or restart
Duplicate Removal — automatically removes duplicate IPs from result files after scan
🔒 Windows EXE Build
Two build scripts included:

build_exe.py — standard Wine + PyInstaller build, produces standalone Windows .exe
build_custom_bootloader.py — AV-bypass build: compiles PyInstaller bootloader from source using MinGW cross-compiler for a unique binary signature
Installation
Termux (Android)
pkg update && pkg upgrade
pkg install python git
git clone https://github.com/justcloneit/SMVirusCamera
cd SMVirusCamera
pip install requests colorama pyfiglet urllib3
python W8CameraHackV3.py

Linux / Mac
git clone https://github.com/justcloneit/SMVirusCamera
cd SMVirusCamera
pip install requests colorama pyfiglet urllib3
python W8CameraHackV3.py
