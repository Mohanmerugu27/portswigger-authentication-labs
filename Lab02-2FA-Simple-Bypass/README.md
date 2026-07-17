# Lab 02 – Username Enumeration via Subtly Different Responses

## Overview

This lab demonstrates how subtle differences in authentication responses can disclose valid usernames. By carefully analyzing server responses, an attacker can enumerate existing accounts without triggering obvious security alerts.

---

## Objective

Identify a valid username by comparing subtle variations in authentication responses.

---

## Vulnerability

The application returns slightly different responses for valid and invalid usernames, allowing an attacker to distinguish legitimate accounts.

---

## Environment

| Item | Details |
|------|---------|
| Platform | PortSwigger Web Security Academy |
| Category | Authentication |
| Difficulty | Practitioner |
| Tools | Burp Suite Professional, Mozilla Firefox |

---

## Methodology

1. Capture the login request using Burp Suite.
2. Send the request to Repeater.
3. Test multiple usernames.
4. Compare response content and length.
5. Identify the valid username.
6. Complete the authentication process.

---

## Result

Successfully identified a valid username by analyzing subtle differences in server responses.

---

## Security Impact

Username enumeration enables attackers to perform targeted password attacks against legitimate accounts.

---

## Mitigation

- Return identical authentication responses.
- Implement rate limiting.
- Enable account lockout.
- Log suspicious authentication attempts.

---

## References

- PortSwigger Web Security Academy
- OWASP Authentication Cheat Sheet
