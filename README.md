# 🦙 QLoRA Fine-Tuning on LLaMA-2

> Fine-tuning LLaMA-2 7B on domain-specific datasets using QLoRA and Chain-of-Thought (CoT) data.

🔗 **[Full Write-Up on Medium](https://medium.com/@venkat.ramrao/fine-tuning-llama-2-using-qlora-and-a-cot-dataset-515f38b3972d)**

---

## 🧠 Overview

This repository showcases the use of **QLoRA (Quantized Low-Rank Adapter)** to fine-tune Meta's **LLaMA-2 7B** model using datasets focused on extractive question answering and reasoning.

📌 Core takeaways:
- **Excellent performance in extractive QA**
- **Limited reasoning capability on smaller model sizes**
- Future testing planned with larger LLaMA-2 variants

---

## 📚 Datasets Used

1. **[KAIST AI CoT Collection](https://github.com/kaistAI/CoT-Collection)**  
   📝 Paper: [arXiv:2305.14045](https://arxiv.org/abs/2305.14045)

2. **[PubMed-QA](https://pubmedqa.github.io/)**  
   📝 Paper: [arXiv:1909.06146](https://arxiv.org/abs/1909.06146)

3. **[Databricks Dolly 15K](https://huggingface.co/datasets/databricks/databricks-dolly-15k)**  
   For instruction tuning and multi-domain QA

---

## 📁 Repo Contents

```
qlora-llama2/
├── qlora_CoT_Calling_ONLY.ipynb           # Fine-tuning with CoT dataset
├── qlora_llama2_clean_CoT-Dataset.ipynb   # Preprocessing CoT data
├── qlora_llama2_clean_Pubmed.ipynb        # Preprocessing PubMedQA data
├── README.md
```

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/<your-username>/qlora-llama2.git
cd qlora-llama2
```

### 2. Install dependencies

> Ensure you're using Python 3.10+ and `transformers`, `peft`, `bitsandbytes`, and `accelerate` are installed.

```bash
pip install -r requirements.txt
```

### 3. Run notebooks

Open and run:
- `qlora_llama2_clean_CoT-Dataset.ipynb` → Prepare CoT dataset  
- `qlora_llama2_clean_Pubmed.ipynb` → Prepare PubMed-QA  
- `qlora_CoT_Calling_ONLY.ipynb` → Fine-tune the model

---

## 📊 Results & Observations

- **Strong results** in extractive QA (PubMed-QA, Dolly)
- **Struggles in CoT-based reasoning tasks** with 7B model
- **Planned**: Scale to 13B or 65B for more reasoning depth

---

## 🙌 Acknowledgements

Thanks to the creators of:
- [Meta's LLaMA-2](https://ai.meta.com/llama/)
- [QLoRA by Tim Dettmers](https://arxiv.org/abs/2305.14314)
- [Hugging Face Transformers](https://huggingface.co/transformers/)

---

## ✍️ Author

**Venkat Ramrao**  
📖 [Medium Blog](https://medium.com/@venkat.ramrao)
