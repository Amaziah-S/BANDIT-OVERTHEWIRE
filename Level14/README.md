📘 Bandit Level 13 → Level 14

🎯 Objective

Log in to the Bandit game and retrieve the next level password using an SSH private key.

🧭 Quick Action Summary

Login as bandit13

Locate the SSH private key file

Use the key to SSH into bandit14

Retrieve the password from the protected file

🔑 Credentials Provided

Username: bandit13

Password: FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn

🔍 Method of Solve

Instead of a password, Bandit Level 13 provides an SSH private key.

This key is used to authenticate directly into the bandit14 account, where the next password is stored in a protected file.

🧪 Steps Followed

Logged in as bandit13

Listed files to locate the private SSH key

Set correct permissions for the key file

Logged in to bandit14 using the key

Read the password file

🧪 Commands Used

ls

chmod 600 sshkey.private

ssh -i sshkey.private bandit14@localhost

cat /etc/bandit_pass/bandit14


🧩 Command Purpose

ls	Lists files in the directory

chmod 600 sshkey.private	Secures the SSH private key

ssh -i sshkey.private bandit14@localhost	Logs in using the private key

cat /etc/bandit_pass/bandit14	Displays the next level password

📸 Screenshot Evidence

<img width="548" height="90" alt="Screenshot 2025-12-26 145854" src="https://github.com/user-attachments/assets/fc9fc087-baa9-4fef-854c-f254c94dea26" />


🔑 Next Level Password

MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS

🧠 Explanation

SSH allows key-based authentication instead of passwords.

The private key must have strict permissions

SSH rejects keys that are readable by others

Once authenticated, the password file becomes accessible

🔐 Concept Learned

SSH key-based authentication is more secure than password authentication when properly configured.

🛡️ Security Insight

Exposed private keys can fully compromise accounts.
Always protect SSH keys with proper permissions and access controls.
