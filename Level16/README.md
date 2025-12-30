📘 Bandit Level 16 → Level 17

🎯 Objective

Log in to the Bandit game and retrieve the next level password by discovering the correct SSL service running on a local port and using it to authenticate.

🧭 Quick Action Summary

Login as bandit16

Scan localhost ports in the given range

Identify the SSL-enabled service

Send the current password securely

Receive the SSH private key for the next level

🔑 Credentials Provided

Username: bandit16

Password: kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx

🔍 Method of Solve

Multiple services are running on localhost ports 31000–32000.

Only one port:

Accepts SSL connections

Returns valid data when the correct password is sent

We first identify the correct port using nmap, then connect securely using openssl.

🧪 Steps Followed

Logged in as bandit16

Scanned the given port range for open ports

Identified the SSL-enabled port

Connected using openssl s_client

Sent the current password

Received the SSH private key

🧪 Commands Used

nmap -p 31000-32000 localhost

openssl s_client -connect localhost:<correct_port>


kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx

🧩 Command Purpose

nmap -p 31000-32000 localhost	Scans the specified port range for open services

openssl s_client -connect localhost:PORT	Connects securely to an SSL/TLS service

📸 Screenshot Evidence

<img width="520" height="320" alt="Screenshot 2025-12-30 232344" src="https://github.com/user-attachments/assets/3680598a-eed8-4c58-a21f-29d6d50ace33" />


🔑 Next Level Password

EReVavePLFHtFlFsjn3hyzMlvSuSAcRD

🧠 Explanation

Several ports are open, but not all use SSL

The correct port accepts encrypted input

Sending the correct password returns an SSH private key

This key is used in the next level to log in

🔐 Concept Learned

Port scanning and service identification are critical skills in network security.

🛡️ Security Insight

Running multiple services on different ports increases attack surface.
Unused or misconfigured services should always be disabled.
