📘 Bandit Level 20 → Level 21
🎯 Objective

Log in to the Bandit game and retrieve the next level password by interacting with a setuid program that communicates over a TCP connection.

🧭 Quick Action Summary

Login as bandit20

Identify the SUID executable

Start a listener on a local port

Send the current password through the SUID program

Receive the next level password

🔑 Credentials Provided

Username: bandit20

Password: 0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO

🔍 Method of Solve

The home directory contains a SUID binary called suconnect.

This program:

Runs with bandit21 privileges

Connects to a TCP port

Sends the current password

Returns the password for the next level if the input is correct

A listener must be running to receive the connection.

🧪 Steps Followed

Logged in as bandit20

Listed files to locate the SUID binary

Started a listener on a local port

Ran the SUID program to send the password

Received the password for bandit21

🧪 Commands Used

ls

nc -lvp 9999

0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO


🧩 Command Purpose

ls	Lists files in the directory

nc -lvp 9999	Starts a TCP listener on port 9999

📸 Screenshot Evidence

<img width="526" height="120" alt="Screenshot 2025-12-27 183208" src="https://github.com/user-attachments/assets/41e0146e-9ea7-4596-9115-1c62aec9be4f" />


🔑 Next Level Password

EeoULMCra2q0dSkYj561DX7s1CpBuOBt

🧠 Explanation

suconnect runs with bandit21 privileges

It connects to the specified port

The password is verified

On success, the next level password is returned

🔐 Concept Learned

Combining SUID binaries with network communication can introduce serious security risks.

🛡️ Security Insight

SUID programs that interact with network services can be exploited if not properly validated and restricted.
