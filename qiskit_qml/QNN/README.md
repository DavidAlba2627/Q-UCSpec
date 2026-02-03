# QNN — Quantum Neural Networks

This folder contains the **Quantum Neural Network (QNN)** experiments developed within the *Q-UCSpec* project. The notebooks in this directory explore **hybrid quantum–classical neural network architectures** for the task of **classifying CaF₂ and Er-doped CaF₂ (CaF₂:Er)** using **optical descriptors**.

All models rely on the optical features provided in the `data/` directory.

---

## Objective

The main objective of this module is to **investigate and benchmark hybrid QNN architectures** that combine **parametrized quantum circuits** with **classical deep learning frameworks**, evaluating their performance, stability, and suitability for materials classification based on optical descriptors.

---

## Notebooks Overview

### 🔹 `qml_qnnsampler.ipynb` (Main Notebook)

This is the **primary notebook** of the QNN module. It implements a **hybrid quantum–classical model** combining:

- **SamplerQNN** (Qiskit Machine Learning)
- **PyTorch** for classical optimization and training

This architecture achieved the **best overall performance** among the evaluated QNN-based approaches.

#### Key Characteristics

- Hybrid training loop integrating quantum circuit outputs with Torch-based optimization.
- Employs classical loss functions and optimizers for end-to-end training.
- Reports performance metrics such as accuracy and ROC AUC where applicable.

This notebook represents the **final and best-performing QNN results** reported in the project.



### 🔹 `qml_qnnestimator.ipynb`

This notebook implements an alternative **hybrid QNN architecture** combining:

- **EstimatorQNN** (Qiskit Machine Learning)
- **PyTorch** for classical optimization and training

#### Purpose

- Evaluates Estimator-based expectation value measurements within a hybrid learning loop.
- Provides a direct comparison with the SamplerQNN-based architecture.
- Explores differences in convergence behavior and performance between QNN variants.



### 🔹 `qml_hqnn_ragu.ipynb`

This notebook explores additional **hybrid QNN configuration**, testing alternative architectural choices and training strategies.

#### Purpose

- Investigates different quantum circuit layouts, ansätze, and hyperparameter settings.

---

## Scope and Context

The QNN experiments in this folder are designed to:

- Evaluate **hybrid quantum–classical neural networks** for materials classification.
- Compare **SamplerQNN- and EstimatorQNN-based architectures**.
- Assess the robustness and expressivity of QNNs when applied to **optical-descriptor-based materials science problems**.

All experiments follow a **hybrid quantum–classical workflow**, leveraging Qiskit Machine Learning and PyTorch for model construction and optimization.

---

## Execution Notes

- Hybrid QNN models are computationally intensive and may require careful tuning.
- Simulator-based experiments can be fully reproduced locally.
- Results may vary depending on the library versions, backend configuration, training hyperparameters, etc.

---

This folder provides a focused evaluation of **hybrid QNN-based approaches** for quantum-enhanced materials classification.
