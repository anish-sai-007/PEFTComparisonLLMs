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

