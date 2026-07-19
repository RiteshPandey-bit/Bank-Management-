# 🎯 𝐁𝐚𝐧𝐤 𝐌𝐚𝐧𝐚𝐠𝐞𝐦𝐞𝐧𝐭 𝐒𝐲𝐬𝐭𝐞𝐦 — CLI (Python + MySQL)

> A clean, modular console-based Bank Management System built with Python and MySQL.  
> Evolved from a Class 12 GUI school project into a backend-focused CLI refactor for reliability, maintainability, and learning best practices. 🚀

---

✨ Features
- ✅ User registration & login (secure, fixed flow)  
- ✅ Collision-free unique account number generation  
- ✅ Deposit, withdrawal, and balance enquiry operations  
- ✅ Modular code (main.py, login_register.py, basic_features.py)  
- ✅ MySQL backend for persistent storage  
- ✅ Simple CLI — ideal for learning DB-backed Python apps

---
Table of Contents
- About
- Project Evolution
- Features
- Project Structure
- Requirements
- Setup (MySQL + Python)
- Database Schema (example)
- Run & Usage
- Notes & Limitations
- Contributing
- License
- Author & Contact

---
About
-------
This project demonstrates moving from a GUI-focused school submission to a robust, modular CLI application suitable for academic demonstration and learning. Focus is on backend design, clear separation of concerns, and safe account number generation.

Project Evolution
------------------
- Version 1.0 — School Project (GUI)
  - Tkinter-based single-file app
  - Random account number generation (possible collisions)
  - User and employee modes
- Version 2.0 — College Refactor (CLI)
  - Modular architecture and clean separation:
    - main.py
    - login_register.py
    - basic_features.py
  - Fixed authentication flow
  - Guaranteed unique account number generation
  - User-only mode
  - Removed GUI to focus on DB and architecture

Key Features ✨
--------------
- Registration & login with password handling
- Unique account number generation (no collisions)
- Deposit / Withdraw / Balance enquiry
- Simple, guided CLI prompts
- MySQL integration for persistent storage

Project Structure
-----------------
```
bank-management-python/
│
├── main.py
├── login_register.py
├── basic_features.py
├── requirements.txt
└── README.md
```

Requirements
-------------
- Python 3.8+
- MySQL Server (5.7+ / 8.x recommended)
- Python dependencies:
  - Listed in requirements.txt — install with:
  ```
  pip install -r requirements.txt
  ```

Run & Usage
-----------
1. Install dependencies:
   ```
   pip install -r requirements.txt
   ```

2. Ensure MySQL is running and database + tables are created.

3. Run the CLI:
   ```
   python main.py
   ```

4. Follow the on-screen prompts to register a new user, login, deposit, withdraw, and check balance.

Account Number Generation
--------------------------
The project uses a deterministic / collision-checked scheme when generating account numbers:
- It ensures uniqueness by checking the DB before accepting a number.
Example flow:
- Register -> system generates an account number -> inserts into users table with initial balance 0.00.

Recommended Improvements
-------------------------
- Use environment variables for DB credentials (dotenv)
- Add stronger password hashing (bcrypt)
- Add transaction logs table for audit/history
- Add tests (unit + integration)
- Optionally reintroduce a Web UI or REST API layer for modern front-ends

Contributing ✍️
---------------
Contributions are welcome! Please:
- Fork the repository
- Create a feature branch: `git checkout -b feature/your-feature`
- Commit changes: `git commit -m "Add awesome feature"`
- Open a pull request with a clear description of changes

License
--------
This project is provided for educational purposes. You can apply a license as you prefer — MIT is recommended:
```
MIT License
Copyright (c) 2025 Ritesh Pandey
```
-------------------------------
Contact / Author
-----------------
Ritesh Pandey   
This project was originally a school GUI project and later refactored during college into this CLI-based, modular system. 🙌

Acknowledgements
-----------------
Thanks to everyone learning, refactoring, and focusing on clean backend design. This repo is a teaching artifact — adapt, improve, and learn!
