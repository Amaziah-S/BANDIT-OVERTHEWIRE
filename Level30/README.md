📘 Bandit Level 30 → Level 31

🎯 Objective

Retrieve the next level password by inspecting Git tags and extracting the hidden information stored inside a tag message.

🧭 Quick Action Summary

Login as bandit30

Clone the provided Git repository

List all available Git tags

Inspect the tag contents

Extract the password from the tag

Retrieve the password

🔑 Credentials Provided

Username: bandit30

Password: qp30ex3VLz5MDG1n91YowTv4Q8l7CDZL

🔍 Method of Solve

In this level:

The repository does not store the password in files or branches

The password is hidden inside a Git tag

Git tags can store messages, similar to commits

By listing and inspecting the tags, the password can be revealed.

🧪 Commands Used

git clone ssh://bandit27-git@bandit.labs.overthewire.org:2220/home/bandit27-git/repo

cd repo

git tag

git show secret



🧩 Command Purpose

git clone ...	Clones the Git repository

git tag	Lists all tags in the repository

git show secret	Displays the tag message containing the password


📸 Screenshot Evidence

<img width="416" height="230" alt="Screenshot 2025-12-30 161905" src="https://github.com/user-attachments/assets/cd33b740-7d1c-4330-9bb7-dee0a09d4cf1" />


🔑 Next Level Password

fb5S2xb7bRyFmAvQYQGEqsbhVyJqhnDy

🧠 Explanation

Git tags can store descriptive messages

The password is embedded inside the tag secret

git show reveals the tag’s contents

No branch or commit inspection is required

🔐 Concept Learned

Git metadata (tags, commits) can leak sensitive data even when files look clean.

🛡️ Security Insight

Repositories should:

Avoid storing secrets in tags

Audit all Git metadata before sharing

Remove sensitive information from history
