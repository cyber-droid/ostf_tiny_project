Library Management System
A beginner-friendly, object-oriented Command-Line Interface (CLI) Library Management System built using pure Python 3.

📖 Project Description
The Library Management System is a modular Python mini-project designed for students and beginners to understand real-world Object-Oriented Programming (OOP), modular file architecture, in-memory data structures, and CLI menu handling without depending on external libraries.

✨ Features
Book Management:

Add new books with unique IDs, titles, and authors.
View all registered books with live availability statuses (Available / Issued).
Case-insensitive search across book titles and authors.
Member Management:

Register new members with unique Member IDs and full names.
View all registered members in a formatted table.
Book Issue:

Issue available books to registered members.
Enforces business rules: prevents issuing non-existent books, unregistered members, or books already borrowed.
Automatically timestamps the issue transaction.
Book Return:

Return borrowed books back to the library.
Instantly updates status back to Available.
Prevents returning books that were not currently issued.
Issued Books Tracking:

View a detailed list of all currently issued books showing Book ID, Title, Member ID, Member Name, and exact Issue Date & Time.
Input Validation & Error Handling:

Prevents empty inputs for IDs, titles, author names, and member names.
Prevents duplicate book IDs and member IDs.
Handles invalid numeric and string menu selections gracefully without crashing.
Clean handling of interruptions (Ctrl+C).
🛠️ Technologies Used
Language: Python 3 (Tested on Python 3.7+)
Paradigm: Object-Oriented Programming (OOP)
Dependencies: None (Uses only Python Standard Library: sys, datetime)
Storage: In-memory hash maps (Python dictionaries)
📁 Project Structure
LibraryManagementSystem/
│
├── main.py        # User interface, interactive menu loop, and CLI workflows
├── books.py       # Book class definition and status tracking methods
├── members.py     # Member class definition
├── library.py     # Library class containing core business logic and validations
└── README.md      # Comprehensive project documentation
Module Responsibilities
books.py: Encapsulates book attributes (book_id, title, author, is_issued, issued_to, issue_date) and state transitions (issue(), return_book(), get_status()).
members.py: Encapsulates library member data (member_id, name).
library.py: Core controller class that coordinates books and members. Maintains collections using fast dictionary lookups, enforces validation rules, and isolates business logic from the user interface.
main.py: CLI view layer that interacts with the terminal user, presents the menu, collects inputs, and invokes library services.
🚀 How to Run the Project
Option A: From Antigravity / Any Terminal
Open PowerShell or Command Prompt.
Navigate to the project directory:
cd C:\Users\SHIVANI\.gemini\antigravity\scratch\LibraryManagementSystem
Run the application:
python main.py
(Alternatively, run directly with the full path:)

python C:\Users\SHIVANI\.gemini\antigravity\scratch\LibraryManagementSystem\main.py
💡 Example Usage
When you run python main.py, you will see:

=====================================
===== LIBRARY MANAGEMENT SYSTEM =====
=====================================
1. Add Book
2. View Books
3. Search Book
4. Register Member
5. View Members
6. Issue Book
7. Return Book
8. View Issued Books
9. Exit
=====================================
Enter your choice (1-9): 
Step-by-Step Sample Session:
View Existing Books:

Enter 2
You will see pre-seeded books (The Great Gatsby, 1984, etc.).
Add a New Book:

Enter 1
Enter Book ID: B105
Enter Title: Python Crash Course
Enter Author: Eric Matthes
Output: Success: Book 'Python Crash Course' (ID: B105) added successfully!
Register a Member:

Enter 4
Enter Member ID: M004
Enter Full Name: David Miller
Output: Success: Member 'David Miller' (ID: M004) registered successfully!
Issue a Book:

Enter 6
Enter Book ID: B105
Enter Member ID: M004
Output: Success: Book 'Python Crash Course' (ID: B105) issued to David Miller (ID: M004).
View Issued Books:

Enter 8
Displays table showing B105 borrowed by M004 (David Miller) with date and time.
Return a Book:

Enter 7
Enter Book ID: B105
Output: Success: Book 'Python Crash Course' (ID: B105) returned successfully.
Exit:

Enter 9
Output: Thank you for using the Library Management System. Goodbye!
🔮 Future Improvements
Persistent Storage: Integrate SQLite or JSON file storage so data is saved across app restarts.
Due Dates & Fines: Add loan periods (e.g. 14 days) and calculate late return penalty fees.
Member Borrow Limit: Enforce a maximum number of active borrowed books per member (e.g., maximum 3 books).
GUI or Web Interface: Build a graphical desktop app with Tkinter / PyQt or a web app with Flask / FastAPI.
