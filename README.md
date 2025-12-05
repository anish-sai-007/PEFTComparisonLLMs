# PEFTComparisonLLMs

**Systematic comparison of LoRA, Prefix Tuning, Prompt Tuning, and hybrid PEFT methods across sentiment analysis, code generation, and mathematical reasoning tasks.**

---

## 📘 Overview

As large language models (LLMs) scale into billions of parameters, full fine-tuning becomes computationally expensive. This project explores **Parameter-Efficient Fine-Tuning (PEFT)** methods that adapt pre-trained models using minimal trainable parameters.

We compare four PEFT strategies:
- **LoRA (Low-Rank Adaptation)**
- **Prefix Tuning**
- **Prompt Tuning**
- **LoRA + Prompt Hybrid**

Across three tasks:
- **Sentiment Analysis** (SST-2 → IMDB)
- **Mathematical Reasoning** (DeepMath, MATH-500, GSM8K, AIME)
- **Code Generation** (CodeParrot → HumanEval)

---

## 🧪 Key Findings

| Task                | Best Method     | Metric         | Trainable Params |
|---------------------|------------------|----------------|------------------|
| Sentiment Analysis  | LoRA             | Accuracy: 79.8% | 0.0136%           |
| Code Generation     | Prompt Tuning    | Pass@1: 89.63%  | 0.65%             |
| Math Reasoning      | LoRA + Prompt    | EM: 68%         | ~1.6M             |

- LoRA is extremely efficient for classification.
- Prompt Tuning preserves code generation capabilities best.
- Hybrid methods outperform others on complex reasoning tasks.

---

## 📁 Repository Structure

PEFTComparisonLLMs/ │ ├── report/ # Final PDF report ├── src/ # Training scripts for each task │ ├── sentiment_analysis/ │ ├── code_generation/ │ └── math_reasoning/ ├── configs/ # PEFT configurations (LoRA, Prompt, Prefix) ├── results/ # Evaluation metrics and logs ├── notebooks/ # Ablation study and analysis └── README.md # Project overview


---

## ⚙️ Setup Instructions

```bash
git clone https://github.com/anish-sai-007/PEFTComparisonLLMs.git
cd PEFTComparisonLLMs
pip install -r requirements.txt
Citation
Popuri, Nimmagadda, Ravinuthala (2025). Systematic Comparison of Parameter-Efficient Fine-Tuning Methods for Large Language Models.
License
This project is licensed under the MIT License.
🙏 Acknowledgements
Special thanks to Professor Dhruv Kumar and Mr. Ayush Gupta for their mentorship and support throughout this project.
