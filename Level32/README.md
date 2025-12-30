📘 Bandit Level 32 → Level 33

🎯 Objective

Retrieve the next level password by escaping a restricted uppercase-only shell using $0.

🧭 Quick Action Summary

Login as bandit32

Encounter a restricted shell that converts input to uppercase

Use $0 to spawn a normal shell

Execute commands normally

Read the password file

Retrieve the password

🔑 Credentials Provided

Username: bandit32

Password: 3O9RfhqyAlVBEZpVb6LYStshZoqoSx5K

🔍 Method of Solve

When logging in as bandit32, you are placed inside a restricted shell where:

All typed commands are converted to UPPERCASE

Normal Linux commands fail because they are case-sensitive

The shell variable $0 still points to the current shell binary

By executing $0, we can spawn a fresh shell that does not enforce uppercase conversion.

🧪 Commands Used

After login, at the restricted prompt:

$0


After escaping to a normal shell:

whoami

cat /etc/bandit_pass/bandit33


🧩 Command Purpose


$0	Spawns a new unrestricted shell

whoami	Confirms the current user

cat /etc/bandit_pass/bandit33	Reads the next level password

📸 Screenshot Evidence

<img width="753" height="706" alt="Screenshot 2025-12-30 142356" src="https://github.com/user-attachments/assets/33bc2de4-9691-4824-8ac8-6a3209787c00" />


🔑 Next Level Password

tQdtbs5D5i2vJwkO8mEyYEyTL8izoeJ0

🧠 Explanation

The restricted shell forces all input to uppercase

$0 executes the current shell binary directly

The new shell does not apply uppercase conversion

Normal commands now work as expected

The password file can be read normally

🔐 Concept Learned

Shell variables like $0 can be abused to escape restricted environments.

🛡️ Security Insight

Restricted shells must:

Prevent shell re-execution

Lock down environment variables

Disable access to interactive shells

Otherwise, restrictions can be bypassed easily.
