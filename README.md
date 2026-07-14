# Brenton's Guitar Ear Trainer — User & Technical Manual

Welcome to **Brenton's Guitar Ear Trainer**, a standalone interactive environment explicitly engineered to bridge functional pitch training with native guitar visualizations. The system generates context-aware, scale-correct, highly musical intervals and tracks your microphone input in real-time, matching standard pitch configurations against standard notation systems and precise guitar tablature formatting.

---

## 🛠️ Step-by-Step Operating Instructions

### 1. Configure the Generation Matrix
Before launching an exercise session, customize the problem space constraints via the top dashboard pane:
* **Root Key & Scale/Vibe Type:** Establish the harmonic center (e.g., E Minor Pentatonic or C Major). The phrase builder creates natural, stepwise progressions and pentatonic guitar licks instead of mechanical, random leaps.
* **Total Notes to Play:** Set this value to `1` to run **Single Note Target Training**. Set it to `2` or higher (up to `16`) to dynamically swap the system into **Multi-Note Riff Mode**.
* **Max Rhythm Syncopation:** Dictates the micro-timing grid constraint. Choosing *Quarter Notes Only* locks targets onto downbeats. Moving to *8th*, *Triplet*, or *16th Notes* commands the mathematical engine to weave in authentic rhythmic subdivisions, allowing users to practice alignment with both downbeats and offbeats.
* **Groove Tempo:** Drag the slider between 40 BPM and 180 BPM to determine playback speed.

### 2. Isolate the Fretboard Focus Range
* Beneath the parameter fields lies a dynamic 13-key focus strip labeled **Open** through **Fret 12**.
* **To Select a Range:** Click your target minimum boundary fret button once, then click your target maximum boundary fret button second. 
* The interface highlights the active block, forcing all procedural note engines to spawn exclusively inside this designated physical guitar tier.

### 3. Execution & Training Interaction Loop
1. Click **Start Session**. This will invoke your browser's Web Audio Context permissions window. Grant access to your microphone device.
2. The trainer instantly processes a scale-correct musical phrase, sounding the prompt using a warm, dual-oscillator acoustic synth framework.
3. **Analyze & Play Back:** 
   * Play the phrase back on your physical guitar or sing directly into your microphone. 
   * The system samples your output through a native autocorrelation pitch-tracker.
   * The coach's HUD feedback panel updates on the fly with real-world studio encouragement, giving clear guidance if you are sharp or flat.
   * Match the target frequencies consistently across frames to clear the sequence.
4. If you miss a note or want to re-hear the vibe, click **Play Again**.

### 4. Reading the Realigned Answer Panels
When you struggle with an exercise or clear the phase, click **Reveal Lick** to deploy the visualization engines:
* **The Standard Notation Canvas:** Standard rendering vectors draw a traditional 5-line musical staff layout. The Treble G-Clef glyph (`𝄞`) sits accurately on the baseline grid, looping its inner core exactly around the second line from the bottom (G4 line). Sharp accidentals (`♯`) and ledger lines align naturally beside note heads.
* **The Grid-Aligned Tablature System:** In Multi-Note Riff Mode, the app drops a standard 6-line textual ASCII tab string. Sub-beat timeline markings (`1`, `e`, `+`, `a`) sit anchored directly above the note columns with character-by-character structural padding alignment, ensuring that variations for double-digit frets (e.g., frets 10, 11, 12) never throw off the vertical timing alignment.

---

## 🎙️ Hands-Free Voice Commands
The software incorporates a native speech processing engine. While an exercise status loop is engaged, you can speak directly into your microphone using these structural command verbs:
* `"Next"` — Commands the interface to execute `nextExercise()`, instantly cleaning the canvas and generating a brand new configuration.
* `"Repeat"` — Commands the media engine to replay the active tone or structural riff block.
* `"Faster"` — Speeds up the target tempo matrix by 20 BPM.
* `"Slower"` — Lowers the active tempo matrix by 20 BPM.

---

## 🖥️ Local Installation & Technical Deployment
No compilation layers or build installations are needed to deploy or utilize the ear trainer:
1. Save the codebase chunk listed in `File 1: index.html` locally onto your computer file system under the filename `index.html`.
2. Double-click the saved `index.html` file to run it locally inside any modern standard desktop web browser (e.g., Chrome, Safari, Firefox, Edge).
3. Ensure you are running the environment locally or over a secure `https://` origin line, as modern browser engines block microphone access loops on insecure network connections.