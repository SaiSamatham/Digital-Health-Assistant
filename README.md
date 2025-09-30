# Health Navigator: Symptom-Based Disease Prediction and Recommendation System

Welcome to **Health Navigator**! This is a web application built with Python and Flask that utilizes a pre-trained Machine Learning model (Support Vector Classifier - SVC) to predict potential diseases based on user-inputted symptoms.

Beyond prediction, the system provides comprehensive, disease-specific health recommendations, including descriptions, necessary precautions, suggested medications, diet plans, and workout routines, all sourced from structured datasets.

## 🚀 Project Objective

The goal of this project is to create an accessible, immediate, and informative tool that:

1. **Predicts** a likely disease from a list of common symptoms using an SVC model.

2. **Delivers** actionable health advice (precautions, diet, workout) for the predicted condition.

3. **Serves** this information through a user-friendly Flask web interface.

## 🛠️ Technologies and Dependencies

This project is built using the following core technologies:

* **Python 3.x**

* **Flask**: Web framework for handling routes and serving HTML templates.

* **Pandas**: For reading, processing, and manipulating the health datasets.

* **NumPy**: For efficient handling of numerical operations, especially creating the symptom input vector.

* **Scikit-learn**: Used for the SVC model (loaded via `pickle`).

### Installation

1. **Clone the repository:**
