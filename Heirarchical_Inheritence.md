# Hierarchical Inheritance in Python

This Python project demonstrates **Hierarchical Inheritance** using a base class `Details` and two derived classes `Employee` and `Patient`. The program collects and displays details for both employees and patients.

## 🎯 Aim

To write a Python program that uses **Hierarchical Inheritance** to input and display **Employee** and **Patient** details.

## 📘 Description

- **Base Class:** `Details`
  - Stores common attributes: `name`, `age`
  - Provides methods: `getName()`, `getAge()`

- **Derived Class 1:** `Employee`
  - Inherits from `Details`
  - Adds: `employee_id`, `department`
  - Method: `getEmployeeDetails()`

- **Derived Class 2:** `Patient`
  - Inherits from `Details`
  - Adds: `patient_id`, `disease`
  - Method: `getPatientDetails()`

## 🧠 Algorithm

1. Create base class `Details` with common attributes.
2. Create `Employee` class extending `Details`, adding employee-specific data.
3. Create `Patient` class extending `Details`, adding patient-specific data.
4. Get user input for employee and patient data.
5. Display collected information using class methods.

## Program
class Details:
    def __init__(self, name, age):
        self.name = name
        self.age = age


class Employee(Details):
    def __init__(self, name, age, emp_id, salary):
        super().__init__(name, age)
        self.emp_id = emp_id
        self.salary = salary

    def display(self):
        print("Employee Details")
        print("Name :", self.name)
        print("Age :", self.age)
        print("Employee ID :", self.emp_id)
        print("Salary :", self.salary)


class Patient(Details):
    def __init__(self, name, age, disease):
        super().__init__(name, age)
        self.disease = disease

    def display(self):
        print("Patient Details")
        print("Name :", self.name)
        print("Age :", self.age)
        print("Disease :", self.disease)


# Employee Input
ename = input()
eage = int(input())
eid = input()
salary = float(input())

# Patient Input
pname = input()
page = int(input())
disease = input()

emp = Employee(ename, eage, eid, salary)
pat = Patient(pname, page, disease)

emp.display()
pat.display()
## Sample Output
Employee Details
Name : Ravi
Age : 30
Employee ID : E101
Salary : 25000.0
Patient Details
Name : Kumar
Age : 45
Disease : Fever
result:
program is executed successfully.

