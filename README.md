# Advanced Voice Changer Tool

This Django application provides an advanced voice changer with multiple customization options for audio transformation.

## Features

- **Pitch Shifting**: Adjust the pitch of audio up or down
- **Speed Control**: Speed up or slow down the audio
- **Volume Adjustment**: Increase or decrease volume
- **Reverb Effect**: Add atmospheric reverberation
- **Echo Effect**: Add echo/delay effect
- **Gender Voice Transformation**: Transform voice to sound more masculine or feminine
  - Male Voice
  - Female Voice
  - Neutral Voice
- **Formant Shifting**: Adjust vocal tract characteristics
- **Preset Effects**: Quick access to popular voice effects
  - Chipmunk
  - Deep Voice
  - Robot
  - Alien

## Installation

1. Clone the repository
2. Install the required dependencies:
   ```
   pip install django pydub
   ```

3. Install Sox (Sound eXchange) for advanced audio processing:
   - On Ubuntu/Debian: `sudo apt-get install sox libsox-fmt-all`
   - On macOS: `brew install sox`
   - On Windows: Download and install from [Sox website](https://sourceforge.net/projects/sox/)

4. (Optional) Install Rubberband for improved formant shifting:
   - On Ubuntu/Debian: `sudo apt-get install rubberband-cli`
   - On macOS: `brew install rubberband`
   - On Windows: Download from [Rubberband website](https://breakfastquay.com/rubberband/)

5. Run migrations:
   ```
   python manage.py migrate
   ```

6. Start the development server:
   ```
   python manage.py runserver
   ```

## Usage

1. Open the application in your web browser
2. Upload an audio file (WAV, MP3, etc.)
3. Adjust the parameters to your liking:
   - Pitch: -12 to +12 semitones
   - Speed: 0.5x to 3.0x
   - Volume: -10 to +10 dB
   - Reverb: 0% to 100%
   - Echo: 0% to 100%
   - Formant Shift: -10 to +10 (lower values for masculine, higher for feminine)
   - Voice Gender: Male, Female, or Neutral
4. Click "Process Audio" to apply the effects
5. Play the resulting audio and download if desired

## Technical Details

The application uses:
- Django for the web framework
- PyDub for audio processing
- Sox for advanced audio effects (pitch shifting, reverb, echo)
- Rubberband (optional) for improved formant shifting and voice gender transformation

## Troubleshooting

- If you encounter issues with effects not applying, make sure Sox is properly installed and available in your system PATH.
- For audio format errors, ensure you're using a supported audio format.
