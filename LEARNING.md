# My AI Engineering Path
<!-- Managed by the ai-engineering-from-scratch learning skills.
     Repo: https://github.com/rohitg00/ai-engineering-from-scratch -->

## Mission
Close foundation gaps. Going slow and thorough, no phases skipped. Build goal: a trained model.
Tutor note: already builds agents that call hosted-LLM APIs with keys. On API, key and SDK topics, review the key points only and skip live API examples and setup. Warm-ups next session should still draw from the Review queue (Phase 0 lessons 1 to 4).

## Placement
- Date: 2026-10-14
- Score: 6/10 (Math & Statistics 1/2, Classical ML 1/2, Deep Learning 1/2, NLP & Transformers 1/2, Applied AI 2/2)
- Entry point: Phase 0: Setup & Tooling (full path by choice; the quiz alone suggested Phase 7)
- Pace: ~10 h/week

## Path
| Phase | Name | Status | Est. hours |
|-------|------|--------|------------|
| 0 | Setup & Tooling | Do | 16 |
| 1 | Math Foundations | Do | 23 |
| 2 | ML Fundamentals | Do | 26 |
| 3 | Deep Learning Core | Do | 15 |
| 4 | Computer Vision | Do | 27 |
| 5 | NLP: Foundations to Advanced | Do | 30 |
| 6 | Speech & Audio | Do | 18 |
| 7 | Transformers Deep Dive | Do | 14 |
| 8 | Generative AI | Do | 14 |
| 9 | Reinforcement Learning | Do | 13 |
| 10 | LLMs from Scratch | Do | 26 |
| 11 | LLM Engineering | Do | 19 |
| 12 | Multimodal AI | Do | 65 |
| 13 | Tools & Protocols | Do | 76 |
| 14 | Agent Engineering | Do | 55 |
| 15 | Autonomous Systems | Do | 20 |
| 16 | Multi-Agent & Swarms | Do | 28 |
| 17 | Infrastructure & Production | Do | 34 |
| 18 | Ethics, Safety & Alignment | Do | 31 |
| 19 | Capstone Projects | Do | 620 |
| | **Total** | | **1170** |

## Progress log
| Date | Lesson | Quiz | Note |
|------|--------|------|------|
| 2026-10-14 | 00/01-dev-environment | 1/3 | Env fully built (uv venv, torch with MPS, Rust, Julia). Missed install order (bottom-up) and the GPU check: assumed plain macOS torch is CPU-only, but it has MPS; cuda False is expected on a Mac. |
| 2026-10-14 | 00/02-git-and-collaboration | 2/3 | Already had fork, upstream remote and learning branch in place. Missed what `git checkout -b` does (thought it downloads a branch; it creates and switches). Warm-up on lesson 1 was 2/2. |
| 2026-10-14 | 00/03-gpu-setup-and-cloud | 1/3 | Machine is M4 Pro, 48 GB unified, MPS recommended max 40.2 GB (~20B fp16 weights-only), matmul MPS 2.8x CPU. Missed: GPU memory ceiling (assumed all RAM), training memory (16 B/param vs 2 for inference), `nvidia-smi`, why `synchronize()` is needed (async GPU). Warm-up on lesson 2 was 2/2. |
| 2026-10-14 | 00/04-apis-and-keys | 2/3 | No API keys set and anthropic SDK not installed yet in the course venv. Ran the wrong-key call live (401 authentication_error). Missed: Anthropic key goes in `x-api-key` (not Bearer). Lesson default model `claude-sonnet-5` is unverified; use an explicit current ID. Warm-up on lesson 3 was 2/2. |

## Review queue
- 00/01-dev-environment (1/3): four-layer stack install order (system, package managers, runtimes, libraries) and GPU verification (`torch.cuda.is_available()` for NVIDIA, `torch.backends.mps.is_available()` on Apple Silicon).
- 00/02-git-and-collaboration (2/3): `git checkout -b <name>` creates a new branch and switches to it (local only, no download).
- 00/03-gpu-setup-and-cloud (1/3): `nvidia-smi` as the NVIDIA check; GPU ops are asynchronous so `synchronize()` is required before timing; training memory is about 16 bytes per parameter with Adam (vs 2 for fp16 inference); on a Mac the GPU limit is the recommended working set (40.2 GB here), not total RAM.
- 00/04-apis-and-keys (2/3): Anthropic authenticates with the `x-api-key` header (OpenAI uses `Authorization: Bearer`).
