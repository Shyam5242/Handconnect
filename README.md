# HandConnect

Real-time neon hand tracking in the browser. One HTML file, no backend, no install.

It uses your webcam and Google's MediaPipe Hands model to track up to two hands (21 points each), draws a glowing neon skeleton on each hand, and joins matching fingertips with rainbow beams and sparks when both hands are visible. A live HUD shows hands detected, FPS, gesture (Open Hand, Fist, Point, Pinch) and finger spread.

Your video never leaves your device. The model runs locally in the browser.

## Features

- Two-hand tracking, 21 landmarks per hand
- Neon skeleton (pink and yellow)
- Rainbow beams and sparks between matching fingertips
- Live HUD: hands, FPS, gesture, spread %
- Single file, vanilla JavaScript, HTML5 Canvas

## Run it

The camera only works on `localhost` or `https`, so start a local server first.

```bash
python3 -m http.server 8000
# or
npx serve .
```

Then open `http://localhost:8000/handconnect.html` in Chrome or Edge and click **Allow** for the camera. Hold up both hands.

## Performance tips

- Default is `modelComplexity: 0` (fast) and 640x480 camera, good for low-end laptops.
- On a faster machine, set `modelComplexity: 1` and camera 1280x720 for better accuracy.
- Good lighting on your hands improves tracking.

## Customize

- Change `HAND_COLORS` and `BEAM_COLORS` for your own theme.
- Ideas: sound on pinch, gesture-controlled slides or games, air drawing with the index finger.

## Tech

MediaPipe Hands, vanilla JavaScript, HTML5 Canvas, webcam API (`getUserMedia`).

## Credits

Based on the "HandConnect: Real-Time Neon Hand Tracking in the Browser" tutorial by [@codewithswaroop](https://instagram.com/codewithswaroop).
