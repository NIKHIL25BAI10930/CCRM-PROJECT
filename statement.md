# Project Statement — Campus Course & Records Manager (CCRM)
 
## Problem Statement
 
Academic institutes typically track student records, course catalogs, enrollments, and grades across scattered spreadsheets or paper files. This makes it hard to enroll a student in a course, compute GPA, generate a transcript, or back up records without manual, error-prone work. CCRM solves this by giving an institute a single Java SE console application that stores student, course, and enrollment data together, computes grades and GPA automatically, and can import, export, and back up that data through the file system.
 
## Scope of the Project
 
**In scope**
- Managing student records: creation, updates, and deactivation.
- Managing course records: creation, updates, search, and instructor assignment.
- Enrolling and unenrolling students in courses, and recording grades.
- Computing GPA and generating transcripts.
- Importing and exporting data as CSV files.
- Creating recursive backups and generating reports.
- Running entirely as a menu-driven command-line interface (CLI) on Java SE 17+.
**Out of scope**
- No graphical or web-based interface; the application is console-only.
- No persistent database; data is held in memory during a session and read from or written to CSV files rather than a relational database.
- No authentication, multi-user accounts, or role-based access control.
- No multi-institution or multi-tenant support — each run of the application manages one institute's data set.
## Target Users
 
- **Institute administrators**, who add and manage student and course records, oversee enrollments, and run backups and reports.
- **Instructors**, whose course assignments and student grade data are tracked within the system.
- **Students**, whose records, enrollments, and transcripts the system stores and generates, even though they do not interact with the CLI directly.
- **Java learners and instructors**, since the project is also structured to demonstrate core Java SE concepts — OOP, NIO.2 file I/O, Streams, the Date/Time API, exceptions, enums, and design patterns such as Singleton and Builder — mapped to specific classes in the codebase.
## High-Level Features
 
- 👩‍🎓 **Student management** — add, update, deactivate, and list students.
- 📘 **Course management** — add, update, search, and assign instructors to courses.
- 📝 **Enrollments & grades** — enroll or unenroll students, assign grades, compute GPA, and list enrollments.
- 📂 **File utilities** — import and export data in CSV format, with initial test data provided in the `data/` folder.
- 🗂️ **Backup & reports** — create timestamped backups and generate summary reports.
- 🧾 **Transcripts** — print a full academic transcript for a student.
- ⌨️ **CLI-driven workflow** — a numbered menu system (Manage Students, Manage Courses, Enrollments & Grades, Import/Export Data, Backup & Reports, Print Transcript, Exit) drives all functionality, with data saved automatically and a final backup created on exit.
 
