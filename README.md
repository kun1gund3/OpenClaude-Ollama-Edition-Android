# 📱 OpenClaude Android (Ollama Edition)

<img width="2400" height="1080" alt="Screenshot_20260413-124242 Termux" src="https://github.com/user-attachments/assets/c447fce1-2eb5-4035-b9ad-b99b67603167" />

**Run an autonomous, hardware-aware AI agent directly on your Android device. This version is modified to run locally via Ollama.**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Platform: Android](https://img.shields.io/badge/Platform-Android-green.svg)]()
[![Powered By: Ollama](https://img.shields.io/badge/Powered%20By-Ollama-white.svg)]()

---

## ✨ Features
- **Local LLM Support:** Run high-performance models locally using **Ollama**.
- **Autonomous UI Control:** The AI can "see" your screen and simulate taps, swipes, and typing using Shizuku and UIAutomator.
- **Hardware Integration:** Control WiFi, Battery, Camera, and Volume directly through the AI chat.
- **1-Click Setup:** Fully automated Termux environment configuration.

## 🛠 Prerequisites
To use the "God-Mode" hardware features, you must have the following installed:

Termux (GitHub/F-Droid version): Do not use the Play Store version.[Termux on F-Droid](https://f-droid.org/packages/com.termux/)

Termux:API: Install the app from GitHub to allow the AI to access hardware sensors. [Termux API on F-Droid](https://f-droid.org/en/packages/com.termux.api/)

Ollama: Must be installed (pkg install ollama) and running (ollama serve) in a separate Termux tab.

Shizuku (Optional but Recommended): Required for autonomous UI interaction without root.

## Shizuku Configuration (System Control)
Shizuku is required to securely bypass the internal Android application sandbox. Without this service, your AI will not have the native authority to execute system commands.
1. Install **Shizuku** from the Google Play Store.
2. Enable **Developer Options** on your Android device (tap "Build Number" 7 times under Settings > About Phone).
3. Inside Developer Options, enable **Wireless Debugging**.
4. Open the Shizuku application, select **Pairing**, and follow the on-screen instructions to authorize the service using an Android pairing code.
5. Tap **Start** to initiate the background service.


## Ollama Installation
Open **Termux** and paste the following command. This will install and run the ollama on your phone
```
termux-setup-storage
pkg install ollama
ollama serve
```
Open a new environment in Termux and paste the following command
```
ollama run gemini-3-flash-preview:cloud
```
If you want a different model, then replace the desired model after the run command.

A link will be generated.

Copy the link and open it in a browser. Follow the instructions until your device is connected. 


## 🚀 One-Line Installation (Leaked ClaudeCode)

Open **Termux** and paste the following command. This will update your system, download the setup script, and configure everything automatically:

```
pkg update -y && pkg upgrade -y && pkg install curl -y && curl -sL https://raw.githubusercontent.com/AbuZar-Ansarii/Leaked-ClaudeCode/master/termux_setup.sh -o ~/termux_setup.sh && chmod +x ~/termux_setup.sh && bash ~/termux_setup.sh
```
## ⚙️ How to Use
```
claude
```
## ⚖️ Disclaimer
This project is for educational and research purposes only. Use "Limitless Mode" with caution as it allows the AI to execute commands on your device autonomously.

Developed by - **AbuZar-Ansarii**


