

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
1. 
  
