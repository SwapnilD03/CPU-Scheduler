# CPU-Scheduler

# Operating System Scheduling Simulator  

## 📌 Overview  
This project is a **C++ implementation of classical CPU scheduling algorithms**, designed to simulate and analyze how different scheduling policies impact process execution in an operating system.  
It provides both **timeline (Gantt chart) visualizations** and **statistical metrics** to compare algorithms on performance and fairness.  

---

## 🚀 Features  
- Supports **8 Scheduling Algorithms**:  
  - **FCFS** – First Come First Serve  
  - **RR** – Round Robin (with configurable quantum)  
  - **SPN** – Shortest Process Next (non-preemptive)  
  - **SRT** – Shortest Remaining Time (preemptive SPN)  
  - **HRRN** – Highest Response Ratio Next  
  - **FB-1** – Feedback Queue (1 unit time slice)  
  - **FB-2i** – Feedback Queue with increasing quantum (2^i)  
  - **Aging** – Priority-based scheduling with aging to prevent starvation  

- **Performance Statistics**:  
  - Finish Time  
  - Turnaround Time  
  - Normalized Turnaround Time  
  - Average metrics across processes  

- **Visualization**:  
  - Gantt chart–style timeline to track execution order  
  - Ready/wait states clearly represented  

---

## 🛠️ Tech Stack  
- **Language**: C++ 
- **Core Concepts**: Operating Systems, Scheduling Algorithms, Process Management  
- **Modules**:  
  - `parser.h` → parses input workload and configuration  
  - `main.cpp` → implementation of algorithms  
  - CLI interface for trace (`trace`) or statistics (`stats`) modes  

---



Example:  

