📘 Bandit Level 07 → Level 08

🎯 Objective

Log in to the Bandit game and retrieve the next level password from a file by searching for a specific keyword.

🧭 Quick Action Summary

Login as bandit7

Locate the data file in the current directory

Search for the keyword millionth

Extract the password

🔑 Credentials Provided

Username: bandit7

Password: morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj

🔍 Method of Solve

The password is stored inside data.txt.
It appears next to the word millionth.

Using command-line search utilities allows direct extraction of the correct line.

🧪 Steps Followed

Logged in as bandit7

Listed files in the current directory to confirm presence of data.txt

Searched the file for the keyword millionth

Read the line containing the password

🧪 Commands Used

ls

cat data.txt | grep "millionth"

🧩 Command Purpose

ls	Lists files in the current directory

cat data.txt | grep ...	Searches for a specific word inside a file

📸 Screenshot Evidence

<img width="528" height="133" alt="Screenshot 2025-12-26 130514" src="https://github.com/user-attachments/assets/efc3c816-b792-4ed2-9b59-6d761232c1e1" />


🔑 Next Level Password

dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc

🧠 Explanation

The data.txt file contains many lines of text.
By combining cat with grep, the command filters the content and directly displays the line containing the word millionth, alongside the password.

🔐 Concept Learned

Using grep with piping to efficiently search large files for specific content.

🛡️ Security Insight

Plain text files containing passwords or sensitive data can be easily discovered if file permissions are not properly restricted.
