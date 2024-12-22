# Yulu Shared Electric Cycle Demand Analysis  

## About Yulu  
Yulu is India's leading micro-mobility service provider, offering eco-friendly and convenient vehicles for daily commutes. With a mission to eliminate traffic congestion, Yulu provides shared, solo, and sustainable commuting solutions through a user-friendly mobile app.  

Yulu zones are strategically located near metro stations, bus stands, residential areas, office spaces, and other key locations to make first and last-mile connectivity smooth, affordable, and convenient.  

Recently, Yulu has faced significant revenue dips and has engaged a consulting team to identify the factors driving the demand for their shared electric cycles in the Indian market.  

---

## Objective  
The primary goals of this analysis are to:  
1. Identify significant variables that influence the demand for shared electric cycles.  
2. Evaluate how well these variables explain the overall demand.  

---

## Dataset  
The dataset contains data on daily electric cycle rentals and related environmental and seasonal factors.  

**Key Features**:  
- **`datetime`**: Date and time of observation.  
- **`season`**: Season of the year (1: Spring, 2: Summer, 3: Fall, 4: Winter).  
- **`holiday`**: Whether the day is a holiday (0 = No, 1 = Yes).  
- **`workingday`**: Whether the day is a working day (0 = No, 1 = Yes).  
- **`weather`**: Weather conditions categorized as:  
  - 1: Clear, Few Clouds, Partly Cloudy  
  - 2: Mist, Cloudy, or Few Clouds  
  - 3: Light Snow or Rain  
  - 4: Heavy Rain or Snow  
- **`temp`**: Temperature in Celsius.  
- **`atemp`**: Perceived temperature in Celsius.  
- **`humidity`**: Humidity percentage.  
- **`windspeed`**: Wind speed.  
- **`casual`**: Count of casual (non-registered) users.  
- **`registered`**: Count of registered users.  
- **`count`**: Total rental bike count, including both casual and registered users.  

---

## Process Overview  

### 1. **Exploratory Data Analysis (EDA)**:  
- Visualized relationships between demand (`count`) and features like `season`, `weather`, `temp`, and `windspeed`.  
- Performed Bi-Variate Analysis to uncover trends and correlations.  

### 2. **Statistical Testing**:  
- **2-Sample t-Test**: Compared means of bike rentals across different groups (e.g., holidays vs. working days).  
- **ANOVA**: Assessed differences in bike demand across seasons.  
- **Chi-Square Test**: Evaluated relationships between categorical variables such as `weather` and `season`.  

### 3. **Key Observations**:  
- Seasonal variations significantly impact demand, with higher rentals observed in fall and summer.  
- Weather conditions have a noticeable effect, with clear weather driving higher demand.  
- Working days tend to see more registered users, while holidays attract more casual users.  

---

## Key Insights  

1. **Seasonality in Demand**:  
   - Rentals peak during favorable weather conditions (fall and summer seasons).  

2. **Weather Influence**:  
   - Clear weather positively correlates with increased bike rentals, while heavy rain or snow significantly reduces demand.  

3. **User Behavior**:  
   - Registered users contribute consistently higher rentals on working days, while casual users drive demand on holidays.  

---

## Tools and Libraries  
This project utilized the following tools:  
- **Python**:  
  - `Pandas` for data manipulation.  
  - `Matplotlib` and `Seaborn` for data visualization.  
  - `Scipy` and `Statsmodels` for statistical testing.  
- **Jupyter Notebook**: For interactive analysis and documentation.  

---

## Repository Structure  
- **`data/`**: Contains the dataset used for analysis.  
- **`notebooks/`**: Jupyter Notebooks documenting the analysis process.  
- **`visualizations/`**: Saved plots and charts.  
- **`README.md`**: Overview of the project (this file).  

---

## Next Steps  
Future work could include:  
1. **Feature Engineering**: Derive new features (e.g., lag variables or rolling averages) to enhance predictive insights.  
2. **Predictive Modeling**: Use machine learning models to forecast bike demand.  
3. **Deep Dive into User Segments**: Analyze behavioral patterns across casual and registered users for targeted marketing strategies.  

---

## Acknowledgments  
- **Dataset Source**: Provided by Scaler for this analysis.  
- **Python Libraries**: Thanks to the open-source Python community for providing versatile data analysis tools.  

---

## License  
This project is licensed for educational and non-commercial use only. If utilizing any part of this repository, please credit the author.  
