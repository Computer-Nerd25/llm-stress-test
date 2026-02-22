# 🗂️ AI Model Card: The Frontier Class (2026 Edition)

This guide ranks the most powerful AI models currently available. Use this as a reference when selecting an "adversary" for the **Ultra Stress Tests**.

---

## 🥇 The "Big Three" (Proprietary Giants)
These models are the current SOTA (State of the Art) for high-level reasoning and complex instruction following.

### 1. Claude Opus 4.6 (Anthropic)
* **The Specialization:** The "Human-Reasoning" King.
* **Best For:** Agentic coding, nuanced creative writing, and the **Lipogram Challenges**.
* **Unique Feature:** "Extended Thinking" mode that spends up to 2 minutes "pre-thinking" before outputting a single word.
* **Stress Test Performance:** Currently holds the record for the most successful completions of the *Non-Euclidean Room* challenge.

### 2. Gemini 3.1 Pro (Google)
* **The Specialization:** The "Context" Titan.
* **Best For:** Massive data analysis and high-level physics/math problems.
* **Unique Feature:** **2 Million+ Token Context Window**. It can ingest 10 entire GitHub repositories at once and find a single variable error.
* **Stress Test Performance:** Dominates the *Spatial Reasoning* and *Large-Scale Logic* categories.

### 3. GPT-5.2 (OpenAI)
* **The Specialization:** The "Generalist" Powerhouse.
* **Best For:** Tool use, structured JSON outputs, and multi-modal tasks (Image + Text).
* **Unique Feature:** "Smart Routing"—automatically switches between "Thinking" (o-series) and "Fast" (flash) kernels depending on prompt difficulty.
* **Stress Test Performance:** Best at the *Polyglot Quine* and *Adversarial Safety* tests.

---

## 🔓 The Open-Weight Disruptors (Run Locally)
These models can be downloaded and run on your own hardware using **Ollama** or **LM Studio**.

### 1. Llama 4 Scout (Meta)
* **Size:** 109B (17B Active - MoE)
* **Why it's in this repo:** It features a massive **10 Million token context window** in an open-weight format.
* **Best Use:** Large-scale local code refactoring.

### 2. DeepSeek V3.2 "Speciale"
* **Size:** 671B (MoE)
* **Why it's in this repo:** It currently outperforms GPT-4o in mathematical benchmarks (AIME/HMMT). 
* **Note:** Requires significant VRAM (Dual A100s or high-end Mac Studio) to run at full precision.

### 3. Qwen 3.5 Max (Alibaba)
* **The "Polyglot" Choice:** Exceptional at cross-language translation and coding in obscure languages like COBOL or Fortran.

---

## 📈 Model Comparison Table (Feb 2026)

| Model | Category | Logic Score | Coding Score | Reasoning Bias |
| :--- | :--- | :--- | :--- | :--- |
| **Claude Opus 4.6** | Proprietary | 98% | 94% | Nuanced/Concise |
| **GPT-5.2** | Proprietary | 96% | 92% | Precise/Tool-Oriented |
| **Gemini 3.1 Pro** | Proprietary | 95% | 89% | Broad/Creative |
| **DeepSeek R1** | Open-Weight | 92% | 95% | Technical/Physics |
| **Llama 4 Scout** | Open-Weight | 88% | 85% | Educational/Clear |

---

## 🛠️ Recommended Setup for Testing
To get the most out of these models for our stress tests:
1. **Temperature:** Set to `0.0` for logic/math (Consistency) and `0.7` for creative prompts (Variety).
2. **Top_P:** Set to `0.9` to allow the model to explore more "creative" token paths in lipogram tests.
3. **Presence Penalty:** Increase this if the AI keeps repeating the same "I cannot do that" refusal.