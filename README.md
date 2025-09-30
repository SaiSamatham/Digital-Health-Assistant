Health Navigator: Symptom-Based Disease Prediction and Recommendation System
Welcome to Health Navigator! This is a web application built with Python and Flask that utilizes a pre-trained Machine Learning model (Support Vector Classifier - SVC) to predict potential diseases based on user-inputted symptoms.

Beyond prediction, the system provides comprehensive, disease-specific health recommendations, including descriptions, necessary precautions, suggested medications, diet plans, and workout routines, all sourced from structured datasets.

🚀 Project Objective
The goal of this project is to create an accessible, immediate, and informative tool that:

Predicts a likely disease from a list of common symptoms using an SVC model.

Delivers actionable health advice (precautions, diet, workout) for the predicted condition.

Serves this information through a user-friendly Flask web interface.

🛠️ Technologies and Dependencies
This project is built using the following core technologies:

Python 3.x

Flask: Web framework for handling routes and serving HTML templates.

Pandas: For reading, processing, and manipulating the health datasets.

NumPy: For efficient handling of numerical operations, especially creating the symptom input vector.

Scikit-learn: Used for the SVC model (loaded via pickle).

Installation
Clone the repository:

git clone [https://github.com/your-username/health-navigator.git](https://github.com/your-username/health-navigator.git)
cd health-navigator


Create a virtual environment (recommended):

python -m venv venv
source venv/bin/activate  # On Linux/macOS
.\venv\Scripts\activate   # On Windows


Install dependencies:
(Note: You will need to create a requirements.txt file listing all necessary packages like Flask, pandas, numpy, and scikit-learn.)

pip install -r requirements.txt


📂 Project Structure
Your project relies on several external files for datasets and the trained model.

health-navigator/
├── main.py                   # The main Flask application logic
├── Models/
│   └── svc.pkl               # The serialized SVC model
├── Datasets/
│   ├── symptoms_df.csv       # Symptom-to-description mapping
│   ├── precautions_df.csv    # Precautions for each disease
│   ├── workout_df.csv        # Workout recommendations
│   ├── description.csv       # Detailed disease descriptions
│   ├── medications.csv       # Medication suggestions
│   └── diets.csv             # Diet recommendations
└── templates/
    ├── index.html            # Main prediction page
    ├── about.html
    ├── contact.html
    ├── blog.html
    └── developer.html


⚠️ Important: Ensure the Models and Datasets folders exist and contain the necessary files, as main.py explicitly loads them.

⚙️ Usage and Running the Application
Run the Flask application:

python main.py


Access the application:
Open your web browser and navigate to the address displayed in the console (typically http://127.0.0.1:5000/).

Prediction:

On the /predict route (usually the home page), enter a comma-separated list of symptoms (e.g., chills, high_fever, headache, nausea).

The application will display the predicted disease along with the description, precautions, medications, diet, and workout suggestions.

🧠 Model & Prediction Logic
The prediction is performed by the get_predicted_value function:

It maps the user's input symptoms to a fixed index using the symptoms_dict.

It creates a one-hot encoded vector of 132 features (representing the 132 possible symptoms).

This vector is passed to the loaded SVC model (svc.pkl) for prediction.

The integer output from the SVC is mapped back to a human-readable disease name using diseases_list.

The helper function then retrieves all associated recommendation data (description, precautions, medications, diets, workouts) for the predicted disease from the corresponding CSV files.

📝 Future Improvements
Improved Symptom Input: Implement a type-ahead search or checkbox system instead of plain comma-separated input to prevent misspelled symptoms.

Model Performance: Explore other machine learning models (e.g., Random Forest, Naive Bayes) for better accuracy and compare their performance.

Authentication and User History: Add user authentication and a database to store past prediction history.

Dynamic Data Loading: The datasets are currently hardcoded and loaded upon app startup. For large datasets, consider using a database or more efficient data access methods.Health Navigator: Symptom-Based Disease Prediction and Recommendation System
Welcome to Health Navigator! This is a web application built with Python and Flask that utilizes a pre-trained Machine Learning model (Support Vector Classifier - SVC) to predict potential diseases based on user-inputted symptoms.

Beyond prediction, the system provides comprehensive, disease-specific health recommendations, including descriptions, necessary precautions, suggested medications, diet plans, and workout routines, all sourced from structured datasets.

🚀 Project Objective
The goal of this project is to create an accessible, immediate, and informative tool that:

Predicts a likely disease from a list of common symptoms using an SVC model.

Delivers actionable health advice (precautions, diet, workout) for the predicted condition.

Serves this information through a user-friendly Flask web interface.

🛠️ Technologies and Dependencies
This project is built using the following core technologies:

Python 3.x

Flask: Web framework for handling routes and serving HTML templates.

Pandas: For reading, processing, and manipulating the health datasets.

NumPy: For efficient handling of numerical operations, especially creating the symptom input vector.

Scikit-learn: Used for the SVC model (loaded via pickle).

Installation
Clone the repository:

git clone [https://github.com/your-username/health-navigator.git](https://github.com/your-username/health-navigator.git)
cd health-navigator


Create a virtual environment (recommended):

python -m venv venv
source venv/bin/activate  # On Linux/macOS
.\venv\Scripts\activate   # On Windows


Install dependencies:
(Note: You will need to create a requirements.txt file listing all necessary packages like Flask, pandas, numpy, and scikit-learn.)

pip install -r requirements.txt


📂 Project Structure
Your project relies on several external files for datasets and the trained model.

health-navigator/
├── main.py                   # The main Flask application logic
├── Models/
│   └── svc.pkl               # The serialized SVC model
├── Datasets/
│   ├── symptoms_df.csv       # Symptom-to-description mapping
│   ├── precautions_df.csv    # Precautions for each disease
│   ├── workout_df.csv        # Workout recommendations
│   ├── description.csv       # Detailed disease descriptions
│   ├── medications.csv       # Medication suggestions
│   └── diets.csv             # Diet recommendations
└── templates/
    ├── index.html            # Main prediction page
    ├── about.html
    ├── contact.html
    ├── blog.html
    └── developer.html


⚠️ Important: Ensure the Models and Datasets folders exist and contain the necessary files, as main.py explicitly loads them.

⚙️ Usage and Running the Application
Run the Flask application:

python main.py


Access the application:
Open your web browser and navigate to the address displayed in the console (typically http://127.0.0.1:5000/).

Prediction:

On the /predict route (usually the home page), enter a comma-separated list of symptoms (e.g., chills, high_fever, headache, nausea).

The application will display the predicted disease along with the description, precautions, medications, diet, and workout suggestions.

🧠 Model & Prediction Logic
The prediction is performed by the get_predicted_value function:

It maps the user's input symptoms to a fixed index using the symptoms_dict.

It creates a one-hot encoded vector of 132 features (representing the 132 possible symptoms).

This vector is passed to the loaded SVC model (svc.pkl) for prediction.

The integer output from the SVC is mapped back to a human-readable disease name using diseases_list.

The helper function then retrieves all associated recommendation data (description, precautions, medications, diets, workouts) for the predicted disease from the corresponding CSV files.

📝 Future Improvements
Improved Symptom Input: Implement a type-ahead search or checkbox system instead of plain comma-separated input to prevent misspelled symptoms.

Model Performance: Explore other machine learning models (e.g., Random Forest, Naive Bayes) for better accuracy and compare their performance.

Authentication and User History: Add user authentication and a database to store past prediction history.

Dynamic Data Loading: The datasets are currently hardcoded and loaded upon app startup. For large datasets, consider using a database or more efficient data access methods.
