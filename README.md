# Brenton's Guitar Ear Trainer

An adaptive, web-based ear training application designed specifically for guitarists. The application generates highly melodic, context-aware riffs based on selected guitar scales, allows real-time interactive pitch tracking via microphone input, and displays musical solutions in both standard notation and cleanly spaced guitar tablature[cite: 1].

---

## 🚀 Key Features & Architectural Enhancements

### 1. Dynamic Rhythmic Engine
* **Flexible Beats Configuration:** The "Total Notes to Play" control references the explicit `#beat-count` parameters mapping out dynamically inside a $4/4$ time structure spanning up to 4 bars (16 quarter beats maximum)[cite: 1].
* **Grid Subdivision Spacing:** Rather than compressing notes back-to-back, the app randomly and authentically spaces notes across subdivisions (Quarter notes, 8th notes, Triplet divisions, or 16th notes) based on the **Max Rhythm Form** chosen[cite: 1].

### 2. Melodic & Guitar-Friendly Riff Logic
* **Musically Intelligible Phrases:** Instead of entirely chaotic, unplayable random intervals, the generator utilizes bounded scales (Major, Minor, Major Pentatonic, Minor Pentatonic) and restricts subsequent movements to musical step-wise motions, scale-wise thirds, or perfect fourths and fifths[cite: 1].
* **Guitar Archetype Phrasing:** Riffs are calculated using realistic play models, alternating between root chord arpeggiations, linear pentatonic box shape paths, and natural progressive resolutions to mimic physical guitar solos.

### 3. Layout Stability (No-Bounce UI)
* **Pre-allocated Container States:** The tracking UI employs structural CSS visibility hidden rules and explicit element heights (`.status-area` and `.notation-container`)[cite: 1]. Elements like the standard notation SVG frame do not cause page elements to violently shift or "bounce" when pitch markers appear or fade out[cite: 1].

### 4. Advanced Visual Realism
* **Continuous Tablature Design:** Removed traditional vertical measure line dividers (`|`) that often segment short computer phrases awkwardly[cite: 1]. Tabs now flow with continuous double-hyphen buffers (`--`) simulating real guitar transcription documents[cite: 1].
* **Integrated Structural Timelines:** Multi-note tabs include a dynamic tracking timeline matrix right above the strings (e.g., `1  +  2  +  3  +  4  +`) to immediately visually call out exact micro-beat intervals and hidden rest pauses cleanly for beginners[cite: 1].
* **Compact Presentation Grid:** The tablature text output styling drops structural horizontal overflow scrolls, utilizing fixed space font tracking to fit the complete 4-bar phrase smoothly into a single view slice[cite: 1].

---

## 🛠️ Technological Stack

* **Frontend Layout:** Semantic HTML5, CSS3 Custom Properties (CSS variables)[cite: 1].
* **Audio Synthesis:** Web Audio API (`OscillatorNode` utilizing a primary warm triangle shape blended with subtle second-harmonic overtone configurations, bounded to a pick-attack transient gain envelope)[cite: 1].
* **Pitch Detection:** Custom Time-Domain Digital Autocorrelation Algorithm analyzing Root-Mean-Square (RMS) signal amplitudes to calculate frequency pitch in cents relative to the active target musical note frequency ($f_{target}$)[cite: 1].
* **Voice Commands API:** Native Web Speech API (`webkitSpeechRecognition`) mapping continuous phrase strings to programmatic actions like speed changes or exercise generation[cite: 1].

---

## 📖 How to Use

1. **Setup Session:** Select your desired **Root Key** and target **Scale Type**[cite: 1].
2. **Define Parameters:** Select the **Total Notes to Play** (up to 16 notes) and set your subdivision limits using **Max Rhythm Form**[cite: 1]. Set your target **Tempo (BPM)**[cite: 1].
3. **Train:** Click **Start Session**[cite: 1]. 
   * Listen closely to the generated note or riff phrase[cite: 1].
   * Play or sing the sequence back note-by-note into your device microphone[cite: 1].
   * Alternatively, use integrated hands-free voice commands[cite: 1]:
     * **"Next"**: Advance to the next exercise target[cite: 1].
     * **"Repeat"**: Replay the current active phrase generation[cite: 1].
     * **"Faster"**: Automatically increases tempo metrics by $+20$ BPM[cite: 1].
     * **"Slower"**: Automatically decreases tempo metrics by $-20$ BPM[cite: 1].
4. **Reveal:** Click **Reveal Answer** to see the interactive standard notation layout, horizontal chronological fretboard pathing numbers (for single-note mode), and real-time spaced text tabs simultaneously[cite: 1].