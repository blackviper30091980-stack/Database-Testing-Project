ID: DB - 01

TITLE: [DB] NULL value inserted into first_name column in 'students' table.

SEVERITY: Major

PRIORITY: High

PRECONDITIONS:

- Database exists.

- students table exists.

- first_name column has NOT NULL constraints.

- Database connection is active.

STEPS TO REPRODUCE:

1.Open the database.

2.Execute an INSERT statement with first_name = NULL.

3.Execute a SELECT query to check whether the record was inserted.

EXPECTED RESULT:

- The database rejects the INSERT operation.

- A NOT NULL constraints failed error is returned.

- No record with student_id is created.

SIMULATED ACTUAL RESULT:

- The database accepts the INSERT operation and creates the record with NULL fist_name in the 'students'table.

- No error message is returned.

VERSION/ENV: SQLite3 Database version 3.52.3; DBeaver 26.1.1; Script-4.sql; 


ID: DB - 02

TITLE: Database accepts INSERT with duplicate PRIMARY KEY student_id in 'students'table.

SEVERITY: Critical

PRIORITY: High

Preconditions:

- student_id is defined as a primary key;

- a student with student_id = 1 already exists.

STEPS TO REPRODUCE:

1.Verify that student_id = 1 already exists.

2.Execute the INSERT statement using the same student_id.

3.Query the table.

EXPECTED RESULT:

- The database rejects the INSERT.

- A UNIQUE constraints primary key constraint error is returned.

- No duplicate student_id is created.

SIMULATED ACTUAL RESULT:

-  Database accepts INSERT with duplicate PRIMARY KEY student_id in 'students'table.

-  Duplicate student_id is created.

-  NO UNIQUE constraints primary key constraint error is returned.

VERSION/ENV: SQLite3 Database version 3.52.3; DBeaver 26.1.1; Script-4.sql; 


ID: DB - 03

SEVERITY: Critical

PRIORITY: High

TITLE: Database accepts INNER JOIN query with non-existing table.

PRECONDITIONS:

- students and courses tables exist.
- The tables have the expected columns.
- Database connection is active.


