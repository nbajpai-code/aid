# 🎨 Vision-Language & Multimodal AI Frameworks

Libraries for processing and generating data beyond plain text, covering computer vision, image generation, speech-to-text, text-to-speech, and vision-language architectures.

---

## 🖼️ Generative Image & Video Models

### Diffusers
Hugging Face's state-of-the-art library for diffusion models. It provides a simple, modular API to generate images, audio, and even 3D molecular structures.
*   **GitHub**: [huggingface/diffusers](https://github.com/huggingface/diffusers)
*   **Key Models Supported**: Stable Diffusion, SDXL, Flux, Kandinsky, ControlNet (for guided generation), and Stable Video Diffusion.
*   **Features**:
    *   Optimized pipelines for low VRAM execution, GPU memory offloading, and half-precision (FP16/BF16) arithmetic.
    *   Support for scheduling algorithms (DDIM, Euler, DPM-Solver) to trade off generation speed and quality.

### ComfyUI
A powerful, node-based graphical user interface (GUI) and backend for Stable Diffusion and general generative model pipelines.
*   **GitHub**: [comfyanonymous/ComfyUI](https://github.com/comfyanonymous/ComfyUI)
*   **Key Strengths**:
    *   Complete control over the execution flow without writing Python code.
    *   Highly optimized; executes models faster and with less VRAM than traditional web GUIs (like AUTOMATIC1111).
    *   Highly extensible via custom nodes.

---

## 🔊 Speech, Audio & Transcription

### Whisper (Speech-to-Text)
OpenAI's state-of-the-art speech recognition and translation model trained on 680,000 hours of multilingual web data.
*   **GitHub**: [openai/whisper](https://github.com/openai/whisper)
*   **Community Optimizations**:
    *   **`faster-whisper`**: A reimplementation using CTranslate2 (a fast inference engine for Transformer models). Up to 4x faster and uses significantly less memory than the original implementation. [GitHub](https://github.com/SYSTRAN/faster-whisper)
    *   **`whisper.cpp`**: High-performance C/C++ port of Whisper. Lightweight, zero dependencies, optimized for Apple Silicon (Core ML support) and standard CPUs. [GitHub](https://github.com/ggerganov/whisper.cpp)

### Speech Synthesis (Text-to-Speech)
- **Bark**: A transformer-based audio generation model by Suno. It can generate highly realistic speech, music, background noise, and simple sound effects. [GitHub](https://github.com/suno-ai/bark)
- **XTTS**: A voice-cloning model that allows you to clone voices in multiple languages using a short 3-second audio clip. [GitHub](https://github.com/coqui-ai/TTS)

---

## 👁️ Computer Vision & Vision-Language Models (VLMs)

### Segment Anything (SAM & SAM 2)
Developed by Meta AI, Segment Anything is a foundation model for image segmentation. It can identify and segment any object in an image or video with a single click or prompt.
*   **GitHub**: [facebookresearch/segment-anything-2](https://github.com/facebookresearch/segment-anything-2)
*   **Use Cases**: Mask generation, object tracking, interactive photo/video editing.

### CLIP (Contrastive Language-Image Pre-training)
OpenAI's model that learns visual concepts from natural language supervision. It maps images and texts to a shared embedding space.
*   **GitHub**: [openai/CLIP](https://github.com/openai/CLIP)
*   **Use Cases**: Image classification without explicit training labels (zero-shot classification), semantic image search, and image retrieval.

### Vision-Language Models (VLMs)
Models that process interleaved image and text inputs to perform tasks like visual question answering, OCR, and document analysis.
*   **Key Models**:
    *   **LLaVA**: An open-source VLM connecting a vision encoder with an LLM for chat-like visual reasoning. [GitHub](https://github.com/haotian-liu/LLaVA)
    *   **Qwen-VL / Qwen2-VL**: Highly capable open vision models capable of understanding long videos, dense text OCR, and UI screen parsing. [GitHub](https://github.com/QwenLM/Qwen2-VL)
