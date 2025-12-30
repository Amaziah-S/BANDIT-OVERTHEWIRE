📘 Bandit Level 29 → Level 30

🎯 Objective

Retrieve the next level password by checking out the dev branch in a Git repository where the password is stored.

🧭 Quick Action Summary

Login as bandit29

Clone the provided Git repository

List all available branches

Checkout the dev branch

Read the password file

Retrieve the password

🔑 Credentials Provided

Username: bandit29

Password: 4pT1t5DENaYuqnqvadYs1oE4QLCdjmJ7

🔍 Method of Solve

In this level:

The default branch does not contain the password

The password is stored in the dev branch

Git preserves all branches locally after cloning

By switching to the dev branch, the hidden password becomes accessible.

🧪 Commands Used

git clone ssh://bandit29-git@bandit.labs.overthewire.org:2220/home/bandit29-git/repo

cd repo

git branch -a

git checkout dev

cat README.md



🧩 Command Purpose

git clone ...	Clones the Git repository

git branch -a	Lists all local and remote branches

git checkout dev	Switches to the development branch

cat README.md	Displays the password for the next level


📸 Screenshot Evidence

<img width="1459" height="634" alt="Screenshot 2025-12-30 161902" src="https://github.com/user-attachments/assets/c2092579-2d31-49b1-ad95-788701c10914" />


🔑 Next Level Password

qp30ex3VLz5MDG1n91YowTv4Q8l7CDZL

🧠 Explanation

The password was intentionally hidden in a non-default branch

git checkout dev switches to the branch containing the password

Git keeps all branches accessible after cloning

Reading the file reveals the next level credentials

🔐 Concept Learned

Secrets stored in Git branches remain accessible even if hidden from the main branch.

🛡️ Security Insight

Always:

Review all branches before sharing repositories

Avoid committing passwords in any branch

Remove secrets from Git history completely

Otherwise, sensitive data can be exposed easily.
