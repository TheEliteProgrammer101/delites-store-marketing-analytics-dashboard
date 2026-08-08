# Delites Store Analytics Dashboard & Executive Report

An end-to-end marketing and customer sentiment analytics solution. This project extracts retail transactional and review data from SQL Server, engineers NLP sentiment features using Python, and builds an interactive Power BI dashboard to monitor store performance KPIs. 

**Bonus Feature:** Includes a professional PowerPoint presentation deck designed specifically for data-driven storytelling and stakeholder reporting.

## Dashboard Interface
*Add a screenshot of your dashboard here*

## Core Insights & Features Captured
*   **Conversion Optimization:** Monitors global conversion baselines (9.6% overall) alongside monthly progression peaks (hitting 17.3% in February).
*   **Social Funnel:** Breaks down customer action depth spanning 9M Views, 414K Likes, and 2M Clicks to evaluate content ROI.
*   **Customer Sentiment Engine:** Tracks a 3.7/10 average rating benchmark. Integrates Python NLP to bridge the gap between raw star ratings and unstructured textual review text.

## Technical Stack & Project Architecture
*   **Data Storage:** SQL Server (Relational DB)
*   **Data Engineering & NLP:** Python 3, Pandas, PyODBC, NLTK (VADER Lexicon)
*   **BI & Analytics Engine:** Power BI Desktop, DAX (Data Analysis Expressions)
*   **Executive Delivery:** Microsoft PowerPoint (Data Storytelling & Reporting)

## Advanced Data Pipeline (Python & SQL)
Rather than relying purely on static numbers, this project features an automated Python engineering layer to score unstructured review text:
1. **Extraction:** Queries `customer_reviews` directly from a local `SQLEXPRESS` environment using `pyodbc`.
2. **Sentiment Scoring:** Implements the `NLTK VADER` framework to calculate a normalized compound score (-1.0 to +1.0) for every review string.
3. **Multi-Dimensional Matrix:** Executes logic via an advanced mapping matrix matching mathematical sentiment against standard user ratings (e.g., separating true `Positive` marks from complex `Mixed Positive` / `Mixed Negative` records).
4. **Export Automation:** Generates a structured operational snapshot (`fact_customer_reviews_with_sentiment.csv`) ready for BI consumption.

## DAX & Data Architecture Layers
*   Designed a clean star-schema relational model connecting social metrics, product dimensions, and date tracking.
*   Authored targeted DAX logic to calculate interactive monthly conversion percentages, rolling metrics, and average product ratings across dynamic timeframes.

## Data Storytelling & Presentation Deck
To mimic a real-world enterprise workflow, this repository contains a structured presentation deck (`Delites_Store_Report.pptx`). It bypasses technical jargon to present findings directly to business end-users:
*   Translates complex dashboard interactions into high-level strategic summaries.
*   Highlights key performance trends, data anomalies, and low-performing product segments.
*   Provides clear, actionable business recommendations for marketing and product management teams.

## How to Run the Infrastructure
1. Run the Python ETL script to extract review records from your SQL server and generate the enriched sentiment dataset.
2. Open the `.pbix` dashboard file.
3. Use the global top slicers to dynamically filter marketing performance by Year (2023-2025) or individual Month blocks.
4. Review the `.pptx` file to see how data insights are structured for non-technical stakeholders.
