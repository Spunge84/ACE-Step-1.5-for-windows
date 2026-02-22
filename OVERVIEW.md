# ACE-Step 1.5 Overview

## Project Mission
ACE-Step 1.5 is a highly efficient open-source music foundation model designed to bring commercial-grade music generation to consumer hardware (running on <4GB VRAM).

## High-Level Architecture
The system uses a novel **hybrid architecture**:
- **LM Planner:** An omni-capable planner (Language Model) that transforms user queries into comprehensive song blueprints. It uses Chain-of-Thought (CoT) to synthesize metadata, lyrics, and captions.
- **DiT (Diffusion Transformer):** The core synthesis engine that generates high-fidelity audio based on the LM's blueprints.
- **Intrinsic RL:** Alignment achieved through reinforcement learning relying on internal mechanisms rather than external reward models.

## Tech Stack
- **Languages:** Python (3.11-3.12), HTML/JavaScript (Studio UI).
- **Core Frameworks:** PyTorch, Hugging Face Transformers, Diffusers.
- **Inference Optimization:** vLLM (standard), MLX (Apple Silicon), ROCm (AMD), Intel XPU.
- **Package Management:** `uv` for fast, reproducible dependency handling.
- **Interfaces:** Gradio (Web UI), FastAPI (REST API), CLI.

## Key Capabilities
- **Text-to-Music:** Multi-language lyrics support (50+ languages).
- **Audio Editing:** Cover generation, Repainting (in-painting), Layering (Lego), and Stem Extraction.
- **Personalization:** LoRA/LoKR training from as few as 8 songs.