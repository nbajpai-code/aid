# ⚡ Inference & Model Serving Engines

Model serving engines are specialized software runtimes designed to compile, load, optimize, and expose Large Language Models (LLMs) and other AI architectures as high-performance APIs (typically OpenAI-compatible endpoints).

---

## 🚀 Cloud & Enterprise Production Servers

These servers are designed to run on high-end GPU clusters (NVIDIA A100, H100, H200, etc.) to serve thousands of concurrent requests.

### vLLM
A highly flexible, fast, and easy-to-use library for LLM inference and serving. vLLM is renowned for introducing **PagedAttention**, which dramatically reduces GPU memory fragmentation.
*   **GitHub**: [vllm-project/vllm](https://github.com/vllm-project/vllm)
*   **Key Features**:
    *   **PagedAttention**: Manages KV-cache memory like virtual memory pages in operating systems.
    *   Continuous batching of incoming requests.
    *   Quantization support: AWQ, GPTQ, SqueezeLLM, FP8, INT4/INT8.
    *   Out-of-the-box OpenAI-compatible API server.

### SGLang
A fast serving engine designed specifically for structured output generation (JSON, tool calling) and multi-turn chat dialogues.
*   **GitHub**: [sgl-project/sglang](https://github.com/sgl-project/sglang)
*   **Key Features**:
    *   **RadixAttention**: Automatically caches KV-cache across multiple queries sharing the same prefix (e.g. system prompts, few-shot examples), resulting in massive throughput gains.
    *   Fast compiler for constrained structured output generation.

### Triton Inference Server
NVIDIA’s multi-framework, industrial-strength serving software.
*   **GitHub**: [triton-inference-server/server](https://github.com/triton-inference-server/server)
*   **Best Used For**: Running mixed workloads (e.g., serving PyTorch, ONNX, and TensorRT models from the same server) and dynamically grouping multiple GPUs.

### TensorRT-LLM
An open-source library by NVIDIA that compiles LLM architectures into highly optimized TensorRT engines.
*   **GitHub**: [NVIDIA/TensorRT-LLM](https://github.com/NVIDIA/TensorRT-LLM)
*   **Best Used For**: Achieving the absolute absolute lowest latency and highest throughput on NVIDIA Tensor Core GPUs. Often run inside Triton Inference Server.

### Hugging Face TGI (Text Generation Inference)
A purpose-built framework for deploying and serving LLMs in production.
*   **GitHub**: [huggingface/text-generation-inference](https://github.com/huggingface/text-generation-inference)
*   **Features**: Speculative decoding, continuous batching, tensor parallel support, and watermarking.

---

## 💻 Local Developer Runtimes

These engines are optimized to run on consumer hardware (MacBooks, local gaming rigs with RTX cards, or CPU-only setups).

### Ollama
The absolute easiest way to get up and running with large language models locally. Ollama packages model weights, configurations, and CPU/GPU runtimes into a single tool.
*   **GitHub**: [ollama/ollama](https://github.com/ollama/ollama)
*   **Key Features**:
    *   Simple command-line interface (`ollama run llama3`).
    *   Automated GPU acceleration detection (Apple Silicon Metal, CUDA, ROCm).
    *   Exposes a local server (`localhost:11434`) with an OpenAI-compatible endpoint.
    *   Imports GGUF models via a custom `Modelfile`.

### llama.cpp
A plain C/C++ implementation of LLM inference designed by Georgi Gerganov. It is the core engine powering the open-weight local LLM revolution.
*   **GitHub**: [ggerganov/llama.cpp](https://github.com/ggerganov/llama.cpp)
*   **Key Features**:
    *   Zero dependencies, compiled with state-of-the-art SIMD instructions (AVX-512, NEON) for CPU execution.
    *   Introduced the **GGUF** model format, enabling mixed CPU-GPU offloading.
    *   Supports Apple Silicon (Metal API) and CUDA.
