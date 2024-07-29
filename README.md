# Application.TutorTube.Service
This is Online Learning Platform Service Backend
# Online-Learning-Platform
Online Learning Platform 
Online Learning Platform Features
User Management:

User registration and authentication.
User management which allows them to change contact information(username, email and password) as well.
Different roles should be assigned to users (like a student and a teacher) and permissions for each role need to be set.
Course Management:

Instructors would have the flexibility to design courses and make them accessible.
The search/filtering option is available on the course level for the users.
Registration management, enables the users to enroll and start using the learning management system.
Course progress tracking can be undertaken for the enrolled users.
Content Management:

Apart from its hosting, uploading and the management of the distinguishable types of content such the files [instruction], audio or the video audiovisual content, for every course.
Providing instructional materials in a modular or sectional format suitable for self-paced and structured learning.
Assessment and Evaluation:

Instructor’s Tasks Related with Quizzes: Creating and Managing them.
Automatic reviewing of the quizzes and a quick response to the students after they have taken quizzes.
Feedback to students in the form of scores after evaluation and completion of quiz exercise.
Progress Tracking and Reporting:

Letting users keep track of their courses’ enrollment status and completion, and display of score for quiz via the progress dashboards to them.
The educational apps should be able to produce reports for teachers which should include the student’s performance and engagement metrics.
Payment and Subscription:

Integration with payment gateways that allows courses to be purchased and subscription plans to be handled.
Consumer payment and transaction management are the key elements that include consumer payment history history tracking.
Entities and Attributes for Online Learning Platform
1. User: Stores information about registered users.

UserID (Primary Key): Unique identifier for each user.
Username: Name of the user.
Email: Email of the user.
Password: Password of the user.
UserType: Type of the user like student, instructor.
2. Course: Contains the details about the course.

CourseID (Primary Key): Unique identifier for each course.
CourseName: Name of the course.
Description: Description of the course.
Price: Price of the course.

3. CourseContent: Contains the details about course content.

ContentID (Primary Key): Unique identifier for each content.
CourseID (Foreign Key): Reference to the course.
ContentType: Type of the content like video, document.
4. Enrollment: Details of the enrollment of courses.

EnrollmentID (Primary Key): Unique identifier for each enrollment.
UserID (Foreign Key): Reference to the user.
CourseID (Foreign Key): Reference to the course.
EnrollmentDate: Date of enrollment.
CompletionStatus: Status of course completion.
5. Payment: Stores information about payments made by users.

PaymentID (Primary Key): Unique identifier for each payment.
UserID (Foreign Key): Reference to the user.
PaymentDate: Date of the payment.
Amount: Amount of the payment.
PaymentMethod: Method of the payment like from UPI, credit card.
6. Result: Contains details of the results of quizzes.

ResultID (Primary Key): Unique identifier for each result.
UserID (Foreign Key): Reference to the user.
CourseID (Foreign Key): Reference to the course.
QuizID (Foreign Key): Reference to the quiz.
Score: Score in the result.
7. Quiz: Stores the details about the quiz.

QuizID (Primary Key): Unique identifier for each quiz.
CourseID (Foreign Key): Reference to the course.
QuizName: Name of the quiz.
Description: Description of the quiz.
TotalMarks: Total marks in the quiz.
Relationships between These Entities
1. User – Course Relationship:

One user can have multiple courses.(Many-to-Many)
A course can have multiple enrolled users.
2. User – Payment Relationship:

A user can make multiple payments.(One-to-Many)
Each payment is made by one user.
3. User – Result Relationship:

A user can have multiple results.(One-to-Many)
Each result associated with one user.
4. Course – Enrollment Relationship:

A course can have multiple enrollments.(One-to-Many)
Each enrollment is for one course.
5. Course – CourseContent Relationship:

A course can have multiple content items.(One-to-Many)
Each content item belongs to one course.
6. Course – Result Relationship:

A course can have multiple results.(One-to-Many)
Each result is for one course.
7. Result – Quiz Relationship:

