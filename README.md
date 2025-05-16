# ✍️ Handwritten Letter Recognizer

Welcome to the Handwritten Letter Recognizer – a smart, intuitive deep learning project that brings handwritten alphabets to life using the power of neural networks! Whether you're a student, educator, or machine learning enthusiast, this project offers a fascinating dive into how machines can read and understand human handwriting – one letter at a time.

📊 Dataset Description
Source: Kaggle dataset nishan192/letterrecognition-using-svm
Classes: 26 (A-Z)
Features: 16 numerical values extracted from images (e.g., width, height, pixel statistics)
Label: letter (A-Z)
Each row represents a single handwritten alphabet image, where features have been pre-extracted using basic image processing techniques. All features are numeric and suitable for direct use in ML models.

📁 Files
File	Description
LetterRecognizer.ipynb	Main Jupyter Notebook containing preprocessing, training, evaluation, and visualization
README.md	Project overview and usage instructions

🧠 Models Used
The following classifiers are trained and evaluated:

✅ Support Vector Machine (SVM) – with RBF kernel
✅ Random Forest – with 100 estimators
✅ K-Nearest Neighbors (KNN) – with K=5
✅ Logistic Regression – max_iter=1000
✅ Voting Classifier (Ensemble) – soft voting over the above four models

🔄 Workflow Overview
Data Loading
Dataset downloaded using kagglehub
CSV loaded into a pandas DataFrame

Preprocessing
Strips extra whitespace from column names
Splits dataset into features X and target y
Encodes labels (letters A-Z → 0–25) using LabelEncoder
Scales features using StandardScaler

Model Training
Each model is trained on the training set
Models are evaluated on the test set (20% split with stratification)

Evaluation
accuracy_score, classification_report, and confusion_matrix for all models
Confusion matrices visualized using Seaborn heatmaps

📈 Results
All models show competitive performance, with the Voting Classifier leveraging the strengths of the individual classifiers to improve accuracy.

🛠️ Tech Stack
Python 
Scikit-learn 
Matplotlib & Seaborn 
KaggleHub
