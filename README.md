# Brenton's Guitar Ear Trainer

An adaptive, web-based ear training application designed specifically for guitarists. The application generates highly melodic, context-aware riffs based on selected guitar scales, allows real-time interactive pitch tracking via microphone input, and displays musical solutions in both standard notation and cleanly spaced guitar tablature.

---

## 🚀 Key Features & Architectural Enhancements

### 1. Dynamic Rhythmic Engine
* **Flexible Beats Configuration:** The "Total Notes to Play" control references the explicit `#beat-count` parameters mapping out dynamically inside a 4/4 time structure spanning up to 4 bars (16 quarter beats maximum).
* **Grid Subdivision Spacing:** Rather than compressing notes back-to-back, the app randomly and authentically spaces notes across subdivisions (Quarter notes, 8th notes, Triplet divisions, or 16th notes) based on the **Max Rhythm Form** chosen.

### 2. Melodic & Guitar-Friendly Riff Logic
* **Musically Intelligible Phrases:** Instead of entirely chaotic, unplayable random intervals, the generator utilizes bounded scales (Major, Minor, Major Pentatonic, Minor Pentatonic) and restricts subsequent movements to musical step-wise motions, scale-wise thirds, or perfect fourths and fifths.
* **Guitar Archetype Phrasing:** Riffs are calculated using realistic play models, alternating between root chord arpeggiations, linear pentatonic box shape paths, and natural progressive resolutions to mimic physical guitar solos.
* **Fretboard Target Span Filtering:** Exercises can be isolated cleanly to designated horizontal sections on the neck (`#fret-span-select`). Choosing options like "Open to Fret 4" filters generated scale targets exclusively inside that visual bracket.

### 3. Layout Stability (No-Bounce UI)
* **Pre-allocated Container States:** The tracking UI employs structural CSS visibility hidden rules and explicit element heights (`.status-area` and `.notation-container`). Elements like the standard notation SVG frame do not cause page elements to violently shift or "bounce" when pitch markers appear or fade out.

### 4. Advanced Visual Realism
* **Precision Notation Placement:** The Treble Clef graphic loops elegantly around the second horizontal line from the bottom (the G line), and the note layout positions have been fine-tuned down to correctly represent pitch coordinates without causing false offset step anomalies.
* **Continuous Tablature Design:** Removed traditional vertical measure line dividers (`|`) that often segment short computer phrases awkwardly. Tabs now flow with continuous double-hyphen buffers (`--`) simulating real guitar transcription documents.
* **Proportional Tablature Scaling:** Dynamically scales font sizes depending on the absolute note count selected. This ensures wide runs compress evenly to fit the screen without clipping edge characters.