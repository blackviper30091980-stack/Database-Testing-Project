FLOW-01 Verify course creation

Module:Courses/CRUD

Preconditions:
- Database is created and accessible.
- courses table exists.
- course_id =    does not exist in the courses table.

Test Data:
- course_id:  ;
- course_name: SQL testing;
- duration:  8.

Steps:
1.Execute an INSERT statement to add the course to the courses table.
2.execute a SELECT query using course_id =  .
3.Verify the returned record.

Expected Result:
- The course is successfully inserted into the courses table.
- The record with course_id =   exists.
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
- course_id:  .

Steps:
1. Execute an INSERT statement to add the student to the students table.
2. Execute a SELECT query using student_id = 6.
3. Verify the returned record.

Expected Result:
- The student is successfully inserted.
- The record with student_id = 6 exists.
- course_id =   is stored for the student.
- The inserted values corresponds to the test data.

Test Type:Positive / Database Testing/CRUD Testing

Test Design Technique: Equivalence Partitioning


FLOW-3 Verify referential integrity between students and courses

Module: Students- Courses/ Foreign Key

Preconditions:
- course with course_id =    exists in the courses table.
- student with student_id = 6 exists in the students table.
- students.course_id is defined as a foreign key.
- Foreign key enforcement is enabled.

Test Data:
- students.course_id:   ;
- courses.course_id:    .

 Steps:
 1.Retrieve student_id = 6 from the students table.
 2. Retrive course_id =    from the courses table.
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
