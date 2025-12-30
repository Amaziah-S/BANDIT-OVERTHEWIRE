📘 Bandit Level 09 → Level 10

🎯 Objective

Log in to the Bandit game and retrieve the next level password from a file that contains human‑readable text mixed with non‑printable characters.

🧭 Quick Action Summary

Login as bandit9

Locate the data.txt file

Extract readable strings

Filter the line containing the password

Copy the password for the next level

🔑 Credentials Provided

Username: bandit9

Password: 4CKMh1JI91bUIZZPXDqGanal4xvAg0JM

🔍 Method of Solve

The file data.txt is not a plain text file.
It contains binary data along with readable text.

Using:

strings extracts readable text

grep "=" filters lines that contain =, which is part of the password format

This isolates the password cleanly without noise.

🧪 Steps Followed

Logged in as bandit9

Confirmed the presence of data.txt

Extracted readable strings from the file

Filtered only the relevant password line

Retrieved the password

🧪 Commands Used
ls

strings data.txt | grep "="

🧩 Command Purpose

strings data.txt	Extracts human‑readable text from a binary/mixed file

grep "="	Filters lines containing = (used in the password format)

📸 Screenshot Evidence

<img width="456" height="143" alt="Screenshot 2025-12-26 131226" src="https://github.com/user-attachments/assets/41bc2668-c19b-4e9b-8fcd-6fab17081524" />

🔑 Next Level Password

FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey

🧠 Explanation

The password is hidden inside a file with unreadable characters.

strings removes binary noise

grep "=" narrows the output to password‑formatted lines

The final visible string after = is the password

This approach avoids manually inspecting large or corrupted files.

🔐 Concept Learned

Piping commands like strings | grep allows efficient filtering of meaningful data from complex files.

🛡️ Security Insight

Obfuscating passwords inside binary files is insecure.
Without encryption, tools like strings can easily extract sensitive data.
