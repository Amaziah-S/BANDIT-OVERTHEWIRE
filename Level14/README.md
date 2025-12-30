📘 Bandit Level 14 → Level 15

🎯 Objective

Log in to the Bandit game and retrieve the next level password by sending the current password to a local network service.

🧭 Quick Action Summary

Login as bandit14

Read the current level password

Send the password to a service running on localhost port 30000

Receive the next level password

🔑 Credentials Provided

Username: bandit14

Password: FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn

🔍 Method of Solve

The password for the next level is not stored in a file.

Instead, a service is listening on port 30000 on localhost.
When the current password is sent to this service, it returns the password for bandit15.

The nc (netcat) command is used to communicate with the service.

🧪 Steps Followed

Logged in as bandit14

Read the current password file

Connected to the local service on port 30000

Sent the password

Received the next level password

🧪 Commands Used

cat /etc/bandit_pass/bandit14

nc localhost 30000
FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn

🧩 Command Purpose

cat /etc/bandit_pass/bandit14	Reads the current level password

nc localhost 30000	Connects to the local service listening on port 30000

📸 Screenshot Evidence

<img width="371" height="126" alt="image" src="https://github.com/user-attachments/assets/2bf1fb27-ec22-47c9-8f04-ef9d338047a6" />


🔑 Next Level Password

8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo


🧠 Explanation

A network service is running locally on port 30000

The service expects the current password as input

Upon correct input, it responds with the next level password

nc enables direct interaction with TCP services

🔐 Concept Learned

Netcat (nc) is a powerful tool for interacting with network services and testing open ports.

🛡️ Security Insight

Services that blindly return sensitive data based on simple input validation are insecure.
Authentication and encryption should always be enforced.
