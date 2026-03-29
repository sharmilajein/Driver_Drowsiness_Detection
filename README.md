# Driver_Drowsiness_Detection
# 🧠 Driver Drowsiness Detection using Deep Learning

## Overview
Driver fatigue is one of the leading causes of road accidents. This project presents a non-intrusive, vision-based system that detects driver drowsiness using facial features such as eye closure and yawning behavior.

The system uses Deep Learning (CNN + MobileNetV2) to classify driver states and further maps them into fatigue levels for real-world interpretation.



# Objectives

- Detect eye state (Open / Closed)
- Detect yawning behavior (Yawn / No Yawn)
- Classify fatigue levels:
  - Alert
  - Mild Fatigue
  - Severe Fatigue
- Analyze fatigue progression over time
- Build an interactive Streamlit application



##  Dataset

The dataset consists of facial images categorized into 4 classes:

- Closed
- Open
- no_yawn
- yawn

Images are resized to 224×224 and normalized for model training.

---

# Tech Stack

- Python
- TensorFlow / Keras
- OpenCV
- NumPy / Matplotlib / Seaborn
- Streamlit

---

## Project Workflow

1. Data Preprocessing
   - Image resizing (224×224)
   - Normalization (0–1)
   - Data augmentation

2. Model Development
   - Custom CNN (baseline)
   - MobileNetV2 (Transfer Learning)

3. Model Evaluation
   - Accuracy & Loss curves
   - Confusion matrix
   - Precision, Recall, F1-score

4. Decision Fusion Logic
   - Convert 4-class output → 3 fatigue levels

5. Fatigue Progression Curve
   - Simulate fatigue over time
   - Detect transitions (Alert → Mild → Severe)

---

## Model Performance

| Model | Training Accuracy | Validation Accuracy |
|------|------------------|--------------------|
| CNN | ~77% | ~66% |
| MobileNetV2 | ~85% | ~78% |

Transfer learning significantly improved performance and reduced overfitting.

---

## Fatigue Classification Logic

Prediction | Fatigue Level 

 Open / no_yawn | Alert 
 yawn | Mild Fatigue 
 Closed | Severe Fatigue 

---

## Fatigue Progression Curve

The system analyzes fatigue over time by:

- Converting predictions into fatigue levels
- Grouping into time intervals
- Applying smoothing and constraints
- Generating a progression curve

This helps identify critical transitions in driver alertness.

---

## Limitations

- Lower accuracy in distinguishing yawn vs no_yawn
- Sensitive to lighting and camera angles
- Requires clear facial visibility

---


