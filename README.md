# Mainflow-SQL-Developer-task-1
Mainflow SQL Developer task-1
Student Management System Project for SQL Developers
 Objective
The project focuses on providing students with practical experience in SQL database creation,data manipulation, and analysis using student performance data.
 Project Steps
 
1. Database Setup
● Create a database named StudentManagement.
● Create a table named Students with the following fields:
○ StudentID: Primary Key, INT, an auto-incrementing integer.
○ Name: Stores the student's name (up to 50 characters).
○ Gender: A single character (VARCHAR, 1 - 'M' for Male, 'F' for Female).
○ Age: INT
○ Grade: Academic grade (VARCHAR, 10 - e.g., 'A', 'B', 'C', etc.).
○ MathScore, ScienceScore, EnglishScore: Integers representing scores in respective subjects.

2. Inserting Data
  Populate the Students table with at least 10 sample records, including a variety of names, genders, grades, and scores in Math, Science, and English.

DATA:
  -- Insert sample data into Students2 table
  INSERT INTO Students2 (Name, Gender, Age, Grade, MathScore, ScienceScore, EnglishScore) VALUES
  ('John Doe', 'M', 15, 'A', 95, 90, 88),
  ('Jane Smith', 'F', 16, 'B', 78, 80, 82),
  ('Sam Wilson', 'M', 14, 'A', 89, 91, 87),
  ('Emily Davis', 'F', 17, 'C', 62, 70, 65),
  ('Mike Johnson', 'M', 15, 'B', 75, 78, 80),
  ('Sophia Brown', 'F', 16, 'A', 92, 94, 93),
  ('Chris Evans', 'M', 14, 'C', 60, 58, 63),
  ('Olivia Green', 'F', 17, 'B', 80, 85, 83),
  ('Liam Taylor', 'M', 15, 'A', 96, 93, 94),
  ('Ava Clark', 'F', 16, 'B', 84, 86, 88);

  ![Screenshot 2024-12-31 002104](https://github.com/user-attachments/assets/53bdb693-c55f-45f3-820d-8dbe7eee74b9)



3. Tasks  Performed
  1. Display all students and their details to get an overview of the data. 
  2. Calculate the average scores for each subject to understand subject-wise performance.
  3. Find the student(s) with the highest total score across all subjects to identify the top performer.
  4. Count the number of students in each grade to observe grade distributions.
  5. Find the average score for male and female students to compare performance by gender.
  6. Identify students whose Math score is above 80 to highlight high achievers in Math.
  7. Update the grade of a student with a specific Student ID to reflect changes or corrections.
     
![Screenshot 2024-12-30 231743](https://github.com/user-attachments/assets/8e4252fa-a4d4-4f18-abca-b3ed02eea7d9)
![Screenshot 2024-12-30 231854](https://github.com/user-attachments/assets/1a68c295-c203-4e8a-a47d-542bf5c79f4b)
![Screenshot 2024-12-30 231923](https://github.com/user-attachments/assets/d4688418-2325-43fc-ab2e-5eb4dfedc039)
![Screenshot 2024-12-30 231953](https://github.com/user-attachments/assets/dd90f221-a226-451f-8b0a-854046221726)
![Screenshot 2024-12-30 232044](https://github.com/user-attachments/assets/3f0635e0-e531-4991-8703-b21b8b208b1c)


