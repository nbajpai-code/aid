# 🧩 Frameworks & Libraries

Welcome to the Frameworks & Libraries section of the AI Developer Resources Hub. This directory contains detailed guides, links, and use cases for the software stacks powering modern AI and ML applications.

---

## 🗺️ Navigation

### 1. [**Core Machine Learning**](core-ml.md)
Foundational frameworks for tensor computation, automatic differentiation, neural networks, and scientific computing.
*   **Key Libraries**: PyTorch, JAX, TensorFlow, SciPy, NumPy.

### 2. [**LLM & Agent Frameworks**](llm-agents.md)
Libraries designed to compose Large Language Models (LLMs) with external tools, stateful logic, and multi-agent interaction.
*   **Key Libraries**: Hugging Face Transformers, LangChain, LlamaIndex, DSPy, LangGraph, AutoGen, CrewAI, PydanticAI.

### 3. [**VLM & Multimodal**](vlm-multimodal.md)
Libraries for processing and generating data across multiple modalities, including computer vision, speech, image generation, and audio synthesis.
*   **Key Libraries**: Diffusers, Whisper, CLIP, Segment Anything (SAM).

---

## 🛠️ Typical Stack Selection Guide

Depending on your engineering goals, here is a quick reference guide on which frameworks to use:

| Project Type | Recommended Frameworks | Why? |
| :--- | :--- | :--- |
| **Deep Learning Research** | PyTorch, JAX | Flexible automatic differentiation, research community standard, TPU acceleration (JAX). |
| **Production LLM Orchestration** | LangGraph, PydanticAI | Predictable graph-based state machines, strict type validation, tool-calling reliability. |
| **Document Search & Q&A (RAG)** | LlamaIndex, LangChain | Out-of-the-box data ingestion, chunking, and advanced vector query retrieval structures. |
| **Generative Media (Image/Video)** | Diffusers, PyTorch | Hugging Face Diffusers is the industry standard for Stable Diffusion, Flux, and other generative models. |
| **Speech-to-Text / Audio** | Whisper, PyTorch | OpenAI's Whisper model (and its community ports like `faster-whisper`) provides state-of-the-art transcription. |

---

## 📈 Choosing Between PyTorch & JAX

For fundamental model development and training:
- **PyTorch** remains the industry standard for production deployments, model sharing on Hugging Face, and has the largest ecosystem of tools, pre-trained weights, and tutorials.
- **JAX** (developed by Google) is highly favored for massive-scale training (especially on Google Cloud TPUs) because of its functional programming design, `jit` compilation, `vmap` (vectorization), and `pmap` (parallelization).
