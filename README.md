# EDA-on-Zomato-Restaurant-Dataset

## Project Overview

This project involves an exploratory data analysis (EDA) of the Zomato restaurant dataset. The goal is to uncover insights into restaurant trends, customer ratings, country-wise distribution of Zomato's presence, and online delivery availability.

## Dataset

The analysis uses two datasets:
1. `zomato.csv`: Contains detailed information about restaurants, including their ID, name, city, address, cuisines, average cost for two, currency, ratings, and more.
2. `Country-Code.xlsx`: Provides a mapping between country codes and country names, which is merged with the main Zomato dataset for better readability and country-specific analysis.

## Analysis Highlights

### 1. Missing Values
- Identified that the `Cuisines` column has 9 missing values.
- Visualized missing data using a heatmap to confirm no other significant missing data patterns.

### 2. Country Distribution
- Performed a merge operation between `zomato.csv` and `Country-Code.xlsx` using `Country Code` to enrich the dataset with country names.
- Generated a pie chart illustrating the top 3 countries with the most Zomato restaurant listings:
    - **India**: Accounts for a dominant percentage of the records.
    - **United States**
    - **United Kingdom**
- **Observation**: Zomato has a maximum presence in India, followed by the United States and the United Kingdom.

### 3. Rating Analysis
- Grouped data by `Aggregate rating`, `Rating color`, and `Rating text` to understand rating distribution.
- **Observations on Ratings:**
    - Ratings between 4.5 to 4.9 are categorized as 'Excellent' (Dark Green).
    - Ratings between 4.0 to 3.4 are categorized as 'Very Good' (Green).
    - Ratings between 3.5 to 3.9 are categorized as 'Good' (Yellow).
    - Ratings between 3.0 to 3.4 are categorized as 'Average' (Orange).
    - Ratings between 2.5 to 2.9 are categorized as 'Average' (Orange).
    - Ratings between 2.0 to 2.4 are categorized as 'Poor' (Red).
- Visualized rating distribution using bar plots, showing:
    - A significant number of restaurants have 'Not Rated' (0.0) ratings.
    - The majority of ratings fall between 2.5 and 3.4.

### 4. Countries with 0 Ratings
- Identified countries where restaurants received a 0.0 rating (White color).
- **Observation**: India accounts for the overwhelming majority of 'Not rated' restaurants (2139 out of 2148 total). This suggests a large number of entries in India have not yet received ratings.

### 5. Currency Usage by Country
- Mapped each country to its respective currency used in the dataset.
- **Examples:**
    - India: Indian Rupees(Rs.)
    - United States: Dollar($)
    - United Kingdom: Pounds(£)

### 6. Online Delivery Options
- Investigated which countries offer online delivery services.
- **Observation**: Online deliveries are primarily available in India and UAE according to this dataset.

### 7. City Distribution
- Explored the distribution of Zomato restaurants across different cities.
- Generated a pie chart for the top 5 cities with the most restaurant listings:
    - **New Delhi**: Dominated the city distribution.
    - **Gurgaon**
    - **Noida**
    - **Faridabad**
    - **Ghaziabad**

## Tools and Libraries

- **Python**
- **Pandas**: For data manipulation and analysis.
- **Numpy**: For numerical operations.
- **Matplotlib**: For basic plotting and customizations.
- **Seaborn**: For enhanced data visualizations.

## How to Use

1.  **Clone the repository:**
    ```bash
    git clone <repository_url>
    ```
2.  **Install dependencies:**
    ```bash
    pip install pandas numpy matplotlib seaborn openpyxl
    ```
3.  **Run the Jupyter Notebook/Colab Notebook:**
    Open `Zomato_EDA.ipynb` (or your notebook file) in a Jupyter environment or Google Colab to reproduce the analysis.

## Future Enhancements

- Deeper dive into cuisine preferences by country.
- Predictive modeling for restaurant ratings based on features.
- Advanced geospatial analysis of restaurant locations.
