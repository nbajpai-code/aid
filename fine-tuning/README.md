# 🔧 Fine-Tuning & Optimization

Fine-tuning allows developers to customize pre-trained foundation models (LLMs, VLMs) on private datasets. This section curates the best libraries, tools, and configurations for Parameter-Efficient Fine-Tuning (PEFT), distributed training, and reinforcement learning from human/AI feedback (RLHF/RLAIF).

---

## 🏎️ High-Performance Fine-Tuning Libraries

### Unsloth
A library that makes LLM fine-tuning up to 5x faster and uses 80% less GPU memory with no loss in accuracy. Unsloth achieves this by rewriting backpropagation kernels in OpenAI's **Triton** language.
*   **GitHub**: [unslothai/unsloth](https://github.com/unslothai/unsloth)
*   **Key Features**:
    *   Supports QLoRA and LoRA on a single GPU (even free Colab tiers).
    *   Fast manual backpropagation.
    *   Supports popular models: Llama 3, Phi-4, Mistral, Gemma 2.

### PEFT (Parameter-Efficient Fine-Tuning)
Hugging Face's standard library for adapting large pre-trained models by training only a small fraction of parameters.
*   **GitHub**: [huggingface/peft](https://github.com/huggingface/peft)
*   **Supported Methods**:
    *   **LoRA (Low-Rank Adaptation)**: Injects trainable rank-decomposition matrices into transformer layers.
    *   **QLoRA (Quantized LoRA)**: Backpropagates gradients through a frozen, 4-bit quantized pretrained model.
    *   Prefix Tuning, Prompt Tuning, and IA3.

### TRL (Transformer Reinforcement Learning)
A full-stack library by Hugging Face to train transformer language models using reinforcement learning and alignment techniques.
*   **GitHub**: [huggingface/trl](https://github.com/huggingface/trl)
*   **Supported Methods**:
    *   **Supervised Fine-Tuning (SFT)**: Simple model instruction tuning.
    *   **DPO (Direct Preference Optimization)**: A simpler alternative to RLHF that optimizes models directly on preference pairs without training a reward model.
    *   **PPO (Proximal Policy Optimization)**: Classical RLHF using actor-critic networks.
    *   **ORPO / KTO**: Pairwise alignment techniques that bypass explicit reference model steps.

---

## 🛠️ Configuration & GUI Frameworks

For orchestrating runs without writing custom PyTorch training loops from scratch.

### Axolotl
A highly flexible tool designed to consolidate various LLM fine-tuning mechanisms. It uses simple YAML configuration files to define datasets, model architectures, hyperparameters, and logging.
*   **GitHub**: [axolotl-ai-co/axolotl](https://github.com/axolotl-ai-co/axolotl)
*   **Key Features**:
    *   Integrates with DeepSpeed, FSDP, FlashAttention, and packaging formats (HF, GGUF).
    *   Highly reproducible: share your YAML file to replicate exact training configurations.

### LLaMA-Factory
An easy-to-use, unified framework for fine-tuning over 100 LLMs. It features **LLaMA Board**, a complete Web UI for managing training runs, evaluating models, and exporting GGUF weights.
*   **GitHub**: [hiyouga/LLaMA-Factory](https://github.com/hiyouga/LLaMA-Factory)
*   **Key Features**:
    *   Training without coding via a web interface.
    *   Supports SFT, DPO, PPO, ORPO, Pre-training, and Direct Preference Optimization.

---

## 🌐 Distributed Scale Training

For training massive models that exceed the memory capacity of a single GPU, requiring sharding across multi-node, multi-GPU clusters.

### DeepSpeed
Microsoft's deep learning optimization library that makes distributed training efficient and easy.
*   **GitHub**: [microsoft/DeepSpeed](https://github.com/microsoft/DeepSpeed)
*   **Core Technology**: **ZeRO (Zero Redundancy Optimizer)**, which shards optimizer states, gradients, and model parameters across GPUs to virtually eliminate memory redundancy.

### FSDP (Fully Sharded Data Parallel)
PyTorch’s native distributed training technology.
*   **Documentation**: [pytorch.org/docs/stable/fsdp](https://pytorch.org/docs/stable/fsdp.html)
*   **Best Used For**: Seamless, standard PyTorch-based scaling of large models across clusters using native CUDA environments.
