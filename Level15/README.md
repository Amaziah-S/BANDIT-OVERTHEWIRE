📘 Bandit Level 15 → Level 16

🎯 Objective

Log in to the Bandit game and retrieve the next level password by communicating with a service that uses SSL/TLS encryption.

🧭 Quick Action Summary

Login as bandit15

Connect to a secure service on localhost port 30001

Use SSL/TLS to communicate

Receive the next level password

🔑 Credentials Provided

Username: bandit15

Password: 8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo

🔍 Method of Solve

The service running on port 30001 requires an encrypted SSL/TLS connection.

Normal nc will not work.
The openssl s_client command is used to establish a secure connection and send the password.

🧪 Steps Followed

Logged in as bandit15

Connected to the SSL service on port 30001

Sent the current password through the encrypted channel

Received the password for bandit16

🧪 Commands Used

openssl s_client -connect localhost:30001


8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo

🧩 Command Purpose

openssl s_client -connect localhost:30001	Connects to an SSL/TLS-enabled service

📸 Screenshot Evidence

<img width="379" height="132" alt="Screenshot 2025-12-27 162213" src="https://github.com/user-attachments/assets/1adedd98-acc3-4ddd-afe4-adda0c26ee45" />


🔑 Next Level Password

kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx

🧠 Explanation

The service expects an encrypted connection

openssl s_client initiates an SSL/TLS handshake

After connecting, the password is sent as input

The service responds with the next level password

🔐 Concept Learned

SSL/TLS communication ensures data confidentiality during transmission.

🛡️ Security Insight

Encrypting network services protects sensitive data from interception.
Plain-text services should never be used for password exchange.
