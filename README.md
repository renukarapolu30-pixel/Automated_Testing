# Automated Testing for Student Management System

## 1. Project Overview

This project demonstrates automated testing of a Python-based Student Management System using Python's built-in `unittest` framework.

The project focuses on testing the main functionalities of the Student Management System, including adding, searching, updating, deleting students, calculating average marks, and checking pass/fail results.

The test suite also covers invalid inputs, missing records, duplicate records, edge cases, and complete student workflows.

---

## 2. Technologies Used

* Python 3
* unittest
* VS Code
* Git/GitHub

No external Python libraries are required.

---

## 3. Project Structure

```text
Automated_Testing/
│
├── student_manager.py
├── test_student_manager.py
├── README.md
└── requirements.txt
```

### File Description

**student_manager.py**
Contains the `StudentManager` class and the main student management functionalities.

**test_student_manager.py**
Contains 18 automated tests using Python's `unittest` framework.

**README.md**
Contains project documentation, testing methodology, test cases, and execution instructions.

**requirements.txt**
Documents the project dependencies. No external dependencies are required.

---

## 4. Functionalities Tested

The Student Management System provides the following functionalities:

* Add a student
* Get student details
* Search for a student
* Update student information
* Delete a student
* Calculate average marks
* Check pass/fail result
* Validate marks
* Handle duplicate student records
* Handle missing student records

---

## 5. Testing Methodology

The project uses a **tests-after-development approach**. The Student Management System was implemented first, followed by automated tests to verify its functionality.

The test suite was designed to cover:

* Normal functionality
* Invalid inputs
* Boundary conditions
* Missing records
* Duplicate records
* Complete workflows
* Multiple student records
* Error conditions

Each test uses a fresh `StudentManager` instance through the `setUp()` method to keep tests independent.

---

## 6. Test Cases

A total of **18 automated tests** were implemented.

### Unit Tests

| Test Case                          | Purpose                                                      |
| ---------------------------------- | ------------------------------------------------------------ |
| `test_add_student`                 | Verifies that a student can be added and retrieved correctly |
| `test_duplicate_student`           | Checks that duplicate student IDs raise an error             |
| `test_get_missing_student`         | Checks handling of a non-existing student                    |
| `test_search_student`              | Verifies student search functionality                        |
| `test_search_missing_student`      | Checks search behavior when no student is found              |
| `test_update_student`              | Verifies updating student name and marks                     |
| `test_update_missing_student`      | Checks updating a non-existing student                       |
| `test_delete_student`              | Verifies successful student deletion                         |
| `test_delete_missing_student`      | Checks deletion of a non-existing student                    |
| `test_average_marks`               | Verifies average mark calculation                            |
| `test_average_empty_records`       | Checks average calculation when there are no students        |
| `test_pass_result`                 | Verifies the pass result                                     |
| `test_fail_result`                 | Verifies the fail result                                     |
| `test_invalid_marks_below_zero`    | Checks rejection of marks below 0                            |
| `test_invalid_marks_above_hundred` | Checks rejection of marks above 100                          |
| `test_invalid_marks_type`          | Checks rejection of non-numeric marks                        |

### Integration Tests

**`test_student_lifecycle`**

Tests a complete student workflow:

```text
Add Student
     ↓
Update Student
     ↓
Search Student
     ↓
Check Result
     ↓
Delete Student
     ↓
Verify Student is Removed
```

This ensures that multiple functionalities work correctly together.

**`test_multiple_students_and_average`**

Tests interaction between multiple student records by:

1. Adding multiple students
2. Calculating their average marks
3. Checking their individual results

This verifies that the system works correctly with multiple records.

---

## 7. Edge Cases and Error Conditions

The following conditions are tested:

* Duplicate student ID
* Student ID not found
* Marks below 0
* Marks above 100
* Non-numeric marks
* Empty student records
* Searching for a non-existing student
* Updating a non-existing student
* Deleting a non-existing student

Expected exceptions such as `ValueError`, `TypeError`, and `KeyError` are verified using `assertRaises()`.

---

## 8. How to Run the Tests

Open PowerShell in the project directory:

```powershell
cd "C:\Users\lenovo\OneDrive\Documents\Automated_Testing"
```

Run all tests using:

```powershell
python -m unittest -v
```

If the `python` command is not available on the system, use the installed Python executable directly:

```powershell
& "C:\Users\lenovo\AppData\Local\Microsoft\WindowsApps\PythonSoftwareFoundation.Python.3.13_qbz5n2kfra8p0\python.exe" -m unittest -v
```

---

## 9. Test Result

The complete test suite was executed successfully.

```text
Ran 18 tests in 0.007s

OK
```

All **18 tests passed successfully**.

---

## 10. Refactoring and Maintainability

The project was reviewed after testing to improve maintainability.

The implementation uses:

* A dedicated `StudentManager` class
* Separate methods for each functionality
* A private `_validate_marks()` method for input validation
* Clear exception handling
* Independent test cases
* `setUp()` to create a fresh test environment for every test

These practices make the code easier to understand, maintain, and extend.

---

## 11. Clean Environment Validation

The project does not require any external Python packages.

The tests use Python's built-in `unittest` framework, making the project self-contained.

The test suite was successfully executed using the installed Python environment, with all 18 tests passing.

---

## 12. Conclusion

This project demonstrates how automated testing can be used to verify a Python application.

The test suite covers normal operations, edge cases, error conditions, unit-level functionality, and integration workflows.

All **18 automated tests passed successfully**, confirming that the Student Management System behaves as expected for the tested scenarios.
