🎓 Smart Campus AI Platform

AI-powered smart classroom system for hackathons – featuring face recognition attendance, AI-driven teacher assessment, and dynamic classroom routine management to automate scheduling and enhance learning efficiency.

🚀 Project Overview

Smart Campus AI Platform is an innovative hackathon project under AI for Education, designed to optimize classroom management and evaluation in universities.

The project includes multiple AI-driven modules:

📸 AI Attendance Tracking – Automatically mark student attendance using face recognition

🧑‍🏫 AI Teacher Assessment – Evaluate teacher performance based on student engagement and reactions captured via classroom cameras

📅 Dynamic Routine System – Automatically allocate classrooms and manage schedules without conflicts

🖥️ Visual Representation – GUI/web dashboard to visualize schedules, attendance, and teacher assessment

This system reduces administrative workload, ensures fair assessment, and improves overall classroom efficiency.

🌟 Features
📌 AI Attendance Tracking (Python + OpenCV)

Real-time face recognition for attendance

Automatic logging into the database

Generates attendance reports per student and class

📌 AI Teacher Assessment (Python + Computer Vision)

Analyzes student engagement from CCTV footage

Measures attention, participation, and reactions

Produces unbiased teacher performance reports

📌 Dynamic Routine System (Java + PostgreSQL)

Automatically assigns classrooms based on availability

Prevents schedule conflicts

Supports multiple buildings and rooms

Integrates with GUI/web visualization

📌 Visual Representation (JavaFX / Web)

Displays timetable and schedules in a user-friendly format

Shows real-time AI-generated teacher and attendance stats

Easy for administrators and students to navigate

🛠️ Tech Stack
Module	Language/Tools	Description
AI Attendance	Python, OpenCV	Face recognition for attendance
Teacher Assessment	Python, OpenCV, NumPy	Analyze classroom engagement
Dynamic Routine	Java, JDBC, PostgreSQL	Automatic room allocation
Visualization	JavaFX / Web (HTML/CSS/JS)	GUI/dashboard for schedules
Database	PostgreSQL	Stores students, schedules, rooms, attendance
🗄️ Database Design

Room Table

Column	Type	Description
room_id	SERIAL	Primary Key
building	TEXT	Building Name
capacity	INT	Room Capacity

ClassSchedule Table

Column	Type	Description
schedule_id	SERIAL	Primary Key
course_name	TEXT	Name of the course
teacher_name	TEXT	Teacher name
day	TEXT	Day of the week
start_time	TIME	Start time
end_time	TIME	End time
room_id	INT	Foreign Key referencing Room

Attendance Table

Column	Type	Description
attendance_id	SERIAL	Primary Key
student_id	INT	Student ID
course_name	TEXT	Course Name
date	DATE	Date of attendance
status	BOOLEAN	Present/Absent

TeacherAssessment Table

Column	Type	Description
assessment_id	SERIAL	Primary Key
teacher_name	TEXT	Teacher Name
course_name	TEXT	Course Name
date	DATE	Assessment Date
engagement_score	FLOAT	AI computed score
💻 Installation & Setup
1️⃣ Clone the repository
git clone https://github.com/your-username/smart-classroom.git

2️⃣ Backend – Java (Dynamic Routine)

Open SmartClassroom in IntelliJ IDEA

Setup PostgreSQL and run SQL scripts to create tables

Update DBConnection.java with your credentials

Run Main.java to test room allocation

3️⃣ Python Modules – AI Attendance & Teacher Assessment
# Create virtual environment
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows

# Install dependencies
pip install opencv-python numpy pandas


Run attendance.py for face recognition attendance

Run teacher_assessment.py for automated engagement analysis

4️⃣ GUI / Web Dashboard

JavaFX (for desktop GUI) or simple HTML/CSS/JS (for web)

Connect to PostgreSQL database to fetch schedules, attendance, and assessment

📅 Usage
Dynamic Routine (Java)

Run Main.java

Input:

Course Name

Teacher Name

Day of the Week

Start & End Time (HH:MM format)

System allocates the first available room automatically

Output: Allocated Room ID or “No room available”

AI Attendance (Python)

Run attendance.py

Camera opens → captures faces

Attendance automatically logged in DB

Teacher Assessment (Python)

Run teacher_assessment.py

Analyze classroom footage

Engagement scores automatically saved in DB

🗂️ Project Structure
smart-classroom/
├── java/                # Dynamic Routine System
│   ├── src/
│   │   ├── Main.java
│   │   ├── dao/
│   │   ├── model/
│   │   └── util/
├── python/              # AI Modules
│   ├── attendance.py
│   └── teacher_assessment.py
├── gui/                 # Optional JavaFX/Web Dashboard
├── README.md
└── requirements.txt

🔧 How It Works

AI Attendance: Face recognition detects student faces → marks attendance

Teacher Assessment: Camera analyzes engagement → scores teachers objectively

Dynamic Routine: Java checks room availability → allocates room → saves in DB

Visualization: GUI displays schedules, attendance, and assessment data in real-time

🌈 Future Improvements

Web dashboard for easy access anywhere

AI optimization for room allocation based on capacity and proximity

More advanced engagement metrics for teachers

PDF/Excel export for schedules and attendance

👥 Contributors
Name	Role
Sami Azraf	Backend (Dynamic Routine), DAO, PostgreSQL
[Teammate 1]	AI Attendance (Python, Face Recognition)
[Teammate 2]	Teacher Assessment (Python, CV Analysis)
[Teammate 3]	GUI / Web Dashboard
[Teammate 4]	Project Coordination & Presentation
⚡ Hackathon Notes

Beginner-friendly but functional AI modules

Modular design: Java backend, Python AI, GUI/web dashboard

Demonstrates automation, AI integration, and visual representation
