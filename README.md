# WRDS-Financial-Ananlysis
This project analyzes financial performance of public companies using Python, focusing on key metrics like ROE, ROA, and revenue growth. It includes data processing, industry comparison, and visualizations to support equity analysis and financial insights.

#Project Title:Financial Performance Analysis Using WRDS Data (Compustat-Based)

#1. Problem & User
This project aims to analyze and compare the financial performance of selected companies against their industry benchmarks.
It is designed for students, analysts, or researchers who want to conduct data-driven financial analysis using WRDS.

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
	•	Jupyter Notebook: WRDS_Financial_Analysis.ipynb

#7. Limitations & next steps
Limitations:
•	Companies in the same industry can be compared (restricted condition)
	•	Requires WRDS access (restricted database)
	•	Annual data only (limited frequency)
	•	Limited set of financial ratios

#8.Next Steps:
	•	Add quarterly data for higher granularity
	•	Include more financial metrics (e.g., margins, leverage ratios)
	•	Integrate machine learning for predictive analysis
	•	Build an interactive dashboard (e.g., using Plotly or Streamlit)
