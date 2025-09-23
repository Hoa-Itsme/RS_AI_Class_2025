# Week 4 Assignment – Cleaning and formatting data

## Objective
This week’s assignment is to practice preparing raw academic documents into structured data for LLM fine-tuning.  
The focus is on:  
1. **Cleaning** raw extracted text  
2. **Chunking** cleaned text into manageable pieces  
3. **Adding metadata** for organization and retrieval  

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
- Split each cleaned file into smaller segments (“chunks”) of around **500–1,000 words** with a small overlap (e.g., 50–100 words).  
- Save the result as `chunks.json` for each file.  

---

### Part D – Metadata
- Add metadata to each chunk (e.g., title, year, tags, section).  
- Save the final version as `chunks_with_metadata.json`.  

---

## Deliverables
Each team must submit:  
1. All `raw_text.txt` files (at least 10).  
2. All `clean_text.txt` files.  
3. Corresponding `chunks.json` files.  
4. Final `chunks_with_metadata.json` files.  

---

## Notes
- **Next week** we will build **Instruction–Answer (I–A) datasets** from these chunks.  
- Keep your work well-organized by topic/paper.  
- You may use Python scripts provided in lecture or your own tools.  

---
