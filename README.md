# Federated Learning for IoT Networks

A complete implementation of Federated Learning (FedAvg) for distributed IoT devices, simulating real-world communication constraints and demonstrating privacy-preserving machine learning.

## Overview
This project implements Federated Learning for a Human Activity Recognition (HAR) system using IoT sensor data. Multiple edge devices train local models on private data, and a central server aggregates updates without accessing raw data.

## Features
- FedAvg implementation from scratch
- Non-IID data partitioning across 10 devices
- Communication constraint simulation (bandwidth, latency, dropouts)
- Comparison with centralized learning
- Privacy-preserving design

## Results

| Metric | Federated | Centralized |
|--------|-----------|-------------|
| Accuracy | 92.60% | 94.44% |
| Accuracy Gap | 1.83% | — |
| Privacy | ✅ Preserved | ❌ Not preserved |
| Data Sharing | None | All raw data |

### Robustness to Device Dropouts
| Dropout Rate | Accuracy |
|--------------|----------|
| 0% | ~92.6% |
| 20% | ~90% |
| 50% | ~85% |

## Notebooks
1. `01_data_preparation.ipynb` — Data loading and non-IID partitioning
2. `02_federated_learning.ipynb` — FedAvg implementation from scratch
3. `03_communication_simulation.ipynb` — Network constraints and dropouts
4. `04_evaluation.ipynb` — Comparison and conclusion

## Technologies
- Python, TensorFlow, NumPy, Scikit-learn
- Matplotlib, Seaborn
- Jupyter Notebook

## Key Findings
- Federated learning achieves comparable accuracy to centralized learning (within 2%)
- Privacy is preserved — no raw data is shared
- System is robust to device dropouts
- Communication cost depends on model size, not dataset size

## Author
Jaweria Siddique