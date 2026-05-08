# Intelligent I/O and Storage Scheduling

This project explores ML-based disk scheduling, replacing or augmenting traditional I/O elevators with machine learning models that predict request service times and optimize queue ordering.

## Research Angles Explored
- **ML-Based Disk Scheduling:** Uses predictive models (like Random Forest) to estimate seek and transfer latency based on Logical Block Addressing (LBA) distance and request size.
- **Evaluation Metrics:** Compares average latency improvements between traditional First-Come-First-Serve (FCFS) and ML-augmented schedulers.

## Project Structure
- `intelligent_io_scheduling.ipynb`: A Jupyter Notebook containing the synthetic trace generation, ML model training, and the scheduler queue simulation.

## Requirements
```bash
pip install numpy pandas scikit-learn matplotlib jupyter
```

## How to Run
1. Clone this repository (placeholder link):
   ```bash
   git clone https://github.com/yourusername/Intelligent-IO-Scheduling.git
   ```
2. Navigate to the directory:
   ```bash
   cd Intelligent-IO-Scheduling
   ```
3. Launch Jupyter Notebook:
   ```bash
   jupyter notebook intelligent_io_scheduling.ipynb
   ```

## Evidence & Results
In simulated environments, reordering I/O queues based on ML-predicted service times can significantly reduce average disk latency by minimizing seek distances, closely matching the behavior of advanced schedulers like `KML-IOSched`.

---
**GitHub Repository Link:** [https://github.com/yourusername/Intelligent-IO-Scheduling](https://github.com/yourusername/Intelligent-IO-Scheduling)
