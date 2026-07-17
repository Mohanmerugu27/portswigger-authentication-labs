# Lab 01 - Username Enumeration

## Objective

Demonstrate how different login responses can reveal whether a username exists.

---

## Vulnerability

The application returns different responses for valid and invalid usernames, allowing an attacker to enumerate existing accounts.

---

## Tools Used

- Burp Suite Professional
- Burp Repeater
- Firefox

---

## Steps Performed

1. Intercepted the login request.
2. Sent the request to Repeater.
3. Tested multiple usernames.
4. Compared server responses.
5. Identified a valid username.

---

## Result

Successfully identified the valid username and completed the lab.

---

## Mitigation

- Use generic login error messages.
- Implement rate limiting.
- Use account lockout mechanisms.
