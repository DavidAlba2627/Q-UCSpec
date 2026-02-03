# QSVM — Quantum Support Vector Machines

This folder contains the **Quantum Support Vector Machine (QSVM)** experiments developed within the *Q-UCSpec* project. The notebooks in this directory focus on benchmarking **classical and quantum kernel-based classifiers** for the task of **classifying CaF₂ and Er-doped CaF₂ (CaF₂:Er)** using **optical descriptors**.

All models rely on the optical features provided in the `data/` directory.

---

## Objective

The main objective of this module is to **systematically compare classical and quantum support vector machines** under different execution settings, evaluating their performance, robustness, and feasibility for materials classification tasks based on optical descriptors.

---

## Notebooks Overview

### 🔹 `qml_qsvc_ibm_benchmark.ipynb` (Main Notebook)

This is the **primary notebook** of the QSVM module. It presents a comprehensive **benchmark study** comparing the following models:

- **Classical SVC**  
  Standard support vector classifier with classical kernels.

- **QSVC (Ideal Simulation)**  
  Quantum Support Vector Classifier evaluated using an **ideal statevector simulator**, providing insight into the expressivity of quantum kernels without sampling noise.

- **QSVC (Noisy Simulation)**  
  QSVC evaluated on a **QASM-style** (shot-based) simulator incorporating noise, emulating realistic hardware conditions.

- **QSVC on IBM Quantum Hardware**  
  Execution of QSVC models on the **IBM quantum processor (ibm_fez)**, enabling an assessment of real-device performance.

#### Key Characteristics

- Uses **training and test slices** to mitigate hardware execution time and cost.
- Ensures consistent data splits across classical and quantum models for fair comparison.
- Reports performance metrics such as accuracy and ROC AUC where applicable.

This notebook represents the **final QSVM results** reported in the project.


### 🔹 `qml_pegasosqsvc.ipynb`

This notebook explores an alternative QSVM training strategy based on the **Pegasos algorithm**, a stochastic sub-gradient descent method adapted for support vector machines.

#### Purpose

- Investigates the feasibility of **Pegasos-based QSVC optimization**.
- Serves as an exploratory comparison against standard QSVC implementations.
- Provides additional perspective on training efficiency and scalability for quantum kernel methods.

---

## Scope and Context

The QSVM experiments in this folder are designed to:

- Benchmark **classical vs. quantum kernel methods** for materials classification.
- Evaluate QSVC performance under **ideal, noisy, and real-hardware conditions**.
- Assess the practicality of deploying QSVMs for **optical-descriptor-based materials science problems**.

All experiments are conducted in a **hybrid quantum–classical workflow**, leveraging Qiskit simulators and IBM Quantum hardware.

---

##  Execution Notes

- Some models are resource-intensive and were performed using **reduced training and/or test slices**.
- Simulator-based experiments can be fully reproduced locally.
- Results may vary depending on the library versions, backend availability, noise levels, shot counts, etc.

---

This folder provides a focused and reproducible evaluation of **QSVM-based approaches** for quantum-enhanced materials classification.
