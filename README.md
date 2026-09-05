## Shivaay Dhondiyal

**I make voice and audio pipelines faster and cheaper.**

My ICML 2026 paper does audio deepfake detection at **34K parameters** — 0.01% the size of the 300M-parameter Wav2Vec2 baseline it matches, while generalising *better* across four datasets it was never trained on.

---

### Research

**FlowFake: Liquid Networks for Audio Deepfake Detection** — first author (equal contribution)
Accepted at the **ICML 2026 Workshop on Machine Learning for Audio**, Seoul.
A Liquid Time-Constant architecture whose hidden state evolves via a learned ODE, with per-neuron adaptive time constants resolving spectral (10 ms) and prosodic (2 s) cues simultaneously. Formal BIBO stability and an O(Δt⁴) RK4 integration error bound.

| | Params | ASVspoof-2019 (trained on FakeOrReal) | Trained on MLAAD |
|---|---|---|---|
| **FlowFake** | **34 K** | **75.29%** | **79.97%** |
| SSL Wav2Vec2 | 300 M | matched | matched |

Outperforms RawGAT-ST and Whisper-DF on every evaluated pair, at 0.01% of Wav2Vec2's parameter count.
📄 [Camera-ready PDF](https://mlforaudioworkshop.github.io/accepted_submissions_2026/CameraReadys%204-83/78/CameraReady/FlowFake%20Liquid%20Network%20for%20Audio%20DeepFake%20Detection.pdf) · [code](https://github.com/shivaay790/FlowFake)

**When Does Disentanglement Enable Compositional Generalization? A Transfer Bound and Its Empirical Validation**
Accepted at the **ICML 2026 CompLearn Workshop**.
[OpenReview](https://openreview.net/forum?id=nl7vgE31k8) · [code](https://github.com/shivaay790/compositional-generalization)

---

### Production

**AI Engineer, stealth startup (partnered with Prosper AI)** — Nov–Dec 2025
- Built voice-agent workflows on STT/TTS stacks for Fortune-30 hospital deployments. Automation went from ~35% to 60%+; backend integration errors down 40%.
- Automated analytics across **1M+ healthcare calls/month**, integrating Metabase dashboards. Escalations reduced to 28%.

**AI Research Intern, Delhi Technological University** — Jun–Jul 2025
- Liquid Neural Network architecture for audio deepfake detection, with cross-dataset generalization beyond Wav2Vec2.0 and Whisper-DF. This became FlowFake.

---

### Things you can click and use right now

- **[Crowd density estimation](https://crowd-counting.shivaaydhondiyal.online/)** — VGG16 + CBAM attention, patch-based inference at 1024², stampede-risk gradients, DBSCAN hotspot clustering. [code](https://github.com/shivaay790/DL_crowd_counting)
- **[Real-time gesture control](https://hand-gesture.shivaaydhondiyal.online/)** — MediaPipe + FastAPI + WebSocket, driving games and serial-connected robotic hardware. [code](https://github.com/shivaay790/hand-gesture-deployed)
- **[Portfolio](https://shivaaydhondiyal.online/)** — React Three Fiber, interactive 3D project explorer.

---

### Consulting

I take **two part-time retainers at a time**, embedded with your engineering team. Voice agent latency and cost, STT/TTS pipeline work, eval and benchmark infrastructure, paper-to-production implementation.

| | |
|---|---|
| **Pilot sprint** | $600 — one week, fixed scope, one metric. If the number doesn't move, don't pay the invoice. |
| **Embedded** | $2,500/mo — 10 hrs/week |
| **Core** | $3,500/mo — 14 hrs/week |
| **Lead** | $5,000/mo — 20 hrs/week |

Start with the pilot. You get a repo, a before/after benchmark you can re-run without me, and a 30-minute readout.

📧 **shivaaydhondiyal23@gmail.com** · [LinkedIn](https://www.linkedin.com/in/shivaay-dhondiyal/)

---

<sub>B.Tech CSE, Delhi Technological University · 1st ZervAI'25 (IIT Bombay) · 1st APOGEE'25 CTF (BITS Pilani) · Smart India Hackathon Grand Finalist · Co-Head, AIMS DTU</sub>
