# Brenton's Guitar Ear Trainer — User & Technical Manual

Welcome to **Brenton's Guitar Ear Trainer**, a standalone interactive environment explicitly engineered to bridge functional pitch training with native guitar visualizations. The system generates context-aware, scale-correct intervals and tracks your microphone input in real-time, matching standard pitch configurations against standard notation systems and guitar tablature formatting.

---

## 🛠️ Step-by-Step Operating Instructions

### 1. Choose Your Exercise Type
The **Exercise Type** dropdown, top-left of the dashboard pane, controls which drill engine generates your notes[cite: 1]. A one-line explainer updates underneath the dropdown whenever you change it, so you always know what you're about to practice[cite: 1]. The four available modes:

* **Musical Phrase** — The original riff engine. Composes authentic, musical-sounding licks within your chosen scale, drawing from classic archetypes like climbing runs, call-and-response cells, arpeggio skips, and neighbor-tone turns[cite: 1]. Best for ear training that sounds like real playing rather than a drill.
* **Scale Run (Linear)** — A straight, stepwise run through the scale, starting from a random point each time rather than always from the root[cite: 1]. Each run is randomly either ascending or descending, so you get both directions across a session without needing to pick one[cite: 1]. This trains you to recognise exactly where you are within the scale shape, not just play it from the top.
* **3 Notes Per String** — The classic technique-building pattern guitarists drill every day[cite: 1]. Each exercise picks one random string (within your fretboard focus range) and drills 3 consecutive in-range notes on it, low to high[cite: 1]. Click **Start Session** or **Play Again** for a new random string each round. If your focus range is too narrow to fit 3 notes on any string, the app will prompt you to widen it[cite: 1].
* **Scale Sequence** — Groups of scale notes that shift up the scale one note at a time — for example, with a group size of 4: 1-2-3-4, then 2-3-4-5, then 3-4-5-6[cite: 1]. The group size is selectable (2 and up), and each round picks a fresh random window of that size rather than always starting at the same spot, building finger independence and scale fluency across the whole neck[cite: 1].

For **3 Notes Per String**, the note count is fixed at 3 and the **Total Notes to Play** field greys out automatically, since the exercise structure itself defines the note count[cite: 1]. For **Musical Phrase** and **Scale Run**, that field stays active and sets how many notes are in each generated riff or run[cite: 1]. For **Scale Sequence**, the same field relabels itself to **Group Size** and sets how many notes are in each shifting window[cite: 1].

### 2. Configure the Generation Matrix
Before launching an exercise session, customize the problem space constraints via the top dashboard pane[cite: 1]:
* **Root Key & Scale Type:** Establish the harmonic center (e.g., E Minor Pentatonic or C Major)[cite: 1]. The engine calculates exact relative frequencies instead of pulling arbitrary pitch loops[cite: 1].
* **Total Notes to Play:** Set this value to `1` to run **Single Note Target Training** (Musical Phrase and Scale Run only)[cite: 1]. Set it to `2` or higher (up to `16`) to dynamically swap the system into **Multi-Note Riff Mode**[cite: 1]. Locked to 3 automatically when 3 Notes Per String is the active exercise; relabels to **Group Size** and stays user-selectable when Scale Sequence is active[cite: 1].
* **Rhythm:** All exercises play strictly on the beat (quarter notes), keeping the timing simple and locked to the downbeat pulse.
* **Click Track:** In Multi-Note Riff Mode, switch this to *4-Beat Count-In* to hear a natural musician's count-in ("1, 2, 3, 4") on the metronome click before the riff plays. It replays before every listen, including "Play Again." Leave it *Off* for no count-in. This option has no effect in Single Note mode.
* **Tempo Controls:** Drag the slider or dial the parameters between 40 BPM and 180 BPM to determine playback speed[cite: 1].

### 3. Isolate the Fretboard Focus Range
* Beneath the parameter fields lies a dynamic 13-key focus strip labeled **Open** through **Fret 12**[cite: 1].
* **To Select a Range:** Click your target minimum boundary fret button once, then click your target maximum boundary fret button second[cite: 1]. 
* The interface highlights the active block, forcing all procedural single-note, riff, or drill engine notes to spawn exclusively inside this designated physical guitar tier[cite: 1].

### 4. Execution & Training Interaction Loop
1. Click **Start Session**[cite: 1]. This will invoke your browser's Web Audio Context permissions window[cite: 1]. Grant access to your microphone device[cite: 1].
2. The trainer instantly processes a scale-correct musical sequence — shaped by whichever exercise type is active — sounding the prompt using a dual-oscillator acoustic synth framework[cite: 1].
3. **Analyze & Play Back:** 
   * Hum, sing, or strike your physical guitar strings into your microphone[cite: 1]. 
   * The system samples your output through a native autocorrelation pitch-tracker[cite: 1].
   * The visual HUD status panel updates on the fly[cite: 1]. If you are slightly off-pitch, it changes color, warning you with clear pitch correction advice[cite: 1].
   * Match the correct frequency steadily for 5 frames to clear the note target[cite: 1].
4. If you miss a note or need a reminder, click **Play Again**[cite: 1].

### 5. Reading the Realigned Answer Panels
When you struggle with an exercise or clear the phase, click **Reveal Answer** to deploy the visualization engines[cite: 1]:
* **The Standard Notation Canvas:** Standard rendering vectors draw a traditional 5-line musical staff layout[cite: 1]. The Treble G-Clef glyph (`𝄞`) sits accurately on the baseline grid, looping its inner core exactly around the second line from the bottom (G4 line)[cite: 1]. Sharp accidentals (`♯`) and custom overhead/under-hanging ledger lines align naturally beside note heads following strict engraving standards (transposed up one octave for native guitar representation)[cite: 1].
* **The Interactive Fretboard Map:** If you are testing a single note, an explicit red marker pops up over the target string matrix, displaying the precise location of the fret to finger[cite: 1].
* **The Grid-Aligned Tablature System:** In Multi-Note Riff Mode, the app drops a standard 6-line textual ASCII tab string[cite: 1]. Beat timeline markers (`1`, `2`, `3`, `4`) sit anchored directly above the note columns with perfect character-by-character structural padding alignment, ensuring absolute readability[cite: 1].

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