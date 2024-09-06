# IBM Data Science Capstone - SpaceX Falcon 9 First Stage Landing Prediction

# Introduction
SpaceX, a leader in the space industry, has revolutionized space travel with reusable rocket technology, specifically the first stage of the Falcon 9 rocket. By predicting whether the Falcon 9 first stage will land successfully, we can estimate the cost of launches more accurately. This project focuses on using machine learning models to predict the success of these landings based on key features such as payload mass, launch site, and orbit type.

# Executive Summary
This project aims to identify the factors influencing a successful Falcon 9 rocket landing. The process involved:

Collecting data through the SpaceX API and web scraping
Cleaning and wrangling the data to create a success/fail variable
Performing exploratory data analysis (EDA) to investigate key factors like payload, launch site, and orbit type
Visualizing data through interactive maps and dashboards
Building machine learning models to predict landing success
Key findings indicate that success rates have improved over time, and specific launch sites and orbit types are associated with higher success rates. The decision tree model provided the best performance among the models used.

# Methodology
Data Collection - API & Web Scraping

Data was collected using the SpaceX API and web scraping from Wikipedia to gather details on Falcon 9 rocket launches.
The API provided key launch data, which was filtered to focus on Falcon 9 missions. Missing values were handled by imputing the mean where necessary.
The data was then wrangled and formatted into a clean dataset for analysis, containing features like launch site, payload mass, orbit type, and mission outcome.
Exploratory Data Analysis (EDA)

Relationships between features and landing success were explored, revealing that certain launch sites (e.g., KSC LC-39A) and orbit types (e.g., ES-L1, GEO) had higher success rates.
The data showed an improvement in landing success rates over time, with higher payloads generally leading to more successful landings.
Visualization

Maps were created using Folium to visualize launch sites and outcomes. Most sites were located near the equator and the coast, helping boost launch success.
An interactive dashboard was built with Plotly Dash, allowing users to explore success rates by launch site, payload mass, and mission outcomes using pie charts and scatterplots.
Predictive Modeling
Four machine learning models were implemented to predict landing success:

Logistic Regression
Support Vector Machine (SVM)
Decision Tree
K-Nearest Neighbors (KNN)
The data was standardized, split into training and test sets, and optimized using GridSearchCV for hyperparameter tuning. Accuracy scores and confusion matrices were used to evaluate model performance. The decision tree model slightly outperformed the others, achieving a GridSearchCV best score of 0.89.

# Results
Launch Success: Success rates have consistently improved, with specific sites like KSC LC-39A showing the highest rates.
Orbits: Orbits such as ES-L1, GEO, HEO, and SSO had a 100% success rate.
Payload Mass: Higher payloads were correlated with better landing outcomes, particularly for certain launch sites.
Geography: Launch sites near the equator and coast provided a natural advantage, reducing fuel needs and boosting success rates.

# Conclusion
The decision tree model was the best predictor of landing success, though other models performed similarly. Insights from this analysis can help estimate launch costs and improve future predictions. With a larger dataset and further feature analysis, these models could become even more accurate, offering valuable information for competitive bidding in the space industry.
