TC-DB-01 Insert student with NULL first_name

MOdule: Students table/ NOT NULL constraints

Precoditions:
- Database exists.
- students table exists.
- first_name column has NOT NULL constraints.
- Database connection is active.

Test Data:
- student_id;
- first_name;
- last_name;
- country;
- course_id.

Steps:
1. Open the database.
2. Execute an INSERT statement with first_name = NULL.
3. Execute a SELECT query to check whether the record was inserted.

Expected Result:
- The database rejects the INSERT operation.
- A NOT NULL constraints failed error is returned.
- No record with student_id is created.

Test Type: Negative/Database Testing

Test Design Technique: Equivalence Partitioning


TC-DB-02 Insert course with NUll duration

Module: Courses table/ NOT NULL constraints

Preconditions:
- courses table exists;
- duration has NOT NULL constraints.

Test Data:
- course_id;
- course_name;
- duration.

Steps:

1.Execute an INSERT statement with valid course_name;

2.Execute an INSERT statement with duration = NULL.

Expected Result:

- The database rejects the INSERT statement.
 
- A NOT NULL constraints violation error is returned.
 
- A course is not added to the courses table.

Test Type: Negative/Database Testing

Test Design Technique: Equivalence Partitioning


TC-DB-03 Insert duplicate student_id

Module: Students table/Primary Key

Preconditions:
- student_id is defined as a primary key;
- a student with student_id = 1 already exists.

Test Data:

 Existing student_id: 1;
 
 New Record:
 - student_id : 1;
 - first_name : Tom;
 - last_name : Brown;
 - country : Canada;
 - course_id : 2.

Steps: 
1. Verify that student_id = 1 already exists.
2.  Execute the INSERT statement using the same student_id.
3.  Query the table.

Expected Result:
- The database rejects the INSERT.
- A UNIQUE constraints primary key constraint error is returned.
- No duplicate student_id is created.

Test Type: Negative /Database Testing

Test Design Technique: Error guessing


TC-DB-04 Insert the student with non-existing course_id

Module:Referential Integity/ Foreign Key

Preconditions:
- students and courses tables exist.
- students.course_id is defined as a foreign key referecing courses.course_id.
- course_id = 999 does not exist in the courses table.

Test Data:
- student_id:6;
- first_name:Anna;
- last_name:Smith;
- country: ukraine;
- course_id:999.

Steps:

1.Execute an INSERT statement into the students table using course_id = 999.

2.Query the students table for student_id = 6

Expected Result:
- The database rejects the INSERT operation.
- A foreign key constraint error is returned.
- Student with student_id = 6 is not added to the table.

Test Type: Referential Integrity Testing

Test Design Technique:Error Guessing


TC-DB-05 Insert invalid data type into duration

Module: Courses table/Data type Validation

Preconditions:
- courses table exists.
- duration is defined as INTEGER.

Test Data:
- course_id : 103;
- course_name: Database Testing;
- duration: "eight".

Steps:

1.Attempt to insert the record with a text value in duration.

2.Retrieve the inserted record.

3.Verify the stored value and its type.

Expected Result:

- The database should reject data that violates the expoected INTEGER type.
 
- If SQLite accepts the value because of its type-affinity rules, the result should be documented as an observed SQLite behavior and evaluated against the project requirements.

Test Type: Negative / Database Testing

Test Design Technique: Equivalence Partitioning


TC-DB-06 JOIN using a non-existing column

Module: SQL Queries/ JOIN

Preconditions:
- students and courses tables exist.
- The tables have the expected columns.
- Database connection is active.

Test Data:
- invalid JOIN column:students.invalid_course_id

Steps:

1.Write an INNER JOIN query using a non-existing column.

2.Execute the query.

3.Observe the database response.

Expected Result:
- The database rejects the query.
- An error indicating that the specified column does not exist is returned.
- NO result set is returned.

Test Type: Negative / Database Testing

Test Design Technique: Error Guessing

TC-DB-07 Query a non-existing table

Module: Database Structure/ SQL Queries

Preconditions:
- Database exists.
- students and courses tables exist.
- a table named teachers does not exist.

Test Data:
- Table: teachers

Steps:
1. Execute: SELECT * FROM teachers;
2. Observe the database response.

Expected Result:
- The database rejects the query.
- An error indicating that the table does not exist is returned.
- No result set is returned.

Test Type: Negative / Database Testing

Test Design Technique: Error Guessing


