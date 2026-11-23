PROJECT TITLE 
customer-segmentation-analysis-using-machine-learning

BRIEF ONE LINE SUMMARY
An unsupervised Machine Learning project that segments customers into five distinct groups based on their annual income and spending scores to identify customer purchasing patterns and support data-driven marketing strategies.

OVERVIEW
Customer Segmentation is a Machine Learning project designed to group customers based on similarities in their purchasing behaviour.

The project uses the K-Means Clustering algorithm to divide customers into different groups based on two important attributes:

Annual Income

Spending Score

By identifying customer segments, businesses can better understand customer behaviour, identify high-value customers, and develop targeted marketing strategies.

The project uses the Mall Customers dataset and applies the Elbow Method to determine an appropriate number of clusters.

The final model identifies five customer segments and visualizes them using a scatter plot with their respective cluster centroids.

PROBLEM STATEMENT
Businesses often have customers with different income levels and spending behaviours. Treating all customers in the same way can result in ineffective marketing strategies and missed business opportunities.

The objective of this project is to apply Machine Learning clustering techniques to:

Analyze customer income and spending patterns.

Identify groups of customers with similar characteristics.

Segment customers into meaningful categories.

Discover potential high-value and low-engagement customer groups.

Support customer-targeted marketing and business decision-making.

The project aims to demonstrate how unsupervised Machine Learning can transform customer data into meaningful business insights.

DATASET
Dataset Name: Mall Customers Dataset

File Name: Mall_Customers.csv

Dataset Dimensions:

Total Records: 200

Total Columns: 5

Features Used for Clustering: 2

Dataset Attributes:

Column                         Description

CustomerID                     Unique identification number of each customer

Gender                         Gender of the customer

Age                            Age of the customer

Annual Income (k$)             Annual income in thousands of dollars

Spending Score (1-100)         Score assigned based on customer spending behaviour

Features Selected for Clustering:

Annual Income (k$)

Spending Score (1-100)

Data Quality Checks:

Examined the dataset structure and dimensions.

Checked column data types.

Reviewed sample customer records.

Checked for missing values.

No missing values were identified in the dataset.

TOOLS AND TECHNOLOGIES
Programming Language:

Python

Libraries:

NumPy – Numerical computations and array operations.

Pandas – Data loading, manipulation, and analysis.

Matplotlib – Data visualization and cluster plotting.

Seaborn – Statistical data visualization.

Scikit-learn – Machine Learning implementation.

Machine Learning Algorithm:

K-Means Clustering

Clustering Optimization Technique:

Elbow Method

Within-Cluster Sum of Squares (WCSS)

Development Environment:

Jupyter Notebook

METHODS AND IMPLEMENTATION
The project follows these implementation steps:

Step 1: Data Collection and Loading

Imported the Mall Customers dataset using Pandas and loaded it into a DataFrame for analysis.

Step 2: Data Exploration

Examined the first five records.

Checked the number of rows and columns.

Reviewed column information and data types.

Checked for missing values.

Step 3: Feature Selection

Selected two important customer attributes for clustering:

Annual Income (k$)

Spending Score (1-100)

These features were extracted using Pandas indexing and converted into a NumPy array.

Step 4: Determining the Optimal Number of Clusters

Applied the Elbow Method to determine a suitable number of clusters.

The K-Means algorithm was executed for cluster values ranging from 1 to 10.

For each iteration, the Within-Cluster Sum of Squares (WCSS) was calculated using the model's inertia value.

An Elbow Graph was plotted to visualize the relationship between the number of clusters and WCSS.

Step 5: Model Development

Implemented the K-Means Clustering algorithm using Scikit-learn.

Model configuration:

Number of Clusters: 5

Initialization Method: K-Means++

Random State: 0

Step 6: Customer Segmentation

Applied fit_predict() to train the clustering model and assign a cluster label to each customer.

Each customer was assigned to one of the five identified clusters.

Step 7: Cluster Visualization

Created a scatter plot using Matplotlib to visualize the five customer segments.

Different colors were used to distinguish the clusters, and the cluster centroids were highlighted separately.

KEY INSIGHTS
The project provides the following observations:

The dataset contains 200 customer records and five attributes.

Annual income and spending score were selected as the primary segmentation variables.

No missing values were identified in the dataset.

The Elbow Method was used to evaluate different cluster configurations.

Five customer segments were created using K-Means Clustering.

Customer groups can be visually distinguished based on income and spending behaviour.

Cluster centroids represent the central positions of the identified customer groups.

Business Interpretation:

