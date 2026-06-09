# 🔍 Evaluation & Observability

Unlike deterministic software, LLM applications are non-deterministic and prone to hallucinations, shifts in user behaviors, and API changes. This section lists the top frameworks for auditing prompts, tracing nested model calls (observability), and scoring model outputs (evaluation).

---

## 🗺️ LLM Engineering & Tracing Platforms

These platforms allow developers to trace execution trees (e.g., chains, agent loops, database queries), log token counts/latency, and manage prompt templates centrally.

### Langfuse
A production-grade, open-source LLM engineering platform. It provides tracing, prompt management, evaluations, and usage/cost metrics.
*   **GitHub**: [langfuse/langfuse](https://github.com/langfuse/langfuse)
*   **Key Features**:
    *   **Open Source & Self-hostable**: Runs via Docker easily.
    *   **OpenTelemetry Compatible**: SDKs for Python, JS/TS, LangChain, and LlamaIndex.
    *   **Prompt Management**: Create, version, and fetch prompts directly from the dashboard, preventing hard-coding.
    *   **Auto-Evaluations**: Schedule LLM-as-a-judge scoring based on latency, user feedback, or cost.

### LangSmith
LangChain's proprietary platform for debugging, testing, evaluating, and monitoring LLM applications.
*   **Website**: [smith.langchain.com](https://smith.langchain.com/)
*   **Key Features**:
    *   Deep native integration with the LangChain ecosystem.
    *   Excellent UI for inspecting complex, nested agent loops.
    *   Allows building custom datasets directly from production logs to run regressions.

### Arize Phoenix
An open-source AI observability platform developed by Arize. It focuses on evaluating LLM applications, tracing execution, and visualizing embedding clusters.
*   **GitHub**: [Arize-AI/phoenix](https://github.com/Arize-AI/phoenix)
*   **Key Features**:
    *   Runs locally inside Jupyter Notebooks.
    *   Specializes in **RAG diagnostics** and detecting drift in vector spaces.
    *   Integrates with LLM-as-a-judge frameworks.

---

## 📊 Evaluation & Benchmarking Libraries

These libraries are designed to run programmatic tests to grade LLM behaviors.

### Ragas (Retrieval Augmented Generation Assessment)
A framework designed specifically to evaluate Retrieval-Augmented Generation pipelines.
*   **GitHub**: [explodinggradients/ragas](https://github.com/explodinggradients/ragas)
*   **Key Metrics**:
    *   **Faithfulness**: Does the generated answer match the retrieved context?
    *   **Answer Relevance**: Does the answer address the question?
    *   **Context Recall/Precision**: Did the retriever fetch all necessary information?

### Promptfoo
A CLI tool and library for testing and evaluating LLM outputs. It is designed to compare prompts, model versions, and temperature parameters side-by-side.
*   **GitHub**: [promptfoo/promptfoo](https://github.com/promptfoo/promptfoo)
*   **Key Features**:
    *   **CLI First**: Fast test runner for CI/CD pipelines.
    *   Runs checks for red-teaming (security vulnerabilities, injection attacks, toxic language).
    *   Compare models (e.g., GPT-4o vs Claude 3.5 Sonnet vs Llama 3) on the same dataset.

### TruLens
An open-source library that helps developers evaluate and track the performance of LLM-based applications.
*   **GitHub**: [truera/trulens](https://github.com/truera/trulens)
*   **Key Concept**: Uses the **RAG Triad** (Context Relevance, Groundedness, Answer Relevance) to run automatic evaluation scripts.

---

## 📈 ML Experiment Tracking

For deep learning research and model fine-tuning runs (tracking GPU metrics, loss, and hyperparameter tables).

### Weights & Biases (W&B)
The industry standard developer tool for machine learning experiment tracking, dataset versioning, and collaborative model analysis.
*   **GitHub**: [wandb/wandb](https://github.com/wandb/wandb)
*   **Key Features**:
    *   Interactive dashboards for tracking system utilization (GPU temp, memory) alongside validation loss.
    *   Automated sweeps for hyperparameter optimization.
