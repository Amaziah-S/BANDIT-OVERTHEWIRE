📘 Bandit Level 19 → Level 20

🎯 Objective

Log in to the Bandit game and retrieve the next level password by using a SUID binary to run commands as another user.

🧭 Quick Action Summary

Login as bandit19

Locate the setuid executable

Use it to execute a command as bandit20

Read the password file

Retrieve the password

🔑 Credentials Provided

Username: bandit19

Password: cGWpMaKXVwDUNgPAVJbWYuGHVn9zl3j8

🔍 Method of Solve

The home directory contains a setuid binary named bandit20-do.

This program allows executing commands as the bandit20 user.

By using this binary to run cat on the password file, the next level password can be read.

🧪 Steps Followed

Logged in as bandit19

Listed files to identify the SUID binary

Executed the binary with cat

Retrieved the password for bandit20

🧪 Commands Used

ls

./bandit20-do cat /etc/bandit_pass/bandit20

🧩 Command Purpose

ls	Lists files in the directory

./bandit20-do	Executes a command as user bandit20

cat /etc/bandit_pass/bandit20	Displays the next level password

📸 Screenshot Evidence

<img width="931" height="270" alt="Screenshot 2025-12-27 182814" src="https://github.com/user-attachments/assets/3cb131ba-02bd-4b89-98dc-2fbb0c2b30dc" />


🔑 Next Level Password

0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO

🧠 Explanation

bandit20-do has the setuid bit set

It runs with bandit20’s privileges

This allows access to files normally restricted

The password file becomes readable

🔐 Concept Learned

SUID binaries execute with the file owner’s privileges and must be handled carefully.

🛡️ Security Insight

Improperly configured SUID programs can lead to privilege escalation.
They should be audited and restricted whenever possible.
