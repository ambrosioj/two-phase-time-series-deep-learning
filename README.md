# A Deep Learning-based Approach for Two-Phase Flow Pattern Classification

This repository contains the implementations used in the preparation of the article **"A Deep Learning-based Approach for Two-Phase Flow Pattern Classification Using Void Fraction Time Series Analysis."** The repository includes scripts for preprocessing, model training, evaluation, and visualization of results.

---

## 📁 Content

### Repository Structure
```plaintext
.
├── README.md                     # Documentation file (this file)
├── data                          # Preprocessed datasets and features/labels
│   ├── gmm                       # GMM processed data
│   ├── window_4000_overlap_1000_hzdr_norm.npy
│   └── window_4000_overlap_1000_tud_norm.npy
├── metrics                       # Evaluation metrics (e.g., confusion matrices)
│   ├── cross_dataset
│   └── single_dataset
├── models                        # Saved models and artifacts
│   ├── cross_dataset
│   └── single_dataset
├── notebooks                     # Jupyter Notebooks for experiments
│   ├── SVM-cross_dataset.ipynb
│   ├── SVM-single_dataset.ipynb
│   ├── results.ipynb
│   ├── tsai_models-cross_dataset.ipynb
│   └── tsai_models-single_dataset.ipynb
└── requirements.txt              # Python dependencies
```

1. **Data**

- **Description**: Contains preprocessed data used for training and evaluation.
- **Structure**:  
    - `gmm`: Processed GMM data.
    - `window_*_hzdr_norm.npy and window_*_tud_norm.npy`: Preprocessed feature and label data.

2. **Metrics**

- **Description**: Contains evaluation results, including JSON files for metrics and confusion matrices.
- **Structure**: 
    - `cross_dataset`: Metrics from cross-dataset evaluations.
    - `single_dataset`: Metrics from single-dataset evaluations.

3. **Models**
- **Description**: Stores saved models and their associated artifacts.
- **Structure**:
    - `cross_dataset`: Models trained for cross-dataset evaluations.
    - `single_dataset`: Models trained for single-dataset evaluations.

4. **Notebooks**
- **Description**: Contains Jupyter Notebooks for experiments and results visualization.
- **Files**:
    - `SVM-cross_dataset.ipynb`: SVM cross-dataset evaluation.
    - `SVM-single_dataset.ipynb`: SVM single-dataset evaluation.
    - `results.ipynb`: Summary and visualization of results.
    - `tsai_models-cross_dataset.ipynb`: Deep learning cross-dataset evaluation.
    - `tsai_models-single_dataset.ipynb`: Deep learning single-dataset evaluation.    

### Key Information
- **HZDR Data Shape**: `(1474, 4003)`  
- **TUD Data Shape**: `(15141, 4003)`  
  - The first dimension represents the number of samples.  
  - The second dimension consists of:  
    - 4000 time-series samples.  
    - 3 elements for the label, formatted using one-hot encoding.

Due to restrictions, the **HZDR** and **TUD** datasets are referenced in the code but are not included in the repository.

---

## ⚙️ Setup

### Tested on
- **Python Version**: `3.12.8`
- **Platform**: WSL2 - Ubuntu 24.04  

### Installation Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/ambrosioj/two-phase-time-series-deep-learning.git
   cd two-phase-time-series-deep-learning
   ```
2. Install the required Python packages:
   ```bash
   pip install -r requirements.txt
   ```
3. Set up a Jupyter Notebook tool to execute the provided `.ipynb` files.

---

## 🔐 Ignored Files
The `.gitignore` file is configured to ignore:
- All `.npy` files except those matching `*_cm.npy` (e.g., confusion matrices).
- Temporary and environment-related files.
- IDE and OS-generated files (e.g., `.vscode`, `.DS_Store`).

---

## 🔄 Acknowledgments
This repository serves as a comprehensive resource for exploring deep learning methods applied to two-phase flow pattern classification.

For any questions or clarifications, please contact the repository maintainer.

Jefferson dos Santos Ambrosio - *jeffersongmg@gmail.com*