📘 Bandit Level 02 → Level 03

🎯 Objective

Log in to the Bandit game and read a file with spaces in its name to obtain the password for the next level.

🧭 Quick Action Summary

Login as bandit2

List files

Identify the file with spaces

Read the file

🔑 Credentials Provided

Username: bandit2

Password: 263JGJPfgU6LtdEvgfWU1XP5yac29mFx

🔍 Method of Solve

The password is stored in a file named spaces in this filename.
Since spaces separate command arguments, the filename must be enclosed in quotes to be accessed correctly.

🧪 Steps Followed

Logged in as bandit2

Listed files in the directory

Identified the file with spaces in its name

Used quotation marks to read the file

Retrieved the password

🧪 Commands Used
ls
cat -- "--spaces in this filename--"

🧩 Command Purpose
Command	Purpose
ls	Lists files in the directory
cat -- "--spaces in this filename--"	Reads a file containing spaces in its name

<img width="641" height="316" alt="image" src="https://github.com/user-attachments/assets/1cd99359-6a6a-4970-842f-ef9253c43fef" />

🔑 Next Level Password

MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx

🧠 Explanation

The ls command reveals the file with spaces.
Quoting the filename allows cat to correctly read its contents and display the password.

🔐 Concept Learned

Handling filenames with spaces using quotation marks in Linux.

🛡️ Security Insight

Using spaces in filenames can cause command errors and should be avoided when possible.
