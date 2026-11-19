# LoginRegisterApp-POE
Added stored messages, search, delete, longest message and report+ unit tests

# How to run the project
Clone the repository
Open in NetBeans IDE
Execute application and then run files inside
Execute Unit Tests

## Project Structure

# Features

### Part 1: Registration & Authentication (Login.java)
- Username Validation: Must contain an underscore (_) and be no longer than 5 characters.
- Password Complexity: Must be at least 8 characters long and include at least one uppercase letter, one digit, and one special character.
- Cell Phone Validation: Validates South African mobile numbers formatted with the international code (+27 followed by 9 digits).
- Login Verification: Authenticates users against captured credentials and displays personalized login status messages.

### Part 2: Messaging & Hashing (Message.java)
- Message Validation: Enforces a 250-character limit and verifies recipient cell phone numbers.
- Unique ID & Hash Generation: Automatically generates a 10-digit message ID and formats a unique hash (<first 2 digits of ID>:<message number>:<FIRSTWORDLASTWORD>).
- Message Actions: Allows users to *Send, **Disregard, or **Store* messages to messages.json using org.json.



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
