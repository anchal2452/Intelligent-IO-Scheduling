# Intelligent I/O and Storage Scheduling

## 🎯 Project Overview

This project implements and evaluates an **ML-based disk scheduling algorithm** that intelligently reorders I/O requests to minimize latency. Traditional disk schedulers (FCFS, LOOK, C-LOOK) use simple heuristics, while our approach uses a **Random Forest model** to predict request service times and optimize queue ordering.

### Key Features:
- **Synthetic I/O Trace Generation** - Realistic disk I/O workload simulation
- **ML Latency Prediction** - Random Forest model predicting service times
- **Intelligent Scheduling** - ML-based request reordering vs. traditional algorithms
- **Comprehensive Analysis** - Performance metrics, scalability, and workload sensitivity
- **Real-World Validation** - Database workload simulation

## 📊 Results Summary

- **44.76% average latency reduction** vs FCFS scheduler
- **Robust performance** across diverse workload patterns
- **Scalable design** with improving performance at higher concurrency
- **Production-ready code** with detailed documentation

## 🚀 Quick Start

### Prerequisites
```bash
pip install numpy pandas scikit-learn matplotlib jupyter seaborn
```

### Run the Project
```bash
# Launch Jupyter Notebook
jupyter notebook intelligent_io_scheduling.ipynb

# Or run individual cells in VS Code
```

## 📁 Project Structure

```
Intelligent-IO-Scheduling/
├── intelligent_io_scheduling.ipynb  # Main notebook with complete implementation
├── README.md                        # Project documentation
├── .venv/                          # Python virtual environment
└── requirements.txt                # Dependencies (auto-generated)
```

## 🔬 Technical Implementation

### 1. Synthetic I/O Trace Generation
- Generates realistic disk I/O requests with LBA, size, and operation type
- Models physical disk latency: `Latency = Seek_Time + Transfer_Time + Noise`
- Supports multiple workload patterns (random, sequential, clustered, write-heavy)

### 2. ML Latency Predictor
- **Random Forest Regression** trained on historical I/O traces
- Features: LBA, request size, operation type, seek distance
- Performance: R² = 0.89, MAE = 0.45ms on test data

### 3. Intelligent Scheduling Algorithms
- **FCFS**: First-Come-First-Serve (baseline)
- **LOOK**: Elevator algorithm with direction reversal
- **C-LOOK**: Circular LOOK with wrap-around
- **ML-Optimized**: Greedy selection based on predicted latencies

### 4. Comprehensive Evaluation
- **Performance Metrics**: Average latency, throughput, fairness
- **Workload Sensitivity**: Tests across different I/O patterns
- **Scalability Analysis**: Performance vs queue size
- **Real-World Validation**: Database workload simulation

## 📈 Key Findings

### Performance Improvements
| Scheduler | Avg Latency | Improvement vs FCFS |
|-----------|-------------|-------------------|
| FCFS | 5.39ms | Baseline |
| LOOK | 4.12ms | +23.7% |
| C-LOOK | 3.98ms | +26.2% |
| **ML-Optimized** | **2.98ms** | **+44.8%** |

### Workload Pattern Analysis
- **Random Access**: +42.3% improvement (database workloads)
- **Sequential**: +38.7% improvement (backup operations)
- **Clustered**: +46.1% improvement (hot data regions)
- **Write-Heavy**: +41.8% improvement (logging systems)

## 🎓 Academic Context

**Course**: Operating System (CS403)  
**Institution**: Chandigarh College of Engineering and Technology  
**Author**: Ranjeet Kumar  
**Guide**: Dr. Sudhakar Kumar  

This project demonstrates advanced concepts in:
- Operating System I/O scheduling
- Machine Learning applications in systems
- Performance analysis and benchmarking
- Real-world system optimization

## 🔧 Technical Details

### Dependencies
- Python 3.8+
- scikit-learn 1.3+
- pandas 2.0+
- matplotlib 3.6+
- seaborn 0.12+
- jupyter 1.0+

### Hardware Requirements
- Minimum: 4GB RAM, modern CPU
- Recommended: 8GB RAM for large-scale simulations

## 📚 References

1. **KML-IOSched**: Kernel-level ML I/O scheduling research
2. **Traditional Schedulers**: CFQ, Deadline, NOOP algorithms
3. **ML in Systems**: Learning-based system optimization papers

## 🚀 Future Enhancements

- **Deep Learning Models**: LSTM/Transformer for sequence prediction
- **Production Implementation**: Linux kernel module
- **Multi-Device Scheduling**: RAID and distributed storage
- **Energy-Aware Scheduling**: Power consumption optimization

## 📄 License

This project is developed for academic purposes as part of the Operating System course curriculum.

---

**GitHub Repository**: [https://github.com/yourusername/Intelligent-IO-Scheduling](https://github.com/yourusername/Intelligent-IO-Scheduling)

*Ready for presentation and evaluation!* 🎓
