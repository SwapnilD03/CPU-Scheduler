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
- **Language**: C++ (STL used for queues, priority queues, etc.)  
- **Core Concepts**: Operating Systems, Scheduling Algorithms, Process Management  
- **Modules**:  
  - `parser.h` → parses input workload and configuration  
  - `scheduling.cpp` → implementation of algorithms  
  - CLI interface for trace (`trace`) or statistics (`stats`) modes  

---

## 📊 Example Usage  

### Input Format  
- **Line 1**: `"trace"` or `"stats"`  
- **Line 2**: A comma-separated list specifying which CPU scheduling policies to be analyzed/visualized, along with their parameters (if applicable).  
  - Each algorithm is represented by a number (see list below).  
  - For **Round Robin** and **Aging**, a parameter specifying the quantum `q` must be included.  
    - Example: `2-4` → Round Robin with `q=4`  
    - Example: `8-1` → Aging with `q=1`  
- **Line 3**: An integer specifying the **last instant** to be used in the simulation (timeline length).  
- **Line 4**: An integer specifying the **number of processes** to be simulated.  
- **Line 5 onwards**: Process descriptions.  

### Process Description  
- For algorithms **1 through 7**, each process line contains:  
  1. Process Name (string)  
  2. Arrival Time (int)  
  3. Service Time (int)  

- For **Aging (algorithm 8)**, each process line contains:  
  1. Process Name (string)  
  2. Arrival Time (int)  
  3. Priority (int)  

📌 **Note**:  
- Processes are assumed to be **sorted by arrival time**.  
- If two processes have the same arrival time, the one with the **lower priority** is assumed to arrive first.  


