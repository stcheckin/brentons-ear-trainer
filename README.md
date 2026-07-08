Brenton's Ear Trainer
A web-based, hands-free ear training application designed for guitarists to practice identifying and matching musical intervals and scale notes.

Features
Scale & Root Selection: Choose your root note and scale type (Major or Natural Minor) to customize your practice session.

Fretboard Windowing: Interactively select specific fret ranges (e.g., frets 0-5) to focus on specific positions on the neck.

Pitch-Matching Engine: Uses the Web Audio API to analyze your microphone input and compare your vocal pitch against the target note.

Hands-Free Controls: Use voice commands like "Next" to advance to the next note or "Repeat" to hear the target note again.

Visual Feedback: Real-time pitch correction hints (Too Low/Too High/Target Match) and a fretboard visualizer to show where the note is located.

Feedback Blackout Window: Includes a 1.5-second "cooldown" window after note playback to prevent the microphone from detecting its own audio output.

How to Use
Select Scale/Range: Choose your preferred root note and scale from the dropdowns at the top. Click the fretboard area to define your "window" of focus.

Start Session: Click "Start Session" to begin. You will be prompted by the browser to allow microphone access.

Voice Matching:

The app will play the target note.

Sing the note to match the pitch.

Once a successful match is detected, you will be prompted to play the same note on your guitar.

Commands: Use your voice to say "Next" or "Repeat" to control the session without putting down your instrument.

Development & Setup
Prerequisites
A modern web browser (Chrome or Edge recommended).

A microphone connected to your computer.

The application must be served over HTTPS or localhost to access the Microphone and Web Audio APIs.

Running Locally
Clone this repository to your machine.

Since this is a single-file application, you can open gemini-code-1783502298442.html directly in your browser.

Note: If you see a blank page or missing UI, ensure you are running it through a local development server (e.g., VS Code "Live Server" extension) to satisfy browser security requirements.

Troubleshooting
UI Not Appearing: If buttons or selectors are missing, check the browser console (F12) for script errors. Ensure your local server is correctly serving the file.

Microphone Not Working: Ensure your browser has explicit "Allow" permissions for your microphone for the specific URL.

Audio Not Playing: The browser blocks audio until the first user interaction (the "Start Session" click). Ensure you are clicking this button to "resume" the AudioContext.

Contributing
We welcome contributions to help improve the pitch detection accuracy and UI stability. To contribute:

Fork this repository.

Create a new branch for your feature.

Submit a Pull Request with a description of your changes.
