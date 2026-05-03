<div align="center">

# RoleForge

**Local-first AI agent harness and automation control plane**

One Drive-style workspace for harnessing role-based agents, model routing, RAG knowledge, voice, OCR, image generation, and 3D mesh workflows.

[![TypeScript](https://img.shields.io/badge/TypeScript-5.x-3178c6?style=flat-square&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Node.js](https://img.shields.io/badge/Node.js-20%2B-339933?style=flat-square&logo=node.js&logoColor=white)](https://nodejs.org/)
[![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=flat-square&logo=python&logoColor=white)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)](LICENSE)

<br/>

![RoleForge workspace](docs/assets/screenshots/hero-workspace.png)

<sub>Web workspace for agents, knowledge, model policy, multimodal runtime panels, and release-safety review.</sub>

<br/>

<a href="https://leeseobaek.github.io/roleforge-portfolio/"><b>Open the GitHub Pages showcase</b></a>
<sub>Rendered portfolio page with a richer visual tour.</sub>

</div>

---

## Overview

RoleForge is a local-first agent harness and operating console for AI agent projects. It was designed to keep agent behavior, model policy, knowledge sources, privacy checks, and multimodal runtime tools in one workspace instead of scattering them across separate CLIs and experimental folders.

The public portfolio repository intentionally contains only the project overview, screenshots, license, and third-party attribution notes. Source code, runtime logs, local model weights, generated artifacts, private roadmap files, and environment secrets are not included.

## Why I Built It

Local AI workflows become hard to manage once they involve more than one model or modality. A chat agent, RAG index, OCR pipeline, voice runtime, image workflow, and 3D generator each need different setup, safety rules, and output handling.

RoleForge approaches that as a harness and control-plane problem:

- define role-based agents and their knowledge boundaries
- route tasks to appropriate local or CLI providers
- separate business, regulated, and research-only model lanes
- keep generated outputs and private session data outside the public release
- make release-safety checks visible before publishing

## Screenshots

The README keeps screenshots readable and simple. The visual showcase is available at [leeseobaek.github.io/roleforge-portfolio](https://leeseobaek.github.io/roleforge-portfolio/).

### Agent Registry

![Agent Registry](docs/assets/screenshots/agent-registry.png)

Role profiles, safety rules, model policy, and knowledge sources.

### Document Intake

![Document Intake](docs/assets/screenshots/document-intake.png)

OCR/PDF extraction and RAG knowledge promotion.

### Release Safety

![Release Safety](docs/assets/screenshots/release-safety.png)

PII, license, and publication checks before public release.

## Core Capabilities

| Area | What RoleForge Handles |
|---|---|
| Agent design | Role profiles, behavior rules, safety config, and per-agent knowledge |
| Model policy | 23-model registry with commercial, conditional, regulated, and research-only lanes |
| RAG | Local document knowledge with offline hash embedding or Ollama `bge-m3` |
| Document intake | Text, PDF, image extraction, OCR adapter, and privacy filtering |
| Voice | STT and TTS adapters for local Korean voice workflows |
| Image | Diffusers and ComfyUI workflow integration with review/export handling |
| 3D | Image-to-mesh workflow with TripoSR/InstantMesh adapter structure |
| Safety | Human-review gates, research-lane separation, and release-safety checklist |
| Ontology | Semantic map of agents, capabilities, models, runtime lanes, and risk domains |

## Tech Stack

<div align="center">

![TypeScript](https://img.shields.io/badge/TypeScript-3178c6?style=for-the-badge&logo=typescript&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Ollama](https://img.shields.io/badge/Ollama-000000?style=for-the-badge&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)

</div>

| Layer | Tools |
|---|---|
| Web console and CLI | TypeScript, Node.js, Express |
| Local LLM and embedding | Ollama, Qwen, BGE-M3 |
| STT | faster-whisper |
| TTS | Chatterbox, Kokoro, Edge TTS |
| OCR | PaddleOCR adapter |
| Image | Stable Diffusion, Diffusers, ComfyUI |
| 3D | TripoSR, InstantMesh |
| Runtime services | FastAPI, Uvicorn |

## Verification Snapshot

The private release package was verified before creating this portfolio snapshot:

```text
Full test suite:  186 / 186 passing
Policy subset:     71 / 71 passing
```

## Public Release Boundary

This portfolio repository does not include:

- application source code
- `.env` files, tokens, API keys, or private config
- local model weights or Hugging Face caches
- session logs and generated runtime artifacts
- generated image, voice, document, review, audit, or 3D output data
- private roadmap notes or development work logs

The goal is to show the product direction, architecture, screenshots, and release-safety posture without exposing private implementation files.

## Attribution

RoleForge can connect to third-party models and runtimes. Model weights and external services are not included in this repository and remain subject to their own licenses and terms.

See [Third-Party Notices](docs/THIRD_PARTY_NOTICES.md) for model, OCR, STT, TTS, image, 3D, and runtime attribution.

## License

MIT. See [LICENSE](LICENSE).
