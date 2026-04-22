---
language: en
license: mit
tags:
- research
- semantic-similarity
- llm-alignment
- ai-diversity
- model-evaluation
- gemini
- llama
- gpt
datasets:
- custom
metrics:
- cosine-similarity
- semantic-divergence
---

# Quantifying the "Artificial Hivemind"

### A Semantic Diversity Audit of Large Language Models via Multi-Model Ensembles

**Author:** Tanishq Mann   
**Status:** Independent Research / Technical Preprint  

---

## 📌 Overview
As Large Language Models (LLMs) become central to autonomous agentic workflows, the risk of "semantic collapse"—where models converge on a single normative consensus—poses a significant challenge to system reliability. This research introduces a reproducible MLOps scaffold to quantify this effect, dubbed the **"Artificial Hivemind."**

## 📊 Key Findings
* **The GPT-Llama Convergence:** We identify a **78.63% semantic agreement** between the GPT-4.1 and Llama-3.3 families, suggesting they are functionally interchangeable in reasoning patterns.
* **The Gemini Outlier:** Gemini-2.5 emerged as a **Strategic Outlier**, maintaining only ~35% agreement with the other models, likely due to its proprietary training silo and differing RLHF alignment.
* **The "Manifold" Trap:** Standard temperature ablation (increasing randomness) failed to significantly expand the semantic diversity within a single model family.

## 🛠 Methodology
We utilized the **Euri Gateway** for standardized inference across multi-model ensembles. 
1. **Phase 1:** Within-model diversity audit via temperature scaling ($T=0.0$ to $T=1.5$).
2. **Phase 2:** Inter-model semantic correlation analysis across disparate model families.
3. **Visualization:** Semantic similarity heatmaps generated using `MiniLM-L6-v2` embeddings.

## 📁 Repository Contents
* `manuscript.pdf`: The full research paper.
* `heatmaps/`: High-resolution semantic similarity matrices (PNG).
* `pipeline/`: Python scripts for automated similarity scoring and inference.

## 🔗 Related Links
* **Full Paper on Academia.edu:** https://www.academia.edu/165864853/The_Echo_Chamber_Effect


## 📜 AI Disclosure & Acknowledgments
This research was developed with technical and structural assistance from Gemini and Prism, facilitating the synthesis of semantic manifold analysis and MLOps framework design. All core experimental logic and data collection were independently conceptualized and executed by **Tanishq Mann**.

---
**Citation**
```bibtex
@misc{mann2026hivemind,
  author = {Mann, Tanishq},
  title = {Quantifying the "Artificial Hivemind": A Semantic Diversity Audit of LLMs},
  year = {2026},
  publisher = {Hugging Face},
  journal = {Hugging Face Repository},
  howpublished = {\url{[https://huggingface.co/YOUR_USERNAME/Artificial-Hivemind-Audit](https://huggingface.co/YOUR_USERNAME/Artificial-Hivemind-Audit)}}
}
