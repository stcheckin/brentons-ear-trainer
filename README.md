#### File 2: README.md
# Brenton's Guitar Ear Trainer — User & Technical Manual

Welcome to **Brenton's Guitar Ear Trainer**, a standalone interactive environment explicitly engineered to bridge functional pitch training with native guitar visualizations[cite: 1]. The system generates context-aware, scale-correct intervals and tracks your microphone input in real-time, matching standard pitch configurations against standard notation systems and guitar tablature formatting[cite: 1].

---

## 🛠️ Step-by-Step Operating Instructions

### 1. Configure the Generation Matrix
Before launching an exercise session, customize the problem space constraints via the top dashboard pane[cite: 1]:
* **Root Key & Scale Type:** Establish the harmonic center (e.g., E Minor Pentatonic or C Major)[cite: 1]. The engine calculates exact relative frequencies instead of pulling arbitrary pitch loops[cite: 1].
* **Difficulty:** Choose **Beginner** (the default) or **Intermediate**. This is a preset, not a lock — it snaps Scale Type, Rhythm, Exercise Format, note count, and fret range to sensible values for that level, but every control can still be adjusted by hand afterward. Beginner narrows Scale Type to the pentatonic options, Rhythm to Quarter Notes, Exercise Format to Riff and Ascending/Descending, caps Total Notes at 4, and sets the fret range to Open–5. Intermediate unlocks everything else the app supports. There is no Advanced tier by design — the app is meant to stay quick to pick up.
* **Exercise Format:** Choose what shape the exercise takes. **Riff** is a freeform improvised phrase; the other five are well-known guitar practice patterns — **Ascending/Descending**, **3-Note-Per-String**, **Scalar Sequence in Thirds**, **Groups of 4**, and **Triad Climb**. A one-line plain-English description of the selected format always appears just below the dropdown.
* **Total Notes to Play:** Only relevant in **Riff** format. Set this value to `1` to run **Single Note Target Training**[cite: 1]. Set it to `2` or higher (up to `16`, or `4` in Beginner difficulty) to dynamically swap the system into **Multi-Note Riff Mode**[cite: 1]. For every other Exercise Format, this field is replaced by a read-only **"This Exercise"** note count, since defined patterns derive their own length from the current scale and fret range rather than taking a user-chosen count.
* **Max Rhythm Form:** Dictates the micro-timing grid constraint[cite: 1]. Choosing *Quarter Notes* locks generated targets strictly onto downbeats[cite: 1]. Moving to *8th Notes*, *Triplet Notes*, or *16th Notes* commands the mathematical model to scatter notes across authentic offbeat slots (Riff format) or to space a defined pattern more densely (other formats), keeping the primary downbeat pulse as the core anchor line[cite: 1].
* **Tempo Controls:** Drag the slider or dial the parameters between 40 BPM and 180 BPM to determine playback speed[cite: 1].

### 2. Isolate the Fretboard Focus Range
* Beneath the parameter fields lies a dynamic 13-key focus strip labeled **Open** through **Fret 12**[cite: 1].
* **To Select a Range:** Click your target minimum boundary fret button once, then click your target maximum boundary fret button second[cite: 1]. 
* The interface highlights the active block, forcing all procedural single-note or riff engine notes to spawn exclusively inside this designated physical guitar tier[cite: 1].

### 3. Execution & Training Interaction Loop
1. Click **Start Session**[cite: 1]. This will invoke your browser's Web Audio Context permissions window[cite: 1]. Grant access to your microphone device[cite: 1].
2. The trainer instantly processes a scale-correct musical sequence, sounding the prompt using a structural node synthesis patch that models real acoustic string attack, pluck presence, and body resonance.
3. **Analyze & Play Back:** 
   * Hum, sing, or strike your physical guitar strings into your microphone[cite: 1]. 
   * The system samples your output through a native autocorrelation pitch-tracker[cite: 1].
   * The visual HUD status panel updates on the fly[cite: 1]. If you are slightly off-pitch, it changes color, warning you with clear pitch correction advice[cite: 1].
   * Match the correct frequency steadily for 5 frames to clear the note target[cite: 1].
4. If you miss a note or need a reminder, click **Play Again**[cite: 1].

### 4. Reading the Realigned Answer Panels
When you struggle with an exercise or clear the phase, click **Reveal Answer** to deploy the visualization engines[cite: 1]:
* **The Standard Notation Canvas:** Standard rendering vectors draw a traditional 5-line musical staff layout[cite: 1]. The Treble G-Clef glyph (`𝄞`) sits accurately on the baseline grid, looping its inner core exactly around the second line from the bottom (G4 line)[cite: 1]. Sharp accidentals (`♯`) and custom overhead/under-hanging ledger lines align naturally beside note heads following strict engraving standards (transposed up one octave for native guitar representation)[cite: 1].
* **The Interactive Fretboard Map:** If you are testing a single note, an explicit red marker pops up over the target string matrix, displaying the precise location of the fret to finger[cite: 1].
* **The Grid-Aligned Tablature System:** In Multi-Note Riff Mode, the app drops a standard 6-line textual ASCII tab string[cite: 1]. Sub-beat timeline markers (`1`, `e`, `+`, `a`) sit anchored directly above the note columns with perfect character-by-character structural padding alignment, ensuring absolute readability[cite: 1].

---

## 🎙️ Hands-Free Voice Commands
The software incorporates a native speech processing engine[cite: 1]. While an exercise status loop is engaged, you can speak directly into your microphone using these structural command verbs[cite: 1]:
* `"Next"` — Commands the interface to execute `nextExercise()`, instantly cleaning the canvas and generating a brand new configuration[cite: 1].
* `"Repeat"` — Commands the media engine to replay the active tone or structural riff block[cite: 1].
* `"Faster"` — Speeds up the target tempo matrix by 20 BPM[cite: 1].
* `"Slower"` — Lowers the active tempo matrix by 20 BPM[cite: 1].

---

## 🖥️ Local Installation & Technical Deployment
No compilation layers or build installations are needed to deploy or utilize the ear trainer[cite: 1]:
1. Save the codebase chunk listed in `File 1: index.html` locally onto your computer file system under the filename `index.html`[cite: 1].
2. Double-click the saved `index.html` file to run it locally inside any modern standard desktop web browser (e.g., Chrome, Safari, Firefox, Edge)[cite: 1].
3. Ensure you are running the environment locally or over a secure `https://` origin line, as modern browser engines block microphone access loops on insecure network connections[cite: 1].