📘 Bandit Level 24 → Level 25

🎯 Objective

Log in to the Bandit game and retrieve the next level password by brute-forcing a PIN over a network service.

🧭 Quick Action Summary

Login as bandit24

Identify the network service running on localhost

Create a brute-force script

Send all possible PIN combinations

Capture the correct response

Retrieve the password

🔑 Credentials Provided

Username: bandit24

Password: gb8KRRCsshuZXI0tUuR6ypOFjiZbf3G8

🔍 Method of Solve

A service is running on localhost port 30002.

The service:

Requires the current password

Requires a 4-digit PIN

Returns the next level password only when both are correct

Since the PIN is numeric (0000–9999), it can be brute-forced by sending all combinations.

🧪 Commands Used

ls

cd /tmp

mkdir bd24

cd bd24

nano brute.sh

chmod +x brute.sh

./brute.sh | nc localhost 30002




🧩 Command Purpose

nc localhost 30002	Connects to the service manually

for i in {0000..9999}	Generates all 4-digit PIN combinations


📸 Screenshot Evidence

<img width="1078" height="439" alt="Screenshot 2025-12-30 155753" src="https://github.com/user-attachments/assets/9e9906d5-23ef-40e7-bd3a-2c6f224b24f9" />

<img width="509" height="237" alt="Screenshot 2025-12-30 155113" src="https://github.com/user-attachments/assets/c4e3e20f-7944-44ff-aa19-2641c869343b" />

<img width="771" height="466" alt="Screenshot 2025-12-30 155114" src="https://github.com/user-attachments/assets/0c84e6c3-b475-428c-91da-842e9cd721b8" />


🔑 Next Level Password

iCi86ttT4KSNe1armKiwbQNmB3YJP3q4

🧠 Explanation

The service expects two inputs: password + PIN

Only one PIN is valid

Brute-forcing 10,000 combinations is fast

When the correct PIN is sent, the service returns the password

All other attempts fail silently

🔐 Concept Learned

Brute-forcing small keyspaces is trivial when rate-limiting is absent.

🛡️ Security Insight

Services must implement:

Rate limiting

Account lockout

Strong authentication

Without these, brute-force attacks succeed easily
