# Sales-Data-Analysis
Sales Data Analysis using PySpark

## 🚀 Project Overview

This project provides an end-to-end data analysis of the Adidas sales dataset. The primary objective is to process and analyze sales data to uncover key business insights and performance metrics. By leveraging the power of PySpark and Spark SQL for big data processing, the project calculates crucial KPIs like total sales, operating profit, and units sold. These metrics are then broken down by various dimensions—including region, state, product, and sales method—to identify trends and support strategic business decision-making. The final analysis is presented through a series of visualizations created with Matplotlib and Seaborn.

## 🛠️ Technologies & Tools Used
* **Language:** `Python`
* **Core Libraries:** `PySpark`, `Spark SQL`, `Pandas`
* **Visualization:** `Matplotlib`, `Seaborn`
* **Environment:** `Jupyter Notebook` (local Spark session)

## 🔧 How to Run This Project

1.  **Prerequisites:** Ensure you have a local Spark environment set up and the required Python libraries installed:
    ```bash
    pip install pyspark pandas matplotlib seaborn jupyterlab
    ```

2.  **Get the Data:** Place the `sales.csv` file in the same directory as the notebook.

3.  **Run the Notebook:** Launch Jupyter and run the cells in the `Sales.ipynb` notebook sequentially.


## 📋 Project Pipeline

The project follows a standard data analysis workflow:

1.  **Environment Setup:** Initializes a local `SparkSession` to enable distributed data processing.
2.  **Data Loading:** Ingests the `sales.csv` dataset into a Spark DataFrame.
3.  **Data Cleaning & Preparation:**
    * Removes commas from numeric columns (`Total Sales`, `Operating Profit`, `Units Sold`).
    * Casts columns to their correct data types (e.g., `double`, `date`).
    * Renames columns to be compatible with SQL queries (e.g., 'Total Sales' to `Total_Sales`).
4.  **Data Analysis:** Creates a temporary SQL view named `sales_analysis` and executes a series of Spark SQL queries to aggregate data and calculate business metrics.
5.  **Visualization:** Converts the aggregated Spark DataFrames into Pandas DataFrames to create static visualizations that clearly present the findings.
