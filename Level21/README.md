📘 Bandit Level 21 → Level 22

🎯 Objective

Log in to the Bandit game and retrieve the next level password by analyzing a cron job script executed automatically by the system.

🧭 Quick Action Summary

Login as bandit21

Inspect cron jobs running on the system

Locate the script executed by cron

Read the output file created by the script

Retrieve the password

🔑 Credentials Provided

Username: bandit21

Password: EeoULMCra2q0dSkYj561DX7s1CpBuOBt

🔍 Method of Solve

A cron job is scheduled to run periodically as bandit22.

This cron job executes a script that:

Reads the password for bandit22

Writes it into a temporary file

Sets permissions allowing bandit21 to read it

By identifying and reading this output file, the next level password can be obtained.

🧪 Steps Followed

Logged in as bandit21

Checked cron job configuration

Identified the script executed by cron

Found the file where the password is written

Read the file to retrieve the password

🧪 Commands Used

ls /etc/cron.d/

cat /etc/cron.d/cronjob_bandit22

cat /usr/bin/cronjob_bandit22.sh

cat /tmp/<generated_filename>


🧩 Command Purpose

ls /etc/cron.d/	Lists cron jobs configured on the system

cat cronjob_bandit22	Displays the cron job schedule

cat cronjob_bandit22.sh	Shows the script executed by cron

cat /tmp/<file>	Reads the file containing the next level password

📸 Screenshot Evidence

<img width="791" height="377" alt="Screenshot 2025-12-28 174615" src="https://github.com/user-attachments/assets/7fdedfc8-4230-4b0a-bf69-4d153db2f889" />


🔑 Next Level Password

tRae0UfB9v0UzbCdn9cY0gQnds9GF58Q

🧠 Explanation

Cron jobs run automatically at scheduled intervals

The script runs as bandit22

It stores the password in a readable temporary file

Accessing this file reveals the password

🔐 Concept Learned

Cron jobs can unintentionally leak sensitive data if file permissions are misconfigured.

🛡️ Security Insight

Automated scripts should never store credentials in world-readable locations.
Temporary files must be protected with strict permissions.
