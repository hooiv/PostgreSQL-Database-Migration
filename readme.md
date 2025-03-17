Process Overview:
RDS Setup: Created a PostgreSQL instance on AWS RDS with a retail dataset.
Self-Hosted Setup: Installed PostgreSQL locally and configured a database.
Migration: Used pg_dump to export from RDS and psql to import into the local instance.
Optimization: Added indexes and tuned queries for performance.
Challenges and Solutions:
Challenge: RDS connection refused.
Solution: Updated the security group to allow port 5432 from my IP.
Challenge: Slow query performance on transactions.
Solution: Added an index on transaction_date.
Performance Improvements:
Example metric:
Before Indexing: Query SELECT * FROM transactions WHERE transaction_date = '2023-01-01' took 500ms.
After Indexing: Reduced to 50ms (90% improvement).
