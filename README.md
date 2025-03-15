# Zoomageddon 🔥

A chaotic desktop prank application that records audio, takes screenshots, plays random sounds, and opens random websites while you're browsing.

![image](https://github.com/user-attachments/assets/422f888e-cc11-4d15-b86f-efb0b43c920b)

## Description

Zoomageddon is a multi-threaded Python application designed to create a hilariously disruptive computing experience. It runs three parallel processes:

1. **Audio Recording & Response Generation**: Records your audio, takes screenshots, analyzes what it sees and hears, and then generates sarcastic voice responses.
2. **Random Sound Player**: Plays random weird sound effects at unpredictable intervals.
3. **Random Website Opener**: Opens bizarre websites randomly when a browser window is detected.

This project was made @ **Scrapyard Hyderabad 2025** by **Team CodeRed**

## Features

- Voice recording and transcription using AssemblyAI
- Screenshot capture and image analysis with LLaMA 3.2 Vision
- Text-to-speech response generation
- Random sound playback from a local directory
- Browser detection and random website opening
- Multi-threaded operation to maximize chaos

## Requirements

### Python Libraries
- time
- base64
- pyttsx3
- pyautogui
- pyaudio
- wave
- assemblyai
- groq
- os
- random
- pygame
- webbrowser
- threading
- platform
- pygetwindow

### API Keys
- AssemblyAI API key
- Groq API key

### Additional Requirements
- A folder named "Weird Sounds" containing .mp3 or .wav sound files
- Internet connection for API calls
- A microphone and speakers

## Quick Start: Pre-configured Version

If you don't want to set up your own music, API keys, or configure the application yourself, you can use our pre-configured version:

### Pre-configured Package

1. Download the pre-configured package from example execution folder.

2. Install all requirements.
   ```
   pip install -r requirements.txt
   ```

3. Run the zoomageddon example execution file:
   ```
   python zoomageddon_exec.py
   ```

The pre-configured version includes:
- 10+ weird sound effects
- Working API keys (with usage limits)
- Default configuration settings
- 10+ prank websites to redirect to

### Usage Notes for Pre-configured Version

- The included API keys have limited usage. For extended use, please replace with your own keys.
- The pre-configured package works out of the box, but has fewer customization options than the source code version.
- Updates to the pre-configured version may lag behind the main repository.

To switch to the full version later, follow the standard installation instructions in the section above.

## Installation

### 

1. Clone the repository.

2. Install required packages:
   ```
   pip install -r requirements.txt
   ```

3. Create a "Weird Sounds" folder and add some .mp3 or .wav files to it.

4. Set up your API keys:
   - Register for AssemblyAI at https://www.assemblyai.com/
   - Register for Groq at https://console.groq.com/
   - Update the API keys in the code:

      ```python
     aai.settings.api_key = "YOUR_ASSEMBLYAI_API_KEY"
     client = Groq(api_key='YOUR_GROQ_API_KEY')
     ```

## Usage

Run the program with Python:
```
python zoomageddon.py
```

To stop the program, press `Ctrl+C` in the terminal.

## How It Works

### Process 1: Audio Recording & Response Generation
- Records 5 seconds of audio and saves it as "output.wav"
- Takes a screenshot and saves it as "screenshot.png"
- Transcribes the audio using AssemblyAI
- Analyzes the screenshot using LLaMA 3.2 Vision model
- Generates a sarcastic response based on the transcription and image analysis
- Converts the response to speech

### Process 2: Random Sound Player
- Loads sound files from the "Weird Sounds" directory
- Waits a random period (5-15 seconds)
- Plays a random sound file

### Process 3: Random Website Opener
- Checks if a browser window is currently in focus
- If a browser is detected, opens a random website from the predefined list
- Waits 10 seconds before potentially opening another website

## Customization

### Adding New Sounds
Add .mp3 or .wav files to the "Weird Sounds" directory.

### Modifying Website List
Edit the `websites` list in the code to add or remove websites.

### Adjusting Timing
- Change the recording duration by modifying the `record_seconds` parameter in the `record_audio` function call
- Adjust the website opening frequency by changing the sleep time in `process_3`
- Modify the sound playing frequency by changing the random range in `process_2`

## Disclaimer

This software is provided for entertainment purposes only. The creators take no responsibility for any chaos, disruption, or awkward situations that may arise from its use. Use at your own risk!

## License

Apache-2.0 license

## Contact

For any inquiries or assistance, you can reach me at:
* pveekshithrao@gmail.com
* jimit.nahar@gmail.com
* gnv.vaibhav@gmail.com
* snithik.reddy.techie@gmail.com
