📘 Bandit Level 08 → Level 09

🎯 Objective

Log in to the Bandit game and retrieve the next level password from a file containing unique text lines.

🧭 Quick Action Summary

Login as bandit8

Locate the data.txt file in the home directory

Sort the file and remove duplicates

Extract the password

🔑 Credentials Provided

Username: bandit8

Password: dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc

🔍 Method of Solve

The password is stored inside data.txt.
Since the file contains multiple lines, some may be duplicates.
Using sort and uniq -u allows filtering out duplicate lines and isolating the unique line containing the password.

🧪 Steps Followed

Logged in as bandit8

Listed files to confirm presence of data.txt

Sorted the file and extracted only unique lines

Read the output to retrieve the password

🧪 Commands Used

ls

sort data.txt | uniq -u

🧩 Command Purpose

ls	Lists files in the current directory

sort data.txt | uniq -u	Sorts the file and prints only lines that are unique

📸 Screenshot Evidence
<img width="447" height="130" alt="Screenshot 2025-12-26 130740" src="https://github.com/user-attachments/assets/a42a0194-fb6a-44d0-9298-cb0a2e6ec79e" />

🔑 Next Level Password

4CKMh1JI91bUIZZPXDqGanal4xvAg0JM

🧠 Explanation

The data.txt file contains repeated and unique lines.

sort arranges the lines in order

uniq -u filters out all duplicates, leaving only the unique line, which contains the password

This method efficiently isolates the correct password without manually scanning through the file.

🔐 Concept Learned

Combining sort and uniq -u is a quick way to find unique entries in a text file on Linux.

🛡️ Security Insight

Storing passwords in plain text files without access restrictions is insecure.
Duplicate data may obscure sensitive information if not carefully handled.
