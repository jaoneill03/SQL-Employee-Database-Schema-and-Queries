# SQL Employee Database

An Oracle SQL project that designs and queries a relational employee
database. Includes a full schema with six related tables, sample data,
and a set of queries demonstrating a range of SQL concepts.

## How to run

This project was written for Oracle SQL. To run it:

1. Open Oracle SQL Developer or SQL*Plus
2. Run the full script to create tables, insert data, and execute queries:
```bash
@employee_database.sql
```

## Database schema

The database models a company with employees, departments, projects,
and dependents across six related tables:

- **employee** — stores employee info including supervisor and department
  references. Uses a self-referencing foreign key for the supervisor relationship.
- **department** — stores department names and their managers
- **dept_locations** — stores multiple locations per department
- **project** — stores projects linked to their controlling department
- **works_on** — junction table tracking which employees work on which
  projects and for how many hours
- **dependent** — stores family dependents for each employee

## Queries demonstrated

The script includes 13 queries covering a range of SQL concepts:

- `GROUP BY` and `COUNT` to count projects per department
- `LIKE` pattern matching to filter by city, name patterns, and character position
- `HAVING` to filter aggregated groups
- `MAX`, `MIN`, `AVG` with `ROUND` for salary statistics per department
- Multi-table joins across two and three tables
- `NATURAL JOIN` between department and dept_locations
- `UPDATE` to modify existing records
- `ALTER TABLE` to add a new column to an existing table

## Files

- `employee_database.sql` — full schema, sample data, and all queries

## Technologies
- Oracle SQL
- DDL (CREATE, ALTER, DROP)
- DML (INSERT, UPDATE, SELECT)
- Aggregate functions
- Multi-table joins
