# ACE-Step 1.5 Technical Map

## Core Pipelines
- **Main Inference Pipeline:** `acestep/acestep_v15_pipeline.py` (Main entry point for generation)
- **Inference Logic:** `acestep/inference.py` (Core model loading and generation logic)
- **Task Handling:** `acestep/handler.py` (Task queue and background processing)

## Model Implementations
- **DiT Models (Base/SFT/Turbo):** `acestep/models/` (Architecture definitions)
- **Language Models (LM):** `acestep/llm_inference.py` (Logic for reasoning and blueprint generation)
- **Adapter Logic:** `acestep/openrouter_adapter.py` (Support for remote LLM backends)

## User Interfaces
- **Gradio UI Root:** `acestep/ui/gradio/` (Primary web interface)
- **Gradio Interfaces:** `acestep/ui/gradio/interfaces/` (UI layout components)
- **Gradio Events/Wiring:** `acestep/ui/gradio/events/`, `acestep/ui/gradio/events/wiring/` (Logic and event handlers)
- **Studio (HTML):** `ui/studio.html` (Lightweight DAW-like interface)

## Training & Personalization
- **LoRA/LoKR Training:** `acestep/training/`, `acestep/training_v2/` (Modules for model fine-tuning)
- **Dataset Management:** `acestep/dataset_handler.py`, `acestep/dataset/` (Data loading and augmentation)

## Utilities & Configuration
- **Audio Processing:** `acestep/audio_utils.py` (Resampling, trimming, and effects)
- **GPU Management:** `acestep/gpu_config.py` (VRAM detection and backend selection)
- **Constants:** `acestep/constants.py` (Global settings and paths)
- **API Server:** `acestep/api_server.py`, `acestep/api/` (FastAPI implementation)
- **Root Utilities:** `cli.py`, `train.py`, `generate_examples.py`, `profile_inference.py`

## Scripts & Maintenance
- **GPU Verification:** `scripts/check_gpu.py`, `scripts/profile_vram.py`
- **Data Preparation:** `scripts/prepare_vae_calibration_data.py`, `scripts/lora_data_prepare/`
- **Workflow Automation:** `scripts/new_pr_branch.ps1`

## External Documentation
- **Guides:** `docs/en/` (API, CLI, Install, etc.)