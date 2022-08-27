Test 1: Server connection: login
1. run Server.java
2. run Client.java
3. select create account button
4. enter name, username, and password
5. select "Student" button, then select "Create Account"
6. select logout
7. close the program
8. run Client.java
9. enter previously created username and password and select login, ensuring the server has stored your information

Result: login successful and student menu should appear 
Status: Passed

Test 2: data persistence
1. run Server.java
2. run Client.java
3. select create account button
4. enter "Buster Dunsmore", bdunsmore, and 000 in the respective text fields
5. select teacher then select create account
6. enter "CS 180" in the create course field and select create course
7. close the program, leaving the server running
8. run Client.java again and login with bdunsmore and 000 username and password
9. ensure the CS 180 course has remained visible

Result: Course CS 180 should be visible from teacher menu
Status: Passed

Test 3: Project 4 features: Quiz Creation and Grade View
1. run Server.java
2. run Client.java
3. select create account button
4. enter "Buster Dunsmore", bdunsmore, and 000 in the respective text fields
5. select teacher then select create account
6. enter "CS 180" in the create course field and select create course
7. select the course options button for newly created course
8. select create quiz
9. select yes to randomize options AND questions, and enter "Midterm" as the quiz name
10. select "Add questions" and enter 2 sample questions (1+1 a)1 b)2 c)3 d)4, 2+2 a)1 b)2 c)3 d)4)
11. logout of this teacher account once the quiz is created
12. select create account button
13. enter "Joe Smith", "jsmith", and "000" in the respective text fields
14. select student then select create account
15. select the enroll in a course button and enter "CS 180"
16. select the course options button for this newly enrolled course
17. select the take quiz button for the Midterm quiz
18. take the quiz, ensuring to select "submit" after the two questions
19. logout of this student account
20. log back into the bdunsmore account with password 000
21. select Course Options for CS 180
22. select View Course Grades to view the student's submission
23. select View submission and view each response
24. logout of the teacher account
25. close the client and the server
26. restart the server, then run the client and check for the data by loggin into student account and checking the grade

Result: student gradebook should display the grade for your quiz
Status: Passed

Test 4: threading
1. run Server.java
2. run Client.java
3. run an additional Client.java
4. in the first client, create a student account
5. in the second client, create a teacher account then create a course called "Math"
6. in the first client, select "Enroll" and view the created Math course
7. close the client and server

Result: student should have enrolled in "Math"
Status: Passed