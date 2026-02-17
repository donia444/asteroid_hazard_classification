# asteroid_hazard_classification
Can we predict which Near-Earth Objects (NEOs) are a potential threat to humanity? This project uses Machine Learning to classify asteroids as hazardous or non-hazardous based on physical and orbital characteristics.  The primary goal is to minimize False Negatives (missing a real threat)



## 🌌 Project Overview

This repository focuses on classifying **Nearest Earth Objects (NEOs)** to determine if they are potentially hazardous. Using data spanning over a century (1910–2024), this machine learning pipeline analyzes physical properties and orbital metrics to predict threats.

### 🎯 The "Zero-Miss" Strategy

In planetary defense, the cost of a **False Negative** (missing a real threat) is catastrophic, while a **False Positive** (a false alarm) is merely an inconvenience.

> **Primary Goal:** Maximize **Recall** for the hazardous class to ensure maximum safety.

---

## 📊 Dataset Insights

The dataset contains detailed observations of thousands of asteroids. Key features used for classification include:

* **Absolute Magnitude:** The intrinsic brightness of the asteroid.
* **Estimated Diameter:** Size range (min/max).
* **Relative Velocity:** Speed at which the object travels relative to Earth.
* **Miss Distance:** The proximity of the asteroid's orbit to Earth.

---

## 🛠️ Technical Workflow

1. **Exploratory Data Analysis (EDA):** Identified that `absolute_magnitude` is the strongest indicator of whether an asteroid is hazardous.
2. **Data Preprocessing:** Handled missing values and performed feature scaling for optimal model performance.
3. **Threshold Optimization:** Adjusted decision thresholds to prioritize the detection of hazardous objects (True Positives) over general accuracy.
4. **Performance Evaluation:** Utilized Confusion Matrices and Classification Reports to validate safety margins.

---

## 📈 Model Performance

The final model was tuned to catch as many threats as possible while maintaining a 90% overall accuracy.

| Metric | Score |
| --- | --- |
| **Overall Accuracy** | **90%** |
| **Recall (Hazardous)** | **75%** |
| **Precision (Hazardous)** | **57%** |

### Confusion Matrix Results:

* ✅ **6,448** Hazardous asteroids correctly identified.
* ❌ **2,184** Hazardous asteroids missed (Area for future optimization).
* 🛡️ **54,232** Non-hazardous objects correctly filtered.

---

## 🚀 Getting Started

### Prerequisites

```bash
pip install numpy pandas scikit-learn matplotlib seaborn

```

### Usage

1. Clone the repository:
```bash
git clone https://github.com/yourusername/asteroid-hazard-classification.git

```


2. Navigate to the project folder and open the notebook:
```bash
jupyter notebook asteroid_hazard_classification.ipynb

```



---

## 🛠️ Built With

* **Pandas & NumPy** - Data manipulation.
* **Scikit-Learn** - Machine Learning algorithms and metrics.
* **Matplotlib & Seaborn** - Data visualization.

---

*Developed as part of a commitment to applying Machine Learning for global safety and astronomical research.*
