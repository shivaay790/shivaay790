## Shivaay Dhondiyal

**I make voice AI systems faster, cheaper, and measurably more reliable.**

I built the STT/TTS voice-agent workflows and the analytics layer for a healthcare stack running **1M+ calls a month**, and I have two ICML 2026 workshop papers on when models hold up under distribution shift. I take two part-time consulting retainers at a time — [details below](#consulting).

---

### Research

**FlowFake: Liquid Networks for Audio Deepfake Detection** — first author (equal contribution)
Accepted at the **ICML 2026 Workshop on Machine Learning for Audio**, Seoul.
[Camera-ready PDF](https://mlforaudioworkshop.github.io/accepted_submissions_2026/CameraReadys%204-83/78/CameraReady/FlowFake%20Liquid%20Network%20for%20Audio%20DeepFake%20Detection.pdf) · [code](https://github.com/shivaay790/FlowFake)

A Liquid Time-Constant architecture whose hidden state evolves via a learned ODE, with per-neuron adaptive time constants resolving spectral (10 ms) and prosodic (2 s) structure at once. Formal BIBO stability and an O(Δt⁴) RK4 error bound.

Cross-dataset accuracy, trained on FakeOrReal — the hardest transfer pair in the benchmark:

| Model | Params | → ASVspoof-2019 | → InTheWild |
|---|---|---|---|
| **FlowFake** | **34 K** | **75.29 ± 3.02** | **70.91 ± 0.62** |
| SSL Wav2Vec2 | 300 M | 65.4 ± 10.3 | 57.8 ± 10.9 |
| Whisper-DF | — | 45.9 ± 0.8 | 54.1 ± 3.4 |
| RawGAT-ST | — | 49.1 ± 18.1 | 49.8 ± 0.4 |

Trained on MLAAD (54 TTS systems, 23 languages) it reaches 79.97% on ASVspoof-2019 — above SSL Wav2Vec2's 78.0% — and **90.41% zero-shot on WaveFake**.

Note the standard deviations. FlowFake's cross-seed spread is ±0.24–3.08 where the baselines swing ±10–44 points — the stability that Theorem 4.2 predicts, confirmed empirically.

**What this result is not.** These are cross-dataset numbers, and cross-dataset EER still sits at 37–47%. FlowFake is a demonstration that a structural prior beats brute capacity in the data-scarce, high-shift regime — not a drop-in production detector. With abundant in-domain data, large fine-tuned SSL models win, and the paper says so explicitly.

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

- **[telephony-asr-bench](https://github.com/shivaay790/telephony-asr-bench)** — speech recognition is benchmarked on clean wideband audio; voice agents receive 8 kHz, G.711-companded, packet-lossy audio. This measures the difference. Reproducible channel chain, pooled corpus WER with bootstrapped confidence intervals, and a hard pre-flight budget guard so a run cannot overspend. 36 tests, no network.

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
| **Pilot sprint** | **$500** — one week, fixed scope, one metric. If the number doesn't move, don't pay the invoice. |
| **Embedded** | $1,500/mo — 10 hrs/week |
| **Lead** | $3,000/mo — 20 hrs/week |

Every engagement ships a repo, a before/after benchmark you can re-run without me, and a written weekly update with numbers in it.

📧 **shivaaydhondiyal23@gmail.com** · [LinkedIn](https://www.linkedin.com/in/shivaay-dhondiyal/)

---

<sub>B.Tech CSE, Delhi Technological University · 1st ZervAI'25 (IIT Bombay) · 1st APOGEE'25 CTF (BITS Pilani) · Smart India Hackathon Grand Finalist · Co-Head, AIMS DTU</sub>
