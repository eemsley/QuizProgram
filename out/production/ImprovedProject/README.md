# Project 05 shared directory for our team (062)

## To compile and run the project, first run the server class then run the client class. 

## Who submitted which part of the Project:
- Evan Emsley - submitted vocareum workspace 
- Harnish Modi - submitted presentation on brightspace 
- Joey Foutty - submitted report on brightspace 

## Classes: 

### Client.java
The client class takes the information of what the user is doing and sends that information to the server class. It uses the socket to do this and therefore it is very closely related to the server class. 
Course.java
Course class is for teachers because courses can only be created by teachers, however, students can enroll in courses. In this class there is the arrayList of quizzes and courseGrades, and the teacher object. There are getters and setters for each of these and there is also a string courseName so it can be accessed by students. This class is related to the student and teacher classes. 

### CourseGrades.java
The course grades class has an array list of the users and creates a new arrayList for the graded quizzes. It reads through the enrolled students and the quizzes that they took. Based on this information it adds a button to the GUI that has the score along with the information on the quiz, so the number of questions it had, etc. In this class a window and multiple panels were created to display this information on the GUI. A back button was also added to this part of the code. This is very closely related to the Quiz and GradedQuiz classes. 

### CreateAccountMenu.java
The CreateAccountMenu.java sets up the basis of the GUI. Here it creates a window to create an account and in that window is the option to enter their name,  username, and password, each with a text box of the same size. Then there is a button for the user to select if they are a teacher or a student. There is a back button and create account button, once the create account button is hit the user is automatically logged in and the information is sent and saved in the server. An error message occurs if one of the text boxes is empty. This class is related to the student, teacher, server, and user classes. 

### CreateQuiz.java
CreateQuiz class is in the teacher section and holds the GUIs for the teachers to create a quiz. The GUIs created in this class were a yes and no button if the teacher would like to randomize options, a yes and no button for if the teacher would like to randomize the questions, and a text box for the teacher to insert the name of the quiz they are creating. There is also a button for the teacher to add questions. If this is selected then the teacher is brought to another part of the code. There are also buttons on the lower panel to “cancel” and for a teacher to import a file on the lower right side. For the add questions there is an arrayList of added questions. A GUI here pops up with 5 text boxes; 4 for the options A-D and 1 for the correct answer input. If any of these texts are blank, an error message occurs and the teacher is required to re-enter the information. This section is all in a do while loop. This information is then sent to the server. This class is closely related to the teacher, Question, and Server class because the information is sent to the server and it is with the teacher as the user.  

### EditQuiz.java 
This class is where the teacher has the option to edit the quizzes that they have already created. It is similar to the CreateQuiz class in that it also has buttons fcrated with JLabels to Randomize the options with a Yes and No button, Randomize Questions with a Yes and No button. This also has the option to Update Quiz Name and finally there is a button to update the quiz name. Once this is selected by the user, the new information is saved and sent to the server. Similarly to the CreateQuiz class there is an error message if not all the information is entered by the user. Finally, at the end of this class there is a confirmation message that appears that tells the user the question set was replaced. This class is very similar to CreateQuiz class and is closely related to Server.java, Question.java, and Teacher.java. 

### FileCreateQuiz.java 
The FileCreateQuiz class is where the code is that allows the teacher to import a file for the quiz they are creating. It has the same information that the createQuiz class does so it has the teacher answer if they would like the questions to be randomized and if they would like the answers to be randomized with Yes and No answers. This is a boolean that was created and based on what the teacher enters, the new information is sent to the server class. Therefore, it is related to the teacher class, CreateQuiz class, and Server class. 

### GradedQuiz.java 
This class is for the quizzes that have been graded by teachers. It is then added to the student’s arraylists of grades and is displayed on their student gradebook. There is an arrayList questionPints which keeps track of how many points the student has earned. There is also a completed quiz object. A score int is created as well which is the total score of a quiz for that student. The toString formats it so it prints the student name, score, and the time of completion, along with the quiz name and quiz questions. This is related to the quiz and question classes because those are needed in order to grade the quiz. Teachers use this class because they are the only users who can grade quizzes.

### MainMenu.java 
The Main class is where the initial GUI is held. It has textboxes for the user to enter their username and password. Then there is a button to login and also a button to create an account if they do not already have one. If that is selected then the user is brought to the CreateAccount class. It calls the readFile method, stores all of the users and their data, calls the welcomeScreen method which allows a chain of methods allowing for the program to run. When the welcome screen is exited after logging out, the data is stored in the files studentinfo.txt and teacherinfo.txt. This is closely related to all of the other classes as this is the start of where the user enters. Based on the information entered here the user can be brought to any of the other classes. 

### Question.java 
The Question class is created so it can be added to a quiz. It has an ArrayList called options, a String question, and a quiz object. There are getters and setters for all of these variables. There is also a toString which formats the format of the question so each question is uniform. Each question has 4 options as answers. This class is closely related to Quiz because the questions are part of a Quiz.

