# 🏎️ AI & LLM Benchmarking Tools (2026 Edition)

Before you try to run the **Ultra Stress Tests**, you need to know your hardware's limits. Use these tools to measure your Tokens Per Second (TPS), VRAM usage, and thermal efficiency.

---

## 🐧 Linux (The Power User Choice)
Linux offers the most "raw" access to GPU kernels, typically yielding 5-10% better performance for Ollama.

* **[Ollama-Benchmark (obench)](https://github.com/geerlingguy/ai-benchmarks):** A simple bash script by Jeff Geerling that runs a standard set of models and outputs a clean Markdown table of your TPS.
* **[nvtop](https://github.com/Syllo/nvtop):** The "htop" for GPUs. Essential for monitoring VRAM spikes while running large models like Llama 4 or DeepSeek V3.
* **[vLLM Benchmark Suite](https://github.com/vllm-project/vllm):** If you are moving past Ollama into production-grade serving, use vLLM's internal benchmarking scripts to test throughput and latency.

---

## 🍏 macOS (Apple Silicon / Metal)
Macs are the kings of "Unified Memory," allowing you to run massive models (70B+) that would normally require $4,000 GPUs.

* **[LM Studio (Built-in)](https://lmstudio.ai/):** Includes a "Hardware Monitor" and a "Developer Lab" that gives real-time stats on Metal GPU utilization.
* **[Ollama Monitor (Menu Bar)](https://github.com/jmoiron/ollama-monitor):** A lightweight utility to keep track of which models are currently residing in your RAM/VRAM.
* **[MLPerf Client](https://mlcommons.org/benchmarks/client/):** The industry standard. The 2026 version (v1.5+) has specific optimizations for the M4/M5 Ultra chips to test sustained AI workloads.

---

## 🪟 Windows (The Gaming & NPU Tier)
Windows 11 in 2026 is heavily optimized for "AI PCs" with dedicated NPUs (Neural Processing Units).

* **[Geekbench AI](https://www.geekbench.com/ai/):** Formerly Geekbench ML. This is the best cross-platform tool to compare your NPU vs. your GPU performance.
* **[NVIDIA ChatRTX](https://www.nvidia.com/en-us/ai-on-rtx/chat-with-rtx-generative-ai/):** While not a benchmark tool itself, it includes a performance overlay specifically for RTX 50-series cards.
* **[Ollama Benchmark Tool (GUI)](https://github.com/CordatusAI/ollama-benchmark):** A Streamlit-based web app that detects your Windows GPU, pulls models automatically, and generates Plotly charts of your performance.

---

## 📊 Standardized Model Tiers for Testing
When reporting your results in this repo, please use these "Hardware Tiers" as a reference:

| Tier | Hardware Example | Recommended Model Size |
| :--- | :--- | :--- |
| **Budget** | 8GB VRAM / 16GB RAM | 1B - 3B (Gemma 3, Phi-4) |
| **Mid-Range** | 16GB VRAM / 32GB RAM | 7B - 14B (Llama 4 Scout, Mistral) |
| **Enthusiast** | 24GB+ VRAM / 64GB RAM | 30B - 70B (Qwen 3, DeepSeek R1) |
| **Workstation** | 128GB+ Unified Memory (Mac) | 100B+ (Llama 4 Maverick, GPT-OSS) |

---

## 🚀 Quick Start: The "1-Minute" Benchmark
If you have **Ollama** installed, run this command in your terminal to get an instant speed reading:

```bash
# On Linux/Mac
curl -s [https://raw.githubusercontent.com/geerlingguy/ai-benchmarks/master/obench.sh](https://raw.githubusercontent.com/geerlingguy/ai-benchmarks/master/obench.sh) | bash

# On Windows (PowerShell)
# Use the LLM-Benchmark Python tool
pip install llm-benchmark
llm_benchmark run