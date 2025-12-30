📘 Bandit Level 26 → Level 27

🎯 Objective

Retrieve the next level password by escaping a restricted environment and accessing the password file.

🧭 Quick Action Summary

Login as bandit26 using SSH

Encounter a restricted shell

Trigger the pager (more)

Open vi from the pager

Escape to a shell

Read the password file

Retrieve the password

🔑 Credentials Provided

Username: bandit26

Authentication: s0773xxkk0MXfdqOfPRVr9L3jJBUOgCZ

🔍 Method of Solve

The bandit26 account uses a restricted shell that prevents normal command execution.

Key observations:

A login banner opens using more

more allows opening vi

vi supports shell execution

By escaping from vi, a normal shell can be accessed.

🧪 Commands Used

ssh bandit26@bandit.labs.overthewire.org -p 2220


(Resize the terminal window to a small height before logging in to force more)

Inside more:

v


Inside vi:

:set shell=/bin/bash
:shell


After escaping to shell:

cat /home/bandit27/.pass


🧩 Command Purpose

ssh bandit26@bandit...	Logs into Bandit as bandit26

more	Pager triggered by limited terminal size

v	Opens vi from within more

:set shell=/bin/bash	Sets bash as the shell inside vi

:shell	Escapes to a normal shell

cat /home/bandit27/.pass	Reads the next level password


📸 Screenshot Evidence

<img width="1898" height="238" alt="Screenshot 2025-12-30 160329" src="https://github.com/user-attachments/assets/c592a671-77a2-4f06-8b74-3a17d0b8a824" />


🔑 Next Level Password

upsNCc7vzaRDx6oZC6GiR6ERwe1MowGB

🧠 Explanation

Bandit26 uses a restricted shell

more is triggered on login

vi can be launched from more

vi allows shell execution

Escaping the shell provides command access

The password file is read normally

🔐 Concept Learned

Editors and pagers can be abused to bypass restricted shells if not properly locked down.

🛡️ Security Insight

Restricted environments must:

Disable shell escapes in editors

Limit interactive pagers

Harden login shells

Without proper controls, restrictions can be bypassed easily.
