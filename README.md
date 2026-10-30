# ✋ Hand Camera Lab

Webcam apps controlled by your hands, running right in the browser. Hand tracking is done by [MediaPipe Hand Landmarker](https://developers.google.com/mediapipe/solutions/vision/hand_landmarker) and everything is processed locally — no video ever leaves your device.

| App | What it does |
|---|---|
| **[Reality Lens](reality-lens.html)** | Hold a window open between your hands and see the world through 16 GPU shader effects (X-ray, thermal, ASCII, hologram, kaleidoscope, pop art, …). ✌️ switches effect, 👍 takes a photo. |
| **[Hand Magic Camera](hand-magic-camera.html)** | Fun effects that follow your fingers: sparks, air drawing, energy orb, lightning, neon skeleton. |
| **[Finger Gym](finger-gym.html)** | A 2‑minute hand-stretch break for people who type all day — the camera counts your reps and tracks a daily streak. |

## Run it

Each app is a single HTML file with no build step.

- **Locally:** open the `.html` file in Chrome or Edge and allow camera access.
- **Online:** enable GitHub Pages (Settings → Pages → Deploy from branch → `main` / root), then open `https://<your-username>.github.io/<repo-name>/reality-lens.html`. Camera access requires HTTPS, which GitHub Pages provides.

An internet connection is needed on first load (libraries and the hand model come from CDNs).

## Reality Lens controls

| Gesture / key | Action |
|---|---|
| 🙌 two hands | open a portal between your fingers |
| 🤏🤏 pinch with both hands | scanner bar |
| 👌 one hand | round magnifier lens |
| ✌️ peace sign | next effect |
| 👍 hold thumbs-up | 3‑2‑1 photo |
| `1`–`9`, `0`, `←` `→`, `space` | pick / cycle effects |
| `S` / `H` | photo / hide UI |

## Tech

Three.js (custom GLSL fragment shader), MediaPipe Tasks Vision 0.10.34, Canvas 2D, Web Audio. No frameworks, no build.
