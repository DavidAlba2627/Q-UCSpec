# VQC — Variational Quantum Classifier

This folder contains **Variational Quantum Classifier (VQC)** experiments developed within the *Q-UCSpec* project. The notebooks in this directory evaluate VQC-based approaches as an **alternative quantum classification method** for distinguishing **CaF₂ and Er-doped CaF₂ (CaF₂:Er)** using **optical descriptors**.

While VQC models were explored and benchmarked, they were not selected as the primary quantum approach. The project ultimately focused on **classical SVM**, **QSVM**, and **QNN** models, as these demonstrated **better performance, higher consistency, and improved stability** across different execution settings.

All models rely on the optical features provided in the `data/` directory.

---

## Objective

The objective of this module is to **assess the feasibility and performance of VQC-based classifiers** and to compare them against **classical and alternative quantum models**, providing additional context for the model selection process adopted in the project.

---

## Notebooks Overview

### 🔹 `qml_vqc.ipynb`

This notebook implements a **Variational Quantum Classifier (VQC)** and provides a direct comparison with:

- **Classical SVC**
- **Quantum Support Vector Classifier (QSVC)**

#### Purpose

- Evaluates VQC performance under ideal simulation conditions.
- Compares VQC results with kernel-based classical and quantum models.
- Serves as a baseline for assessing variational circuit-based classifiers.

---

### 🔹 `qml_vqc_ibm.ipynb`

This notebook is designed to extend the same comparison to **IBM Quantum hardware**.

#### Purpose

- Provides a ready-to-run implementation for executing VQC on real quantum hardware.
- Allows users to evaluate the impact of hardware noise and finite sampling.
- Serves as a reproducibility and extension resource for future hardware-based studies.

> **Note:** This notebook was prepared for hardware execution but was **not fully executed** as part of the final reported results.

---

## Scope and Context

The VQC experiments in this folder are intended to:

- Provide an alternative perspective on **variational quantum classifiers**.
- Support the rationale for selecting **QSVM and QNN** as the primary quantum approaches.
- Highlight the relative strengths and limitations of VQC models in optical-descriptor-based materials classification tasks.

All experiments follow a **hybrid quantum–classical workflow**, using Qiskit primitives and classical optimization routines.

---

## Execution Notes

- Simulator-based experiments can be reproduced locally.
- Results may vary depending on the library versions, backend availability, noise levels, optimizer settings, etc.

---

This folder provides a comparative evaluation of **VQC-based approaches** and contributes to the model selection analysis.
