📘 Bandit Level 10 → Level 11

🎯 Objective

Log in to the Bandit game and retrieve the next level password from a file that contains Base64-encoded data.

🧭 Quick Action Summary

Login as bandit10

Locate the data.txt file

Decode the Base64 content

Extract the password

🔑 Credentials Provided

Username: bandit10

Password: FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey

🔍 Method of Solve

The password inside data.txt is Base64-encoded, meaning it is not readable in its current form.

Using the base64 -d command decodes the content and reveals the original readable password.

🧪 Steps Followed

Logged in as bandit10

Listed files to confirm presence of data.txt

Decoded the Base64 content

Retrieved the password from the decoded output

🧪 Commands Used

ls

base64 -d data.txt

🧩 Command Purpose

ls	Lists files in the current directory

base64 -d data.txt	Decodes Base64-encoded content

📸 Screenshot Evidence
<img width="726" height="164" alt="Screenshot 2025-12-26 131607" src="https://github.com/user-attachments/assets/f145e40a-83ac-460a-8c19-46d90a27a171" />




🔑 Next Level Password

dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr

🧠 Explanation

The data.txt file does not store the password in plain text.

Base64 encoding converts readable text into encoded format

base64 -d reverses this encoding

The decoded output directly reveals the password

This is a common technique used to store or transmit data safely, but it is not encryption.

🔐 Concept Learned

Base64 encoding is reversible and should not be used to protect sensitive information.

🛡️ Security Insight

Encoding is not encryption.
Any attacker with access to the file can easily decode Base64-encoded passwords.
