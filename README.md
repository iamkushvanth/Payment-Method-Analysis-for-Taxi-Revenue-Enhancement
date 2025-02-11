# Maximizing Revenue Using Hypothesis Testing

## Objective

The primary objective of this project is to conduct an A/B test to examine the relationship between the total fare and the method of payment. Utilizing Python for hypothesis testing and descriptive statistics, the aim is to derive insights that can assist taxi drivers in maximizing earnings. Specifically, the goal is to determine whether there exists a substantial disparity in fares between customers paying with credit cards versus those paying with cash.

## Insights Gained Through Analysis

- **Higher Average Trip Distance and Fare Amount for Card Payments**: Customers paying with cards tend to have a slightly higher average trip distance and fare amount compared to those paying with cash. This indicates that customers prefer to pay more with cards when they have high fare amounts and long trip distances.

- **Preference for Card Payments**: The proportion of customers paying with cards is significantly higher than those paying with cash, with card payments accounting for 67.5% of all transactions compared to cash payments at 32.5%. This indicates a strong preference among customers for using card payments over cash, potentially due to convenience, security, or incentives offered for card transactions.

- **Single-Passenger Rides Dominate Card Payments**: Among card payments, rides with a single passenger (`passenger_count = 1`) comprise the largest proportion, constituting 40.08% of all card transactions. Similarly, card payments are predominantly associated with single-passenger rides, making up 20.04% of all cash transactions.

- **Decrease in Transactions with Increased Passenger Count**: There is a noticeable decrease in the percentage of transactions as the passenger count increases, suggesting that larger groups are less likely to use taxis or may opt for alternative payment methods.



### Data Dictionary

Dataset Description

<img src="Pics\data_dictionary_trip_records_yellow_pages-to-jpg-0001.jpg">

### Problems Addressed

- Impact of payment methods on fare pricing.
- Patterns and trends in passenger behavior.
- Relationship between payment methods and revenue.

### Methodology

1. **Data Collection**: Imported and analyzed taxi trip data to investigate the impact of payment methods on fare pricing.
2. **Data Preprocessing**: Cleansed the dataset, handling missing values, removing duplicates, and filtering outliers for robust analysis.
3. **Exploratory Data Analysis**: Utilized visualization techniques to explore patterns and trends in passenger behavior and fare amounts.
4. **Statistical Analysis**: Conducted hypothesis testing to determine the relationship between payment methods and fare amounts.
5. **Insights Generation**: Extracted actionable insights to help taxi drivers optimize earnings by nudging customers towards specific payment methods.



### Distribution of Fare Amount and Trip Distance

We're interested on exploring the relationship between payment type and passenger behavior concerning trip distance and fare amount. Are there variations in the distribution of payment types concerning different fare amounts or trip distances?

To investigate this, I used plot histograms to visualize the distribution of passenger counts paying with either card or cash.

<img src="Pics\Distribution.png">


### Payment Type Preference

In order to examine the passenger's preference regarding their choice of payment method, we will assess the proportion of the two payment types. To provide a visual representation, I have opted to utilize a pie chart.


<img src="Pics\PieChart.png">


### Customer Analysis

Subsequently, we aim to conduct an analysis of the payment types in relation to the passenger count. Our objective is to investigate if there are any changes in preference contingent upon the number of passengers traveling in the cab.

To facilitate this examination, I have employed a visualization technique known as a stacked bar plot.

<img src="Pics\Cust_Analysis.png">

### Hypothesis Testing

In order to select the most suitable test for our scenario, our initial step involves evaluating whether the distribution of fare amounts adheres to a normal distribution. While the histogram depicted above suggests otherwise, we will further confirm this by generating a QQ plot.

Quantile-quantile (QQ) plots can be used to assess whether the fare amount distributions for each payment type are approximately normally distributed. If the data points closely align with the diagonal line in the plot, it suggests that the data follows a normal distribution.


<img src="Pics\Hypothesis Testing.png">

The data values clearly do not follow the red 45-degree line, which is an indication that they do not follow a normal distribution. So, z distribution will not be good for this. That's why we will use T test.

Given that the T-test can be applied to both small and large samples and does not require the population standard deviation, it is a more universally applicable approach for hypothesis testing in many practical research scenarios, including analyses of taxi trip data.

In the analysis of NYC Yellow Taxi Trip Records, where you're likely dealing with an unknown population standard deviation and potentially large datasets, the T-test offers a more appropriate and flexible method for comparing means between two groups (e.g., fare amounts by payment type). It provides a reliable way to infer about the population, accommodating the uncertainty that comes with estimating population parameters from sample data.

**Null hypothesis:** There is no difference in average fare between customers who use credit cards and customers who use cash.

**Alternative hypothesis:** There is a difference in average fare between customers who use credit cards and customers who use cash

## Recommendations

- **Encourage Card Payments**: Encourage customers to pay with credit cards to capitalize on the potential for generating more revenue for taxi cab drivers.
- **Incentivize Card Usage**: Implement strategies to incentivize customers to choose this payment method.
- **Enhance Payment Options**: Provide seamless and secure credit card payment options to enhance customer convenience and encourage adoption of this preferred payment option.

### Conclusion

The Payment Method Analysis project provides valuable insights into the relationship between payment methods and taxi revenue, empowering drivers to maximize earnings without compromising customer satisfaction.

### For Dataset

Dataset/DataFiles

```bash
https://drive.google.com/file/d/1RC8UPcwN9wZ2j589n6KS4Z7hW5Tq0hg5/view?usp=sharing
```
or 
```bash
https://www.kaggle.com/datasets/gauravpathak1789/yellow-tripdata-2020-01
```
