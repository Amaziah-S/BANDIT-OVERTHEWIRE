📘 Bandit Level 17 → Level 18

🎯 Objective

Log in to the Bandit game and retrieve the next level password by finding the difference between two files.

🧭 Quick Action Summary

Login as bandit17

Locate the two text files

Compare the files

Extract the line that differs

Retrieve the password

🔑 Credentials Provided

Username: bandit17

Password: EReVavePLFHtFlFsjn3hyzMlvSuSAcRD

🔍 Method of Solve

The home directory contains two files:

passwords.old

passwords.new

The password for the next level is the only line that differs between these two files.

Using the diff command highlights the changed line.

🧪 Steps Followed

Logged in as bandit17

Listed files to locate both password files

Compared the files

Identified the changed line

Retrieved the password

🧪 Commands Used

ls

diff passwords.old passwords.new

🧩 Command Purpose

ls	Lists files in the current directory

diff passwords.old passwords.new	Shows differences between two files

📸 Screenshot Evidence

<img width="551" height="276" alt="Screenshot 2025-12-27 180758" src="https://github.com/user-attachments/assets/9291ed9c-b6c7-40a5-9f32-d1cf699697b5" />


🔑 Next Level Password

x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO

🧠 Explanation

Both files are nearly identical

Only one line has changed

diff outputs the modified line

That line contains the password for bandit18

This avoids manually checking large files.

🔐 Concept Learned

The diff command is useful for identifying changes between files quickly.

🛡️ Security Insight

Storing passwords in versioned text files is unsafe.
Sensitive data should be encrypted and access-controlled.
