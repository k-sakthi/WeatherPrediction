
  # 🌡️ Weather Prediction using Machine Learning

  This project focuses on predicting the **Apparent Temperature** of a location based on various weather parameters using regression
  techniques. It demonstrates a full data science pipeline, from data cleaning and exploratory data analysis (EDA) to model
  evaluation.

  ## 📊 Dataset
  The project uses the `weatherHistory.csv` dataset, which contains detailed weather recordings including:
  - **Temperature (C)**
  - **Humidity**
  - **Wind Speed (km/h)**
  - **Wind Bearing (degrees)**
  - **Visibility (km)**
  - **Pressure (millibars)**
  - **Precipitation Type** (Rain, Snow, etc.)

  ## ⚙️ Project Pipeline

  ### 1. Data Preprocessing
  - **Cleaning**: Handled missing values in `Precip Type` using mode imputation.
  - **Feature Selection**: Removed irrelevant columns like `Formatted Date`, `Summary`, and `Daily Summary`.
  - **Encoding**: Converted categorical data (`Precip Type`) into numerical format using One-Hot Encoding.
  - **Scaling**: Applied `StandardScaler` to normalize features for the Linear Regression model.

  ### 2. Exploratory Data Analysis (EDA)
  The project includes several visualizations to understand data relationships:
  - **Correlation Heatmap**: To identify which weather features strongly influence the apparent temperature.
  - **Distribution Plot**: To analyze the spread of the target variable.
  - **Scatter Plots**: Specifically analyzing the relationship between Humidity and Temperature.

  ### 3. Machine Learning Models
  Two different regression models were implemented and compared:
  - **Linear Regression**: A baseline model to establish a linear relationship.
  - **Random Forest Regressor**: An ensemble model used to capture complex, non-linear patterns.

  ## 📈 Results

  The models were evaluated using MAE, MSE, RMSE, and $R^2$ Score.

  | Model | MAE | RMSE | $R^2$ Score |
  | :--- | :--- | :--- | :--- |
  | **Linear Regression** | 0.844 | 1.070 | 0.990 |
  | **Random Forest** | **0.014** | **0.055** | **1.000** |

  **Conclusion**: The Random Forest model significantly outperformed Linear Regression, achieving nearly perfect accuracy in
  predicting the apparent temperature.

  ## 🛠️ Tech Stack
  - **Language**: Python
  - **Libraries**:
    - `Pandas` (Data Manipulation)
    - `NumPy` (Numerical Computing)
    - `Matplotlib` & `Seaborn` (Data Visualization)
    - `Scikit-Learn` (Machine Learning)

  ## 🚀 How to Run
  1. Clone the repository:
     ```bash
     git clone https://github.com/k-sakthi/WeatherPrediction.git
  2. Open the WeatherPrediction.ipynb file in Jupyter Notebook or Google Colab.
  3. Ensure you have the weatherHistory.csv file in the same directory.
  4. Run all cells to see the analysis and predictions.
