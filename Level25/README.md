📘 Bandit Level 25 → Level 26

🎯 Objective

Log in to the Bandit game and retrieve the next level password by escaping a restricted shell using vi.

🧭 Quick Action Summary

Login as bandit25

Notice the restricted shell behavior

Trigger the pager that opens vi

Escape from vi to a normal shell

Read the password file

Retrieve the password

🔑 Credentials Provided

Username: bandit25

Password: iCi86ttT4KSNe1armKiwbQNmB3YJP3q4

🔍 Method of Solve

When logging in as bandit25, the account uses a restricted shell.

Characteristics of the shell:

Normal commands like ls, cat, cd are restricted

A pager program opens using vi

vi allows execution of shell commands

By escaping from vi, we can obtain a normal shell and read the password.

🧪 Commands Used

ls

ls -l bandit26.sshkey

ssh -i bandit26.sshkey bandit26@localhost -p 2220


iCi86ttT4KSNe1armKiwbQNmB3YJP3q4

Inside the pager (vi):

:set shell=/bin/bash
:shell


After escaping to shell:

cat /home/bandit26/.pass


🧩 Command Purpose

vi	Opens the pager where escape is possible

:set shell=/bin/bash	Sets bash as the shell inside vi

:shell	Escapes from vi to a normal shell

cat /home/bandit26/.pass	Reads the next level password


📸 Screenshot Evidence

<img width="667" height="225" alt="Screenshot 2025-12-30 160125" src="https://github.com/user-attachments/assets/9060848b-a907-4613-95ce-cdb57007ece7" />
minimize it.
<img width="365" height="156" alt="Screenshot 2025-12-30 160213" src="https://github.com/user-attachments/assets/418c4dbf-38a6-4a77-80e3-fb0bca3626d4" />
Click vi
<img width="524" height="902" alt="Screenshot 2025-12-30 160242" src="https://github.com/user-attachments/assets/cf1e7be9-96a7-4448-a3ec-c1a2fd41e60e" />

<img width="243" height="103" alt="Screenshot 2025-12-30 160257" src="https://github.com/user-attachments/assets/6dd298da-e701-4945-b69c-792077e06405" />

<img width="452" height="195" alt="Screenshot 2025-12-30 160328" src="https://github.com/user-attachments/assets/674d910f-54a6-4561-9040-d4e7b1a99183" />



🔑 Next Level Password

s0773xxkk0MXfdqOfPRVr9L3jJBUOgCZ

🧠 Explanation

Bandit25 uses a restricted shell

vi is still allowed and can execute shell commands

Setting the shell to /bin/bash breaks the restriction

Once escaped, the password file can be read normally

🔐 Concept Learned

Text editors like vi can be abused to escape restricted environments.

🛡️ Security Insight

Restricted shells must:

Limit editor escape capabilities

Disable shell execution inside pagers

Avoid granting interactive tools unnecessarily

Without proper hardening, restricted shells can be bypassed easily.
