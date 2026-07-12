# Brenton's Guitar Ear Trainer

An adaptive, web-based ear training application designed specifically for guitarists. The application generates highly melodic, context-aware riffs based on selected guitar scales, allows real-time interactive pitch tracking via microphone input, and displays musical solutions in both standard notation and cleanly spaced guitar tablature.

---

## 🚀 Key Features & Architectural Enhancements

### 1. Dynamic Rhythmic Engine
* **Flexible Beats Configuration:** The "Total Notes to Play" control references the explicit `#beat-count` parameters mapping out dynamically inside a 4/4 time structure spanning up to 4 bars (16 quarter beats maximum).
* **Grid Subdivision Spacing:** Rather than compressing notes back-to-back, the app randomly and authentically spaces notes across subdivisions (Quarter notes, 8th notes, Triplet divisions, or 16th notes) based on the **Max Rhythm Form** chosen.

### 2. Melodic & Bounded Focus Selection Logic
* **Musically Intelligible Phrases:** Bounded scales (Major, Minor, Major Pentatonic, Minor Pentatonic) determine melodic note structures, matching authentic intervals over step-wise sequences.
* **Fret Range Selection Isolation:** A compact selector strip from Open to Fret 12 sits cleanly inside the exercise setup panel. Min and max limits allow users to restrict exercises to narrow sectors, establishing absolute note location familiarity before expanding to broader zones.

### 3. Layout Stability & Precision Rendering
* **Pre-allocated Container States:** Elements like standard notation panels preserve zero-bounce layout constraints through explicit height boundaries and visibility transformations.
* **Accurate Treble Clef Balancing Vector:** The graphic rendering loops center directly across standard lines, matching standard formatting conventions, while procedural note placement accurately pairs accidental elements ($♯$) and custom multi-ledger parameters directly to the executed frequency array.
* **Pixel-Perfect Tablature Alignment Grid:** Fixed structural widths inside the generator buffer force sub-beat indicators (`1`, `e`, `+`, `a`) to align strictly overhead of note columns, eradicating alignment drift for multi-digit frets.