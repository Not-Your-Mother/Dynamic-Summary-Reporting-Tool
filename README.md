# Movie Recommendation System (SQL)

This project demonstrates how to build a real-time reporting layer on top of a transactional PostgreSQL database using stored procedures, triggers, and transformation logic. It uses the publicly available [DVD Rental database](https://neon.com/postgresql/postgresql-getting-started/postgresql-sample-database) provided by Neon Tech as its base schema.

## Project Overview

The DVD Rental database is normalized for transactional operations, making it less suitable for direct reporting. This project adds a dynamic summary table that recommends movies from new categories based on a customer’s rental history. The goal is to provide personalized suggestions by analyzing past genre preferences.

## Features

- Transformation logic to recommend movies based on past customer rental patterns
- Stored procedure to refresh the summary table on demand
- Trigger to automatically update the summary table on insert/update/delete
- Deployment-ready SQL script that builds all components

## Technologies Used

- PostgreSQL
- SQL
- Stored Procedures
- Triggers
- Database Design
- ETL (Extract, Transform, Load)

## Files

- `movie-recommendation-system.sql` – Full SQL script to deploy the recommendation system (tables, procedure, trigger)

## How to Run

1. **Set up the DVD Rental database**
   - Download and restore the base schema from [here](https://neon.com/postgresql/postgresql-getting-started/postgresql-sample-database).
   - Import it into your local PostgreSQL environment.

2. **Run the script**
   - Execute `movie-recommendation-system.sql` in your SQL client (e.g., pgAdmin, DBeaver).
   - This will create the summary table, stored procedure, and trigger.

3. **Verify results**
   - After inserting or updating rental activity, check the customer_summary table to view updated movie recommendations.
   - You can also manually call the `refresh_summary()` procedure if needed.

4. **Explore and adapt**
   - Extend the logic to other summary metrics.
   - Integrate into reporting dashboards or BI tools as needed.

## License

This project is for educational use and demonstration purposes only. Based on publicly shared schema from [Neon Tech's DVD Rental sample database](https://neon.com/postgresql/postgresql-getting-started/postgresql-sample-database).
