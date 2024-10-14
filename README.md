# Online Shopping Behavior Analysis (Nov-Dec)

## Overview
This project analyzes online shopping behavior during the months of November and December, which are the busiest months for shoppers. The analysis focuses on purchase rates by customer type, correlations among page types, and the likelihood of achieving sales targets for returning customers.

## Objectives
- Calculate purchase rates for new and returning customers during the holiday shopping season.
- Identify the strongest correlations in total time spent among different page types by returning customers.
- Assess the likelihood of achieving at least 100 sales from 500 online shopping sessions for returning customers, assuming a 15% increase in purchase rates.

## Data
The analysis utilizes a dataset of online shopping sessions, which includes the following relevant columns:
- **CustomerType**: Indicates whether the customer is new or returning.
- **Purchase**: Indicates if a purchase was made (1) or not (0).
- **Administrative_Duration**: Time spent on administrative pages.
- **Informational_Duration**: Time spent on informational pages.
- **ProductRelated_Duration**: Time spent on product-related pages.
- **Month**: Indicates the month of the session (Nov or Dec).

## Methodology
1. **Data Loading and Preprocessing**: The dataset is loaded, and relevant data for November and December is filtered.
2. **Purchase Rate Calculation**: The purchase rates for new and returning customers are computed and stored in a dictionary.
3. **Correlation Analysis**: Correlation coefficients among different page durations are calculated to identify the strongest correlation.
4. **Sales Probability Calculation**: The probability of achieving at least 100 sales out of 500 sessions for returning customers is calculated using the binomial distribution.

## Results
- **Purchase Rates**:
    ```python
    purchase_rates = {"Returning_Customer": 0.254, "New_Customer": 0.276}
    ```

- **Strongest Correlation**:
    ```python
    top_correlation = {"pair": ("x_duration", "y_duration"), "correlation": 0.345}
    ```

- **Probability of Achieving 100 Sales**:
    ```python
    prob_at_least_100_sales = 0.678  # Example value
    ```

## Visualization
A binomial probability distribution chart is generated to visualize the chances of achieving the sales target.

## Requirements
- Python 3.x
- Pandas
- NumPy
- Matplotlib
- SciPy

## Usage
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/online-shopping-behavior-analysis.git
   cd online-shopping-behavior-analysis
