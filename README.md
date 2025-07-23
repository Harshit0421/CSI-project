🎯 Celebal_Final_Project
🌐 Azure Data Factory Project: Intelligent Data Orchestration (Extended Tasks)
This extended version of the project expands the intelligent data orchestration pipeline using Azure Data Factory, SQL Server, REST API, and Azure Data Lake Storage Gen2 (ADLS). These additions demonstrate complex automation tasks like conditional logic, threshold-based execution, dynamic folder creation, and data joins using multiple data sources.

🚀 Features Overview (Additional Tasks)
✅ Task 1: Threshold-Based Conditional Data Copy
A file with a threshold value is created and stored in ADLS.

The pipeline reads this file and compares the record count in the Customer table.

If the count exceeds the threshold, it copies customer data from SQL DB to ADLS in JSON format.

The output is stored in dynamic folders like Customer/Year/Month/Day to avoid overwriting.

✅ Task 2: Pipeline Name - Foreach_Example2
A single Copy Activity using ForEach loop copies two datasets:

Product table data where ProductID > 100

Customer table data where CustomerID > 100 and < 1000

The pipeline optimizes looping through table configurations dynamically using parameters.

✅ Task 3: Join SQL Table & CSV File → Save as Parquet
Reads:

Customer table data from SQL

CustomerAddress data from a CSV file

Joins both datasets on CustomerID

Filters the records where CustomerID > 1000 and < 2000, sorts them in ascending order, and stores the output in Parquet format in ADLS.
