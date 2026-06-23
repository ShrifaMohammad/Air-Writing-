# Air Writing Pro ✍️

Draw in the air using just your webcam and hand gestures — no mouse, no touchscreen, no stylus. Built with [MediaPipe Hands](https://developers.google.com/mediapipe/solutions/vision/hand_landmarker) for real-time hand tracking, running entirely in the browser.

## Try it live

🔗 **[Open Air Writing Pro](https://YOUR_USERNAME.github.io/air-writing-pro/)** *(enable GitHub Pages — see below — and put your link here)*

Just allow camera access and hold up your index finger to start drawing.

## How it works

The app tracks your hand in real time and maps finger gestures to actions:

| Gesture | Action |
|---|---|
| ☝️ 1 finger up | Draw (line thickness reacts to how fast you move) |
| ✌️ 2 fingers up | Clear the canvas |
| 🤟 3 fingers up | Cycle to the next neon color |
| ✊ Closed fist | Pause drawing |

The drawing has a glowing neon trail effect, and you can save your creation as a PNG at any time.

## Why I built it

I wanted to explore computer-vision-based interaction — using body movement itself as an input device instead of traditional peripherals. It's a fun demonstration of how accessible real-time hand tracking has become, since everything runs client-side with no server, no installation, and no AI API calls — just the browser and a webcam.

## Tech stack

- [MediaPipe Hands](https://developers.google.com/mediapipe/solutions/vision/hand_landmarker) — real-time hand landmark detection
- Vanilla JavaScript + HTML5 Canvas — drawing logic and neon glow rendering
- No frameworks, no build step, no dependencies to install

## Run it locally

Since it only needs a static file server (camera access requires HTTPS or localhost), the simplest way is:

```bash
git clone https://github.com/YOUR_USERNAME/air-writing-pro.git
cd air-writing-pro
python3 -m http.server 8000
```

Then open `http://localhost:8000` in your browser and allow camera access.

## Deploy your own live demo (GitHub Pages)

1. Push this repo to GitHub
2. Go to **Settings → Pages**
3. Under "Source", select the `main` branch and `/ (root)` folder
4. Save — GitHub will give you a live URL (e.g. `https://YOUR_USERNAME.github.io/air-writing-pro/`) within a minute or two
5. Update the "Try it live" link at the top of this README with your new URL

## What I'd improve next

- Add a brush size slider and more color options
- Support two-handed drawing
- Add an "undo last stroke" gesture instead of full clear
- Mobile camera support (currently optimized for front-facing webcams)
