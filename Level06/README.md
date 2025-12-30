📘 Bandit Level 06 → Level 07

🎯 Objective

Log in to the Bandit game and locate the password file owned by a specific user and group to retrieve the next level password.

🧭 Quick Action Summary

Login as bandit6

Search the entire filesystem

Filter files by owner and group

Read the correct file

🔑 Credentials Provided

Username: bandit6

Password: HWasnPhtq9AVKe0dmk45nxy20cvUa6EG

🔍 Method of Solve

The password is stored somewhere on the system.
The file is:

Owned by user bandit7

Owned by group bandit6

Exactly 33 bytes in size

The find command is used to locate the file matching these conditions.

🧪 Steps Followed

Logged in as bandit6

Searched the root directory

Filtered files by owner, group, and size

Ignored permission errors

Read the correct file

🧪 Commands Used

ls -la

find / -size 33c -group bandit6 -user bandit7 2>/dev/null

cat /var/lib/dpkg/info/bandit7.password



🧩 Command Purpose

find	Searches files by ownership and size

2>/dev/null	Suppresses permission denied errors

cat	Displays file contents


📸 Screenshot Evidence
<img width="847" height="281" alt="Screenshot 2025-12-26 125005" src="https://github.com/user-attachments/assets/f97d4740-43f2-48d3-a327-e9329e1e808c" />


🔑 Next Level Password

morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj

🧠 Explanation

The find command scans the entire system and filters files based on user, group, and size.
Redirecting errors keeps the output clean.
Once found, cat is used to read the password.

🔐 Concept Learned

Searching system-wide files using ownership and permission attributes.

🛡️ Security Insight

Incorrect file ownership and permissions can unintentionally expose sensitive credentials
