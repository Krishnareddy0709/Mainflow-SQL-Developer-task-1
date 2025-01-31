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


## Mainflow-SQL-Developer-task-2
Mainflow SQL Developer task-2
Advanced Queries with Joins and Filtering

#Objective:
Analyze relationships between multiple tables and use SQL joins and filtering techniques to extract meaningful insights from the data.

Project Steps
Step 1: Database Setup
Tables to Create
1. Students:
 ○ Already created in Task 1.
 ○ Contains student details such as student_id, name, and email.
2. Courses:
 ○ Fields:
   ■ course_id: Primary Key.
   ■ course_name: Name of the course.
   ■ course_description: Optional field for details.
3. Enrolments:
 ○ Fields:
   ■ enrolment_id: Primary Key.
   ■ student_id: Foreign Key referencing the Students table.
   ■ course_id: Foreign Key referencing the Courses table.
   ■ enrolment_date: Date of enrolment.

   ![Screenshot 2025-01-09 232406](https://github.com/user-attachments/assets/c64f4cbe-7509-4b3f-b68c-a16db42f68ef)
   ![Screenshot 2025-01-09 232531](https://github.com/user-attachments/assets/218f450b-3d18-48ea-b223-8ba99b62dff7)


Task 1: List all students and the courses they are enrolled in.
   ● Use an INNER JOIN to combine Students, Courses, and Enrolments tables.
   ● Select the student name and course name for all enrolled students. 
  
   
Task 2: Find the number of students enrolled in each course.
   ● Use a LEFT JOIN between Courses and Enrolments.
   ● Use GROUP BY to group results by course_id and course_name.
   ● Use COUNT(student_id) to calculate the number of enrolled students.
   ● Ensure courses with no enrolments are included in the results.
   ![Screenshot 2025-01-09 232614](https://github.com/user-attachments/assets/010a0456-458f-4256-a4e8-b7b5fd4902dc)

Task 3: List students who have enrolled in more than one course.
   ● Use the Enrolments table.
   ● Group data by student_id.
   ● Use COUNT(course_id) to calculate the number of courses per student.
   ● Use the HAVING clause to filter students with enrolments greater than 1.  
   ![Screenshot 2025-01-09 232651](https://github.com/user-attachments/assets/027f2b57-2f65-42fd-a03d-4dbc5f2687d3)

Task 4: Find courses with no enrolled students.
   ● Use a LEFT JOIN between Courses and Enrolments.
   ● Use WHERE enrolment_id IS NULL to filter courses with no enrolments.
   ![Screenshot 2025-01-09 232718](https://github.com/user-attachments/assets/cf5ee548-c003-45bf-90ce-e20821bcb966)


## Mainflow-SQL-Developer-task-3
   Subqueries and Aggregations

   Objective;
Use subqueries to extract insights from a dataset and perform data aggregations to summarize
and analyze the data.

Project Steps
Step 1: Database Setup
1. Table: Students
○ Fields:
  ■ student_id: Primary Key.
  ■ name: Name of the student.
  ■ math_score: Math test score.
  ■ science_score: Science test score.
  ■ english_score: English test score.
  ■ total_score: The sum of all scores for each student (optional if
calculated dynamically).
2. Insert sample data with scores for Math, Science, and English for multiple
students.

![Screenshot 2025-01-17 001627](https://github.com/user-attachments/assets/789ab081-fe90-45fb-a543-88a2b233d327)

Step 2: Tasks to Perform
Task 1: Identify Top Students by Total Scores
  ● Use a subquery to calculate the total score (math_score + science_score +
  english_score) for each student.
  ● Use an ORDER BY clause to rank students by their total scores in descending order.
  ● Limit the results to show only the top students (e.g., top 5).

![Screenshot 2025-01-17 001723](https://github.com/user-attachments/assets/892b9565-d879-4bbc-a47b-cbc96365cecb)

Task 2: Calculate Averages Based on Specific Conditions
● Use subqueries to filter and group data for average calculations:
  ○ Example 1: Calculate the average score of students who scored above 70 in
  Math.

  ![Screenshot 2025-01-17 001802](https://github.com/user-attachments/assets/427492f3-cfb0-4921-9431-101f8d4a6d37)

  ○ Example 2: Calculate the average total score of students grouped by a specific
  condition, such as a score range (e.g., students scoring 200–250 in total)

![Screenshot 2025-01-17 001825](https://github.com/user-attachments/assets/0517cf50-1ffa-436a-b612-7fe343c282c1)


Task 3: Find Second-Highest Math Scores
● Use a subquery to determine the highest Math score and exclude it in a second query to
  find the next highest value.
● Example:
  ○ Use MAX(math_score) in a subquery to find the highest score.
  ○ Use WHERE math_score < (SELECT MAX(math_score) FROM
  Students) to exclude the top score and then use MAX again to find the second
  highest score.

  ![Screenshot 2025-01-17 001901](https://github.com/user-attachments/assets/63082c4a-2c01-491f-9b72-79cd0d2a8c0b)


  # Mainflow-SQL-Developer-task-4
  Task 4: Window Functions
 Objective: Utilize SQL window functions to rank students and perform cumulative analysis.

Project Steps
1. Dataset Setup
● Create and Populate Table:
  Define a table Students with fields like:
  ○ StudentID (Primary Key)
  ○ Name
  ○ MathScore
  ○ TotalScore
● Populate with sample data for the analysis.

![Screenshot 2025-01-22 122155](https://github.com/user-attachments/assets/cfac653c-b4f5-495c-998b-2750965ede4b)

2. Tasks to Perform
 Task 1: Rank Students Based on Total Scores
● Query Objective: Use the RANK() function to assign ranks to students based on their TotalScore.
● Query Explanation:
  ○ Use RANK() OVER (ORDER BY TotalScore DESC) to rank students in descending order of their total scores.
  ○ If two students have the same score, they receive the same rank, and the next rank is skipped.
Task 2: Calculate Running Totals for Math Scores
● Query Objective: Use the SUM() function with OVER() to calculate running totals of MathScore ordered by StudentID.
● Query Explanation:
  ○ Use SUM(MathScore) OVER (ORDER BY StudentID) to compute a cumulative total.
  ○ This provides the total Math score up to each student in the order specified. How to Execut


![Screenshot 2025-01-22 122218](https://github.com/user-attachments/assets/e4c6a9fb-8f68-4117-bc7b-7be2554d7a0e)





