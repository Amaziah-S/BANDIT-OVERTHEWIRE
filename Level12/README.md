📘 Bandit Level 12 → Level 13

🎯 Objective

Log in to the Bandit game and retrieve the next level password from a file that contains multiple layers of compressed and encoded data.

🧭 Quick Action Summary

Login as bandit12

Locate the data.txt file

Convert hex dump back to binary

Repeatedly decompress the file

Extract the password from the final text output

🔑 Credentials Provided

Username: bandit12

Password: 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4

🔍 Method of Solve

The file data.txt is a hexdump of a compressed file.

The process involves:

Converting the hex dump back into binary

Identifying the compression type at each stage

Decompressing step-by-step until readable text appears

🧪 Steps Followed

Logged in as bandit12

Listed files and confirmed data.txt

Converted hex dump to binary format

Identified file type after each extraction

Decompressed repeatedly

Retrieved the password from the final output

🧪 Commands Used
ls

xxd -r data.txt > data

file data

mv data data.gz

gunzip data.gz

file data

bunzip2 data

file data

mv data data.tar

tar -xf data.tar

file data

mv data data.gz

gunzip data.gz

cat data


🧩 Command Purpose

xxd -r	Converts hex dump back to binary

file	Identifies file type

gunzip	Decompresses gzip files

bunzip2	Decompresses bzip2 files

tar -xf	Extracts tar archives

cat	Displays final readable content

📸 Screenshot Evidence
<img width="657" height="187" alt="Screenshot 2025-12-26 134311" src="https://github.com/user-attachments/assets/2fada8f0-cca7-4c0d-a30c-ca78e5dba860" />



🔑 Next Level Password

FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn

🧠 Explanation

The password is hidden behind multiple compression layers.

Each extraction reveals another compressed format

file helps identify the next step

Repeating this process eventually reveals plain text

The password appears in the final readable output

🔐 Concept Learned

Understanding file formats and compression tools is essential when dealing with layered data.

🛡️ Security Insight

Obfuscating data with multiple compression layers is not secure without encryption.
Anyone with basic Linux knowledge can extract the content.
