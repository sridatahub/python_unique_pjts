# College Student Database Management System

This repository contains a Python-based College Student Database Management System. It allows users to perform various operations like adding, removing, updating, and listing student records.  The system uses a dictionary to store student information, making it efficient for data retrieval and manipulation.

## Features

*   **Add Student:** Adds a new student record to the database.
*   **Remove Student:** Removes an existing student record from the database.
*   **Update Student:** Updates the details of an existing student.
*   **List Students:** Displays all student records in a formatted way.

## Code Explanation

### 1. `add_student(student_dict, roll_no, name, branch, cgpa, city)`

This function adds a new student to the `student_dict`.

```python
def add_student(student_dict, roll_no, name, branch, cgpa, city):
    if roll_no not in student_dict:
        student_dict[roll_no] = {'Name': name, 'Branch': branch, 'CGPA': cgpa, 'City': city}
        print("New student successfully added!")
    else:
        print("Error: Roll number already exists.")
