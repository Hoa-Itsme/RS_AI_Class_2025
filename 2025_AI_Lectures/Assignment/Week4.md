# Week 4 Assignment – Preparing Training Data (Cleaning → Chunking → Metadata → I–A)

## Objective
This week’s assignment is to practice preparing raw academic documents into structured data for LLM fine-tuning.  
The focus is on:  
1. **Cleaning** raw extracted text  
2. **Chunking** cleaned text into manageable pieces  
3. **Adding metadata** for organization and retrieval  
4. **Building Instruction–Answer (I–A) examples**  

---

## Tasks

### Part A – Collect & Extract
- Each team must collect at least **10 documents** (PDF, DOC, or DOCX) related to **remote sensing, geology, or machine learning**.  
- Extract raw text from each file and save as `.txt` (e.g., `raw_text.txt`).  

---

### Part B – Cleaning
- Manually clean the extracted `.txt` files by removing:
  - Page numbers, headers/footers, watermarks  
  - Figure captions and broken tables (if images/tables are excluded)  
  - Redundant line breaks and extra spaces  
- Standardize chemical/mineral notations (e.g., `CO32-` → `CO3^2-`, `Fe2+` → `Fe^2+`).  
- Save cleaned files as `clean_text.txt`.

---

### Part C – Chunking
- Split each cleaned file into smaller segments (“chunks”) of around **500 words** with **50 words overlap**.  
- Save the result as `chunks.json` for each file.  

---

### Part D – Metadata
- Add minimal metadata to each chunk (e.g., title, year, tags, section).  
- Save the final version as `chunks_with_metadata.json`.  

---

### Part E – Build Instruction–Answer (I–A)
- From the `chunks_with_metadata.json`, create at least **20 instruction–answer pairs per team**.  
- Each **Instruction (I)** should be a natural language question a user might ask.  
- Each **Answer (A)** should be drawn directly from the chunk text (clean, paraphrased if needed).  

**Example:**
```json
{
  "instruction": "What are the main carbonate rock types identified in the study?",
  "answer": "The study classified carbonate rocks into limestone and dolostone, with marble and impure limestone merged into the limestone category for mapping."
}
