# Week 5 – Assignment  
**Topic: Fine-Tuning Workflow (LoRA/QLoRA on Llama-3.1-8B)**

---

## Part A. Parameter Analysis  
Each group must analyze and explain the meaning and role of the following parameters used in fine-tuning.  
For each, answer:  
1. **What does this parameter control?**  
2. **What happens if we increase or decrease it?**  
3. **What is the typical good range or default value?**  
4. **Why is this important for our fine-tuning task (geology / hyperspectral domain)?**

**Parameters to analyze:**
- `learning_rate`  
- `num_train_epochs`  
- `per_device_train_batch_size`  
- `gradient_accumulation_steps`  
- `max_length` / `max_new_tokens`  
- `lora_r` (rank)  
- `lora_alpha`  
- `lora_dropout`  
- `include_mlp` (LoRA applied to MLP or not)  
- `warmup_ratio`  
- `lr_scheduler_type`  
- `bf16 / fp16` choice  
- `logging_steps`  

Prepare your answers in a short **report or slides**, with examples where possible.  

---

## Part B. Fine-Tuning Practice  
Each group will perform their own fine-tuning using their prepared `.jsonl` file from last week.  

1. **Prepare data**  
   - Verify your `.jsonl` has the required fields:  
     `system`, `instruction`, `context`, `answer`  
   - Minimum: at least **20 samples** to fine-tune.  

2. **Run fine-tuning**  
   - Use the provided training script (`train_lora.py`).  
   - Make sure you set the correct path to your `.jsonl` file.  
   - Save your adapter model in your group folder.  
   - Track and report your **final train loss and perplexity**.  

3. **Test the fine-tuned model**  
   - Use the provided `inference_lora.py` script.  
   - Each group must prepare **at least 5 test questions** (instructions + context) related to your dataset.  
   - Compare the model’s answers with your expected answers.  

4. **Discussion**  
   - Was the model’s output correct and useful?  
   - Did fine-tuning improve over the base model?  
   - Which parameters seemed most critical in your run?  

---

## Deliverables
- **One report or presentation per group**, containing:  
  - Parameter analysis (Part A)  
  - Screenshots or logs from training (loss values, TensorBoard if available)  
  - At least 5 test Q&A results from your fine-tuned model (Part B)  
  - Your group’s reflections: what worked, what was difficult, what you would improve.  

---

## Submission
- Submit your **slides (.pptx) or report (.pdf)** on GitHub Classroom.  
- Deadline: **Next week before class**.  

---

👉 This assignment will help you not only **understand what each parameter does** but also **see directly how your fine-tuned model behaves** on geology/hyperspectral Q&A tasks.
