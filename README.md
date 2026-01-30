# 🚀 SpaceX Falcon 9 First Stage Landing Prediction

## 📄 Project Overview
This project is an end-to-end data science capstone designed to predict the successful landing of the SpaceX Falcon 9 rocket first stage. By analyzing historical launch data, we determine the factors that contribute to a successful landing, which is critical for estimating launch costs. A successful landing allows the first stage to be reused, significantly lowering the cost of a launch to approximately $62 million, compared to $165 million for a non-reusable launch.

This repository contains the full pipeline: **Data Collection, Data Wrangling, Exploratory Data Analysis (SQL & Visualization), Interactive Analytics (Folium & Plotly Dash), and Machine Learning Prediction.**

## 🗂️ File Structure & Methodology

The project is structured into sequential stages, each represented by specific notebooks and scripts in this repository:

### 1. Data Collection
* **`Data_collection_BY_API.ipynb`**: Fetches up-to-date launch data from the **SpaceX REST API**, including details on rocket boosters, launch pads, payloads, and landing outcomes.
* **`Data_collection_by_WebScraping.ipynb`**: Scrapes historical Falcon 9 launch records from Wikipedia using **BeautifulSoup** to supplement the API data.

### 2. Data Wrangling (Cleaning)
* **`Data wrangling.ipynb`**: Cleans the raw dataset by handling missing values, filtering for Falcon 9 launches, and processing the target variable (Class 1 = Success, Class 0 = Failure). It produces the cleaned datasets (`dataset_part_1.csv`, `dataset_part_2.csv`).

### 3. Exploratory Data Analysis (EDA)
* **`EDA_BY_SQL.ipynb`**: Executes **SQL queries** to derive insights, such as total payload mass, success rates by orbit, and identifying major launch sites.
* **`EDA_Data_Visualization.ipynb`**: visualizes relationships between variables (e.g., Payload vs. Orbit, Flight Number vs. Launch Site) using **Matplotlib** and **Seaborn**.

### 4. Interactive Visual Analytics
* **`Interactive Visual Analytics with Folium.ipynb`**: Uses **Folium** to create interactive maps, visualizing launch sites and the success/failure distribution of landings at each location.
* **`spacex-dash-app.py`**: A fully functional **Plotly Dash** web application. It features:
    * A Launch Site Dropdown to filter data.
    * Pie charts showing success rates for specific sites.
    * A Range Slider to filter by Payload Mass.
    * Scatter charts to analyze the correlation between Payload Mass and Success.

### 5. Machine Learning Prediction
* **`Machine_Learning_Prediction.ipynb`**: The core predictive modeling notebook.
    * **Preprocessing:** Standardizes data and performs One-Hot Encoding.
    * **Model Training:** Trains four different classification models:
        1.  Logistic Regression
        2.  Support Vector Machine (SVM)
        3.  Decision Tree Classifier
        4.  K-Nearest Neighbors (KNN)
    * **Optimization:** Uses `GridSearchCV` to tune hyperparameters for each model.
    * **Evaluation:** Compares models based on accuracy to determine the best performer for landing prediction.

## 🛠️ Technologies Used
* **Languages:** Python, SQL
* **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, Folium, Plotly, Dash, Requests, BeautifulSoup
* **Tools:** Jupyter Notebook, GitHub

## 📊 Key Insights
* **Launch Sites:** Different launch sites have varying success rates, with specific sites (e.g., KSC LC-39A) showing higher reliability for heavy payloads.
* **Payload vs. Orbit:** There is a distinct correlation between payload mass and orbit type, influencing the likelihood of a successful landing.
* **Temporal Trends:** Success rates have improved significantly over time as SpaceX refined their technology.

## 🚀 How to Run the Project

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/kamalkishor-roj/IBM-Data-Science-Capstone-SpaceX-Project.git](https://github.com/kamalkishor-roj/IBM-Data-Science-Capstone-SpaceX-Project.git)
    ```
2.  **Install Dependencies:**
    Ensure you have the required libraries installed:
    ```bash
    pip install pandas numpy matplotlib seaborn scikit-learn folium plotly dash requests beautifulsoup4
    ```
3.  **Run the Notebooks:**
    Open the `.ipynb` files in Jupyter Notebook or JupyterLab in the order listed above to replicate the analysis.
4.  **Launch the Dashboard:**
    Run the python script to start the local server:
    ```bash
    python spacex-dash-app.py
    ```
    Then, open your browser and go to `http://127.0.0.1:8050/`.

## 👨‍💻 Author
**Kamalkishor Roj**
* [GitHub Profile](https://github.com/kamalkishor-roj)
