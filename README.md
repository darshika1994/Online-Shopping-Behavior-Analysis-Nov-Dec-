# Customer Behavior Analysis: Online Shopping Behavior Analysis (Nov-Dec)

## Project Overview

Using statistics and probability techniques, this project aims to identify differences between customers' browsing habits and shopping patterns during November and December, the busiest months for online shoppers. These insights will help the marketing team understand customer engagement on the website and optimize future campaigns.

### Key Objectives:
1. **Calculate Purchase Rates**: Analyze and compare purchase rates for both returning and new customers.
2. **Identify Strongest Correlation**: Determine the strongest correlation in time spent among page types for returning customers.
3. **Campaign Impact**: Estimate the likelihood of achieving at least 100 sales out of 500 online shopping sessions for returning customers, given a 15% boost in the purchase rate.

## Methodology

### 1. Purchase Rates Calculation:
- The purchase rates for **Returning** and **New Customers** during November and December are calculated by measuring the proportion of sessions resulting in a purchase.
- This gives the marketing team insights into how different customer types engage during peak shopping months.

### 2. Strongest Correlation:
- For returning customers, the total time spent on different page types (e.g., **Administrative**, **Informational**, and **Product-related** pages) is examined.
- The **strongest correlation** between time spent on these pages is identified to understand how customer attention is distributed across various activities.

### 3. Campaign Impact (Sales Probability):
- A hypothetical **15% boost** in the purchase rate for returning customers is introduced.
- The **likelihood of achieving at least 100 sales out of 500 sessions** is calculated using a **binomial distribution**. This helps forecast the potential outcomes of a new marketing campaign.

## Hypothesis Testing

### **Purchase Rates Hypothesis**:

**Hypothesis**: Returning customers have a higher purchase rate than new customers during November and December.

- **Null Hypothesis (H₀)**: The purchase rate of returning customers is **equal to or less** than that of new customers.
- **Alternative Hypothesis (H₁)**: The purchase rate of returning customers is **higher** than that of new customers.

This hypothesis can be tested using a **proportion test** to compare the purchase rates between the two customer types. If the null hypothesis is rejected, it confirms that returning customers engage more during the busiest shopping months.

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

### Key Question:
- **Do returning customers have a higher purchase rate than new customers?**

## Results
- **Purchase Rates**:
    ```python
    purchase_rates = {"Returning_Customer": 0.195, "New_Customer": 0.273}
    ```

- **Strongest Correlation**:
    ```python
    top_correlation = {'pair': ('Administrative_Duration', 'ProductRelated_Duration'), 'correlation': 0.3898546003206963}
    ```

- **Probability of Achieving 100 Sales**:
    ```python
    prob_at_least_100_sales = 0.901 
    ```

## Visualization
A binomial probability distribution chart is generated to visualize the chances of achieving the sales target.

## Conclusion

Through this analysis, the marketing team can gain insights into the behavior of online shoppers in November and December, enabling them to make data-driven decisions about future campaigns and customer engagement strategies. The project also provides a strong foundation for understanding customer preferences based on their browsing patterns, helping to identify opportunities for increasing conversions.

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
