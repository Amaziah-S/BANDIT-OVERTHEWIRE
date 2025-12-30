Bandit Level 01 → Level 02

🎯 Objective
Read a file with a special filename to retrieve the password.

🧭 Quick Action Summary

Login as bandit1

Handle special filename

Read password file

🔑 Credentials Provided

Username: bandit1

Password: ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If

🔍 Method of Solve

The password is stored in a file named -.

Since - is treated as stdin, it must be accessed using a relative path.

🧪 Steps Followed

List files

Read the file using ./-

🧪 Commands Used

ls

cat ./-

🧩 Command Purpose

cat ./-	Reads file named -

<img width="471" height="102" alt="image" src="https://github.com/user-attachments/assets/e2a2f6d7-3a11-4c92-b8ac-356389bc9556" />


🔑 Next Level Password

263JGJPfgU6LtdEvgfWU1XP5yac29mFx

🔐 Concept Learned

Handling special characters in filenames.

🛡️ Security Insight

Improper filename handling can cause command misuse.
