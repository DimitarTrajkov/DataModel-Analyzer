# DataModel-Analyzer

## Introduction

This repository investigates the application of machine learning models for predicting brain stroke outcomes, leveraging publicly available datasets. We evaluate the performance of various classification and regression models.

## Structure

```
.
├── Charts/
├── Code/
├── Dataset_Target_feature/
├── Dataset_info/
├── Dataset_meta_features/
├── Dataset_processed/
├── Datasets/
├── Preprocessing_code/
├── 'related PDFs'/
├── README.md
└── Results_LITE/
```

### Code

The **Code** folder contains scripts for all models. The regression models are stored in the `reg_models` subdirectory, while classification models are located in the `clf_models` subdirectory.

To run any of the scripts, you need Python installed on your machine along with the following libraries:

- `joblib`
- `scikit-learn`
- `time`
- `json`
- `numpy`
- `pandas`
- `itertools`
- `copy`
- `xgboost`
- `mord`

You can install all the required libraries using pip with the following command:

```bash
pip install joblib scikit-learn time json numpy pandas itertools copy xgboost mord
```

#### Example:

---

⚠️ **WARNING: some of the paths are hard coded with slashes ( unix based ) so if you are using windows based machine you will get an error**

---

- if you want to run all the models for a given dataset X you can go to the directory `Code` and run the following command:

```bash
cd Code
python3 master.py 1
```

in general:

```bash
cd Code
python3 master.py number
```

- but if you wanrt to run only a particular model you can do:

```bash
cd Code
python3 ./reg_models/Adaboost.py 1 True
```

in general:

```bash
cd Code
python3 ./type/model.py number is_multitarget
```

.........

### Charts

In the Charts folder, you can find various visualizations of the features from each dataset, including violin plots, histograms, pie charts, and correlation matrices.

### Dataset_Target_feature

This directory contains the original datasets, where the name of the target feature in each dataset has been changed to "Target." These files were used for calculating meta-features.

### Dataset_info

This folder includes basic information for each dataset. This information is also available in the `Documentation.pdf` located in the `related PDFs` folder.

### Dataset_meta_features

This directory contains different types of meta-features that were calculated, including Basic, Statistical, and Informational Theory metrics on both the original and processed datasets.

### Dataset_processed

Each dataset was manually preprocessed, and the results are stored in this folder.

If you have any questions or need further clarification, please refer to the documentation and the paper located in the related PDFs folder or contact me at dt18806@student.uni-lj.si.
