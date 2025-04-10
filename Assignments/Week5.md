# Week 5 – User Interface and Experience
## 🎯 Goal:
In addition to Start and Stop buttons, add two more buttons: Pause and Resume

- Pause:
Temporarily halts the task but keeps the thread alive.
Disables itself and enables Resume.
- Resume:
Continues the task from where it paused.
Disables itself and re-enables Pause.
Use pause flags (e.g., pause_thread = True/False) inside your task loop so that when Pause is clicked, the thread waits until Resume is clicked. Remember to update button states with button.config(state=tk.DISABLED) or tk.NORMAL appropriately.

---

## 🛠️ while pause_thread and not stop_thread:
	          time.sleep(0.1) 


---


