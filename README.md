# Borrower Demographics Analysis Dashboard

Data Source used - https://www.kaggle.com/datasets/janiobachmann/bank-marketing-dataset

## Inspiration to use the Dataset

This Dataset was originally uploaded to the **UC Irvine Machine Learning Repository**. The data is related with direct marketing campaigns (phone calls) of a Portuguese banking institution. The classification goal is to predict if the client will subscribe a term deposit.
In order to find the best strategies to improve for the next marketing campaign. How can the financial institution have a greater effectiveness for future marketing campaigns? In order to answer this, we have to analyze the last marketing campaign the bank performed and identify the patterns that will help us find conclusions in order to develop future strategies. 

## Creation of the Dashboard

- Dependencies: The code imports Streamlit, NumPy, Pandas, time, and Plotly Express.
- Data Loading: The code reads a CSV file from a GitHub repository and loads it into a Pandas DataFrame (`df`).
- Dashboard Configuration: The Streamlit dashboard is configured with a specific page title, icon, and layout.
- Dashboard Title: The dashboard title is set as "Real-Time / Live Data Science Dashboard".
- Top-level Filters: Users can select a job filter using a dropdown select box based on the "job" column in the dataset.
- Single-element Container: A container is created to display real-time data updates.
- DataFrame Filtering: The DataFrame `df` is filtered based on the selected job filter.
- Near Real-time Data Simulation: A loop simulates real-time data updates. It generates new columns `age_new` and `balance_new` in `df` by multiplying random values with the existing "age" and "balance" columns.
- Key Performance Indicators (KPIs): KPIs such as average age, count of married individuals, and average account balance are calculated based on the modified DataFrame.
- KPI Display: KPIs are displayed in a three-column layout using the `st.metric` function, showing labels, values, and deltas.
- Chart Display: Two columns are created for displaying charts. The first is a density heatmap, and the second is a histogram.
- Detailed Data View: The filtered DataFrame is displayed in a table format.
- Real-time Simulation: A delay of 1 second is introduced between iterations to simulate real-time updates.
- Loop Termination: The loop runs for 200 iterations before terminating.

This code allows users to interact with a Streamlit dashboard to analyze marketing campaign data in real-time.

## Insights from the datasets

1. Customers with secondary education are less likely to subscribe for term deposit.
2. Customers with 'blue-collar' and 'services' jobs are less likely to subscribe for term deposit.
3. Married Customers are less likely to subscribe for term deposit.
4. Customers with 'cellular' type of contact are less likely to subscribe for term deposit.
5. Customers with unknown poutcome are less likely to subscribe for term deposit.
6. People who subscribed for term deposit tend to have greater balance and age values.
7. People who subscribed for term deposit tend to have fewer number of contacts during this campaign
