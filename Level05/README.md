📘 Bandit Level 05 → Level 06

🎯 Objective

Log in to the Bandit game and locate the password file using specific file properties to retrieve the next level password.

🧭 Quick Action Summary

Login as bandit5

Navigate to the inhere directory

Search for the file with given size and permissions

Read the file

🔑 Credentials Provided

Username: bandit5

Password: 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw

🔍 Method of Solve

The password is stored in a file within the inhere directory.
The file has specific properties: human-readable, exactly 1033 bytes, and not executable.
The find command helps filter files based on these conditions.

🧪 Steps Followed

Logged in as bandit5

Entered the inhere directory

Searched for the file with required properties

Identified the correct file

Read the file to obtain the password

🧪 Commands Used
ls
cd inhere
find . -type f -size 1033c ! -executable
cat ./maybehere07/.file2

🧩 Command Purpose
Command	Purpose
ls	Lists files
cd inhere	Changes directory
find	Searches files by conditions
cat	Displays file contents
📸 Screenshot Evidence

<img width="538" height="132" alt="image" src="https://github.com/user-attachments/assets/305db77a-d48e-4eb4-b804-64ffe8b00dfa" />


🔑 Next Level Password

HWasnPhtq9AVKe0dmk45nxy20cvUa6EG

🧠 Explanation

The find command filters files by size and permissions.
Once the correct file is found, cat is used to display the password.

🔐 Concept Learned

Advanced file searching using file attributes in Linux.

🛡️ Security Insight

Storing sensitive data with predictable file properties can expose it to attackers
