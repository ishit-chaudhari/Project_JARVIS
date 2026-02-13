# JARVIS AI Assistant

A modular, voice-controlled AI assistant featuring a futuristic HUD interface, advanced automation skills, and a "living" responsiveness. Built with Python, PyQt6, and Groq's LLM engine.

## 🌟 Core Features

- **Futuristic HUD**: A "Starark-style" interface featuring:
  - **Arc Reactor**: Central animated core that pulses with voice activity.
  - **Hexagon Panel**: Dynamic background visualizations.
  - **Telemetry**: Real-time visual feedback bars.
- **Dual Modes**: 
  - **Voice Mode**: Full hands-free interaction using speech recognition and TTS.
  - **Text Mode**: Silent command-line interface for distinct environments.
- **Modular Skill System**: Ease of extensibility. New capabilities can be added as drop-in modules in the `skills/` directory.

## 🧠 Skills & Capabilities

JARVIS is equipped with a diverse set of skills:

### 🌐 Web & Communication
- **Web Operations**: Performs Google searches and opens websites (`web_ops`).
- **WhatsApp**: Automates messaging via selenium-driven web interface (`whatsapp_skill`).
- **Email**: Capable of managing email operations (`email_ops`).

### 👁️ Vision & Sensing
- **Computer Vision**: Real-time object detection using YOLO (`detection_skill`).
- **Camera Access**: Captures photos and processes visual input (`camera_skill`).
- **Screen Awareness**: Takes and analyzes screenshots (`screenshot_ops`).
- **Gemini Live**: Advanced multimodal interaction capabilities (`gemini_live_skill`).

### 🛠️ System Control
- **System Operations**: Controls volume, screen brightness, and application management (`system_ops`).
- **File Management**: Create, read, and organize files (`file_ops`).
- **Context Awareness**: Tracks date, time, and maintains long-term memory (`memory_ops`, `datetime_ops`).

## 🚀 Setup & Installation

### Prerequisites
- Python 3.10+
- A [Groq API Key](https://console.groq.com/) for the LLM brain.

### Installation

1. **Clone the Repository**
   ```bash
   git clone <YOUR_REPO_URL>
   cd JARVIC
   ```

2. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```
   *Note: This project relies on `PyQt6` for the GUI and `ultralytics` for vision.*

3. **Configure Environment**
   Create a `.env` file in the root directory:
   ```env
   GROQ_API_KEY=your_key_here
   # Add other keys as needed by specific skills
   ```

## 💻 Usage

**Standard Voice Mode (with GUI)**
```bash
python main.py
```
- The HUD will launch.
- Speak naturally to interact.
- Click the center reactor to **Pause/Resume** listening.

**Text-Only Mode**
```bash
python main.py --text
```
- Runs in the terminal without voice I/O. Ideal for debugging or quiet environments.

## 📂 Project Structure

- `core/`: The brain (Engine), voice processing, and skill registry.
- `gui/`: PyQt6 application logic and rendering.
- `skills/`: Individual capability modules.
- `assets/`: Images and resources.

