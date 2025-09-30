# Credit-Card-Abandonment-Predictive-Modelling---Python
Predictive Modeling for Credit Card Application Abandonment
This project simulates a real-world data science initiative for a leading provider of private-label and co-branded credit cards for major retail partners like The Home Depot, Macy's, and Best Buy. The primary objective is to build and interpret a machine learning model that predicts whether a customer will abandon their online credit card application.
The repository contains the full workflow in a Jupyter Notebook, from synthetic data generation that mimics real user behavior to model building, evaluation, and the final business recommendations.

1. The Business Problem & The Client
The Client: Operates in a highly competitive market where customer acquisition is key. Their business model relies on successfully converting online shoppers into new credit card holders for their retail partners.
The Core Problem: A significant portion of potential revenue is lost due to application abandonment. Users start an online application with high intent but drop off before submitting it. This friction in the digital journey represents a direct loss of a new customer for both Client and its retail partner.
The business needed to move from a reactive approach (analyzing past abandonment rates) to a proactive strategy (identifying at-risk users in real-time to prevent abandonment).

2. The Project's End Goal
The end goal of this project is not just to build an accurate predictive model, but to translate its outputs into an actionable, data-driven business strategy.
Specifically, we aim to:
Identify Key Drivers: Determine the most significant factors and user behaviors that lead to application abandonment.
Develop a Predictive Tool: Build a robust classification model that can assign a real-time "abandonment probability score" to each active user session.
Formulate a Recommendation: Propose a targeted intervention strategy that uses the model's predictions to reduce the overall abandonment rate and increase the number of successful applications.

3. The Data
Since the actual customer data is proprietary, this project uses a synthetic dataset generated to realistically mimic the patterns and challenges observed in the real world.
The dataset covers a full year (2024) of user sessions, with approximately 600k-1M records per month. Each record represents a unique application session and includes the following features:
device_type: Whether the user is on Mobile or Desktop.
marketing_channel: The source that brought the user to the application (e.g., Web Banner, QR Code).
used_prefill: A binary flag (1/0) indicating if the user leveraged the data pre-fill feature.
time_on_page_seconds: Time spent on the application form.
pages_visited: Number of pages visited before reaching the form.
form_errors_encountered: The count of validation errors the user experienced.
abandoned_application (Target Variable): A binary flag (1/0) indicating if the session ended without a submission.

4. Methodology & Key Technologies
This project follows a standard data science workflow:
Data Generation & EDA: Synthetic data creation and exploratory analysis to uncover initial insights.
Preprocessing: Using Scikit-learn's ColumnTransformer and Pipeline for robust feature scaling and encoding.
Model Building: Training and comparing two models:
Logistic Regression: For its high interpretability to understand the "why" behind predictions.
XGBoost: For its high predictive power and ability to generate feature importance scores.
Evaluation: Assessing model performance using metrics like AUC-ROC, Precision, and Recall.
Interpretation: Translating model results (feature importances, coefficients) into business insights.
Key Technologies Used:
Python: The core programming language.
Pandas & NumPy: For data manipulation and generation.
Matplotlib & Seaborn: For data visualization and EDA.
Scikit-learn: For data preprocessing, pipelines, and logistic regression modeling.
XGBoost: For building the high-performance gradient boosting model.
Jupyter Notebook: For structuring and documenting the entire workflow.

5. Key Findings & Business Recommendations
The XGBoost model performed exceptionally well, achieving an AUC of 0.96, which gives us high confidence in its ability to distinguish between users who will complete the application and those who will abandon it.
The model's Feature Importance analysis revealed three critical insights that directly inform our final recommendations:
Finding 1: The "Pre-fill" Feature is a Game-Changer.
The single most impactful factor in preventing abandonment was whether a user utilized the data pre-fill feature.
Recommendation: Provide the business with the statistical proof needed to justify a full-scale rollout of the "PROVE-Prefill" feature across all retail partners. This feature should be a top priority for future investment.
Finding 2: Form Errors are a Conversion Killer.
The number of validation errors a user encounters is the second most significant predictor of abandonment. Each error dramatically increases the likelihood that a user will give up.
Recommendation: Launch a dedicated UX/UI review project focused on simplifying the application form. Implement better real-time validation, clearer instructions, and error messages to prevent users from making mistakes in the first place.
Finding 3: The Mobile Experience Needs Special Attention.
Being on a mobile device was a significant independent risk factor for abandonment. The mobile journey is inherently more challenging for users.
Recommendation: Create a "Mobile-First Optimization" initiative. Instead of simply ensuring the site is responsive, the entire application flow should be redesigned specifically for the constraints and user patterns of mobile devices.
The Final Strategic Recommendation: Real-Time Intervention
Based on the model's predictive power, we recommend implementing a real-time risk scoring system.
How it Works: The model will run in the background, assigning an "abandonment probability score" to each active user session.
The Intervention: If a user's score crosses a predetermined threshold (e.g., 75%), the system will automatically trigger a targeted intervention, such as a "Need help?" live chat pop-up or an offer for assistance.
This strategy moves the business from being reactive to proactive, using data science to save conversions before they are lost and directly increasing the number of new credit card acquisitions
