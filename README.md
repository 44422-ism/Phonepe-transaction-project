# Phonepe-transaction-project
The PhonePe Transaction Insights project is an end-to-end data analysis initiative developed using real public fintech data provided by the PhonePe Pulse GitHub repository. The core objective of this project is to extract, transform, and analyze large-scale digital payment data to generate business insights and visualize trends.
The project follows a structured Exploratory Data Analysis (EDA) approach, where no predictive modeling is involved. Instead, the focus is on uncovering patterns, trends, and anomalies in the dataset. The data consists of quarterly transaction details spanning from 2018 to 2023, including user activity, transaction types, regional usage, and device brand penetration.

To handle this rich dataset, a complete data pipeline was built using Python and SQLite within a Google Colab environment. The process began by cloning the official PhonePe Pulse GitHub repository. The JSON-based data was categorized into three types: aggregated data (state-level), map data (district-level), and top data (pincode-level). These were further divided into three domains: transactions, users, and insurance.

A custom ETL (Extract, Transform, Load) pipeline was written in Python to iterate through nested directories, parse JSON files, and insert cleaned data into structured SQL tables. The database schema was designed with scalability in mind and included nine primary tables: aggregated_transaction, aggregated_user, aggregated_insurance, map_user, map_map, map_insurance, top_user, top_map, and top_insurance.

Once the database was populated, several SQL queries were written to perform descriptive analytics. Key insights were extracted such as:

Top 10 states by transaction volume
Top 10 pincodes by transaction amount
Most commonly used device brands across regions
Total registered users per state
Quarter-over-quarter transaction growth across India
These results were visualized using Matplotlib and Plotly Express to create bar charts, pie charts, and interactive line graphs. One of the highlights of the analysis was a timeline chart that showed consistent and exponential growth in digital transactions across all regions, particularly post-2020. Device brand usage analysis revealed that Xiaomi, Samsung, and Vivo lead in terms of user base.

In addition, SQL views were created to abstract common queries and improve performance. These views included view_transaction_growth, view_top_pincodes, and view_top_brands, enabling faster dashboard integration. The project was designed to be dashboard-ready, and a Streamlit application script was also developed to support filtering by year, quarter, state, and transaction type. The dashboard could be deployed to enable decision-makers to interact with insights in real-time. This project does not involve machine learning or classification. It remains an EDA and Business Intelligence (BI) initiative. However, it lays the foundation for future enhancements, such as regression forecasting of transaction volume, clustering of user behavior patterns, or anomaly detection in district-level growth.

In conclusion, the PhonePe Transaction Insights project demonstrates a complete pipeline — from raw public data to clean structured storage, to SQL-based querying and business insight visualization. It showcases essential skills in data engineering, SQL schema design, and analytical storytelling, making it an ideal reference project in the fintech analytics space.
