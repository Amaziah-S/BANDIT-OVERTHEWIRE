📘 Bandit Level 31 → Level 32

🎯 Objective

Retrieve the next level password by interacting with a Git repository that enforces strict commit rules, requiring the use of git add key.txt.

🧭 Quick Action Summary

Login as bandit31

Clone the provided Git repository

Read the repository rules

Create the required file

Add the file to Git staging

Commit the changes

Push to the remote repository

Receive the password

🔑 Credentials Provided

Username: bandit31

Password: fb5S2xb7bRyFmAvQYQGEqsbhVyJqhnDy

🔍 Method of Solve

In this level:

The repository contains a README explaining strict rules

A specific file named key.txt must be created

The file must contain the correct text

Only properly staged and committed changes are accepted

The password is revealed after a successful push.

🧪 Commands Used

git clone ssh://bandit31-git@bandit.labs.overthewire.org:2220/home/bandit31-git/repo

cd repo

cat README.md

echo "May I come in?" > key.txt

git add key.txt

git commit -m "Add key"

git config user.name "bandit31"

git config user.email "bandit31@bandit.labs"

git commit -m "Add key"

git push origin master



🧩 Command Purpose

git clone ...	Clones the Git repository

cat README.md	Reads instructions and rules

echo "May I come in?" > key.txt	Creates the required file with correct content

git add key.txt	Stages the file for commit

git commit -m "Add key"	Commits the staged file

git push	Pushes changes to the remote repository


📸 Screenshot Evidence

<img width="1234" height="739" alt="Screenshot 2025-12-30 163406" src="https://github.com/user-attachments/assets/5cfe9def-a621-4d37-a0b9-d78275d7c558" />


<img width="806" height="836" alt="Screenshot 2025-12-3016407" src="https://github.com/user-attachments/assets/c00a0699-3a24-47a6-9766-4b046b44e2cf" />


🔑 Next Level Password

3O9RfhqyAlVBEZpVb6LYStshZoqoSx5K

🧠 Explanation

The repository rejects pushes unless rules are followed

git add key.txt ensures the correct file is staged

A valid commit and push triggers the server response

The server reveals the password after successful validation

🔐 Concept Learned

Git hooks and repository rules can enforce workflow and security policies.

🛡️ Security Insight

Repositories can:

Enforce commit structure

Restrict file changes

Validate content before accepting pushes

This helps prevent unauthorized or accidental changes.
