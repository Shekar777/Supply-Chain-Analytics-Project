🚀 Project Overview
It features a real-world supply chain analytics project combining Quadratic (an AI-powered spreadsheet) and n8n (an automation workflow tool) 
Goal: automate data ingestion → processing → analysis to solve supply chain issues.

🧩 Tech Stack & Flow
1. Automating Data Intake with n8n

n8n is set up to monitor incoming emails (specifically those labeled "Daily Sales") for CSV attachments.
It parses:
file_aggregate.csv (~57 rows)
file_order_line.csv (~109 rows) 

2. Data Storage in Supabase

Parsed data is loaded into a PostgreSQL database hosted on Supabase.
The project uses a star schema: fact tables (fact_aggregate, fact_order_line) + dimension tables (dim_product, dim_customer, dim_date, fact_summary) 

3. AI‑Driven Analytics with Quadratic

Quadratic connects directly to the Supabase DB.
Analysts use natural-language prompts inside Quadratic to:
Create date dimensions (dim_date)
Pull exchange rates (USD→INR) via Open Exchange Rates API
Build KPI tables and summaries n8n Docs

4. KPI Visualization & Reporting

The tool helps generate:
Total order lines
Line fill rate
Volume fill rate
Top 5 customers (global & India)
Python & SQL run interactively within the sheet 

🌟 Highlights & Benefits
Fully automated pipeline: from email to KPI with zero manual steps.
AI + code transparency: Quadratic offers editable, prompt‑driven analysis that’s reproducible 
Efficiency gain: what used to take hours daily is now done seamlessly—ideal for teams.
Collaboration-friendly: real-time workflows, database integration, and version history all supported 

📝 Additional Resources
The project includes downloadable materials:
n8n configuration guide
Supabase/PostgreSQL setup
Gmail OAuth instructions
Prompts and Quadratic exercises
Sample datasets
