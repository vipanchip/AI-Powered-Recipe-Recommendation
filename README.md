# AI-Powered Recipe-Recommendation 


## Introduction  
This project is a **Recipe Recommendation System** designed to suggest recipes based on user-provided nutritional values and ingredients. It combines **machine learning techniques** with a user-friendly **web application framework** to deliver personalized recipe recommendations.

---

## Dataset  

### Overview  
The dataset used for this project is a CSV file named `recipe_final (1).csv`, containing detailed information about various recipes, which is essential for building the recommendation system.  

### Features  
The dataset includes the following columns:  
- `Unnamed: 0`: Index column.  
- `recipe_id`: Unique identifier for each recipe.  
- `recipe_name`: Name of the recipe.  
- `aver_rate`: Average rating of the recipe.  
- `image_url`: URL to an image of the recipe.  
- `review_nums`: Number of reviews for the recipe.  
- `calories`: Number of calories in the recipe.  
- `fat`: Amount of fat in grams.  
- `carbohydrates`: Amount of carbohydrates in grams.  
- `protein`: Amount of protein in grams.  
- `cholesterol`: Amount of cholesterol in milligrams.  
- `sodium`: Amount of sodium in milligrams.  
- `fiber`: Amount of dietary fiber in grams.  
- `ingredients_list`: List of ingredients used in the recipe.  

---

## Data Preprocessing  

### Ingredient Processing  
- The `ingredients_list` column is processed using **TF-IDF (Term Frequency-Inverse Document Frequency) Vectorizer** to convert text data into numerical vectors, capturing the importance of each ingredient within the dataset.  

### Numerical Feature Normalization  
- Numerical features such as `calories`, `fat`, `carbohydrates`, `protein`, `cholesterol`, `sodium`, and `fiber` are normalized using **StandardScaler**, ensuring equal contribution to distance calculations in the recommendation model.  

### Feature Combination  
- The numerical features and ingredient vectors are combined to form a **comprehensive feature set**, representing each recipe in a high-dimensional space.  

---

## Machine Learning Model  

### K-Nearest Neighbors (KNN)  
The recommendation system uses the **K-Nearest Neighbors (KNN)** algorithm to identify the most similar recipes based on **Euclidean distance** in the feature space.  
- The KNN model is trained on the combined feature set, enabling it to recommend recipes by comparing similarities in both numerical and textual data.  

---

## Web Application  

### Framework  
- The system is built using **Flask**, a lightweight Python web framework, which provides the backend infrastructure for handling user input and generating recommendations.  

### Functionality  
1. **Form Submission**: Users input their desired nutritional values and ingredients via a web form.  
2. **Recommendation Generation**: The system processes the input, computes similarity using the trained KNN model, and retrieves the top 5 most similar recipes.  
3. **Display**: Recommended recipes are displayed with details such as recipe name, ingredients, and an image.  

### User Interface  
- Designed with **Bootstrap** for responsiveness and user-friendliness.  
- Includes:  
  - A form for user input.  
  - A visually appealing card layout to display recommended recipes.  

---

## Techniques and Tools  

### Data Processing  
- **TF-IDF Vectorizer**: Converts ingredient lists into numerical vectors.  
- **StandardScaler**: Normalizes numerical features.  
- **NumPy**: Handles numerical operations and feature combination.  

### Machine Learning  
- **K-Nearest Neighbors (KNN)**: Finds similar recipes using Euclidean distance.  

### Web Development  
- **Flask**: Backend framework for the web application.  
- **Bootstrap**: Ensures responsive and modern UI.  

---

## Conclusion  
This **Recipe Recommendation System** integrates **data processing**, **machine learning**, and **web development** to deliver personalized recipe recommendations. By leveraging advanced techniques like **TF-IDF vectorization** and **KNN**, the system effectively matches user preferences with suitable recipes, providing a seamless and engaging user experience.  

---

## How to Run  

1. Clone the repository:  
   ```bash
   git clone https://github.com/vipanchip/AI-Powered-Recipe-Recommendation.git
   
2. Install dependencies:   
   ```bash
   pip install -r requirements.txt

3. Run the Flask application:
   ```bash
   python app.py

4. Open your browser and navigate to:
   ```bash
   http://127.0.0.1:5000/
   
