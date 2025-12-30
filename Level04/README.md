📘 Bandit Level 04 → Level 05

🎯 Objective

Log in to the Bandit game and locate the human-readable file to retrieve the password for the next level.

🧭 Quick Action Summary

Login as bandit4

Navigate to the inhere directory

Identify the readable file

Read the file

🔑 Credentials Provided

Username: bandit4

Password: 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ

🔍 Method of Solve

The password is stored in one of several files inside the inhere directory.
Only one file contains human-readable text.
The file command helps identify readable files.

🧪 Steps Followed

Logged in as bandit4

Moved into the inhere directory

Checked file types

Identified the readable file

Read the file to obtain the password

🧪 Commands Used
ls
cd inhere
file ./*
cat ./-file07

🧩 Command Purpose
Command	Purpose
ls	Lists directory contents
cd inhere	Enters the inhere directory
file ./*	Shows the type of each file
cat ./-file07	Displays the readable file content
📸 Screenshot Evidence

<img width="762" height="514" alt="Screenshot 2025-12-26 010847" src="https://github.com/user-attachments/assets/4de386e0-1463-437b-8d6d-ce7296bb8822" />


🔑 Next Level Password

4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw

🧠 Explanation

The file command identifies file formats.
The readable file is detected and opened using cat to retrieve the password.

🔐 Concept Learned

Identifying file types and handling filenames starting with special characters.

🛡️ Security Insight

Obscuring data among many files does not ensure security without proper access control.
