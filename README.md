# Building my own LLM

> A from-scratch implementation of a Large Language Model, aiming for performance comparable to Claude and enabling greater AI automation.

[![License: Apache 2.0](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![Python 3.10+](https://img.shields.io/badge/python-3.10%2B-blue.svg)](https://www.python.org/downloads/)

## About The Project
This repository documents my journey of building a Large Language Model from the ground up. The primary objective is to create a model whose capabilities are equal or relative to leading models like Claude, with the ultimate goal of enabling more advanced AI automation.

## Getting Started
To get a local copy up and running, follow these simple steps.

### Prerequisites
*   Python 3.10 or higher
*   pip or another package manager (e.g., `uv`, `poetry`)

### Roadmap

    [x) Initialize repository and basic structure
    □

    Implement tokenizer
    □

    Implement Transformer architecture
    □

    Set up training loop
    □

    Train on small dataset
    □

    Scale up and evaluate
    □

    Compare performance against target benchmarks

### Installation
1.  Clone the repo
    ```sh
    git clone https://github.com/AbeerImran1/Building-my-own-LLM.git
    cd Building-my-own-LLM





## Hardware Requirements

Building and training a Large Language Model is a highly compute-intensive task. Because the ultimate goal of this project is to build a model with capabilities relative to Claude, the training process requires enterprise-scale GPUs that are not feasible to run on standard consumer hardware.

This project is designed with a **"Thin Client" workflow**: local machines are used for development and code management, while the heavy computational lifting is offloaded to cloud environments.

### 1. Local Development (Minimum)
These are the requirements to write code, manage Git, and prepare datasets. *Note: This setup is not sufficient for training or running large models locally.*
*   **OS:** Windows 10/11, macOS, or Linux
*   **CPU:** Standard multi-core processor (e.g., Intel i5 or equivalent)
*   **RAM:** 8GB (16GB+ highly recommended to prevent system crashes during data prep)
*   **Storage:** 10GB+ free space
*   **GPU:** Integrated graphics or entry-level dedicated GPU (e.g., GTX 1060). 
    *   *Use Case:* Code editing, Git operations, and running extremely small models (e.g., 0.5B parameters) using CPU-based tools like `llama.cpp`.

### 2. Training & Fine-Tuning (Recommended Cloud Setup)
To train the model or perform heavy fine-tuning, you will need access to cloud GPUs with dedicated VRAM and modern architectures (Tensor Cores).
*   **GPU:** NVIDIA T4 (16GB VRAM) for basic fine-tuning, or NVIDIA A100 / H100 (40GB-80GB VRAM) for full pre-training.
*   **System RAM:** 12GB - 32GB+
*   **Storage:** 50GB+ high-speed SSD (NVMe)

**Recommended Platforms:**
*   **Google Colab (Free/Pro):** Excellent for learning and fine-tuning smaller models (7B-8B) using free T4 GPUs.
*   **Kaggle (Free):** Provides 30 hours/week of free GPU compute (P100 or dual T4s).
*   **RunPod / Vast.ai (Paid):** Cost-effective GPU rental (e.g., ~$0.30 - $1.50/hour for an RTX 3090 or A100). Recommended for longer, uninterrupted training runs.

### 3. Inference (Running the Final Model)
Once trained, running the model locally requires enough memory to load the model's weights.
*   **Local (Quantized):** Models can be compressed (quantized to 4-bit or 8-bit) to run on standard consumer hardware using `llama.cpp` or `Ollama`. A 7B parameter model requires roughly **4GB - 6GB of RAM/VRAM**.
*   **Cloud (Full Precision):** For full-precision inference, hosting the model on a GPU cloud server is required to maintain fast response times.

> **Note on Scale:** Training a model truly comparable to Claude from scratch requires tens of thousands of GPUs and millions of dollars. This project focuses on implementing the architecture from scratch and fine-tuning existing open-source foundations to achieve high-performance automation on a practical scale.
