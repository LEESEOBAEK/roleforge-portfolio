<div align="center">

# RoleForge

**A local-first AI agent harness and runtime control plane.**

RoleForge brings role-based agents, model policy, RAG knowledge, voice, OCR,
image generation, and 3D mesh workflows into one responsive Drive-style local workspace.

[![TypeScript](https://img.shields.io/badge/TypeScript-5.x-3178c6?style=flat-square&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Node.js](https://img.shields.io/badge/Node.js-20%2B-339933?style=flat-square&logo=node.js&logoColor=white)](https://nodejs.org/)
[![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=flat-square&logo=python&logoColor=white)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)](LICENSE)

<br/>

![RoleForge workspace](docs/assets/screenshots/hero-workspace.png)

<sub>Responsive Web Drive workspace for agents, knowledge, model policy, multimodal runtime panels, and release-safety review.</sub>

<br/>

<a href="https://leeseobaek.github.io/roleforge-portfolio/"><b>Open the GitHub Pages showcase</b></a>
<sub>Rendered portfolio page with a richer visual tour.</sub>

</div>

---

## Project Summary

RoleForge started from a practical local-AI problem: once a project uses more
than one model or modality, the workflow quickly fragments across terminals,
temporary scripts, runtime folders, and safety notes.

The project reframes that as a control-plane problem. Instead of treating chat,
RAG, OCR, voice, image generation, 3D mesh creation, and model selection as
separate experiments, RoleForge gives them a shared workspace, policy layer,
artifact model, and release-safety path.

This portfolio repository is intentionally **README-only**. It shows the product
direction, screenshots, architecture, and safety posture without publishing the
application source code, private runtime logs, generated artifacts, local model
weights, or environment secrets.

---

## Product Highlights

| Area | What the project demonstrates |
|---|---|
| Agent operating model | Role profiles, safety rules, model policy, and per-agent knowledge boundaries |
| Provider routing | Request-level routing across Ollama, Codex CLI, Claude CLI, Gemini CLI, and runtime adapters |
| RAG workflow | Local document knowledge with hash-local embedding or Ollama `bge-m3` |
| Document intake | Text, PDF, OCR extraction, privacy filtering, and knowledge promotion |
| Voice runtime | faster-whisper STT and Korean TTS adapter flows |
| Image workflow | Diffusers and ComfyUI integration with review/export handling |
| 3D workflow | Image-to-mesh adapter contract for TripoSR/InstantMesh-style runtimes |
| Research safety | Separate research lanes, human-review gates, and blocked egress before approval |
| Release safety | PII, license, artifact, and source-boundary checks before publication |

---

## Screenshots

The README keeps screenshots readable and focused. The visual showcase is
available at [leeseobaek.github.io/roleforge-portfolio](https://leeseobaek.github.io/roleforge-portfolio/).

### Agent Registry

![Agent Registry](docs/assets/screenshots/agent-registry.png)

Role profiles, safety rules, model policy, and knowledge sources.

### Document Intake

![Document Intake](docs/assets/screenshots/document-intake.png)

OCR/PDF extraction and RAG knowledge promotion.

### Release Safety

![Release Safety](docs/assets/screenshots/release-safety.png)

PII, license, and publication checks before public release.

---

## Architecture at a Glance

```text
Web Drive Console
  -> Agent Registry / Model Registry / Runtime Controls
  -> Chat + Provider Routing
  -> Document Intake + RAG Promotion
  -> Voice / OCR / Image / 3D Panels
  -> Review Queue + Release Safety

Runtime Adapters
  -> Ollama
  -> CLI providers
  -> FastAPI services
  -> ComfyUI / Diffusers
  -> TripoSR-style 3D services
```

The important design choice is that policy and runtime state are not hidden in
one-off scripts. They are surfaced through registries, review gates, operational
events, and a workspace UI so the user can see what is running and why a task
routes to a specific provider.

---

## Technical Stack

| Layer | Tools |
|---|---|
| Web console and CLI | TypeScript, Node.js, native HTTP server |
| Local LLM and embedding | Ollama, Qwen, BGE-M3 |
| STT | faster-whisper |
| TTS | Chatterbox, Kokoro, Edge TTS |
| OCR | PaddleOCR adapter |
| Image | Stable Diffusion, Diffusers, ComfyUI |
| 3D | TripoSR, InstantMesh-compatible adapter contract |
| Runtime services | FastAPI, Uvicorn |
| Safety and policy | Model registry, review queue, PII filtering, release checklist |

Primary development environment: Windows 11 + WSL2 Ubuntu + NVIDIA GPU.

---

## Verification Posture

The private source package uses `npm run check:v0.1` as the stable automated
baseline. Runtime smoke tests are run separately when the corresponding local
servers are available.

Representative checks:

```text
npm run check:v0.1
npm run ocr:smoke
npm run image:smoke:comfyui
npm run 3d:ui-smoke
npm run research:smoke:ollama
```

The portfolio repository does not claim to be a runnable package. It is a public
showcase boundary for a larger private/local-first system.

---

## Public Boundary

This repository does not include:

- application source code
- `.env` files, tokens, API keys, or private config
- local model weights or Hugging Face caches
- session logs and generated runtime artifacts
- generated image, voice, document, review, audit, or 3D output data
- private roadmap notes or development work logs

The goal is to show the project direction, architecture, screenshots, and
release-safety discipline without exposing private implementation files or local
runtime data.

---

## Attribution

RoleForge can connect to third-party models and runtimes. Model weights and
external services are not included in this repository and remain subject to
their own licenses and terms.

See [Third-Party Notices](docs/THIRD_PARTY_NOTICES.md) for model, OCR, STT, TTS,
image, 3D, and runtime attribution.

---

## License

MIT. See [LICENSE](LICENSE).
