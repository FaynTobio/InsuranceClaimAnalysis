📌 Project Overview

This project showcases a complete data engineering workflow using PostgreSQL, focusing on the design, creation, and analysis of insurance claim data.
It includes:

- Database schema design

- Realistic sample data

- Analytical SQL queries

- Performance optimization (indexing)

- Role-based access control

- Monthly trend analysis

This project is created to strengthen foundational SQL and data engineering skills.

🏗️ Database Schema (ERD)

Here is the relationship between all tables:

Customers ───< Policies >─── PolicyTypes
      │              
      └──────────< Claims


A customer can have multiple policies.
Each policy has a policy type.
Each policy can generate multiple claims.

🗃️ Tables Included
1. Customers

Stores customer demographic details.

2. PolicyTypes

Defines the type of insurance coverage (Auto, Home, Life, Health).

3. Policies

Links customers with their policy details.

4. Claims

Contains all insurance claims filed by customers.

🧪 Sample Data Inserted

- The project includes realistic scenarios such as:

- Different customer demographics

- Multiple policy types

- High-value and low-value claims

- Approved, denied, and pending claims

This makes the dataset suitable for analytics and performance testing.

📊 Analysis & Queries
🔹 1. Total Claims per Policy Type

Identifies which type of policy receives the most claims.

🔹 2. Monthly Claim Frequency & Average Amount

Uses:

- DATE_TRUNC()

- Aggregations

- Trend analysis

This helps to understand seasonal claim patterns.

🔹 3. Performance Optimization

Index added to speed up date-based queries:

CREATE INDEX idx_claims_claimdate ON Claims(ClaimDate);

🔐 Role-Based Access Control (RBAC)
Roles Created
Role	Access Level
ClaimsAnalyst	Read-only access to Claims, Policies, PolicyTypes
ClaimsManager	Full access: SELECT, INSERT, UPDATE, DELETE

This simulates real company data governance.

🛠️ Tech Stack

- PostgreSQL

- pgAdmin4

- SQL (DDL, DML, Joins, Indexing, RBAC)

🚀 How to Run This Project

1. Clone or download the repository

2. Open pgAdmin4

3. Create a new database

4. Run the SQL script in order:

  - Table creation

  - Insert statements

  - Analysis queries

  - Index creation

  - Role & permission setup

5. Explore output and modify queries as needed

📈 Future Enhancements

- Add triggers for automatic claim validation

- Build Python + Pandas analytics notebook

- Integrate Power BI dashboard

- Create ETL pipelines (Airflow or SSIS)

- Add stored procedures for automation

🙌 About

This is my first data engineering project, and I aim to continue building more SQL, ETL, and analytics projects to grow my skills.

If you find this useful or have suggestions for improvement — feel free to reach out!
