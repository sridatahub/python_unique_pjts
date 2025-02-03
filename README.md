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
```

### 2. `remove_student(student_dict, roll_no)`

This function removes a student from the `student_dict`.

```python
def remove_student(student_dict, roll_no):
    if roll_no in student_dict:
        del student_dict[roll_no]
        print("Student has been successfully removed.")
    else:
        print("Error: Roll number not found.")
```
### 3. `update_student(student_dict, roll_no, name=None, branch=None, cgpa=None, city=None)`

This function updates the details of a student in the `student_dict`.
```python
def update_student(student_dict, roll_no, name=None, branch=None, cgpa=None, city=None):
    if roll_no in student_dict:
        if name:
            student_dict[roll_no]['Name'] = name
        if branch:
            student_dict[roll_no]['Branch'] = branch
        if cgpa is not None:  # Important: Check for None explicitly for CGPA
            student_dict[roll_no]['CGPA'] = cgpa
        if city:
            student_dict[roll_no]['City'] = city
        print("Student details updated successfully.")
    else:
        print("Error: Roll number not found.")
```
### 4.`list_students(student_dict)`

This function lists all the students in the `student_dict`.
```python
def list_students(student_dict):
    print("\n\n College Student Database \n")
    if not student_dict:
        print("Currently, there are no students to show.")
    for roll_no, details in student_dict.items():
        print(f"Roll No: {roll_no}, Name: {details['Name']}, Branch: {details['Branch']}, CGPA: {details['CGPA']}, City: {details['City']}")
```

