📘 Bandit Level 22 → Level 23

🎯 Objective

Log in to the Bandit game and retrieve the next level password by analyzing a cron job script that copies the password to a predictable temporary file.

🧭 Quick Action Summary

Login as bandit22

Navigate to the cron directory

Identify the cron job for bandit23

Analyze the script logic

Recreate the hashed filename

Read the generated file from /tmp

🔑 Credentials Provided

Username: bandit22

Password: tRae0UfB9v0UzbCdn9cY0gQnds9GF58Q

🔍 Method of Solve

A cron job runs periodically as bandit23.

The script:

Uses the username

Generates a filename using MD5 hash

Copies the password into /tmp/<hash>

By recreating the same hash manually, the password file location can be predicted and read.

🧪 Commands Used

ls

cd /etc/cron.d

ls

cat cronjob_bandit23

cat /usr/bin/cronjob_bandit23.sh

echo I am user bandit23 | md5sum | cut -d ' ' -f 1

cat /tmp/8ca319486bfbbc3663ea0fbe81326349


🧩 Command Purpose

ls	Lists files in the current directory

cd /etc/cron.d	Navigates to the cron jobs directory

cat cronjob_bandit23	Displays the cron job schedule for bandit23

cat /usr/bin/cronjob_bandit23.sh	Shows the script executed by the cron job

echo I am user bandit23 | md5sum | cut -d ' ' -f 1	Recreates the hashed filename used by the script

cat /tmp/8ca319486bfbbc3663ea0fbe81326349	Reads the file containing the next level password

📸 Screenshot Evidence

<img width="762" height="487" alt="Screenshot 2025-12-28 175156" src="https://github.com/user-attachments/assets/215f9559-f60d-4590-99bd-9c6df29645bd" />


🔑 Next Level Password

0Zf11ioIjMVN551jX3CmStKLYqjk54Ga

🧠 Explanation

The cron job runs automatically as bandit23

The script hashes the string I am user bandit23

The password is copied into /tmp/<md5_hash>

Reproducing the hash reveals the file location

Reading the file gives the password

🔐 Concept Learned

Predictable hashing and cron automation can expose sensitive data if not designed securely.

🛡️ Security Insight

Temporary directories and predictable filenames should never be used to store credentials.
Cron jobs must enforce strict access control.
