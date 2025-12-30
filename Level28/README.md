📘 Bandit Level 28 → Level 29

🎯 Objective

Retrieve the next level password by examining a Git repository and finding the password hidden in another branch.

🧭 Quick Action Summary

Login as bandit28

Clone the provided Git repository

Inspect the repository contents

List available branches

Switch to the correct branch

Read the password file

Retrieve the password

🔑 Credentials Provided

Username: bandit28

Password: Yz9IpL0sBcCeuG7m9uQFt8ZNpS4HZRcN

🔍 Method of Solve

In this level, the password is not present in the current version of the repository.

However:

Git stores all previous changes

Removed content can be recovered from commit history

git log -p shows the exact line‑by‑line differences between commits

By reviewing the patches, the deleted password can be found.

🧪 Commands Used

git clone ssh://bandit28-git@bandit.labs.overthewire.org:2220/home/bandit28-git/repo

cd repo

git log -p


🧩 Command Purpose


git clone ...	Clones the Git repository

git log -p Displays commit history with patch differences


📸 Screenshot Evidence

<img width="649" height="132" alt="image" src="https://github.com/user-attachments/assets/21e1bb11-d113-4d64-84eb-9241413b531d" />

<img width="525" height="616" alt="Screenshot 2025-12-30 161144" src="https://github.com/user-attachments/assets/1813ac00-615e-4272-a86c-df35e409c317" />



🔑 Next Level Password

4pT1t5DENaYuqnqvadYs1oE4QLCdjmJ7

🧠 Explanation

The password was removed in a later commit

Git history still contains the deleted line

git log -p reveals both additions and deletions

The password appears in the diff output

🔐 Concept Learned

Deleted data can still be recovered from Git commit history.

🛡️ Security Insight

To protect secrets in Git:

Never commit passwords

Rotate credentials immediately if exposed

Rewrite history to remove sensitive data
