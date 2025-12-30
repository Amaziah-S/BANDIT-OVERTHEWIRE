📘 Bandit Level 27 → Level 28

🎯 Objective

Retrieve the next level password by cloning a Git repository and inspecting its contents.

🧭 Quick Action Summary

Login as bandit27

Locate the provided Git repository URL

Clone the repository to a writable directory

Explore the repository files

Find the password stored inside

Retrieve the password

🔑 Credentials Provided

Username: bandit27

Password: upsNCc7vzaRDx6oZC6GiR6ERwe1MowGB

🔍 Method of Solve

The home directory of bandit27 contains a file that points to a Git repository.

The task requires:

Cloning the repository

Navigating into the cloned directory

Reading the file that contains the password for bandit28

🧪 Commands Used

git clone ssh://bandit27-git@bandit.labs.overthewire.org:2220/home/bandit27-git/repo

cd repo

ls

cat README



🧩 Command Purpose

git clone ...	Clones the Git repository locally

cd repo	Enters the cloned repository

ls	Lists repository files

cat README	Displays the file containing the password


📸 Screenshot Evidence

<img width="1325" height="678" alt="Screenshot 2025-12-30 161141" src="https://github.com/user-attachments/assets/9960cb56-da73-4a0d-b25d-51a25180dcac" />


🔑 Next Level Password

Yz9IpL0sBcCeuG7m9uQFt8ZNpS4HZRcN


🧠 Explanation

The password is stored directly in the repository

No exploitation is required—only Git usage

Cloning reveals the repository contents locally

Reading the file gives the next level password

🔐 Concept Learned

Sensitive information should never be stored in plaintext inside repositories.

🛡️ Security Insight

Avoid storing secrets in Git repositories

Use environment variables or secret managers

Audit repositories before sharing
