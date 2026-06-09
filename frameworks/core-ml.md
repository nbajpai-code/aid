# 📐 Core Machine Learning Frameworks

The foundational libraries for numerical computing, tensor manipulations, deep learning model architectures, and scientific computing.

---

## 🔥 Deep Learning Frameworks

### PyTorch
The premier open-source machine learning library for researchers and production engineers alike. Developed initially by Meta AI, it is built on a dynamic computational graph design (Eager Mode) and provides seamless CUDA acceleration.
*   **GitHub**: [pytorch/pytorch](https://github.com/pytorch/pytorch)
*   **Documentation**: [pytorch.org/docs](https://pytorch.org/docs/)
*   **Key Strengths**:
    *   Large and active community; almost all modern research papers publish code in PyTorch.
    *   Robust compiler subsystem (`torch.compile`) introduced in PyTorch 2.0.
    *   Rich ecosystem of domain libraries: `torchvision` (Computer Vision), `torchaudio` (Audio/Speech), `torchtext` (NLP).

### JAX
Developed by Google, JAX combines Autograd and XLA (Accelerated Linear Algebra) for high-performance numerical computing and machine learning research. JAX uses a functional programming model.
*   **GitHub**: [google/jax](https://github.com/google/jax)
*   **Documentation**: [jax.readthedocs.io](https://jax.readthedocs.io/)
*   **Key Strengths**:
    *   **Composability**: Transform functions via decorators like `@jit` (Just-In-Time compile to GPU/TPU), `@grad` (automatic differentiation), `@vmap` (automatic vectorization), and `@pmap` (parallel execution on multiple devices).
    *   Excellent choice for large-scale distributed training on TPUs and GPU clusters.
*   **Popular JAX Neural Network Libraries**:
    *   **Flax**: A high-performance neural network library and ecosystem for JAX. [GitHub](https://github.com/google/flax)
    *   **Equinox**: Neural networks and libraries in JAX via callable PyTrees. [GitHub](https://github.com/patrick-kidger/equinox)
    *   **Optax**: Gradient processing and optimization library for JAX. [GitHub](https://github.com/google-deepmind/optax)

### Keras 3
Keras is a high-level API designed for human beings, not machines. Keras 3 is a multi-backend framework supporting **PyTorch**, **JAX**, and **TensorFlow** interchangeably.
*   **GitHub**: [keras-team/keras](https://github.com/keras-team/keras)
*   **Documentation**: [keras.io](https://keras.io/)
*   **Key Strengths**:
    *   Write model code once and run it on top of any backend.
    *   Enables training models using PyTorch on GPUs, or JAX on TPUs, with the exact same codebase.

---

## 📊 Classical Machine Learning & Data Science

Even in the era of Deep Learning, traditional machine learning and high-performance data processing libraries are critical for feature engineering, baseline models, and data loading pipelines.

### Scikit-learn
The industry standard library for classical machine learning algorithms (regression, classification, clustering, dimensionality reduction).
*   **GitHub**: [scikit-learn/scikit-learn](https://github.com/scikit-learn/scikit-learn)
*   **Use Cases**: Random forests, Gradient Boosting, SVMs, PCA, K-Means clustering, and data preprocessing.

### NumPy & SciPy
*   **NumPy**: The fundamental package for scientific computing in Python, offering powerful N-dimensional array objects and mathematical operations. [Website](https://numpy.org/)
*   **SciPy**: A collection of mathematical algorithms and convenience functions built on NumPy (integration, optimization, statistics, signal processing). [Website](https://scipy.org/)

### Pandas & Polars
*   **Pandas**: The classic data analysis and manipulation library. Ideal for handling tabular data via DataFrames. [GitHub](https://github.com/pandas-dev/pandas)
*   **Polars**: A lightning-fast, multithreaded DataFrame library written in Rust and optimized for large datasets. Offers significant speedups over Pandas via a lazy execution engine. [GitHub](https://github.com/pola-rs/polars)
