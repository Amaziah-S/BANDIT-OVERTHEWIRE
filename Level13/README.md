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
cat sshkey.private
chmod 700 private13.key

ssh bandit14@bandit.labs.overthewire.org -p 2220 -i private13.key
 
 cat /etc/bandit_pass/bandit14

🧩 Command Purpose

ls	Lists files in the directory

chmod 700 sshkey.private	Secures the SSH private key

 ssh bandit14@bandit.labs.overthewire.org -p 2220 -i private13.key	Logs in using the private key
 
cat /etc/bandit_pass/bandit14	Displays the next level password

📸 Screenshot Evidence

<img width="984" height="736" alt="Screenshot 2025-12-30 222247" src="https://github.com/user-attachments/assets/b7a7e4c1-a653-4ab6-b36c-657eb9ac8fb9" />
<img width="675" height="429" alt="Screenshot 2025-12-30 223135" src="https://github.com/user-attachments/assets/d15793db-5635-48df-8724-aa8ac56b0010" />
<img width="658" height="174" alt="Screenshot 2025-12-30 223144" src="https://github.com/user-attachments/assets/ddfe8fc8-49a5-453b-b7d5-8478f84afc5f" />



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
