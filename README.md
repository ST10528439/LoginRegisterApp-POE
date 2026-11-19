# LoginRegisterApp-POE
Added stored messages, search, delete, longest message and report+ unit tests

# Features

## Part 1: Registration & Authentication (Login.java)
- Username Validation: Must contain an underscore (_) and be no longer than 5 characters.
- Password Complexity: Must be at least 8 characters long and include at least one uppercase letter, one digit, and one special character.
- Cell Phone Validation: Validates South African mobile numbers formatted with the international code (+27 followed by 9 digits).
- Login Verification: Authenticates users against captured credentials and displays personalized login status messages.

## Part 2: Messaging & Hashing (Message.java)
- Message Validation: Enforces a 250-character limit and verifies recipient cell phone numbers.
- Unique ID & Hash Generation: Automatically generates a 10-digit message ID and formats a unique hash (<first 2 digits of ID>:<message number>:<FIRSTWORDLASTWORD>).
- Message Actions: Allows users to *Send, **Disregard, or **Store* messages to messages.json using org.json.
- 
## Part 3: Array Management & Reporting (MessageManager.java)
- Parallel & Category Arrays: Tracks sent, stored, and disregarded messages alongside their IDs, hashes, and recipients.
- JSON Reloading: Reads previously saved messages from messages.json on startup.
  # Stored Message Sub-Menu:
  1. Display sender and recipient for all stored messages.
  2. Identify and display the longest stored message.
  3. Search for a message by its 10-digit Message ID.
  4. Search for all sent or stored messages associated with a recipient's cell number.
  5. Delete a message using its Message Hash (and sync changes back to messages.json).
  6. Generate full formatted reports for sent and stored messages.

### Project Structure

```text
src/
├── main/java/com/mycompany/logintegisterapp/
│   ├── LoginRegisterApp.java    # Main entry point and console menu flow
│   ├── Login.java               # Registration and login validation logic
│   ├── Message.java             # Message creation, hashing, and JSON I/O
│   └── MessageManager.java      # Parallel arrays, search, delete, and reporting
└── test/java/com/mycompany/logintegisterapp
    ├── LoginTest.java           # Unit tests for registration and login (Part 1)

# How to run the project
Clone the repository
Open in NetBeans IDE
Execute application and then run files inside
Execute Unit Tests

    ├── MessageTest.java         # Unit tests for message validation and hashing (Part 2)
    └── MessageManagerTest.java  # Unit tests for arrays, JSON loading, and reports (Part 3)
