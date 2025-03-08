# Virtual Personal Assistant

## Overview

This is a virtual personal assistant developed in Python, designed to perform a variety of tasks using advanced technologies. Leveraging voice recognition, text-to-speech synthesis, and automation tools, this assistant can handle web browsing, system monitoring, task scheduling, and integration with external applications like WhatsApp, email, and a webcam.

## Features

- **Voice Recognition**: Utilizes the `SpeechRecognition` library to interpret voice commands.
- **Text-to-Speech**: Implements the Windows Speech API (SAPI) via `win32com.client` for natural voice responses.
- **Web Browsing**: Opens websites (e.g., YouTube, Gmail, Wikipedia) using the `webbrowser` module.
- **Task Scheduling**: Schedules reminders and tasks with the `schedule` library.
- **Application Integration**: Supports interaction with WhatsApp, email (via SMTP), and camera (via OpenCV).
- **System Monitoring**: Retrieves system information such as CPU usage, RAM usage, and disk usage using `psutil`.
- **Automation**: Automates GUI tasks with `pyautogui` (e.g., sending WhatsApp messages).
- **Information Retrieval**: Fetches Wikipedia summaries using the `wikipedia-api` library.

## Prerequisites

- **Python 3.x**: Ensure Python 3.6 or higher is installed on your system.
- **Operating System**: Currently optimized for Windows (due to `win32com.client` and other Windows-specific features).
- **Dependencies**: The following Python libraries are required:
  - `pyaudio`
  - `dateparser`
  - `schedule`
  - `opencv-python` (for `cv2`)
  - `psutil`
  - `SpeechRecognition`
  - `pywin32`
  - `pyautogui`
  - `wikipedia-api`

## Installation

1. **Clone the Repository**:

   - Fork or clone this repository to your local machine:
     ```bash
     git clone https://github.com/your-username/Virtual-Voice-Assistant.git
     cd Virtual-Voice-Assistant
     ```
2. **Set Up a Virtual Environment** (Recommended):

   - Create a virtual environment to isolate dependencies:
     ```bash
     python -m venv .venv
     .venv\Scripts\activate  # On Windows
     ```
   - On Unix-like systems (e.g., Linux/Mac):
     ```bash
     source .venv/bin/activate
     ```
3. **Install Dependencies**:

   - Install all required packages using the provided `requirements.txt` file:
     ```bash
     pip install -r requirements.txt
     ```
4. **Verify Installation**:

   - Run the script to ensure everything works:
     ```bash
     python Virtual_Assistant.py
     ```

## Usage

- **Run the Assistant**:

  - Activate the virtual environment (if used) and execute the script:
    ```bash
    python Virtual_Assistant.py
    ```
  - The assistant will greet you based on the time of day and listen for voice commands.
- **Supported Commands**:

  - "Open YouTube" – Opens YouTube in your default browser.
  - "Set a reminder" – Schedules a reminder (specify time, e.g., "in 10 minutes").
  - "Send WhatsApp message" – Sends a message to a contact (requires manual input via GUI).
  - "Open camera" – Opens your webcam.
  - "Tell me the time" – Announces the current time.
  - "Wikipedia [topic]" – Provides a summary from Wikipedia (e.g., "Wikipedia Python").
- **Customization**:

  - Edit `Virtual_Assistant.py` to add new commands or modify existing ones.
  - Update email settings in the `send_email_jarvis` function with your SMTP credentials.

## Troubleshooting

- **Microphone Errors**: Ensure your microphone is properly configured and accessible.
- **Missing Modules**: Verify all dependencies are installed via `pip list` and match `requirements.txt`.
