# PuzzleCam — Gesture Capture

**© 2026 aiwithunnati — all rights reserved**

A hand-gesture controlled photobooth puzzle game that runs entirely in the browser. No installation, no backend, no dependencies to install.

---

## What it does

PuzzleCam uses your webcam and hand tracking to let you:

1. **Frame a photo with your hands** — hold both hands up, the space between your index fingertips becomes the camera frame
2. **Pinch to capture** — both hands pinch → 3-second countdown → photo taken with a color photobooth effect
3. **Solve the puzzle** — photo splits into a 3×3 grid, solve it by dragging pieces with a pinch gesture
4. **Fist to save** — completed puzzle shatters with a physics animation and saves to your photo strip
5. **Download your strip or video** — collect 3 puzzles and download as PNG, or download a video of your solve

---

## Demo

- Frame your shot with both hands
- Pinch to start the countdown
- Drag pieces with one-hand pinch to solve the puzzle
- Make a fist to save — watch it shatter!
- All 3 completed puzzles stack into a downloadable vertical photo strip

---

## Gesture controls

| Gesture | Action |
|---|---|
| Both hands pinching | Freeze the frame area and start countdown |
| One hand pinching over a piece | Drag the puzzle piece |
| Closed fist (hold) | Save completed puzzle / reset board |

---

## Features

- Real-time hand landmark tracking via MediaPipe (no install needed)
- Color photobooth effect with contrast boost and film grain
- 3×3 puzzle with snap-to-cell and animated piece displacement
- Physics-based shatter animation on save
- Sound design — countdown beeps, piece snap, shatter burst, completion chime
- Video recording of each solve, downloadable as WebM
- Photo strip sidebar — collect 3 puzzles, download as PNG

---

## How to run

```bash
git clone https://github.com/Unnati-23/puzzlecam.git
cd puzzlecam
```

Open in VS Code and click **Go Live** (Live Server extension by Ritwick Dey), then open `http://localhost:5500` and allow camera access.

> Requires internet on first load to download the MediaPipe hand tracking model (~10MB)

---

## Tech stack

- **MediaPipe Tasks Vision** `v0.10.14` — 21-point hand landmark detection
- **Canvas 2D API** — all rendering, effects, puzzle logic, shatter physics
- **Web Audio API** — all sound effects generated in code, no audio files
- **MediaRecorder API** — canvas capture for video download
- **Vanilla JavaScript (ES Modules)** — no frameworks, no build step

---

## Browser support

| Browser | Support |
|---|---|
| Chrome / Edge | Recommended |
| Firefox | Compatible |
| Safari | Limited |
| Mobile | Not recommended |

---

## License

MIT — free to use, modify, and share.
