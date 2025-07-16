# 🚗 Unsupervised Learning Project – Automotive Domain

This project demonstrates applications of unsupervised learning through two case studies in the automotive domain:

- **Part A**: Car segmentation using **K-Means Clustering**
- **Part B**: Vehicle type classification using **PCA + SVM**

---

## ✅ PART A: Car Segmentation using K-Means Clustering

### 🏁 Objective
Segment different types of cars into meaningful clusters based on attributes like mileage, weight, horsepower, and more.

### 📁 Data Used
- `Car name.csv` – Contains car identifiers
- `Car-Attributes.json` – Contains numeric and categorical features like `mpg`, `cyl`, `disp`, `hp`, `wt`, etc.

---

### 🔧 Workflow Summary

#### 1. Data Understanding & Exploration
- Loaded CSV and JSON files into DataFrames and merged them.
- Inspected the shape, column names, and data types.
- Printed 5-point summary using `describe()` to understand numerical distributions.

#### 2. Data Cleaning & Analysis
- Checked and imputed missing values (e.g., `hp` had '?').
- Checked for and removed duplicate records.
- Plotted pairplots and scatterplots (`wt` vs `disp`, `wt` vs `mpg`) colored by number of cylinders.
- Shared insights from visual trends.
- Checked and handled unexpected values (like `?` in numerical fields).

#### 3. Clustering
- Applied **K-Means clustering** for cluster sizes 2 through 10.
- Used **Elbow Method** to find optimal number of clusters.
- Re-trained K-Means using the optimal k-value.
- Added cluster labels as a new feature in the dataset.
- Visualized final clusters in a 2D scatter plot.
- Predicted the cluster for a new datapoint using the trained model.

---

## ✅ PART B: Vehicle Silhouette Classification using PCA + SVM

### 🏁 Objective
Classify vehicle silhouettes into types (bus, van, or car) based on shape-derived geometric features using PCA for dimensionality reduction and SVM for classification.

### 📁 Data Used
- `vehicle.csv` – Contains numerical features extracted from vehicle silhouettes with class labels.

---

### 🔧 Workflow Summary

#### 1. Data Understanding & Cleaning
- Loaded the dataset and examined missing values.
- Visualized class distribution using a pie chart.
- Identified and removed duplicate rows.

#### 2. Data Preparation
- Split the data into features `X` and labels `y`.
- Standardized feature values using `StandardScaler`.

#### 3. Model Building
- Trained a base **Support Vector Machine (SVM)** model on original data.
- Evaluated using classification metrics (precision, recall, accuracy, F1).

#### 4. Dimensionality Reduction using PCA
- Applied PCA retaining 10 components and plotted **explained variance ratio**.
- Visualized cumulative variance and identified number of components required to retain 90% variance.
- Re-applied PCA with optimal number of components.
- Trained a second SVM on reduced data and compared performance.

#### 5. Performance Tuning
- Tuned SVM hyperparameters on PCA-reduced features (e.g., `kernel`, `C`).
- Compared results between:
  - Base model
  - PCA-reduced model
  - Tuned PCA-SVM model

#### 6. PCA Concepts
- Explained PCA prerequisites (e.g., numerical data, standardization).
- Listed advantages (noise reduction, faster computation) and limitations (loss of interpretability).

---

## 🧰 Tech Stack
- Python 3
- pandas, numpy
- seaborn, matplotlib
- scikit-learn
- json

---

## 🧪 Learning Outcomes
- Practical application of unsupervised learning (clustering, dimensionality reduction)
- Clustering interpretation using elbow method
- PCA concepts and performance tuning
- Visualization and data cleaning workflows

---

## 🚀 Getting Started

```bash
# Install dependencies
pip install -r requirements.txt


