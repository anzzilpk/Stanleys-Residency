Stanley’s Residency Analytics Pipeline
Project Overview
This project implements an end-to-end ETL and analytics pipeline for hospitality booking data from Stanley’s Residency. The pipeline automates data ingestion, cleaning, transformation, and loading into a structured database, while powering interactive dashboards in Tableau Public. The dashboard highlights key performance indicators and visualizations that support business decision-making. Advanced analytics modules extend the project with recommendations, customer lifetime value estimation, and fraud detection.

Workflow
- Extract
- Source booking data from CSV files.
- Automated ingestion using Python (pandas).
- Transform
- Clean column names, handle missing values, validate business logic.
- Feature engineering: cash_collected, stay_duration, booking_lead_time.
- Anonymize sensitive fields (addresses, phone numbers).
- Load
- Store cleaned data into MySQL using SQLAlchemy.
- Export CSV for Tableau Public dashboards.
- Visualize
- Interactive Tableau Public dashboard includes:
- Key Metrics:
- Total Amount: 1,795,122
- Cash Collected: 1,561,708
- Number of Customers: 201
- Sales by Month: Line chart showing monthly sales trends (July–December).
- Sales by Room: Bar chart comparing revenue across rooms, with averages highlighted.
- Advanced Extensions
- Recommendation System: Suggest rooms/packages based on customer history.
- Customer Lifetime Value (CLV): Estimate long-term revenue from repeat customers.
- Fraud Detection: Spot anomalies in invoice numbers or payments using Isolation Forest.

Tech Stack
- Python: pandas, NumPy, scikit-learn, SQLAlchemy
- Database: MySQL
- Visualization: Tableau Public
- Automation: Windows Task Scheduler
- Data Privacy: Anonymization of sensitive fields

How to Run
- Clone this repository.
- Install dependencies:
pip install pandas numpy scikit-learn sqlalchemy pymysql
- Run the ETL pipeline:
python etl_pipeline.py
- Connect Tableau Public to the generated etl_output.csv.
- Refresh dashboards to view updated analytics.

Dashboard Preview
The Tableau Public dashboard provides:
- KPIs for total revenue, cash collected, and customer count.
- Monthly sales trends with peaks and declines.
- Room-level sales analysis with averages for comparison.

Future Enhancements
- Deploy pipeline with Airflow or Prefect for cloud scheduling.
- Migrate dashboards to Tableau Server for live database connections.
- Expand fraud detection with deep learning anomaly models.
