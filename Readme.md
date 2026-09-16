# Campus Course & Records Manager (CCRM)

## 📖 Project Overview
Campus Course & Records Manager (CCRM) is a **Java SE console-based application** that helps institutes manage:
- 👩‍🎓 Students (create/update, enroll/unenroll, transcripts)
- 📘 Courses (create/update, search, assign instructors)
- 📝 Enrollments & Grades (record marks, compute GPA, generate transcripts)
- 📂 File Utilities (import/export CSV, recursive backups, reports)

It demonstrates **Java OOP, NIO.2 file I/O, Streams, Date/Time API, exceptions, enums, design patterns (Singleton, Builder)**, and more.

---

📜 Evolution of Java (Brief Timeline)

1995: Java 1.0 released by Sun Microsystems
2004: Java 5.0 introduced Generics, Enums
2011: Oracle takes over Java
2014: Java 8 with Lambdas & Streams
2017: Java 9 modular system (Project Jigsaw)
2023+: Java 21 (LTS)


Java ME vs SE vs EE

Edition	:  Usage
Java ME :  Mobile & embedded devices
Java SE	:  Core platform for desktop & CLI apps
Java EE	: Enterprise apps (web servers distributed systems)



🔷JDK, JRE, JVM

JDK – Developer kit (compiler, debugger, libraries)
JRE – Runtime environment (to run Java apps)
JVM – Virtual machine that executes bytecode

Interaction:
Source Code (.java) → compiled by javac → Bytecode (.class) → runs on JVM inside JRE.


🖥️ Install Java on Windows

Download JDK from Oracle/OpenJDK
Install & set JAVA_HOME in Environment Variables

Verify:
java -version
javac -version


Eclipse IDE Setup

Install Eclipse IDE
File → New → Java Project → CCRM
Import src/ folder
Right-click CLIApp.java → Run As → Java Application


📑Mapping (Syllabus → Code)
Syllabus Topic	       File/Class
Encapsulation	       Student.java (private fields + getters/setters)
Inheritance	           Person.java → Student, Instructor
Abstraction	           Person.java (abstract methods)
Polymorphism	       TranscriptService.java using toString()
Singleton	           AppConfig.java
Builder	               Course.Builder
Exceptions	           DuplicateEnrollmentException.java
File I/O (NIO.2)	   ImportExportService.java
Recursion	           RecursionUtils.java
Enums	               Grade.java, Semester.java

✅ Assertions
Enable assertions when running:

java -ea -cp bin edu.ccrm.cli.CLIApp


##  How to Run
```bash
# Compile
javac -d bin src/edu/ccrm/cli/MainMenu.java src/edu/ccrm/cli/CLIApp.java src/edu/ccrm/domain/*.java src/edu/ccrm/service/*.java src/edu/ccrm/io/*.java src/edu/ccrm/util/*.java src/edu/ccrm/config/*.java

# Run
java -cp bin edu.ccrm.cli.CLIApp

# 📘 Usage Guide – Campus Course & Records Manager (CCRM)
by NIKHIL AGARWAL 25BAI10930

This guide explains how to *set up, run, and use* the Campus Course & Records Manager (CCRM) application.

---

## 🔧 Prerequisites

Before running this project, ensure the following are installed:

- *Java SE 17+* (or any latest Java SE version)  
  Verify installation:
  ```bash
  java -version

Git (to clone the repository)

Optional: Eclipse IDE or VS Code for editing/debugging



---

▶ Setup & Run

1. Clone the Repository

2. Compile the Source Code

javac -d bin src/edu/ccrm/cli/MainMenu.java src/edu/ccrm/cli/CLIApp.java src/edu/ccrm/domain/*.java src/edu/ccrm/service/*.java src/edu/ccrm/io/*.java src/edu/ccrm/util/*.java src/edu/ccrm/config/*.java

3. Run the Program

java -cp bin edu.ccrm.cli.CLIApp

---

📑 CLI Menu Overview

When you run the program, you’ll see:

===== Campus Course & Records Manager =====
1. Manage Students
2. Manage Courses
3. Enrollments & Grades
4. Import/Export Data
5. Backup & Reports
6. Print Transcript
7. Exit
Enter choice:


---

🔹 Functionalities

1️⃣ Manage Students

1. Add Student
2. List Students
3. Deactivate Student
4. Back


2️⃣ Manage Courses

1. Add Course
2. List Courses
3. Back


3️⃣ Enrollments & Grades

1. Enroll Student
2. Assign Grade
3. List Enrollments
4. Back


4️⃣ 4. Import/Export Data

1. Import All Data
2. Export All Data
3. Back


5️⃣ Backup & Reports

1. Create Backup Now
2. Show Reports
3. Back


6️⃣ Print Transcript

7️⃣ Exit 

Saves all data automatically.

Creates a final backup before closing.

---
## 📂 Data & Test Files

The data/ folder contains initial CSV files which serve as *test data* for the Campus Course & Records Manager (CCRM):

- data/students.csv → initial student records  
- data/courses.csv → initial course records  
- data/enrollments.csv → initial enrollment records

When the program runs:  
- It reads data from these files to populate the system.  
- Exported data is saved in the exports/ folder.  
- Backups are created in timestamped folders inside the backups/ folder.  

---
