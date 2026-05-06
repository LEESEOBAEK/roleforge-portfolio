# Third-Party Notices

RoleForge is released under the MIT license, but it can connect to external model weights, runtimes, Python packages, Node packages, and command-line tools. Those third-party components are not relicensed by this repository.

This repository does not include model weights, checkpoints, Hugging Face caches, generated media, session logs, or private runtime artifacts. Users are responsible for downloading third-party models from their upstream sources and complying with the upstream license, acceptable-use policy, and model card.

This file is an attribution and review aid, not legal advice. Upstream terms control if they differ from this summary.

## Model Registry Sources

| Registry ID | Upstream name | Recorded license / terms | Source |
|---|---|---|---|
| `qwen3-14b` | Qwen3 14B (`qwen3:14b` backend) | Apache-2.0 | https://huggingface.co/Qwen/Qwen3-14B |
| `gemma3-12b-it` | Gemma 3 12B IT | Gemma Terms | https://huggingface.co/google/gemma-3-12b-it |
| `qwen3-coder-next` | Qwen3-Coder-Next-FP8 | Apache-2.0 | https://huggingface.co/Qwen/Qwen3-Coder-Next-FP8 |
| `bge-m3` | BGE-M3 | MIT | https://huggingface.co/BAAI/bge-m3 |
| `gte-multilingual-base` | GTE Multilingual Base | Apache-2.0 | https://huggingface.co/Alibaba-NLP/gte-multilingual-base |
| `whisper-large-v3-turbo` | Whisper large-v3-turbo | MIT | https://huggingface.co/openai/whisper-large-v3-turbo |
| `kokoro` | Kokoro TTS | Apache-2.0 | https://huggingface.co/geneing/Kokoro |
| `paddleocr-vl` | PaddleOCR-VL | Check upstream model card | https://huggingface.co/PaddlePaddle/PaddleOCR-VL |
| `dinov2-registers-base` | DINOv2 Registers Base | Apache-2.0 | https://huggingface.co/facebook/dinov2-with-registers-base |
| `flux-schnell` | FLUX.1-schnell | Apache-2.0 | https://huggingface.co/black-forest-labs/FLUX.1-schnell |
| `realvisxl-v5` | RealVisXL V5.0 | OpenRAIL++ | https://huggingface.co/SG161222/RealVisXL_V5.0 |
| `stable-diffusion-v1-5` | Stable Diffusion v1.5 | CreativeML OpenRAIL-M | https://huggingface.co/stable-diffusion-v1-5/stable-diffusion-v1-5 |
| `sdxl-base-1.0` | Stable Diffusion XL Base 1.0 | CreativeML OpenRAIL++-M | https://huggingface.co/stabilityai/stable-diffusion-xl-base-1.0 |
| `medgemma-4b-it` | MedGemma 4B IT | Health AI Developer Foundations Terms | https://huggingface.co/google/medgemma-4b-it |
| `meditron-7b` | Meditron 7B | Llama 2 | https://huggingface.co/epfl-llm/meditron-7b |
| `triposr` | TripoSR | MIT | https://huggingface.co/stabilityai/TripoSR |
| `instantmesh` | InstantMesh | Apache-2.0 | https://huggingface.co/TencentARC/InstantMesh |
| `privacy-filter` | Local regex privacy filter | Internal fallback | local implementation |
| `qwen3-14b-uncensored` | Qwen3-14B-Uncensored | Apache-2.0 | https://huggingface.co/nicoboss/Qwen3-14B-Uncensored |
| `qwen3-5-35b-aggressive` | Qwen3.5-35B-A3B Aggressive | Apache-2.0 | https://huggingface.co/HauhauCS/Qwen3.5-35B-A3B-Uncensored-HauhauCS-Aggressive |
| `floppa-gemma3-uncensored` | Floppa-12B Gemma3 Uncensored | Gemma Terms | https://huggingface.co/Ryex/Floppa-12B-Gemma3-Uncensored |
| `flux-dev` | FLUX.1-dev | FLUX dev non-commercial | https://huggingface.co/black-forest-labs/FLUX.1-dev |
| `flux-kontext-dev` | FLUX.1 Kontext dev | FLUX dev non-commercial | https://huggingface.co/black-forest-labs/FLUX.1-Kontext-dev |

## Runtime And Tool Sources

| Component | Purpose | Source |
|---|---|---|
| Ollama | Local LLM and embedding runtime | https://ollama.com |
| Claude CLI | Optional provider route | https://docs.anthropic.com |
| Codex CLI | Optional provider route | https://developers.openai.com/codex |
| Gemini CLI | Optional provider route | https://ai.google.dev |
| ComfyUI | Optional image workflow runtime | https://github.com/comfyanonymous/ComfyUI |
| Hugging Face Diffusers | Optional image generation runtime | https://github.com/huggingface/diffusers |
| faster-whisper | Local STT runtime | https://github.com/SYSTRAN/faster-whisper |
| Chatterbox TTS | Local multilingual TTS runtime | https://pypi.org/project/chatterbox-tts/ |
| edge-tts | Optional Edge TTS adapter | https://pypi.org/project/edge-tts/ |
| PaddleOCR | OCR runtime | https://github.com/PaddlePaddle/PaddleOCR |
| TripoSR | 3D image-to-mesh runtime | https://github.com/VAST-AI-Research/TripoSR |
| InstantMesh | Optional 3D image-to-mesh runtime | https://github.com/TencentARC/InstantMesh |
| FastAPI | Python HTTP runtime | https://fastapi.tiangolo.com |
| Uvicorn | Python ASGI server | https://www.uvicorn.org |
| TypeScript | Type checking and build toolchain | https://www.typescriptlang.org |
| Node.js | JavaScript runtime | https://nodejs.org |

## Release Rules

- Do not commit model weights, checkpoints, generated media, or local caches.
- Keep `.env`, API keys, tokens, session logs, and runtime artifacts out of Git.
- Re-check upstream model cards before public or commercial use.
- Treat `conditional`, `non-commercial`, medical, uncensored, or research-only models as blocked from public output unless reviewed.
- Keep attribution links current when changing `data/models/model-registry.json`.