### Quiz.java 
The Quiz class holds the information for the quizzes taken and created by the students and teachers. It contains the questions in the quizzes. There is an arrayList of questions, a course object, quizname, and boolean randomized.  The arraylist stores the questions in the quiz so that it can be saved and taken by the student. The boolean randomized allows for the option of the questions in the quiz to be random. This is related to the Question class because it has the questions for the quiz. It is also related to the GradedQuiz class where the grades from those quizzes are. The course class is also related because to have a quiz it must be under a specified course.

### QuizTaker.java 
The QuizTaker class is for the student users and it will iterate through each question once the nextButton is clicked. Once the student is done taking the quiz then there is a message that pops up showing that there was a complete submission. The information is then sent to the server so that the teacher can see what the student did and can view the grade and submissions of those enrolled in their course. This is very closely related ot the Quiz, server, and gradedQuiz classes. 

### Server.java 
This class is where all of the information is sent to and stored. It has a socket that is used to connect the information. There is a loop that consistently looks for other users. If there is a new user then it creates a thread for that user and that is done in the loop. This class also looks for the codes that are sent with the information and there are several if statements that say if a certain code is sent then it tells it what the information to be added to. For example, if a “CS” code is found then it should be added to the student arrayList and written to the users. It iterates through each option and has nested for loops in order to read through all the possibilities. This is related to all of the classes because all of the information that is taken is sent to this socket to be read and given back to. 

### Student.java
The student class is for the users that create a student account. Similar to the teacher class, it extends the user class. There is an ArrayList of courses they are enrolled in, an ArrayList of quizzes they have completed, and an ArrayList grades which holds their graded quizzes.
The student class also has a name, username, and password from the User class. There is a boolean dropCourse that removes the selected course from the arraylist courses and “drops the course

### StudentCourseMenu.java
This class holds the GUIs for the Student Course Menu. It pops up a display with button options of viewing assigned quizzes. It gets the course name that they are in and sends the information that is needed for that class. Like usual there is also a button to logout and to go back to the student menu. Once the student enters the information in what course they would like this information is sent to the server. This class is related to the student, server, and course class. 

### StudentGradesMenu.java
The SutdentGradesMenu class is where the menu for the student grades pops up for the user. If the student has taken quizzes then they are atumiatcally graded and this is where they can see their grades for the quizzes that they took. This class gets the name of the quiz and student to display. There is also a back to student menu as an option and if they have not taken any grades then a message shows up saying that there are “No Grades Yet!”. This class is closely related to the student, gradedQuiz, server, and QuizTaker class. 

### StudentMenu.java
The studentMenu is where the student has options to choose what they would like to do. In this class there is a button to edit the account, logout, view student grades, and have a new course. It gets the information for the student based on their username and full name and it gets the information of courses that they have already enrolled in and displays that on the screen. There is also an option to edit their account, similar to the teacherMenu class. This information is also sent to the server. The classes that this is related to are the StudentCourse, student, server, and client classes. 

### StudentViewGrades.java
This is the class where the student can see the grades to the quizzes they took. Similar to the other classes, there is a button to go back to the student menu, one to update the score, and it displays the amount of points the student has for each quiz they took. There is a scrollbar so if there are multiple quiz grades, they have the mobility to see all of them. This class is closely related to the student, studentGradesMenu, studentCourse, and server classes. 

### Teacher.java
This class extends the user class. It is for when users create a Teacher account. There is an arrayList of courses and an arrayList of quizzes which store the courses and quizzes that teachers can create. This class uses the Teacher’s name, username, and password from the user class. There is also a boolean dropCourse which reads through the courses, finds the course, and removes it from the arrayList.

### TeacherCourseMenu.java
The teacherCourseMenu is where the teachers can see the information on the courses that they have created. There is a button to create a new quiz, to delete a quiz, to name a quiz, and to edit an already existing quiz. There is also the option to go back to the teacher menu and to logout. Then there is a button to view the course grades and if clicked, this displays the course grades for all the students who took their quiz. If any of this information is edited, it is sent to the server class where it is saved. This class is closely related to almost all of the classes because it gets information from the students who are enrolled and sends information to the server and client class. 

### TeacherMenu.java
The teacher menu class is where the GUIs are built to show the teachers all of their options. The options for the teachers in this class are to logout, go back, edit account, and create a new account. There is an error message that occurs if Depending on what the teacher inputs, it is given a piece of code, for example “NC” that is seany information is missing but then it is sent to the server. This way it is recognized in the server and in that class it will know what to do. This class is very closely related to the server class. 

### TeacherViewGrade.java
This class allows the teachers to see the grades of all of their students. It iterates through the graded quizzes and the questions and then it adds a button saying the correct answer and the answer that the student put. This class also has a back button and a button that will update the score. This class is closely related to the quiz, server, student, studentGrades, and teacher classes. 

### User.java
The User class is the simplest version of an account. A user (either teacher or student) is required to continue doing anything in the program. A user has a name, username, and password which are all strings. There are getters and setters for each of these strings. 
This is the superclass of the student and teacher class.
