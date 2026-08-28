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

