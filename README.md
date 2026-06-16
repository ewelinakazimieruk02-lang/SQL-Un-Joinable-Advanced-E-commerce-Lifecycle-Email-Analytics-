# 🛒 Un-Joinable
SQL: E-commerce User & Email Analytics

# I. Introduction
This project delivers a clean, end-to-end analytical solution designed for a global e-commerce platform. Using Google BigQuery for data processing and Looker Studio for visualization, the main goal is to connect user registration trends with email marketing performance. It provides a clear view of how account setup choices affect customer behavior.

# II. Project Details
The project focuses on tracking user activity across different countries based on account verification, subscription status, and messaging intervals. To solve this, the SQL code uses  **Common Table Expressions (CTEs)** to break down the logic into clean, manageable steps. It successfully merges daily account creation numbers with key email metrics like sends, opens, and link clicks. The final output represents a unified dataset that feeds directly into an interactive dashboard, turning raw database rows into clear business insights.

# III. Challenges and Highlights
The biggest challenge was that account creations and email events happen at completely different times and frequencies. Using a traditional **JOIN** would have duplicated the data, inflating the marketing metrics. The standout feature of this project is avoiding this trap by using a **UNION ALL** approach with technical **NULL** placeholders to keep the data perfectly accurate. Additionally, to keep cloud compute costs low and ensure the **Looker Studio** report loads instantly, all heavy lifting - including ranking the **TOP 10** countries via **DENSE_RANK** window functions - is done directly inside BigQuery. This ensures stakeholders get a fast, honest report on their best-performing global markets.
