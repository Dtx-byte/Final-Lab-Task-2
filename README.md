# [Finals-Lab-Task-2](https://github.com/user-attachments/files/19631554/Soguilon.Carl.Asnef.B.FINALS2.EDM.SQL.docx)
- This portfolio demonstrates my understanding of MySQL database creation using a simplified student assignment submission system. It covers the step-by-step creation of tables representing students, assignments, and their submissions. This exercise applies data types, relationships, and constraints like primary keys, foreign keys, and composite keys to build a fully functional relational schema.

# Step By Step Process
### 1. Create the student table:
- Define username as a VARCHAR(50).
- Set username as the Primary Key.

### 2. Create the assignment table:
- Define shortname as a VARCHAR(50) and set it as the Primary Key.
- Define due_date as a DATE NOT NULL.
- Define url as a VARCHAR(255), which can be null.

### 3. Create the submission table:
- Define username and shortname both as VARCHAR(50).
- Define version as an INT.
- Define submit_date as a DATE NOT NULL.
- Define data as TEXT.
- Set a composite primary key of (username, shortname, version).
- Add foreign keys referencing the student and assignment tables.

# Table Relationships
### 1. **`student` table**
- **Primary Key:** `username`
- **Relationships:**
  - **One-to-Many** relationship with `submission`
    - One student (`username`) can have **many submissions**.

### 2. **`assignment` table**
- **Primary Key:** `shortname`
- **Relationships:**
  - **One-to-Many** relationship with `submission`
    - One assignment (`shortname`) can have **many submissions** from different students (or multiple versions from the same student).

### 3. **`submission` table**
- **Composite Primary Key:** `(username, shortname, version)`
- **Relationships:**
  - **Many-to-One** with `student`
    - Each submission belongs to **one student**.
  - **Many-to-One** with `assignment`
    - Each submission is for **one assignment**.
  - Overall, it represents a many-to-many relationship between students and assignments, with a version to track multiple submissions.


# Screenshots
## Query Statements
1. Student Table
- ![Image](https://github.com/user-attachments/assets/65bb70d5-9864-46ea-96af-8424b4e79a97)

2. Assignment Table
- ![Image](https://github.com/user-attachments/assets/b8dcd7f3-8443-4be2-9f87-f69e9ba68437)

3. Submission Table
- ![Image](https://github.com/user-attachments/assets/53043940-901d-4f7f-99d2-e6b2a0174ad8)

## Table Structure
1. Student Table
- ![Image](https://github.com/user-attachments/assets/5d2c547a-591b-4aa3-8216-fd8534177855)

2. Assignment Table
- ![Image](https://github.com/user-attachments/assets/0e969cb9-382c-4f01-a491-1d9d2eaab07b)

3. Submission Table
- ![Image](https://github.com/user-attachments/assets/e53bf254-3af7-4405-ae97-d8b1a76fc2e3)

## EER Diagram
- ![Image](https://github.com/user-attachments/assets/1d29925b-4f4f-4a7a-9937-afa7efa96811)
- ![Image](https://github.com/user-attachments/assets/7e6b2f31-14a3-4f67-900b-f17e6f85e954)
