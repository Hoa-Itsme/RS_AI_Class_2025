# Week 7 – Assignment  
**Topic:** Advanced System Prompts and Prompt Chaining  

---

## 🎯 Objective  
Continue **incremental LoRA training** with new data, then design and test your own **prompt chaining strategy** to compare reasoning and response quality with previous results.

---

## 🧩 Tasks  

### **Part A – Incremental Training**  
1. Merge new dataset with replay samples into a single `.jsonl` file.  
2. Load your **Week 6 adapter** and perform **incremental fine-tuning** with the new data.  
3. Save the new adapter as `week7_adapter`.  

---

### **Part B – Prompt Chaining Test**  
1. Load both **Week 6** and **Week 7** adapters in Text Generation WebUI (or equivalent).  
2. Each team designs their **own system prompt** that applies **prompt chaining logic** (multi-step reasoning or structured answering).  
3. Test both adapters with the same few questions and compare responses:
   - Structure and reasoning flow  
   - Technical accuracy  
   - Clarity and consistency  

Use at least **three test questions** relevant to your dataset.

---

### **Part C – Report**  
Create a brief table comparing outcomes:

| Adapter | Prompt Type | Reasoning Quality | Accuracy | Notes |
|----------|--------------|------------------|-----------|-------|
| Week6 | Normal |  |  |  |
| Week6 | With Chaining |  |  |  |
| Week7 | Normal |  |  |  |
| Week7 | With Chaining |  |  |  |

Add 3–5 sentences summarizing your observations.

---

## 📘 Submission  
- `week7_training_log.txt`  
- `week7_results.txt` (sample outputs)  
- `week7_report.docx` (table + discussion)

---

**Goal:**  
Evaluate how incremental fine-tuning enhances knowledge and how prompt chaining affects reasoning style and output quality.
