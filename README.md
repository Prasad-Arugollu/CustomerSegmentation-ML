# Customer Segmentation Using KMeans Clustering

## Project Overview
This project segments customers of a retail store using KMeans clustering based on key features such as Age, Annual Income, and Spending Score. Customer segmentation enables better targeted marketing efforts, personalized offers, and improved customer experience.

## Dataset
The dataset contains 200 customers with the following attributes:
- **CustomerID**: Unique identifier
- **Gender**: Male or Female
- **Age**: Age of the customer in years
- **Annual Income (k$)**: Annual income in thousands of dollars
- **Spending Score (1-100)**: A score assigned based on customer's spending behavior

## Exploratory Data Analysis (EDA)
- Visualization of demographic data (gender distribution, age groups)
- Analysis of spending scores and income distributions
- Relationships between age, income, and spending patterns

## Clustering Methodology
- Utilized **KMeans clustering** algorithm from scikit-learn
- Selected features: Age and Spending Score (additional analyses on Income as well)
- Used the Elbow Method to determine the optimal number of clusters (WCSS vs cluster count)
- Visualized the resulting clusters with cluster centroids for intuitive understanding

## Technologies Used
- Python 3.x
- Pandas for data manipulation
- Matplotlib and Seaborn for data visualization
- Scikit-learn for machine learning models

## How to Run
1. Clone this repository:
```bash
git clone https://github.com/Prasad-Arugollu/AI-Powered-Resume-Analyzer.git
cd AI-Powered-Resume-Analyzer
```
