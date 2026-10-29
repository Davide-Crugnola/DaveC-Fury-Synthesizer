# DaveC-Fury Analog Synthesizer 🎹⚡

An interactive, browser-based quad-oscillator (4-VCO) analog subtractive synthesizer built entirely using the **Web Audio API** and **Tailwind CSS**. Inspired by classic vintage hardware synthesizers (like the Korg Mono/Poly), DaveC-Fury combines authentic analog DSP modeling with modern Web MIDI support and a custom 200-preset bank architecture.

![DaveC-Fury Synthesizer](https://img.shields.io/badge/Audio--Engine-Web%20Audio%20API-amber) ![MIDI](https://img.shields.io/badge/MIDI-Web%20MIDI%20API-emerald) ![License](https://img.shields.io/badge/License-MIT-blue)

---

## 🌟 Key Features

* **Quad-Oscillator (4-VCO) Audio Engine:**
  * **4 Independent Oscillators:** Choice of *Sawtooth, Square, Triangle, and Pulse-Width Modulation (PWM)* waveforms across 32' to 2' octaves with fine detuning.
  * **Voice Allocation Modes:** Monophonic, Unison (with spread control), Chord/Polyphonic, and classic Mono/Poly-style **4-VCO Round-Robin Cycling**.
  * **Portamento / Glide:** Adjustable glide time with *Always* or *Legato* triggering.
  * **VCO Hard Sync:** Oscillator-sync emulation for rich, tearing lead tones.

* **24dB VCF & Modulation:**
  * **Resonant Ladder Filter:** 24dB/octave Low-Pass Filter with resonance, cutoff tracking, and dedicated Filter Envelope depth.
  * **Dual Envelopes:** Independent 4-stage (ADSR) envelopes for both Filter (EG1) and Amp (EG2).
  * **Modulation Generator (LFO):** Multi-waveform LFO with routing to Pitch, Cutoff, and Pulse Width.

* **54-Pattern Arpeggiator:**
  * Comprehensive arpeggiator supporting 54 rhythmic patterns (*Up, Down, Up/Down, Random, Converge/Diverge, Euclidean, Fibonacci, Brownian walk*, and more).
  * Variable BPM tempo control (40–240 BPM).

* **Integrated Master Effects Chain:**
  * **Drive / Distortion:** Soft-clip to heavy transistor saturation.
  * **Modulated Stereo Chorus:** Variable rate and depth.
  * **Syncable Delay:** Tempo-synced or free-running delay with feedback control.
  * **Convolution Reverb:** Algorithmic space and hall simulation.
  * **Bitcrusher:** Variable bit-depth and sample-rate reduction.
  * **Customable FX Routing:** Re-order effect modules on the fly.

* **200 Factory Preset Library:**
  * Categorized into 8 distinct banks: `BASS`, `LEAD`, `PAD`, `ARP`, `ANALOG`, `KEYS`, `SFX`, and `FX`.
  * Built-in **Bank Grid Manager** with search filtering and instant loading.
  * Export/Import single presets via JSON files.

* **Interactive Hardware Visuals & Input:**
  * **CRT Oscilloscope:** Real-time Waveform and FFT Spectrum signal visualizer.
  * **2-Octave Piano Keyboard:** Full QWERTY computer keyboard mapping + mouse/touch interaction.
  * **Web MIDI API Integration:** Play live using any external USB/MIDI keyboard controller.

---

## 🚀 Quick Start

No build step or node installation is needed! The synth is completely self-contained in a single Web page.

1. Clone or download this repository:
   ```bash
   git clone https://github.com/Davide-Crugnola/DaveC-Fury-Synthesizer.git
   ```

2. Open `DaveC_Fury_synthesizer.html` directly in any modern Web Browser (*Chrome, Edge, Firefox, or Safari*).

3. Click the **AUDIO START** button in the top right corner to activate the Web Audio context.

---

## 🎹 Keyboard Controls (QWERTY)

You can play the synth directly using your computer keyboard across 2 octaves ($C_3$ to $C_5$):

* **White Keys (Bottom Row):** `Z` `X` `C` `V` `B` `N` `M` `,` `.` `/` `Q`
* **Black Keys (Top Row):** `S` `D` `G` `H` `J` `2` `3` `5` `6` `7`
* **Octave Shift:** Use the `- OCT` and `+ OCT` buttons to transpose the active range up or down.

---

## 🛠️ Tech Stack

* **Web Audio API** — Custom Web Audio DSP graphs, custom oscillator generation, dynamics processing, and real-time audio visualization via AnalyserNode.
* **HTML5 Canvas** — CRT Oscilloscope rendering.
* **Tailwind CSS** — Hardware chassis, wood side panels, and panel graphics styling.
* **Web MIDI API** — Plug-and-play MIDI input.

---

## 📄 License

This project is open-source under the **MIT License**.