# WRDS-Financial-Ananlysis
This project analyzes financial performance of public companies using Python, focusing on key metrics like ROE, ROA, and revenue growth. It includes data processing, industry comparison, and visualizations to support equity analysis and financial insights.

#Project Title:Financial Performance Analysis Using WRDS Data (Compustat-Based)

#1. Problem & User

The objective of this project is to develop a data-driven framework to evaluate the financial performance of selected publicly listed companies and compare them with their industry peers. The analysis focuses on profitability, efficiency, and growth to provide a multi-dimensional assessment.

The intended audience includes finance students and junior analysts who are interested in applying Python to real-world financial datasets and who are willing to use the data to better help with their investment decisions.

#2. Data
	Source: WRDS (Compustat Fundamentals Annual - comp.funda)
	
	Access Date: April 2026
	Key Fields:
		at (Total Assets)
		sale (Revenue)
		ni (Net Income)
		ceq (Common Equity)
		datadate (Report Date)
		gvkey, tic (Company identifiers)

#3. Methods (main Python steps)

The project follows a structured data pipeline:

	1.	Data Access
	•	Connect to WRDS database using Python (wrds package)
	2.	Data Extraction
	•	Retrieve firm-level financial data from Compustat
	•	Identify relevant industry classification
	3.	Data Cleaning
	•	Handle missing values
	•	Remove duplicates
	•	Filter invalid financial records (e.g., negative assets)
	4.	Feature Engineering
	•	Calculate financial ratios:
	•	ROA (Return on Assets)
	•	ROE (Return on Equity)
	5.	Aggregation & Comparison
	•	Compare company-level metrics with industry averages
	6.	Visualization
	•	Line charts (trend analysis)
	•	Scatter plots (ROA vs ROE)
	•	Bar charts (comparisons)
	•	Box plots (distribution analysis)

#4. Key Findings

	•	Company performance varies significantly across time and relative to industry benchmarks
	•	ROA and ROE provide complementary insights into profitability and efficiency
	•	Some firms consistently outperform industry averages, indicating competitive advantage
	•	Data cleaning is critical, as raw financial data contains missing and inconsistent values
	•	Visualization helps identify trends and outliers more effectively than raw tables

#5. How to run

	1.Install required packages: 
		code: python code:pip install pandas numpy matplotlib wrds
	2.	Set up WRDS credentials
	3.	Run the Jupyter Notebook:  JiayiQiu24_Financial_Analysis.ipynb
	4.	Input:
		•	Company tickers (e.g. NKE, LULU, UAA)
		•	Industry name (e.g. Sportswear & Apparel)
		•	Time range (e.g. start_date: 2005-11-26  end_date: 2025-11-26 )

#6. Product link

	•	Jupyter Notebook: JiayiQiu24_Financial_Analysis.ipynb

#7. Limitations & next steps

Limitations:

	•	Companies in the same industry can be compared (restricted condition)
	•	Requires WRDS access (restricted database)
	•	Annual data only (limited frequency)
	•	Limited set of financial ratios

Next Steps:

	•	Add quarterly data for higher granularity
	•	Include more financial metrics (e.g., margins, leverage ratios)
	•	Integrate machine learning for predictive analysis
	•	Build an interactive dashboard (e.g., using Plotly or Streamlit)
