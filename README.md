## Shivaay Dhondiyal

**I make voice and audio pipelines faster and cheaper.**

My ICML 2026 paper detects audio deepfakes with **34,000 parameters** — 0.01% the size of the 300M-parameter Wav2Vec2 baseline — and beats it by **+9.8 points** on the hardest cross-domain pair in the benchmark.

---

### Research

**FlowFake: Liquid Networks for Audio Deepfake Detection** — first author (equal contribution)
Accepted at the **ICML 2026 Workshop on Machine Learning for Audio**, Seoul.
[arXiv:2606.19579](https://arxiv.org/abs/2606.19579) · [camera-ready PDF](https://mlforaudioworkshop.github.io/accepted_submissions_2026/CameraReadys%204-83/78/CameraReady/FlowFake%20Liquid%20Network%20for%20Audio%20DeepFake%20Detection.pdf) · [code](https://github.com/shivaay790/FlowFake)

A Liquid Time-Constant architecture whose hidden state evolves via a learned ODE, with per-neuron adaptive time constants resolving spectral (10 ms) and prosodic (2 s) structure at once. Formal BIBO stability and an O(Δt⁴) RK4 error bound.

Cross-dataset accuracy, trained on FakeOrReal — the hardest transfer pair in the benchmark:

| Model | Params | → ASVspoof-2019 | → InTheWild |
|---|---|---|---|
| **FlowFake** | **34 K** | **75.29 ± 3.02** | **70.91 ± 0.62** |
| SSL Wav2Vec2 | 300 M | 65.4 ± 10.3 | 57.8 ± 10.9 |
| Whisper-DF | — | 45.9 ± 0.8 | 54.1 ± 3.4 |
| RawGAT-ST | — | 49.1 ± 18.1 | 49.8 ± 0.4 |

Trained on MLAAD (54 TTS systems, 23 languages) it reaches 79.97% on ASVspoof-2019 — above SSL Wav2Vec2's 78.0% — and **90.41% zero-shot on WaveFake**.

Note the standard deviations. FlowFake's cross-seed spread is ±0.24–3.08; the baselines swing ±10–44 points. Small, fast, and it doesn't move under you.

**When Does Disentanglement Enable Compositional Generalization? A Transfer Bound and Its Empirical Validation**
Accepted at the **ICML 2026 CompLearn Workshop**.
[OpenReview](https://openreview.net/forum?id=nl7vgE31k8) · [code](https://github.com/shivaay790/compositional-generalization)

---

### Production

**AI Engineer — stealth startup (partnered with Prosper AI)**, Nov–Dec 2025
- Voice-agent workflows on STT/TTS stacks for Fortune-30 hospital deployments. Automation ~35% → 60%+; backend integration errors down 40%.
- Automated analytics across **1M+ healthcare calls/month** with Metabase dashboards. Escalations reduced to 28%.

**AI Research Intern — Delhi Technological University**, Jun–Jul 2025
- Liquid Neural Network architecture for audio deepfake detection, with cross-dataset generalization beyond Wav2Vec2.0 and Whisper-DF. This became FlowFake.

---

### Selected engineering

- **[Crowd density estimation](https://crowd-counting.shivaaydhondiyal.online/)** — live. VGG16 + CBAM attention, patch-based inference at 1024², stampede-risk gradient analysis, DBSCAN hotspot clustering. [code](https://github.com/shivaay790/DL_crowd_counting)
- **[Real-time gesture control](https://hand-gesture.shivaaydhondiyal.online/)** — live. MediaPipe + FastAPI + WebSocket, driving games and serial-connected robotic hardware. [code](https://github.com/shivaay790/hand-gesture-deployed)
- **[Internal RAG Assistant](https://github.com/shivaay790/Internal-RAG-Assistant)** — ensemble retrieval (Chroma + Gemini embeddings + BM25), query classification, source citations, PII detection and masking, per-user rate limiting. The unglamorous parts of RAG that decide whether it survives contact with real users.
- **[InternSathi](https://github.com/shivaay790/sih_proj)** — internship recommendation platform; resume parsing with GitHub enrichment, skill-gap analytics, learning roadmaps. Smart India Hackathon grand finalist.
- **[Portfolio](https://shivaaydhondiyal.online/)** — React Three Fiber, interactive 3D project explorer.

---

### Consulting

I take **two part-time retainers at a time**, embedded with your engineering team: voice agent latency and cost, STT/TTS pipeline work, eval and benchmark infrastructure, paper-to-production implementation.

| | |
|---|---|
| **Pilot sprint** | **$600** — one week, fixed scope, one metric. If the number doesn't move, don't pay the invoice. |
| **Embedded** | $2,500/mo — 10 hrs/week |
| **Core** | $3,500/mo — 14 hrs/week |
| **Lead** | $5,000/mo — 20 hrs/week |

Every engagement ships a repo, a before/after benchmark you can re-run without me, and a written weekly update with numbers in it.

📧 **shivaaydhondiyal23@gmail.com** · [LinkedIn](https://www.linkedin.com/in/shivaay-dhondiyal/)

---

<sub>B.Tech CSE, Delhi Technological University · 1st ZervAI'25 (IIT Bombay) · 1st APOGEE'25 CTF (BITS Pilani) · Smart India Hackathon Grand Finalist · Co-Head, AIMS DTU</sub>
