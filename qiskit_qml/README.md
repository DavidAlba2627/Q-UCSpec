# Quantum Machine Learning Models
This folder contains the **Qiskit-based Quantum Machine Learning (QML) implementations** used in the *Q-UCSpec* project. The models developed here are designed to classify CaF₂ and Er-doped CaF₂ (CaF₂:Er) using optical descriptors.

---

## Problem Description
The primary task addressed in this module is a **binary materials classification problem**, where the goal is to distinguish between **CaF₂** and **CaF₂:Er** based on their **optical response**.

The input features consist of **optical descriptors** (energy, extinction coefficient, absoptio coefficient, among others) stored in the `Q-UCSpec/data/` directory. These descriptors were obtained via Lr-TDDFT spectroscopy simulations in `Q-UCSpec/simulations_gpaw/sim_master.ipynb`.

---

## Models and Approach
Multiple **quantum machine learning models and variants** were explored during the development of this work, including different circuit architectures, feature maps, ansatz, and training strategies. While several approaches were evaluated, the final analysis focuses on two representative and complementary QML methods:

- **Quantum Neural Network (QNN) + PyTorch**  
  Implemented as **hybrid quantum–classical architecture**, where parametrized quantum circuits are trained using classical optimizers.

- **Quantum Support Vector Machine (QSVM)**  
  Based on **quantum kernel methods**, enabling classification through implicit feature mappings in Hilbert space.

These models were selected due to their relevance, interpretability, and suitability for datasets typical of materials science applications.

---

## Final Results and Notebooks

The notebooks that reflect the **final selected models** and the **reported results** of this work are:

- `/QNN/qml_qnnsampler.ipynb` — QNN-based hybrid quantum classifier.
- `/QSVM/qml_qsvc_ibm_benchmark.ipynb` — QSVM-based classification using quantum kernels.

These notebooks contain the complete workflows, including data loading, model construction, training and evaluation.
