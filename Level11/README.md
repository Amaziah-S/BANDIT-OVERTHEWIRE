📘 Bandit Level 11 → Level 12

🎯 Objective

Log in to the Bandit game and retrieve the next level password from a file that contains ROT13-encoded text.

🧭 Quick Action Summary

Login as bandit11

Locate the data.txt file

Decode the ROT13 text

Extract the password

🔑 Credentials Provided

Username: bandit11

Password: dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr

🔍 Method of Solve

The content of data.txt is encoded using ROT13, a simple letter-substitution cipher.

Using the tr command allows translating characters and decoding the text back to readable form.

🧪 Steps Followed

Logged in as bandit11

Listed files to confirm presence of data.txt

Decoded the ROT13 content

Retrieved the password from the output

🧪 Commands Used

ls

cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'

🧩 Command Purpose

ls	Lists files in the current directory

cat data.txt	Displays file content

tr 'A-Za-z' 'N-ZA-Mn-za-m'	Decodes ROT13-encoded text

📸 Screenshot Evidence

<img width="940" height="205" alt="Screenshot 2025-12-26 132117" src="https://github.com/user-attachments/assets/ad9eeaa7-dd9a-433f-9ad9-713f78784143" />


🔑 Next Level Password

7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4

🧠 Explanation

ROT13 shifts each alphabet letter by 13 positions.

tr replaces each letter with its ROT13 equivalent

Uppercase and lowercase letters are handled separately

The decoded output directly reveals the password

🔐 Concept Learned

The tr command is useful for character substitution and decoding simple ciphers.

🛡️ Security Insight

ROT13 provides no real security.
It is easily reversible and should never be used to protect sensitive data.
