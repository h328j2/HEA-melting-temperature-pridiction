# Physically Consistent Machine Learning for Melting Temperature Prediction of Refractory High-Entropy Alloys

## Overview
This repository contains the complete code and data-processing workflow used in the study:

**Physically Consistent Machine Learning for Melting Temperature Prediction of Refractory High-Entropy Alloys**

The work applies machine learning models with physically meaningful descriptors to predict the melting temperature of refractory high-entropy alloys (RHEAs).  
All experiments are implemented in a single Jupyter notebook to ensure transparency and reproducibility.

---

## Repository Structure

├── notebook.ipynb # Main notebook (data loading → preprocessing → training → evaluation)
├── data/ # Dataset (if public) or placeholder
├── figures/ # Generated plots (optional)
└── README.md

---

## Dataset Description
- The dataset consists of compositional and thermophysical descriptors of refractory high-entropy alloys.
- **Target variable:** Melting Temperature (Tₘ)
- **Features include:**
  - Composition-derived elemental descriptors
  - Entropy and thermodynamic features
  - Phase-related indicators, including multiphase information retained as separate columns

### Data Source
The dataset was compiled from published literature and publicly available materials databases.
 Machaka, R., Motsi, G. T., Raganya, L. M., & Radingoana, P. M. (2021). Machine learning-based prediction 
of phases in high-entropy alloys: A data article. Data in Brief, 38, 107346. 
https://doi.org/10.1016/j.dib.2021.10734
---

## Methodology
1. Data preprocessing (cleaning and normalization)
2. Feature engineering using physically consistent descriptors
3. Supervised regression model training
4. Model evaluation using quantitative error metrics

---

## Evaluation Metric
**Mean Squared Error (MSE)** is used as the primary evaluation metric because:
- Melting temperature is a continuous thermophysical property
- Larger prediction errors are penalized more strongly
- MSE is standard in regression-based materials property prediction

---

## Limitations
- Microstructural features (grain size, phase morphology) are not explicitly included due to limited availability of consistent datasets.
- The model is composition-based and does not replace experimental validation.
- Predictions may be less reliable for compositions far outside the training domain.

---

## Reproducibility

### Requirements
- Python ≥ 3.8
- numpy
- pandas
- scikit-learn
- matplotlib
- seaborn

Install dependencies:
```bash
pip install numpy pandas scikit-learn matplotlib seaborn
Running the Notebook
jupyter notebook notebook.ipynb


Run all cells sequentially to reproduce the results.

Results

The trained models demonstrate reasonable predictive accuracy for melting temperature trends in refractory high-entropy alloys and highlight the importance of physically meaningful descriptors.

Citation

 Machaka, R., Motsi, G. T., Raganya, L. M., & Radingoana, P. M. (2021). Machine learning-based prediction 
of phases in high-entropy alloys: A data article. Data in Brief, 38, 107346. 
https://doi.org/10.1016/j.dib.2021.10734

Mohd Hasnain,
"Physically Consistent Machine Learning for Melting Temperature Prediction of Refractory High-Entropy Alloys",


Author

Mohd Hasnain
Graduate Student, Materials Science
National Institute of Technology, India

Disclaimer

This work is intended for research and educational purposes only.
Predictions should not be used for industrial or engineering decisions without experimental validation.
