ID: DB - 01

TITLE: [DB] NULL value inserted into first_name column in 'students' table.

SEVERITY: Major

PRIORITY: High

PRECONDITIONS:

-Database exists.

-students table exists.

-first_name column has NOT NULL constraints.

-Database connection is active.

STEPS TO REPRODUCE:

1.Open the database.

2.Execute an INSERT statement with first_name = NULL.

3.Execute a SELECT query to check whether the record was inserted.

EXPECTED RESULT:

-The database rejects the INSERT operation.
-A NOT NULL constraints failed error is returned.
-No record with student_id is created.

SIMULATED ACTUAL RESULT:

- The database accepts the INSERT operation and creates the record with NULL fist_name in the 'students'table.

- No error message is returned.

VERSION/ENV: SQLite3 Database version 3.52.3; DBeaver 26.1.1; Script-4.sql; 





