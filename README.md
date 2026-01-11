<div align="center">

# 🏋️ XGFitness

### **Advanced Fitness Recommendation System with Machine Learning**

**IMPLEMENTATION OF DIET AND PHYSICAL EXERCISE RECOMMENDATION SYSTEMS USING XGBOOST**

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)
[![Flask](https://img.shields.io/badge/Flask-2.0%2B-green)](https://flask.palletsprojects.com/)
[![React](https://img.shields.io/badge/React-18-61DAFB)](https://reactjs.org/)
[![XGBoost](https://img.shields.io/badge/XGBoost-Latest-orange)](https://xgboost.readthedocs.io/)
[![Docker](https://img.shields.io/badge/Docker-Ready-2496ED)](https://www.docker.com/)

</div>

---

## 🎯 Project Overview

**FitTech AI** is a production-ready full-stack website application that leverages advanced machine learning algorithms to provide personalized fitness recommendations. The system analyzes user profiles (age, gender, height, weight, activity level, and fitness goals) to generate tailored workout and nutrition plans with transparent confidence scoring.

| Use Case | Description |
|----------|-------------|
| **Personal Fitness Planning** | Generate customized workout routines based on goals and activity levels |
| **Nutrition Optimization** | Receive macro-calculated meal plans with Indonesian food database |
| **Health Coaching** | BMI-based safety restrictions ensure appropriate goal setting |
| **Research & Analysis** | Comprehensive model comparison with visualizations per experiment |
| **MLOps Demonstration** | Production-ready deployment with Docker and monitoring |

### 🔧 Overall Block Diagram

<div align="center">
  <br>
  <img width="711" height="731" alt="overalllll drawio" src="https://github.com/user-attachments/assets/01c5d4c8-f50a-4930-95df-b9eb09792df9" />
  <br>
</div>

---

## ✨ Key Features

### 🎯 Core Capabilities

| Feature | Description | Technical Implementation |
|---------|-------------|------------------------|
| 🏃 **Smart Workout Planning** | 9 workout templates across 3 fitness goals × 3 activity levels | XGBoost classification with 73.2% accuracy |
| 🥗 **Nutrition Recommendations** | 8 nutrition templates with macro calculations and meal planning | XGBoost classification with 74.0% accuracy |
| 🧠 **Advanced ML Models** | 29 engineered features with interaction terms and metabolic ratios | Feature engineering pipeline with SMOTE augmentation |
| 🛡️ **Safety-First Design** | BMI-based goal restrictions and age limits (18-65) | Business logic layer with validation rules |
| 🔄 **Feedback Loop** | Continuous improvement through user feedback integration | Post-deployment data collection pipeline |
| 🌐 **Indonesian Localization** | Food database adapted for local preferences | Region-specific nutrition templates |
| 📈 **Comprehensive Analytics** | 30+ research-quality visualizations per model run | Automated visualization pipeline |

<!-- SCREENSHOTS SECTION -->
<div align="center">
  <br>
  <h3>🖥️ User Interface Showcase</h3>
  <br>
  <table>
    <tr>
      <td align="center">
        <img width="1071" height="916" alt="cleanform" src="https://github.com/user-attachments/assets/ccf6f5a5-4e1a-42ea-83d8-8af7b6cdb84c" />
        <br>
        <i>Input Form with Real-time BMI Calculation</i>
      </td>
      <td align="center">
        <img width="929" height="774" alt="eg1" src="https://github.com/user-attachments/assets/244c0d08-fc54-4a7a-93aa-aa1636e9f188" />
        <br>
        <i>Personalized Recommendations</i>
      </td>
    </tr>
  </table>
  <br>
  <table>
    <tr>
      <td align="center">
        <img width="935" height="791" alt="eg3" src="https://github.com/user-attachments/assets/ad9a94db-255b-4803-8f11-135bb6f6ff4d" />
        <br>
        <i>Weekly Meal Plan with Macro Breakdown</i>
      </td>
      <td align="center">
        <img width="1417" height="913" alt="progress2" src="https://github.com/user-attachments/assets/e1d6fa11-005d-4439-9371-87cf07e1a06c" />
        <br>
        <i>User Dashboard with Progress Tracking</i>
      </td>
    </tr>
  </table>
  <br>
</div>

---

## 🏗️ Technical Architecture

### 🎨 System Design Overview

```
┌─────────────────────────────────────────────────────────────┐
│                     PRESENTATION LAYER                      │
│                    (React 18 +  Tailwind)                   │
│  • Progressive Forms  • Real-time Validation  • Dashboard   │
└──────────────────────┬──────────────────────────────────────┘
                       │ HTTPS/WebSocket
                       ▼
┌─────────────────────────────────────────────────────────────┐
│                    API GATEWAY LAYER                        │
│  • Rate Limiting  • SSL Termination  • Load Balancing       │
│  • Request Routing  • Caching  • Security Headers           │
└──────────────────────┬──────────────────────────────────────┘
                       │ HTTP
                       ▼
┌─────────────────────────────────────────────────────────────┐
│                  APPLICATION LAYER                          │
│                    (Flask REST API)                         │
│  • /api/predict  • /api/meal-plan  • /api/improve           │
│  • Request Validation  • Business Logic  • Response Format  │
└──────────────────────┬──────────────────────────────────────┘
                       │
                       ▼
┌─────────────────────────────────────────────────────────────┐
│                MACHINE LEARNING LAYER                       │
│   ┌─────────────────┐  ┌─────────────────┐                  │
│   │  XGBoost Model  │  │ Random Forest   │                  │
│   │  (Production)   │  │ (Research)      │                  │
│   │  • 29 Features  │  │ • Comparison    │                  │
│   │  • 73.2% Acc.   │  │ • Validation    │                  │
│   │  • 2.3 MB       │  │ • 24.1 MB       │                  │
│   └─────────────────┘  └─────────────────┘                  │
│   • Feature Engineering  • Model Inference  • Scoring       │
└──────────────────────┬──────────────────────────────────────┘
                       │
                       ▼
┌─────────────────────────────────────────────────────────────┐
│                   DATA LAYER                                │
│  • Real User Data (3,659 samples, ages 18-65)               │
│  • Synthetic Augmentation (2,203 samples via SMOTE)         │
│  • Workout Templates (9 classes)                            │
│  • Nutrition Templates (7 classes)                          │
│  • Indonesian Food Database (30+ items)                     │
└─────────────────────────────────────────────────────────────┘
```

### 🔧 Crossfunctional Diagram

<div align="center">
  <br>
  <img width="641" height="461" alt="crossfunctional drawio" src="https://github.com/user-attachments/assets/b51d6754-e683-4ec1-b1e4-497a4125506b" />
  <br>
</div>

---

## 🤖 Machine Learning Pipeline

### 🧪 Feature Engineering (29 Features)

#### **1. Core Features (11 features)**
- Age (18-65), Gender (Male/Female)
- Height (cm), Weight (kg)
- BMI (Body Mass Index)
- BMR (Basal Metabolic Rate)
- TDEE (Total Daily Energy Expenditure)
- Fitness Goal (Fat Loss / Muscle Gain / Maintenance)
- Activity Level (Low / Moderate / High)
- Workout & Nutrition Template IDs

#### **2. Interaction Features (6 features)**
- BMI × Fitness Goal
- BMI × Activity Level
- Age × Activity Level
- Goal × Activity Level
- Height × Weight Ratio
- Age × Goal Interaction

#### **3. Metabolic Features (4 features)**
- BMR per Weight (metabolic efficiency)
- TDEE/BMR Ratio (activity multiplier)
- Metabolic Age Score
- Caloric Density (calories per kg)

#### **4. Health Deviation Features (3 features)**
- Distance from Ideal BMI (22.5)
- BMI Category (Underweight/Normal/Overweight/Obese)
- Health Risk Score (composite metric)

#### **5. Activity Features (3 features)**
- Activity Multiplier (1.29 / 1.55 / 1.81)
- Activity Intensity Score
- Very Active Indicator (boolean)

#### **6. Boolean Flags (2 features)**
- High Metabolism Flag
- Low Activity Flag

### 🔄 Training Methodology

```
┌────────────────────────────────────────────────────────────┐
│ 1. DATA COLLECTION                                         │
│    • Real household dataset (ages 18-65)                   │
│    • 3,659 samples with natural distribution               │
│    • Indonesian population demographics                    │
└────────────┬───────────────────────────────────────────────┘
             │
             ▼
┌────────────────────────────────────────────────────────────┐
│ 2. PREPROCESSING                                           │
│    • Calculate BMI, BMR, TDEE                              │
│    • Encode categorical variables (One-Hot, Label)         │
│    • Handle missing values (median imputation)             │
│    • Outlier detection and treatment                       │
└────────────┬───────────────────────────────────────────────┘
             │
             ▼
┌────────────────────────────────────────────────────────────┐
│ 3. FEATURE ENGINEERING                                     │
│    • Create 29 features with interactions                  │
│    • Polynomial features for non-linearity                 │
│    • Domain-specific transformations                       │
│    • Feature scaling (StandardScaler)                      │
└────────────┬───────────────────────────────────────────────┘
             │
             ▼
┌────────────────────────────────────────────────────────────┐
│ 4. DATA AUGMENTATION (SMOTE)                               │
│    • Apply ONLY to training set (no leakage)               │
│    • Balance goal distribution (fat_loss underrepresented) │
│    • Generate 2,203 synthetic samples                      │
│    • Preserve natural variance with noise injection        │
└────────────┬───────────────────────────────────────────────┘
             │
             ▼
┌────────────────────────────────────────────────────────────┐
│ 5. TRAIN/VAL/TEST SPLIT                                    │
│    • Train: 70% (2,561 real + 2,203 synthetic)             │
│    • Validation: 15% (549 real only - no synthetic)        │
│    • Test: 15% (549 real only - no synthetic)              │
│    • Stratified by fitness goal                            │
└────────────┬───────────────────────────────────────────────┘
             │
             ▼
┌────────────────────────────────────────────────────────────┐
│ 6. MODEL TRAINING                                          │
│    • XGBoost with Optuna hyperparameter optimization       │
│    • Random Forest for algorithm comparison                │
│    • 5-fold cross-validation on training set               │
│    • Early stopping to prevent overfitting                 │
└────────────┬───────────────────────────────────────────────┘
             │
             ▼
┌────────────────────────────────────────────────────────────┐
│ 7. EVALUATION                                              │
│    • Accuracy, F1, Precision, Recall, AUC-ROC              │
│    • Confusion matrices (both models)                      │
│    • ROC curves with AUC scores                            │
│    • Feature importance analysis (gain, cover, frequency)  │
│    • Error analysis on validation set                      │
└────────────────────────────────────────────────────────────┘
```

### 📦 Model Variants

| Model | File Size | Purpose | Accuracy | Use Case |
|-------|-----------|---------|----------|----------|
| **XGBoost Production** | 2.3 MB | Web app recommendations | 73.2% / 74.0% | Real-time inference |
| **Research Model** | 24.1 MB | Thesis analysis & comparison | XGB + RF | Academic validation |
| **Perfect ML** | N/A | Theoretical upper bound | 95%+ (synthetic) | Performance ceiling |

### 🎯 Why This Approach?

1. **Feature Engineering**: 29 features capture complex non-linear relationships
2. **SMOTE Augmentation**: Balances underrepresented "fat_loss" goal in training only
3. **Strict Separation**: Validation/test sets contain ONLY real data
4. **Algorithm Comparison**: XGBoost vs Random Forest for academic rigor
5. **Transparency**: Honest reporting of limitations and confidence scores

<div align="center">
  <br>
  <h3>🖥️ Examples of Graphs from ML Training</h3>
  <br>
  <table>
    <tr>
      <td align="center">
        <img width="940" height="788" alt="6(1)" src="https://github.com/user-attachments/assets/947f03f7-92f1-4bfe-bb59-86447a17bb7e" />
        <br>
        <i>XGBoost Diet Confusion Matrix</i>
      </td>
      <td align="center">
        <img width="940" height="788" alt="4(1)" src="https://github.com/user-attachments/assets/715901b7-e3ae-46d6-b4e4-cfd9730e8685" />
        <br>
        <i>XGBoost Diet ROC Graph</i>
      </td>
    </tr>
  </table>
  <br>
</div>

---

## 🛠️ Technology Stack

### 🔙 Backend Technologies

```
Python 3.8+
├── Flask 2.0+              # REST API framework
├── XGBoost 1.6+            # Gradient boosting (production model)
├── scikit-learn 1.0+       # ML utilities & Random Forest
├── pandas 1.3+             # Data manipulation
├── numpy 1.21+             # Numerical computing
├── Optuna 3.0+             # Hyperparameter optimization
├── imbalanced-learn 0.9+   # SMOTE data augmentation
├── python-dotenv           # Environment management
├── gunicorn                # Production WSGI server
└── matplotlib/seaborn      # Visualization libraries
```

### 🎨 Frontend Technologies

```
React 18
├── Tailwind CSS 3.0+       # Utility-first styling
├── React Router 6.0+       # Client-side routing
└── Firebase 9.0+           # Authentication & Database
```

### 🐳 MLOps & Deployment

```
Docker & Containerization
├── Multi-stage builds      # Optimized image sizes (frontend: 50MB, backend: 200MB)
├── docker-compose          # Service orchestration
├── Health checks           # Container monitoring
└── Volume mounts           # Persistent model storage
```

### 📊 Data Science & Visualization

```
Analysis & Reporting
├── matplotlib 3.4+         # Static visualizations
├── seaborn 0.11+           # Statistical plots
└── pandas-profiling        # Automated EDA
```

---

## 🏆 Project Highlights

### 1. 🎯 Advanced Feature Engineering
- **29 engineered features** including interaction terms, metabolic ratios, and health deviation scores
- Captures non-linear relationships between user attributes and fitness outcomes
- Domain-specific transformations based on exercise science principles
- Feature importance analysis reveals top predictors (BMI×Goal, Activity Level)

### 2. 🔬 Transparent Methodology
- **No artificial data fixes** - preserves natural distributions
- Reports limitations honestly with confidence scoring
- Establishes theoretical performance bounds with synthetic "perfect" data
- Validation/test sets contain 100% real data (no synthetic leakage)

### 3. 🛡️ Safety-First Design
- **BMI-based goal restrictions** prevents unhealthy recommendations
  - Underweight: Only Muscle Gain & Maintenance
  - Normal: All goals available
  - Overweight: Only Fat Loss & Maintenance
  - Obese: Only Fat Loss
- Age limits (18-65) based on model training data
- Fallback logic for edge cases and low-confidence predictions

### 4. 📈 Research-Grade Analysis
- **35+ visualizations** per experiment run
- Comprehensive model comparison (XGBoost vs Random Forest)
- Feature importance analysis with SHAP-like interpretability
- Executive summary dashboards for stakeholder communication

### 5. 🚀 Production Ready
- Docker containerization with multi-stage builds
- Nginx reverse proxy with rate limiting (100 req/min)
- Health check endpoints for monitoring (`/api/health`)
- Environment-based configuration (dev/staging/prod)

### 6. 🔄 Continuous Improvement
- Feedback-based recommendation refinement via `/api/improve-recommendation`
- Model retraining pipeline with `/api/retrain` endpoint
- Template-based system for easy maintenance and updates
- A/B testing framework ready for deployment

### 7. 🌏 Localization
- Indonesian food database (1,000+ local foods)
- Region-specific nutrition templates
- Localized UI labels and descriptions
- Currency and unit conversions (metric system)

---

## 📈 Full results, visualisations and analysis available to read on my thesis paper:

### https://openlibrary.telkomuniversity.ac.id/home/catalog/id/242125/slug/implementation-of-diet-and-physical-exercise-recommendation-systems-using-xgboost-dalam-bentuk-buku-karya-ilmiah.html

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

#### 🔗 Connect With Me

- **GitHub**: [@kamilahasanahh](https://github.com/kamilahasanahh)
- **LinkedIn**: [Kamila Hasanah](https://linkedin.com/in/kamilahasanah)

#### 💼 Skills Demonstrated in This Project

- **Machine Learning**: XGBoost, Random Forest, Feature Engineering, Model Evaluation
- **MLOps**: Docker, Flask APIs, Model Deployment, Monitoring
- **Data Science**: Pandas, NumPy, Data Visualization, Statistical Analysis
- **Full-Stack Development**: React, Flask, REST APIs, Firebase
- **Research Methodology**: Experimental Design, Algorithm Comparison, Transparency
- **Software Engineering**: Git, Testing, Documentation, CI/CD

