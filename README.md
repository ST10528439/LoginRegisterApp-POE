# LoginRegisterApp-POE
Added stored messages, search, delete, longest message and report+ unit tests

# How to run the project
Clone the repository
Open in NetBeans IDE
Execute application and then run files inside
Execute Unit Tests
## Project Structure

```text
src/
├── main/java/com/mycompany/logintegisterapp/
│   ├── LoginRegisterApp.java    # Main entry point and console menu flow
│   ├── Login.java               # Registration and login validation logic
│   ├── Message.java             # Message creation, hashing, and JSON I/O
│   └── MessageManager.java      # Parallel arrays, search, delete, and reporting
└── test/java/com/mycompany/logintegisterapp/
    ├── LoginTest.java           # Unit tests for registration and login (Part 1)
    ├── MessageTest.java         # Unit tests for message validation and hashing (Part 2)
    └── MessageManagerTest.java  # Unit tests for arrays, JSON loading, and reports (Part 3)