The five customer segments can be interpreted in terms of their income and spending behaviour:

High-Income, High-Spending Customers – Potential premium and high-value customers.

High-Income, Low-Spending Customers – Potential customers for targeted engagement campaigns.

Low-Income, High-Spending Customers – Customers who demonstrate relatively high spending despite lower income.

Low-Income, Low-Spending Customers – Customers with relatively lower income and spending.

Average-Income, Average-Spending Customers – Customers with moderate income and spending behaviour.

These are general business interpretations of income-spending segments; the notebook does not calculate or assign these descriptive names to individual clusters.

DASHBOARD / MODEL / OUTPUT
Model: K-Means Clustering

The project currently implements a Machine Learning clustering model using Jupyter Notebook rather than an interactive dashboard.

Final Model Configuration:
Parameter                Value

Algorithm                K-Means Clustering

Number of Clusters       5

Initialization           K-Means++

Random State             0

Input Features           Annual Income, Spending Score

Total Customers          200

Output Generated:

The project generates two major visual outputs:

1. Elbow Method Graph

Displays the WCSS values for different numbers of clusters to help determine an appropriate cluster count.

2. Customer Segmentation Scatter Plot

Displays the five identified customer groups using different colors, along with their corresponding centroids.

Model Output:

Each customer receives a cluster label ranging from 0 to 4.

The resulting clusters can be used to understand customer purchasing patterns and develop targeted business strategies.

Note: K-Means is an unsupervised learning algorithm, so classification accuracy is not used as the primary evaluation metric.




HOW TO RUN THIS PROJECT?
Follow these steps to execute the project locally.

Prerequisites:

Python 3.x

Jupyter Notebook

Basic knowledge of Python and Machine Learning

Step 1: Clone the Repository
git clone <your-repository-url>

Step 2: Navigate to the Project Directory
cd <your-project-folder>

Step 3: Install Required Libraries
pip install numpy pandas matplotlib seaborn scikit-learn jupyter

Step 4: Add the Dataset
Place the Mall_Customers.csv file inside the project directory.
Update the dataset loading statement in the notebook:
customer_data = pd.read_csv("Mall_Customers.csv")

Step 5: Launch Jupyter Notebook
jupyter notebook

Step 6: Execute the Notebook

Open Customer Segmentation Project.ipynb and execute the cells sequentially.

The notebook will:

Load the customer dataset.

Perform data exploration.

Select relevant customer features.

Calculate WCSS values.

Generate the Elbow Graph.

Train the K-Means clustering model.

Assign customer cluster labels.

Visualize the five customer segments and their centroids.

RESULTS AND CONCLUSION
The project successfully demonstrates the application of unsupervised Machine Learning for customer segmentation using the K-Means Clustering algorithm.

The model divides 200 customer records into five distinct groups based on annual income and spending scores.

The Elbow Method was used to examine different cluster configurations, and the selected model was configured with five clusters.

The final visualization provides a clear representation of customer groups and their respective centroids.

Through this project, practical experience was gained in:

Data loading and preprocessing.

Exploratory Data Analysis.

Feature selection.

Unsupervised Machine Learning.

K-Means Clustering.

Elbow Method and WCSS.

Data visualization.

Business-oriented customer segmentation.

The project demonstrates how Machine Learning can help businesses understand customer behaviour and support data-driven marketing decisions.

FUTURE WORK
The project can be enhanced through the following improvements:

Advanced Exploratory Data Analysis: Include age-wise, gender-wise, and income-wise customer behaviour analysis.

Feature Scaling: Apply StandardScaler or MinMaxScaler and examine how scaling affects clustering results.

Algorithm Comparison: Experiment with Hierarchical Clustering and DBSCAN to compare segmentation approaches.

Cluster Evaluation: Use Silhouette Score, Davies-Bouldin Index, and Calinski-Harabasz Score to evaluate clustering quality.

Interactive Dashboard: Develop a customer segmentation dashboard using Power BI, Tableau, or Streamlit.

Customer Profiling: Generate detailed customer profiles based on income, spending patterns, and demographic characteristics.

Business Recommendations: Develop targeted marketing strategies for each customer segment.

Model Deployment: Build an interactive web application that allows users to input customer information and receive a predicted cluster assignment.

AUTHOR AND CONTACT
Author: Arhan
Project: Customer Segmentation Analysis Project Using Machine Learning
LinkedIn:www.linkedin.com/in/arhan-gogi-34aa992b9
Github: https://github.com/arhan7-ux
Email: arhangogi07@gmail.com
