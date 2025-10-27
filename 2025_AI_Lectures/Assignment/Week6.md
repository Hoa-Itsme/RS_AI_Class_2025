# Week 6 – Assignment  
**Topic: Incremental LoRA Fine-Tuning with Replay Sets**

---

## Part A. Practical Implementation  
Each team must perform an **incremental LoRA fine-tuning** using their previous fine-tuned model and a merged replay dataset.

### Tasks:
1. **Prepare the final dataset (`incremental_replay_final.jsonl`):**
   - Collect new geology or hyperspectral Q&A pairs (5–10 examples minimum).  
   - Select **10–30%** of samples from your **previous Week5 fine-tuning dataset** as the **replay set**.  
   - Merge both parts (new data + replay samples) into **one final `.jsonl` file**.  
   - This final file is your **training dataset** for incremental LoRA.

2. **Perform Incremental LoRA Fine-Tuning:**
   - Use your previously fine-tuned LoRA adapter as the **base model**.  
   - Train again using the merged `incremental_replay_final.jsonl`.  
   - Save the new adapter as **`lora_incremental_v2`**.

3. **Compare Results:**
   - Test both your **old LoRA model (`lora_v1`)** and your **new incremental model (`lora_incremental_v2`)** using at least **5 identical geology or hyperspectral questions**.  
   - Record differences in **accuracy, detail, and domain relevance**.

4. **Document Training Settings:**
   - List the following parameters in your report:  
     - `learning_rate`  
     - `num_train_epochs`  
     - `lora_r`, `lora_alpha`, `lora_dropout`  
     - `warmup_ratio`  
     - `per_device_train_batch_size`  
     - `gradient_accumulation_steps`

---

## Part B. Reflection and Discussion  
Answer the following in your report:

1. What improvements or changes were observed after incremental fine-tuning?  
2. How did the replay data help retain previous knowledge?  
3. What challenges occurred when merging replay data with new data?  
4. What is your plan for the next incremental update?

---

### 💡 Notes
- The **replay set is included inside the final `.jsonl` file**, not separated.  
- You only need **one `.jsonl` file** for incremental training.  
- Keep replay samples small (10–30%) to balance new learning and memory retention.  
- Continue using your Week5 LoRA fine-tuning script as the base structure.
