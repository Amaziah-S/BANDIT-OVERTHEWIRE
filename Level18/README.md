📘 Bandit Level 18 → Level 19

🎯 Objective

Log in to the Bandit game and retrieve the next level password despite the shell logging you out immediately after login.

🧭 Quick Action Summary

Login to bandit18 via SSH

Prevent the forced logout

Read the password file directly

Retrieve the password

🔑 Credentials Provided

Username: bandit18

Password: x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO

🔍 Method of Solve

The bandit18 account is configured to immediately log out users after login.

To bypass this:

Execute a command directly via SSH

Read the password file without opening an interactive shell

🧪 Steps Followed

Attempted normal SSH login (auto-logout observed)

Used SSH command execution to bypass the logout

Read the password file successfully

Retrieved the next level password

🧪 Commands Used

ssh bandit.labs.overthewire.org -l bandit18 2220 cat readme

🧩 Command Purpose

ssh user@host command	Executes a command without opening a shell

cat readme	Displays the next level password

📸 Screenshot Evidence

<img width="706" height="312" alt="Screenshot 2025-12-27 181741" src="https://github.com/user-attachments/assets/997e9520-ad76-4e9e-8a7d-7158e9277ea5" />


🔑 Next Level Password

cGWpMaKXVwDUNgPAVJbWYuGHVn9zl3j8

🧠 Explanation

The shell exits immediately after login

SSH allows remote command execution without an interactive session

The command runs before logout is triggered

Password is displayed directly

🔐 Concept Learned

SSH can be used for non-interactive command execution, useful when shell access is restricted.

🛡️ Security Insight

Restricting interactive shells is not sufficient protection.
Command execution access must also be properly controlled.
