

TC-DB-01 Verify database structure
Module: Database Structure

Preconditions:
- Database is created;
- Database is accessible.

Test Data:
- students;
- courses.

Steps:
1. Connect to the database.
2. Execute the query to retrieve all tables.
3. Review the returned tables names.

Expected Result:
- The database contains the 'students' and 'courses' tables.
-  No unexpected tables are present.

  Test Type: Structural Testing

  Test Design Technique: Checklist-based testing


  TC-DB-02 Verify students table columns

  Module: Tables and Columns

  Preconditions: 
  - Database is accessible.

Test Data: students expected columns:
- student_id
- first_name
- last_name
- country
- course_id

Steps:
1. Open the database.
2. Execute PRAGMA table_info(students)
3. Compare the returned columns with the expected structure.

Expected Result:
- All expected columns exist.
- Column names correspond to the expected database structure.

Test Type: Structural Testing

Test Design Technique: Checklist- based testing


TC-DB-03  Verify courses table column

Module: Tables and Columns

Preconditions:
- Database is accessible.

Test Data: courses expected columns:
- course_id
- course_name
- duation

Steps: 
1. Open the database.
2. Execute PRAGMA table_info (courses).
3. Compare the returned columns with the expected structure.

Expected Result:
- All expected columns exist.
- Column names correspond to the expected database structure.

Test Type: Structural Testing

Test Design Technique: Checklist-based testing


 TC-DB-04 Verify NOT NULL constraints in students table

 Module: Constraints

 Preconditions: 
 - 'students' table exists.
 - Requied columns are configured as NOT NULL.

Test Data: 
- student_id;
- first_name;
- last_name;
- country;
- couse_id.

Steps:
1. Execute the INSERT statement using the provided data.
2. Retrieve the newly created record using SELECT.
3. Verify that all supplied values are stored correctly.

Expected Result: 
- The record is successfully inserted.
- All required fields contain the provided values.
- No constraints violation occurs.

Test Type: Functional Testing/Database Testing

Test design Technique: Positive Testing


TC-DB-05 Verify NOT NULL constraints in courses table

Module: Constraints

Preconditions: 
- courses table exists.
- Requied columns are configured as NOT NULL.

Test Data:
- course_id;
- course_name;
- duration.

Steps: 
1. Execute the INSERT statement using the provided data.
2. Retrieve the newly created record using SELECT.
3. Verify that all supplied values are stored correctly.

Expected Result:
  - The record is successfully inserted.
- All required fields contain the provided values.
- No constraints violation occurs.

Test Type: Functional Testing/Database Testing

Test design Technique: Positive Testing.


TC-DB-06 Verify valid data types

Module: Data Types

Preconditions:
- students and courses table exist.

Test Data:
| Table  | Column | Expected Type  |
|students |student_id|INTEGER |
|students| first_name|TEXT | 
|students| last_name|TEXT |
| students| country| TEXT | 
| students| course_id| INTEGER | 
| courses| course_id| INTEGER | 
| courses| course_name| TEXT| 
| courrses| duration| INTEGER | 

Steps:
1.Execute PRAGMA table_info(students).
2.Execute PRAGMA table_info(courses)
3.Compare the returned data types with the expected types.

Expected Result:
- Each column has the declared data type.
- Valid values can be stored in the corresponding columns.

Test Type: Structural Testing/ Database Testing

Test design Technique: Checklist-based testing


TC-DB-07 Verify data integrity and consistency

Modul: Data Integrity

Preconditions:
- Student with student_id = 1 exists.
- Course with course_id = 1 exists.

Test Data:
STUDENT:
-student_id;
-first_name;
-last_name;
-country;
-course_id

COURSE:
-course_id;
-course_name;
-duration

Steps:
1.Retrieve the student record using student_id=1.
2.Retrieve the corresponding course using course_id =1.
3.Compare the storedvalues with the expected test data.
4.Verify that course_id in the students record coresponds to the existing course.

Expected Result:
- stored student data matches the expected data.
- stored course data matches the expected data.
- related data remains consistent.

Test Type: Data Integity Testing

Test Design Technique: Equivalence Partitioning


TC-DB-08 Verify primary key

Modul: Keys and Relationships

Preconditions: 'students' and 'courses' table exist

Test Data: 
- students.student_id
- courses.course_id

Steps:
1.Execute PRAGMA table_info(students);
2.Check the pk value for student_id;
3.Execute PRAGMA table_info(courses);
4.Check the pk value for course_id.

Expected Result:
- students.student_id is defined as a primary key;
- courses.course_id is defined as a primarykey.

Test Type: Structural Testing

Test Design Technique: Checklist-based testing


TC-DB-09 Verify foreign key relationship

Module: Keys and Relationships

Preconditions:
- students and courses tables exist;
- a course with course_id = 1 exist.

Test Data:
- courses.course_id = 1
- students.student_id =1

Steps:
1.Execute PRAGMA foreign_key_list(students);
2.Verify that students.course_id references courses.course_id.
3.Insert or use a student record with course_id=1.
4.Retrieve the student record.
5.Verify that the referenced course exists.

Expected Result:
- students.course_id is defined as a foreign key;
- it references courses.course_id;
- a student can successfully reference an existing course.

Test Type: Referential Integrity Testing

Test Design Technique: Positive Testing


TC-DB-10 Verify JOIN operation between students and courses

Module:Data Relationships/JOIN

Preconditions:
- students contains a student with course_id = 1;
- courses contains a course with coures_id =1.

Test Data:
- students.course_id =1;
- courses.course_id =1.

Steps:
1.Execute an INNER JOIN between students and courses.
2.Join the tables using students.course_id = courses.course_id.
3.Retrieve student and course information.
4.Compare the returned values with the source records.

Expected Result:
- the query executes successfully;
- the student is matched with the correct course;
- the result contains the expected student and course information.

Test Type: FunctionL Testing/Database Testing

Test Design Technique: Positive Testing





