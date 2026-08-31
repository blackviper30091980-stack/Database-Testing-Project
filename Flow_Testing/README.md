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
