# From_Regression_to_Deep_Learning

# 📘 Spiral Experiments — README

A clean and well‑structured README for the notebook exploring **non-linear datasets**, **PyTorch models**, and **decision region visualization**.

---

## 🎯 Project Overview

This notebook demonstrates how neural networks learn **non‑linear patterns** using the classic **spiral dataset**. It mirrors the content from **Lesson 1** — going from simple regression intuition to deep learning experiments.

We will:

* Generate a custom 2D spiral dataset
* Train PyTorch models of different sizes and depths
* Visualize training/validation loss
* Plot decision boundaries for each experiment
* Compare model capacity and behavior

---

## 🧰 Environment Setup

Before starting, ensure the following libraries are installed:

```bash
pip install torch matplotlib numpy
```

The notebook prints current versions of Python, NumPy, and PyTorch for reproducibility.

---

## 🔵 Dataset — Spiral Generator

The project uses a custom function `make_spiral()` to generate two interwoven spirals. Parameters:

* **n** — number of samples
* **noise** — level of Gaussian noise
* **seed** — reproducibility

A scatter plot provides an initial visualization of class separation.

---

## 🧠 Baseline Model

A compact neural network is built using:

* **Two hidden layers (8 → 8)**
* **ReLU activation**
* **Sigmoid output** for binary classification

Training includes:

* **BCE loss** (Binary Cross-Entropy)
* **Adam optimizer**
* **Train/validation split**
* Tracking of losses and accuracy

---

## 📉 Training Curves

For each model, the notebook plots:

* Training loss
* Validation loss

This helps evaluate overfitting, underfitting, and training stability.

---

## 🎨 Decision Region Visualization

A **mesh-grid** over the 2D input space is used to compute predictions and visualize decision boundaries. This shows how network complexity affects decision shaping.

---

# 🧪 Experiments Summary

The notebook includes **five experiments**, each with a different architecture.

---

## **Experiment 1 — Shallow & Narrow (2 → 4 → 1)**

A small model with limited capacity. Useful for observing underfitting.

* 1 hidden layer with 4 units
* Fast training but limited expressiveness
* Plots: losses + decision regions

---

## **Experiment 2 — Wide & Deeper (2 → 16 → 16 → 1)**

A more capable model with wider layers.

* Better at capturing non-linear patterns
* Higher accuracy expected
* Smoother decision region

---

## **Experiment 3 — Deep & Narrow (2 → 3 → 3 → 3 → 3 → 1)**

Shows how depth alone affects learning.

* Narrow layers but many of them
* Can sometimes approximate complex shapes despite small width

---

## **Experiment 4 — Minimalist Model (2 → 2 → 1)**

Extremely small capacity.

* Demonstrates strong underfitting
* Good educational contrast

---

## **Experiment 5 — Wide & Deep (2 → 32 → 32 → 16 → 16 → 8 → 1)**

The most powerful model in the notebook.

* Deep and wide layers
* Learns complex spiral structure
* Good accuracy and expressive decision boundaries

---

# 📊 Outputs for Each Experiment

Each experiment includes:

* Final validation accuracy
* Training and validation curves
* Decision region plot

#### Experiment 1 Architecture: (2 → 4 → 1) accuracy: 0.575
#### Experiment 2 Architecture: (2 → 16 → 16 → 1) accuracy: 0.85
#### Experiment 3 Architecture: (2 → 3 → 3 → 3 → 3 → 1) accuracy: 0.4938
#### Experiment 4 Architecture: (2 → 2 → 1) accuracy: 0.525
#### Experiment 5 Architecture: (2 → 32 → 32 → 16 → 16 → 8 → 1) accuracy: 0.8750

This gives a clear comparison of how architecture size affects performance.

---

## 📚 Educational Value

This notebook is excellent for beginners learning:

* How neural networks approximate nonlinear boundaries
* Why deeper or wider models behave differently
* How to evaluate classification performance
* How to visualize learned decision regions

---


## ✔️ Final Notes

This README is formatted for clarity, presentation, and GitHub friendliness. Feel free to extend the experiments, add new architectures, or test different datasets.

Happy learning and experimenting with neural networks! 🚀
