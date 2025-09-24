## Project Overview

[cite_start]The **Campus Course & Records Manager (CCRM)** is a console-based Java application designed to help an institution manage its students, courses, and academic records[cite: 4]. [cite_start]This project demonstrates a wide range of core Java SE concepts and modern APIs through a menu-driven command-line interface (CLI)[cite: 11, 35].

## Features

* **Student Management**: Add, list, update, and deactivate students. [cite_start]Each student record includes an ID, registration number, full name, email, and enrollment status[cite: 17, 18].
* **Course Management**: Create, list, update, and deactivate courses. [cite_start]Courses have a code, title, credits, instructor, semester, and department[cite: 21, 22]. [cite_start]You can search and filter courses using the Java Stream API[cite: 23].
* [cite_start]**Enrollment & Grading**: Enroll or unenroll students in courses with business rules, such as maximum credit limits[cite: 25]. [cite_start]The system can record marks, compute letter grades, and calculate GPAs[cite: 26]. [cite_start]It also generates a transcript view for students[cite: 28].
* [cite_start]**File Operations**: Import student and course data from simple CSV-like text files and export current data to files[cite: 30, 31]. [cite_start]A backup command creates a timestamped folder of exported data[cite: 32].
* [cite_start]**Advanced Concepts**: The application showcases **OOP** principles (Encapsulation, Inheritance, Abstraction, Polymorphism), robust **exception handling** with custom exceptions, and design patterns like **Singleton** and **Builder**[cite: 12, 58, 78, 82]. [cite_start]It also uses the **NIO.2 API** for file operations and the **Date/Time API** for timestamps[cite: 12, 90, 94].

## How to Run

1.  **Prerequisites**: Ensure you have the **Java Development Kit (JDK)** installed. The project was built and tested with JDK 17.
2.  **Clone the Repository**:
    `git clone <your-repo-link>`
3.  **Navigate to the Project Directory**:
    `cd CCRM`
4.  **Compile the Code**: If you are not using an IDE, compile the Java files from the `src` directory.
5.  **Run the Application**:
    `java edu.ccrm.cli.Main`
    This will launch the menu-driven CLI.

---

## Java Platform Explained

### Evolution of Java

* **1995**: Java 1.0 (JDK 1.0) is released by Sun Microsystems.
* **1998**: J2SE 1.2 is released, introducing the Java Collections Framework.
* **2004**: J2SE 5.0 introduces generics, enums, and autoboxing.
* **2014**: Java 8 introduces Lambdas and the Stream API.
* **2017**: Java 9 introduces the Java Platform Module System (JPMS).
* **2021**: Java 17, a Long-Term Support (LTS) release, is published.

### Java ME vs. Java SE vs. Java EE

| Feature | [cite_start]Java ME (Micro Edition) [cite: 43] | [cite_start]Java SE (Standard Edition) [cite: 43] | [cite_start]Java EE (Enterprise Edition) [cite: 43] |
| :--- | :--- | :--- | :--- |
| **Purpose** | [cite_start]Building applications for mobile and embedded devices[cite: 43]. | [cite_start]Developing desktop, console, and applet applications[cite: 43]. | [cite_start]Creating large-scale, distributed enterprise applications[cite: 43]. |
| **APIs** | [cite_start]Limited set of APIs[cite: 43]. | [cite_start]Core Java APIs (Collections, Streams, I/O)[cite: 43]. | [cite_start]Extensive APIs for web services, EJBs, etc.[cite: 43]. |
| **Example** | [cite_start]Simple mobile games or utilities[cite: 43]. | [cite_start]This CCRM application[cite: 4, 11]. | [cite_start]Web servers (Apache Tomcat), enterprise systems[cite: 43]. |

### JDK, JRE, and JVM

* **JVM (Java Virtual Machine)**: The core component that executes Java bytecode. [cite_start]It's the engine that runs your Java program[cite: 44].
* **JRE (Java Runtime Environment)**: Includes the JVM, the Java Class Library, and other supporting files. [cite_start]It provides the environment needed to run a Java program[cite: 44].
* **JDK (Java Development Kit)**: The complete kit for Java developers. It contains the JRE plus development tools like the compiler (javac), debugger, and others. [cite_start]You need the JDK to develop, compile, and run Java programs[cite: 44].

### Windows Install & Eclipse Setup

_Please refer to the `screenshots` folder in the repository for visual guides on:_
* [cite_start]_Installing the JDK and verifying the installation with `java -version`_[cite: 45, 139].
* [cite_start]_Creating and configuring the Eclipse project_[cite: 46, 140].
* [cite_start]_Screenshots of the program's menus, operations, and generated export/backup folders_[cite: 141, 142].

---

## Technical Demonstrations

This table maps project requirements to specific files or methods where they are implemented.

| Syllabus Topic | Location in Code |
| :--- | :--- |
| **Encapsulation** | [cite_start]`edu.ccrm.domain.Student` (private fields, getters/setters) [cite: 59] |
| **Inheritance** | [cite_start]`edu.ccrm.domain.Student` and `edu.ccrm.domain.Instructor` (extend `Person` abstract class) [cite: 60] |
| **Polymorphism** | [cite_start]`edu.ccrm.cli.TranscriptService` (`printTranscript` method using `toString()` overrides) [cite: 28, 62] |
| **Singleton Pattern** | [cite_start]`edu.ccrm.config.AppConfig` [cite: 80] |
| **Builder Pattern** | [cite_start]`edu.ccrm.domain.Course.Builder` or `edu.ccrm.service.TranscriptService.Builder` [cite: 81] |
| **Custom Exceptions** | [cite_start]`edu.ccrm.exceptions.DuplicateEnrollmentException`, `edu.ccrm.exceptions.MaxCreditLimitExceededException` [cite: 86] |
| **NIO.2 API** | [cite_start]`edu.ccrm.io.BackupService` (`copy` and `walk` methods) [cite: 32, 91] |
| **Java Streams** | [cite_start]`edu.ccrm.service.CourseService` (`search` method with filters) [cite: 23, 93] |
| **Enums with fields** | [cite_start]`edu.ccrm.domain.Semester` and `edu.ccrm.domain.Grade` [cite: 27, 74] |
| **Recursion** | [cite_start]`edu.ccrm.util.RecursiveUtils` (e.g., method to compute directory size) [cite: 33] |

### Enabling Assertions

[cite_start]To run the application with assertions enabled (e.g., to check for non-null IDs), use the `-ea` flag when running the program[cite: 89, 137].
