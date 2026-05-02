# 🎹 Pixel Piano

*A retro 8-bit chiptune synthesizer. Click keys or use your keyboard. Make bloopy music. No samples — pure oscillators.*

---

## What is this?

It's a pixel-art piano that sounds like it's from 1987. Click the keys or use your keyboard (A through L) to play notes. Tweak the waveform for classic video game sounds: square (NES-like), sawtooth (sharper), triangle (softer), sine (pure). Adjust attack and release for note envelope. Change octaves. Turn on the arpeggiator for automated patterns. Watch the frequency visualizer react to your playing.

Zero samples, zero latency, pure Web Audio API. It's like having a tiny synthesizer in your browser.

---

## Features

- **Virtual piano** — 15 keys (one octave + 2 extra notes)
- **Keyboard support** — A, W, S, E, D, F, T, G, Y, H, U, J, K, O, L map to keys
- **Waveform selection:** Square (8-bit), Sawtooth (sharp), Triangle (soft), Sine (pure)
- **ADSR envelope** — adjustable attack (0.01–1s) and release (0.01–2s)
- **Volume control**
- **Octave shift** — up/down buttons, supports octaves 0–7
- **Arpeggiator** — toggle on/off, plays up/down pattern automatically
- **Real-time frequency visualizer** — bar graph of output spectrum
- **Pixel aesthetic** — neon colors, simple UI, instant feedback
- **Single HTML file** — no dependencies

---

## How to Use

1. Open `index.html` (use speakers or headphones)
2. Click piano keys or press keyboard keys (see labels on keys)
3. Adjust waveform to change timbre
4. Tweak attack/release for shorter or longer notes
5. Change octave with +/- buttons
6. Enable arpeggiator to hear a repeating pattern
7. Toggle visualizer to see frequencies

*Pro tip: Square wave + fast attack + medium release = classic NES.*

---

## Technical Notes

- Uses `AudioContext` with `OscillatorNode` and `GainNode`
- Master gain chain includes `AnalyserNode` for visualizer
- Envelope: linearRampToValueAtTime for attack/release
- Frequency calculation: base frequency * 2^octave
- Keyboard mapping includes black keys ( sharps/flats )
- Visualizer: `getByteFrequencyData` rendered as bars
- Automatically resumes AudioContext on first interaction (browser policy)

---

## The Real Story

I wanted a simple instrument that feels like you're playing an old computer. No samples to load, just math. The arpeggiator adds a bit of compositional assistance if you just want to jam. The visualizer is eye candy but also shows you're making sound.

Also: the piano keys are clickable and the keyboard support makes it actually playable. Try playing a tune! (Good luck with polyphony — it's monophonic per key press but you can spam keys.)

---

*Made with ✨ and some傅立葉 transform vibes during a heartbeat build cycle.*

**Repo:** https://github.com/Kiloooai/pixel-piano
