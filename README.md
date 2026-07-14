# MetricMind
...
# MetricMind Project - Day 1 Plan

## What is this project?
MetricMind is a smart chat tool. A person can ask a question like "Why did sales drop in Europe?" and the tool gives a correct answer using real numbers, not fake AI guesses. It does this by using a "Semantic Layer" — a place where all business terms (like Revenue, Margin, Quarter) are defined clearly, so the numbers are always correct and consistent.

## Goal for Day 1
Today we only build the **foundation**. No AI code yet. We just prepare the data and the project structure.

---

## Step 1: Choose Simple Tools (Free, No Cloud Needed)
Instead of expensive tools like Snowflake, we use free tools that work on a normal laptop:
- **Database**: PostgreSQL or DuckDB (both are free)
- **Language**: Python (for generating data)

Later in your report, you can write: "This project is designed so it can scale to Snowflake or Databricks in production."

---

## Step 2: Create Fake Company Sales Data
We will create a fake dataset that looks like real company sales. It will have these columns:

| Column Name     | Meaning                                  |
|------------------|-------------------------------------------|
| order_id         | Unique ID for each order                  |
| date             | Date of the order                         |
| region           | Europe, Asia, or US                       |
| product_category | Type of product sold                      |
| revenue          | Money earned from the order               |
| material_cost    | Cost of raw material                      |
| shipping_cost    | Cost of shipping                          |
| quarter          | Q1, Q2, Q3, or Q4                         |

This data will be created using a Python script (given below in a separate file).

---

## Step 3: Load Data into Database
- Take the CSV file created by the script
- Load it into PostgreSQL or DuckDB as a table named `raw_sales`
- Run a simple query like `SELECT * FROM raw_sales LIMIT 10;` to check it worked

---

## Step 4: Create Project Folder Structure
Make folders like this on your computer:

```
metricmind/
├── data/           -> raw CSV files go here
├── dbt_project/    -> business logic models (we build this later)
├── cube_project/   -> semantic layer files (we build this later)
├── backend/        -> AI agent code (we build this later)
├── frontend/       -> chat interface code (we build this later)
└── README.md       -> project description
```

---

## Day 1 Checklist
- [ ] Install PostgreSQL or DuckDB
- [ ] Run the Python script to generate fake sales data
- [ ] Load the CSV into the database
- [ ] Run a test query to confirm data looks correct
- [ ] Create the folder structure above
- [ ] Create a GitHub repo for this project (looks good to show your company/teacher)

---

## Why This Matters
Every big project needs a strong base. Today's work (data + structure) is what tomorrow's AI agent and chat interface will be built on top of. Without good data, the whole project will not work properly later.
