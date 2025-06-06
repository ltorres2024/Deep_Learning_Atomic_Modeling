# Deep Learning for Atomic Structure Modeling

This project explores the application of **deep learning techniques** to predict atomic ground state energies, specifically using data generated from *ab initio* methods such as Hartree-Fock, Møller–Plesset (MP2), and Multiconfiguration Dirac–Hartree–Fock (MCDHF). The goal is to bridge traditional computational atomic physics with modern machine learning methods for faster and scalable energy predictions.

---

## Overview

The pipeline includes:
- Processing shell-structured atomic data (e.g., Z = 2–114)
- Normalizing and formatting features from MP2 and CCD energies
- Training a neural network to approximate MCDHF energy outputs
- Using Python and TensorFlow to build and evaluate model performance

---

## Repository Structure

- `Data Processing and Neural Network.ipynb`  
  ➤ Jupyter notebook containing the core data pipeline, preprocessing steps, and deep learning model code (Keras/TensorFlow).

- `atomic_calculations.sb`  
  ➤ SLURM batch script for running calculations or neural network jobs on HPC systems like OSC.

- `training_data_0.0-0.83.txt`  
  ➤ Training data file containing processed energy values for atoms at various densities.

- `Research paper.pdf`  
  ➤ Final research report documenting the project’s background, methodology, results, and conclusions.

---

## Scientific Context

Atomic energy predictions often rely on computationally intensive *ab initio* methods. This project uses supervised machine learning to **approximate MCDHF energies** using cheaper methods (MP2 and CCD) as input features. The ultimate goal is to reduce the computational burden for future large-scale atomic structure calculations.

---

## Model Summary

- **Input Features**: MP2 and CCD correlation energies, nuclear charge Z, shell structure, density
- **Output Target**: MCDHF energy
- **Model Type**: Fully-connected feedforward neural network
- **Libraries Used**:
  - `TensorFlow` / `Keras`
  - `NumPy`, `pandas`, `matplotlib`

---

## Acknowledgments

This project includes code adapted from:

- 📁 [`main.cpp`](https://github.com/ManyBodyPhysics/LectureNotesPhysics/blob/master/Programs/Chapter8-programs/cpp/CCD/src/main.cpp)  
  Original implementation by **Morten Hjorth-Jensen** and contributors, from the [ManyBodyPhysics/LectureNotesPhysics](https://github.com/ManyBodyPhysics/LectureNotesPhysics) repository.  
  Licensed under [GNU General Public License v3.0](https://github.com/ManyBodyPhysics/LectureNotesPhysics/blob/master/LICENSE).

> Adaptations were made to support atomic data generation for training neural networks. All uses are in accordance with the GPL license.

---


## Citation & References

If using or adapting this project, please cite:

- Sanchez, L. (2025). *Advancing Atomic Modeling: Integration of Computational Clusters & Neural Network Techniques*. [GitHub Repository](https://github.com/ltorres2024/Deep_Learning_Atomic_Modeling)
- Hjorth-Jensen, M. (2024). *LectureNotesPhysics*, [https://github.com/ManyBodyPhysics/LectureNotesPhysics](https://github.com/ManyBodyPhysics/LectureNotesPhysics)
