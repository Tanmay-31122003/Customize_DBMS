# Customised Database Management System

## Overview
The Customised Database Management System is a simple Java-based application designed to manage student records. This system allows users to insert, display, and filter student records based on various criteria.

## Features
- **Insert Records**: Add new student records with a unique roll number, name, city, and marks.
- **Display Records**: View all student records.
- **Filter Records**: Retrieve student records based on city.

## Classes and Methods

### `node` Class
The `node` class represents a single student record.
- **Fields**:
  - `int Rno`: The roll number of the student.
  - `String Name`: The name of the student.
  - `String City`: The city of the student.
  - `int Marks`: The marks of the student.
  - `node next`: The reference to the next node (student record) in the linked list.

- **Constructor**:
  - `node(String B, String C, int D)`: Initializes a new student record with the given name, city, and marks. The roll number is automatically assigned.

### `DBMS` Class
The `DBMS` class provides methods to interact with the student records.
- **Fields**:
  - `node first`: The reference to the first student record in the linked list.

- **Constructor**:
  - `DBMS()`: Initializes the database management system and creates the student table.

- **Methods**:
  - `void InsertIntoTable(String Name, String City, int Marks)`: Inserts a new student record into the table.
  - `void SelectStarFrom()`: Displays all student records.
  - `void SelectStarFromWhereCity(String str)`: Displays student records where the city matches the given string.

## Usage
1. **Initialize the DBMS**:
    ```java
    DBMS dbms = new DBMS();
    ```

2. **Insert Records**:
    ```java
    dbms.InsertIntoTable("Amit", "Pune", 89);
    dbms.InsertIntoTable("Rahul", "Mumbai", 76);
    ```

3. **Display All Records**:
    ```java
    dbms.SelectStarFrom();
    ```

4. **Filter Records by City**:
    ```java
    dbms.SelectStarFromWhereCity("Pune");
    ```

## Example
Here is a simple example demonstrating how to use the Customised Database Management System:

```java
public class Main {
    public static void main(String[] args) {
        DBMS dbms = new DBMS();
        
        dbms.InsertIntoTable("Amit", "Pune", 89);
        dbms.InsertIntoTable("Rahul", "Mumbai", 76);
        dbms.InsertIntoTable("Priya", "Pune", 93);
        
        dbms.SelectStarFrom();
        
        dbms.SelectStarFromWhereCity("Pune");
    }
}
