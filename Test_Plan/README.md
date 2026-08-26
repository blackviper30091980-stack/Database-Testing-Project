TEST PLAN -- SQL DATABASE TESTING

1.PROJECT OVERVIEW

This project demostrates basic database testing using SQLite and DBeaver.
The database represents a simple student and course management system and consists of two related tables:
- ' students '
- ' courses '
The project demostrate how QA principles can be applied to database testing, including database structure validation,data validation,CRUD operations,constraints,data integrity,SQL query validation and testing of relationships between tables.

2.TEST OBJECTIVES

The main objectives of this project are:

- verify the database structure;
- verify tables and columns;
- verify data types;
- verify primary keys and foreign keys;
- verify NOT NULL constraints;
- verify valid and invalid data;
- verify CRUD operations;
- verify data integrity and consistency;
- verify relationships between tables;
- verify SQL query results;
- verify JOIN operations;
- identify and document database defects.

3.DATABASE STRUCTURE

The database contains two related tables.

3.1 Student Table

Column | Data Type | Constraints | Description |
'student_id' | INTEGER | PRIMARY KEY | Unique student identifier |
| 'first_name' | TEXT | NOT NULL | Student's first name | 
| 'last_name' | TEXT | NIT NULL | student's last name | 
| 'country' | TEXT | - | student's country | 
| 'course_id' | INTEGER | FOREIGN KEY | Reference to the course |

3.2 Course Table

Column| Data Type | Constraints | Description | 
'course_id' | INTEGER | PRIMARY KEY | Unique course identifier | 
| 'course_name' | TEXT | NOT NULL | Course name | 
| 'duration' | INTEGER | NOT NULL | Course duration in weeks | 

3.3 Relationships
The tables are related through:
' student.course_id----
---- 'courses.couse_id'
Relationship Type: ** One-to-Many **.One course can be assigned to multiple students.

4.SCOPE
4.1 In Scope
The following areas will be tested:
- database schema;
- table structures;
- column names;
- data types;
- primary keys;
- foreign keys;
- NOT NULL constraints:
- data insertion;
- data retrieval;
- data updating;
- data deletion;
- positive testing;
- negative testing;
- data validation;
- data integrity;
- data consistency;
- filtering and sorting;
- aggregate functions;
- GROUP BY;
- HAVING;
- JOIN operation;
- SQL query results.

5.TEST STRATEGY

The following testing approaches will be used:
5.1 Schema validation
Verify that :
- required tables exist;
- required columns exist;
- column names are correct;
- datatypes are correct;
- primary keys are defined correctly;
- required constraints are applied.
5.2 Positive testing
  Verify that valid data and valid SQL operations are accepted and produce the expected result.
5.3 Negative testing
  Verify that invalid data and invalid operations are rejected or handled according to the expected database behavior.
5.4 CRUD testing
  The following operations will be tested:
  - CREATE - INSERT
  - READ - SELECT
  - UPDATE - UPDATE
  - DELETE - DELETE
  5.5 Data Integrity testing
    Verify that data remains accurate and consistent after INSERT,UPDATE and DELETE operations.Particular attention will be paid to the relationship between 'students' and 'cuorses'.
  5.6 SQL Query testing
    Verify SQL queries using SELECT,WHERE,ORDER BY,DISTINCT,aggrigate functions,GRUOP BY,HAVING,JOIN.
  5.7 Relationship testing
    Verify that:
  - a student can be assigned to the existing course;
  - a student cannot reference a non-existing course;
  - data from both tables can be retrieved using JOIN;
  - the relationships between tables return the expected data.

  6.TEST DATA

  Test data will contain both valid and invalid records

  Positive Test Data
  Valid student records will contain:
  - valid student ID;
  - first name;
  - last name;
  - country;
  - existing courrse ID;

  Valid course records will contain:
  - valid course ID;
  - course name;
  - course duration in weeks.

  Negative Test Data
  Negative test data will include:
  - NULL values in requiered fields;
  - duplicate primary key values;
  - non-existing foreign key values;
  - invalid duration values;
  - invalid or incomplete records.

  7. TEST ENVIRONMENT

  | Components | Details |

  | Database | SQLite |
  | Database Management Tool | DBeaver |
  |
  | Query Language | SQL |
  | Operating System | Windows |
  | Vesion Control | Git |
  | Repository | GitHub |

  8.TEST AREAS

  | ID | Test Area |
  | ---|---|
  |DB - 01 |Database and table structure|
  | DB - 02|Data types|
  | DB - 03| Primary key validation|
  | DB - 04| Foreign key validation|
  | DB - 05| NOT NULL constraints|
  | DB - 06| Data insertion|
  | DB - 07| Data retrieval|
  | DB - 08| Data update|
  | DB - 09| Data deletion|
  | DB - 10| Data integrity|
  | DB - 11| Data consistency|
  | DB - 12| SQL queries|
  | DB - 13| JOIN operation|
  | DB - 14| Positive scenarios|
  | DB - 15| Negative scenarios|

  9.ENTRY CRITERIA

  Testing can begin when:
  - the SQLite database has been created;
  - the 'students' and 'courses' tables have been created;
  - the database structure has been defined;
  - the relationships between the tables has been configured;
  - the database is accessible through DBeaver;
  - test data has been prepared;
  - expected results have been defined.

  10.EXIT CRITERIA

  Testing can be completed when:
  - all planned test cases have been executed;
  - database structure has been verified;
  - primary and foreign keys have been tested;
  - CRUD operations have been tested;
  - positive and negative scenarios have been executed;
  - data integrity and consistency have been verified;
  - JOIN queries have been tested;
  - identified defects have been documented;
  - a summary report has been prepared.

  11.DEFECT REPORTING

  Identified defects will be documented using the following information:
  - Defect ID;
  - Title;
  - Preconditions;
  - Steps to Reproduce;
  - Expected Result;
  - Actual Result;
  - Severity;
  - Priority;
  - SQL Query
  - Evidence/Screenshots

  12.TEST DELIVERABLES

  The following artifacts will be included in the project:
  - Test Plan;
  - Database Schema;
  - SQL scripts;
  - Test Data;
  - Positive Test Cases;
  - Negative Test Cases;
  - CRUD Test Cases;
  - Data Integrity Test Cases;
  - SQL Query Test Cases;
  - JOIN Test Cases;
  - Screenshots;
  - Summary Report.

  13.TOOLS

  - SQLite
  - DBeaver
  - SQL
  - Git
  - GitHub


 
