FLOW-01 Verify course creation

Module:Courses/CRUD

Preconditions:
- Database is created and accessible.
- courses table exists.
- course_id =  7  does not exist in the courses table.

Test Data:
- course_id:  ;
- course_name: SQL testing;
- duration:  8.

Steps:

1.Execute an INSERT statement to add the course to the courses table.

2.execute a SELECT query using course_id = 7 .

3.Verify the returned record.

Expected Result:
- The course is successfully inserted into the courses table.
- The record with course_id =  7 exists.
- All inserted values corresponds to the test data.

Test Type: Positive/ Database Testing/CRUD Testing

Test Design Technique: Equivalence Patitioning


FLOW-02 Verify student creation

Module:Student / CRUD

Preconditions:
- courses table contains a course with course_id =   .
- students table exists.
- student_id = 6 does not exists in the students table.
- Foreign -key enforcement is enabled.

Test Data:
- student_id: 6;
- first_name: Anna;
- last_name: Smith;
- country: Ukraine;
- course_id:7  .

Steps:
1. Execute an INSERT statement to add the student to the students table.
2. Execute a SELECT query using student_id = 6.
3. Verify the returned record.

Expected Result:
- The student is successfully inserted.
- The record with student_id = 6 exists.
- course_id =  7 is stored for the student.
- The inserted values corresponds to the test data.

Test Type:Positive / Database Testing/CRUD Testing

Test Design Technique: Equivalence Partitioning


FLOW-3 Verify referential integrity between students and courses

Module: Students- Courses/ Foreign Key

Preconditions:
- course with course_id = 7   exists in the courses table.
- student with student_id =5/ 6 exists in the students table.
- students.course_id is defined as a foreign key.
- Foreign key enforcement is enabled.

Test Data:
- students.course_id: 7  ;
- courses.course_id:  7  .

 Steps:
 
 1.Retrieve student_id =5/ 6 from the students table.
 
 2. Retrive course_id =  7  from the courses table.
 3. 
 3.Compare students.course_id with courses.course_id.

 4.Verify that the referenced course exists.

 Expected Result:
 - students.course_id contains a value that exists in the courses.course_id.
 - The student is correctly associated with the SQL Testing course.
 - Referential integrity between two tables maintained.

Test Type: Positive/ Database Testing/ Referential Integrity Testing

Test Design Technique: Equivalence Partitionign


FLOW-04  Verify INNER JOIN operation

Module: SQL Queries/ JOIN

Preconditions:
- students with student_id = 6 exists.
- course with course_id =     exists.
- The student is associated with the course through  students.course_id.

 Test Data:
 - student_id: 6;
 - course_id:    .

Steps:
1.Execute an INNER JOIN between students and courses.
2. Join the tables using students.course_id = courses.course_id.
3. Filter the results for student_id=6.
4.Verify the returned data.

Expected Result:
- The query executes successfully.
- One matching record is returned.
- The result contains the information from both tables.

  Test Type:Positive/ Database Testing

  Test Design Technique: Equivalence Partitioning


  FLOW-05 Verify data updating after insertion

  Module: Students- Courses/ CRUD

  Preconditions:
  - Student with student_id = 6 exists.
  - Course with course_id =    exists.
  - The student is associated with the course.

  Test Data:
  INITIAL:
  - course_id:   ;
  - course_name: SQL Testing;
  - duration: 8.
  UPDATED:
- duration: 10.

Steps:
1.Execute an update statement for course_id =   .
2.Change duration from 8 to 10.
3.Execute a SELECT query for course_id =   .
4.Execute the existing INNER JOIN query for student_id = 6.
5.Verify the updated data.

Expected Result:
- The duration value is successfully updated from 8 to 10.
- The student remains associated with course_id.
- The JOIN result displays the updated course duration.

Test Type: Positive/ Database Testing

Test Design Technique: Equivalence Partitioning


FLOW-06 Verify student deletion

Module: Students/ CRUD

Preconditions:
- Student with student_id exists.
- Student is associated with course_id  =  .
- Course with course_id =    exists.

Test Data:
- student_id:6.

Steps:
1. Executea DELETE statement for student_id = 6.
2. Execute a SELECT query for student_id =6.
3. Verify the database response.

Expected Result:
- The student record is successfully deleted from the students table.
- No record with student_id = 6 is returned.

Test Type: Positive / Database Testing

Test Design Technique: Equivalence Partitioning


FLOW-07 Confirm student deletion

Module: Students/Data Verification

Preconditions:
- student_id = 6 has been deleted in FLOW-06.
- courses table remains available.
- course_id =    still exists.

Test Data:
- student_id:6.

Steps:
1. Execute a SELECT query for student_id = 6.
2. Execute an INNER JOIN query filtering by student_id = 6.
3. Verify both query results.

Expected Result:
- The SELECT query returns no record for student_id = 6.\
- The INNER JOIN query also returns no record for student_id = 6.
- The associated course remains in the courses table.

Test Type: Positive Database Testing

Test Design Technique: Equivalence Partitioning

  


  
