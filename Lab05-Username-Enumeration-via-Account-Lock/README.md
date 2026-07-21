# Lab 05 – Username Enumeration via Account Lock

## Overview

This lab demonstrates how an account lockout mechanism can unintentionally disclose valid usernames. By observing the application's behavior after multiple failed authentication attempts, an attacker can distinguish existing accounts from non-existent ones.

---

## Objective

Identify a valid username by exploiting differences in the application's account lockout behavior.

---

## Lab Information

| Property | Value |
|----------|-------|
| Platform | PortSwigger Web Security Academy |
| Category | Authentication |
| Difficulty | Practitioner |
| Vulnerability | Username Enumeration |
| Tools Used | Burp Suite Professional, Mozilla Firefox |

---

## Vulnerability Description

The application locks valid user accounts after a defined number of failed login attempts, while invalid usernames do not trigger the same behavior. This difference allows attackers to enumerate valid usernames without requiring successful authentication.

---

## Attack Methodology

1. Intercept the authentication request using Burp Suite.
2. Send repeated login attempts with different usernames.
3. Observe the application's account lockout behavior.
4. Identify the username that triggers the account lock mechanism.
5. Use the valid username to complete the authentication process.
6. Successfully solve the lab.

---

## Outcome

A valid username was successfully identified by exploiting differences in the application's account lockout mechanism.

---

## Security Impact

Information disclosed through account lockout behavior enables attackers to enumerate valid usernames, increasing the effectiveness of password guessing and credential stuffing attacks.

---

## Recommended Mitigations

- Return identical responses for all authentication failures.
- Apply account lockout consistently without revealing account validity.
- Implement rate limiting and adaptive authentication.
- Enable Multi-Factor Authentication (MFA).
- Monitor authentication logs for enumeration attempts.

---

## References

- PortSwigger Web Security Academy
- OWASP Authentication Cheat Sheet
- OWASP Top 10 – Identification and Authentication Failures

---

## Disclaimer

This lab was completed within the controlled environment provided by the PortSwigger Web Security Academy. All testing activities were performed solely for educational purposes on intentionally vulnerable applications.
