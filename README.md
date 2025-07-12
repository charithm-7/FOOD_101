# 🍱 Food Prediction and Calorie Estimation using Machine Learning

This project uses machine learning to predict the type of food and estimate its calorie content based on input features such as ingredients, quantity, and nutritional values. It aims to help users make healthier food choices and track their daily intake.

---

## 📌 Key Features

- 🔍 **Food Item Classification** from user input or dataset
- 🔢 **Calorie Prediction** using regression models
- 📊 Trained on a labeled dataset with food names, ingredients, and calories
- ✅ Cleaned, preprocessed, and normalized data
- 📈 Evaluated using accuracy, RMSE, and R² score

---

## 🧠 Machine Learning Models Used

- Classification: Random Forest, Logistic Regression, SVM
- Regression: Linear Regression, Decision Tree Regressor
- Feature Scaling: MinMaxScaler
- Model Evaluation: Accuracy, MAE, RMSE, R²

---



## 🗃️ Dataset

- 📥 **Source:** [Food-101 Dataset on Kaggle](https://www.kaggle.com/datasets/dansbecker/food-101)
- Contains 101 categories of food images and labels
- Used for both classification (food prediction) and calorie estimation (when combined with nutritional data)
- Ideal for image-based and ingredient-based food ML tasks

**Features (when extended with calorie info):**
- Food Name / Category
- Image data (JPEG)
- Ingredients (manually mapped or extracted)
- Calories (estimated per 100g or per serving)

## ▶️ How to Run

```bash
# Step 1: Install dependencies
pip install -r requirements.txt

# Step 2: Run the main script
python food_prediction.py
