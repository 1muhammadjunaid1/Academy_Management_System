# Academy Management System

A desktop application built with Qt and C++ for managing day-to-day operations of an educational institution. It connects to a local MySQL database and provides a clean interface for handling students, attendance, marks, tasks, and fees: all in one place.

## What it does

The application is organized into multiple views, each focused on a specific area of academy management.

**Student Management**: Add, edit, and delete student records including personal details, class, and profile photo. A live search bar lets you find any student instantly.

**Attendance**: Mark daily attendance for all students from a single table view. The system automatically calculates and updates each student's attendance percentage after every submission. A circular progress widget displays the percentage visually on each student's profile.

**Marks & Progress**: Assign marks to students per subject, test type, and class. A progress chart on each student's profile tracks academic performance across the semester by visualizing average monthly scores.

**Tasks**: Upload assignments and tests as PDFs with details like subject, type, class, and due date. Uploaded tasks are displayed in a list with a direct button to open the attached PDF.

**Fee Management**: Add monthly fee records for each student, track payment status, and mark fees as paid. Summary labels show total paid amount, outstanding balance, and last payment date.

**Teacher Section**: Dedicated pages for teacher information, salaries, and related records, accessible via a context menu.

## Tech Stack

- C++ with Qt framework (Qt Widgets, Qt SQL)
- MySQL via Qt's QMYSQL driver
- QMake build system

## Setup

1. Make sure MySQL is running locally and create a database named `Academy`.
2. Update the credentials in `mainwindow.cpp` inside `connectToDatabase()` to match your MySQL setup.
3. Open `Acedmy.pro` in Qt Creator and build the project.

The app expects tables for `students`, `attendance`, `marks`, `tasks`, and `fees`. You can find the schema in the `RE` and `Resocrces` folders.

## Notes

This was a semester project built to practice database integration with Qt. The focus was on building a functional, multi-page desktop app with real SQL queries rather than mock data.
