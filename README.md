# Loan Approval – Rule Extraction & DMN Generation

## Overview

This project demonstrates how to:

* Generate a synthetic loan dataset
* Transform data into categorical variables
* Train machine learning models
* Extract decision rules
* Export rules into **DMN (Decision Model and Notation)** format

The project combines:

* **Data generation**
* **Rule-based learning (PRISM)**
* **Decision Trees (CART)**
* **DMN (Decision Model and Notation) generation**

---

## Project Structure

```bash
dataset_loan.csv
dataset_categorical.csv
LoanPrism.dmn
LoanTree.dmn
loan_decision_tree.png
generate_dataset.ipynb
loan_approval.ipynb
README.md
```

---

## 1. Dataset Generation

## 2. Data Transformation

The numerical dataset was manually transformed into categorical variables using Excel.

### Age Categories:
- underage (<18)  
- middle (18–65)  
- old (>65)  

### Income Categories:
- low (≤33,000)  
- mid (33,001–65,000)  
- high (65,001–100,000)  

### Output:
- dataset_categorical.csv


## 2. Data Transformation

The numerical dataset is converted into **categorical variables**:

### Age → Categories:

* underage (<18)
* middle (18–65)
* old (>65)

### Income → Categories:

* low (≤33,000)
* mid (33,001–65,000)
* high (65,001–100,000)

### Output:

* `dataset_categorical.csv`

---

## 3. PRISM Rule-Based Model

Custom implementation of the **PRISM algorithm**:

* Learns rules per class
* Selects best attribute-value combinations
* Produces interpretable IF–THEN rules

### Example:

### Output:

* Console rules
* `LoanPrism.dmn`

---

## 4. CART Decision Tree Model

Implemented using **Scikit-learn**:

* Uses one-hot encoding for categorical features
* Trains a classification tree
* Extracts rules from tree paths

### Outputs:

* `LoanTree.dmn`
* `loan_decision_tree.png`

---

##  5. DMN Export

Both models are converted into **DMN decision tables**:

* Compatible with tools like **Camunda**
* Automatically generated XML structure
* Includes default rules

---

## Technologies

* Python
* Pandas
* NumPy
* Scikit-learn
* Graphviz
* XML (ElementTree, minidom)

---

## How to Run

1. Install dependencies:

```bash
pip install pandas numpy scikit-learn graphviz
```

2. Run dataset generation:

```bash
python generate_dataset.py
```

3. Run PRISM & CART model:

```bash
python loan_approval.ipynb
```

---

## Key Idea

This project shows how **machine learning models can be transformed into interpretable decision logic** using:

* Rule-based systems (PRISM)
* Tree-based models (CART)
* Standardized decision format (DMN)

---


## Author

Iordana Kouimtzidou


