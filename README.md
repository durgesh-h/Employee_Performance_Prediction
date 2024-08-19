## Employee Performance Prediction Project Documentation
# Overview
This project involves creating a machine learning model to analyze and predict employee performance by evaluating various factors. The model is implemented using the XGBoost algorithm due to its outstanding performance in predicting outcomes compared to linear regression and random forest models.

# Technologies Used
- Python: The primary programming language for model development.
- Flask: A lightweight web framework used to develop the application.
- HTML/CSS: For the frontend structure and styling of the web pages.
- Bootstrap: For making the frontend design responsive and modern.
- XGBoost: The machine learning algorithm chosen for its high R2 score.
- Pickle: Used for serializing and saving the trained machine learning model.

## Installation and Setup
# Clone the Repository:

bash
Copy code
git clone [https://github.com/your-repo/employee_performance_analysis.git](https://github.com/abhinavomer/Employee_Performance_Analysis/edit/main/README.md)
cd employee_performance_analysis
Create and Activate a Virtual Environment:

bash
Copy code
python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
Install Required Dependencies:

bash
Copy code
pip install -r requirements.txt
Run the Flask Application:

bash
Copy code
python app.py
Access the Web Application:
Open your web browser and navigate to http://127.0.0.1:5000/.

# Project Structure
graphql
Copy code
employee_performance_analysis/

│

├── app.py                  # Main Flask application entry point

├── model.h5                # Serialized XGBoost model file

├── templates/              # HTML templates directory

│   ├── base.html           # Base template with common elements

│   ├── home.html           # Home page template

│   ├── about.html          # About page template

│   ├── predict.html        # Form page for predictions

│   ├── submit.html         # Page to display prediction results

└── README.md               # Project documentation file


# Model Development
The dataset includes a variety of features related to employee performance, such as:

- Quarter: Time period of evaluation
- Department: Specific department within the organization
- Day: Day of the week
- Team: Team identifier
- Targeted Productivity: Productivity goals set for employees
- SMV: Standard Minute Value
- Over Time: Overtime hours worked
- Incentive: Additional incentives provided
- Idle Time: Time employees were idle
- Idle Men: Number of idle employees
- No. of Style Changes: Number of changes in work style
- No. of Workers: Total number of workers
- Month: The month in which performance is evaluated
- Model Selection
- Three different machine learning models were considered during the development process:

- Linear Regression: A basic model for comparison.
- Random Forest: An ensemble learning method.
- XGBoost: Chosen for its superior accuracy and R2 score.

# Model Training
The XGBoost model was trained with a carefully prepared dataset. The data was divided into training and testing sets, and hyperparameters were tuned to ensure optimal performance.

# Model Serialization
After training, the XGBoost model was serialized using the Pickle library. This allows the trained model to be easily loaded and used in the Flask application for making predictions.

#  Flask Application
Routes:

- Home (/): The main landing page.
- About (/about): Details about the project and its objectives.
- Predict (/predict): A form where users can input data to receive predictions.
- Submit (/submit): Displays the results after data submission.
- Prediction Endpoint (/pred): Backend route handling the form submissions and generating predictions.
- 
HTML Templates:
- base.html: Contains common elements such as navigation and styles, including Bootstrap integration.
- home.html: Template for the homepage.
- about.html: Provides information about the project.
- predict.html: The form page where users can input data for predictions.
- submit.html: Displays the results after submitting the prediction form.

Static Files:
- styles.css: Custom styles defined for the application, included in the base template.
# Usage
- Navigate to the Prediction Page: Access the prediction page by clicking the "Predict" link in the navbar.
- Fill Out the Form: Enter all required details into the provided form fields.
- Submit the Form: Click the "Submit" button to process the data and generate a prediction.
- View the Prediction: The result will be displayed on the "Submit" page, showing the predicted performance.
# Conclusion
This project offers a streamlined interface for predicting employee performance using a machine learning model integrated with a Flask web application. The XGBoost model's high accuracy ensures reliable predictions, while the user-friendly interface allows easy data input and results retrieval.
