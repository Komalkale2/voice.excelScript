# 🎙️ Mimi – AI Voice-Controlled Excel Assistant

**Mimi** is a local, voice-activated AI assistant designed to automate spreadsheet management hands-free. Powered by OpenAI's Whisper model and Python, Mimi continuously listens for a wake word, processes natural language voice commands, and updates Excel files in real time with text-to-speech confirmation.

---

## ✨ Features

- 🔒 **100% Offline & Local:** Uses local OpenAI Whisper models—no external API keys or cloud subscriptions needed.
- 🗣️ **Wake-Word Activation:** Listens in the background for **"Hey Mimi"** before capturing updates.
- 📊 **Smart Excel Parsing:**
  - Create new columns dynamically (e.g., *"Add column Name"*).
  - Add text or numeric entries to columns (e.g., *"Put 500 under Amount"*).
  - Modify specific cell coordinates directly (e.g., *"Set B2 to 1500"*).
- 🔊 **Voice Feedback:** Confirms spreadsheet updates using local text-to-speech (`pyttsx3`).
- ⚡ **Lightweight Execution:** Optimized with Whisper's `tiny.en` model for near-instant offline execution.

---

## 🛠️ Tech Stack

- **Python 3.10+**
- **OpenAI Whisper** (`tiny.en`) – Speech-to-text recognition
- **openpyxl** – Excel file reading and manipulation
- **pyttsx3** – Text-to-speech engine
- **sounddevice & scipy** – Audio capture and recording
- **word2number** – Converts spoken words (e.g., "five hundred") to numeric values
- **FFmpeg** – Audio processing backend

---

## 📂 Project Structure

```text
voice.excelScript/
│
├── voice_excel.py         # Main assistant script & command processor
├── my_budget.xlsx         # Target Excel workbook
├── ffmpeg.exe             # Audio engine binary
├── Launch Assistant.bat   # 1-Click launcher script
└── README.md              # Project documentation



## 🚀 Complete Installation & Setup Guide

### 1. Prerequisites Setup

* **Install Python:**
  * Download Python (3.10 or newer) from [python.org](https://www.python.org/).
  * ⚠️ **Important:** During installation, make sure to check the box that says **"Add Python to PATH"**.

* **Install & Setup FFmpeg:**
  * Download the FFmpeg essentials build from [gyan.dev/ffmpeg/builds](https://www.gyan.dev/ffmpeg/builds/).
  * Extract the downloaded `.zip` archive.
  * Copy `ffmpeg.exe` directly into your root project folder (`voice.excelScript`).

---

### 2. Clone or Download the Project

Clone the repository using PowerShell:

```powershell
git clone [https://github.com/your-username/mimi-voice-excel.git](https://github.com/your-username/mimi-voice-excel.git)
cd mimi-voice-excel
(Alternatively, download the project as a ZIP file and extract it into your desired folder).

3. Create & Activate Virtual Environment (Optional but Recommended)
Set up a virtual environment inside your project folder:

PowerShell
# Create virtual environment
python -m venv venv

# Activate virtual environment on Windows
.\venv\Scripts\activate
4. Install Project Dependencies
Install all required Python libraries with one command:

PowerShell
pip install -r requirements.txt
(Or install manually):

PowerShell
pip install openai-whisper sounddevice openpyxl pyttsx3 scipy numpy word2number keyboard
