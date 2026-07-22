# Lab 08 – 2FA Bypass Using a Brute-Force Attack

## Overview

This lab demonstrates an insecure two-factor authentication (2FA) implementation where the verification code can be brute-forced due to insufficient protection against repeated authentication attempts. The lack of effective rate limiting and account lockout mechanisms enables an attacker to guess the verification code and bypass the second authentication factor.

---

## Objective

Assess the application's two-factor authentication implementation and identify a method to bypass it through a brute-force attack against the verification code.

---

## Lab Information

| Property | Value |
|----------|-------|
| Platform | PortSwigger Web Security Academy |
| Category | Authentication |
| Difficulty | Expert |
| Vulnerability | Weak 2FA Protection |
| Tools Used | Burp Suite Professional, Mozilla Firefox |

---

## Vulnerability Description

The application allows repeated submission of two-factor authentication codes without implementing sufficient protections such as request throttling, account lockout, or temporary delays. This enables an attacker to systematically test possible verification codes until the correct value is identified.

---

## Attack Methodology

1. Authenticate using valid user credentials.
2. Capture the two-factor authentication request using Burp Suite.
3. Configure Burp Intruder to automate verification code attempts.
4. Execute the brute-force attack against the 2FA verification endpoint.
5. Identify the valid verification code from the server response.
6. Successfully authenticate and complete the lab.

---

## Outcome

The two-factor authentication mechanism was successfully bypassed by brute-forcing the verification code, demonstrating inadequate protection against repeated authentication attempts.

---

## Security Impact

Weak protection of 2FA verification endpoints significantly reduces the effectiveness of multi-factor authentication. Attackers who obtain valid credentials can bypass the additional security layer through automated verification code guessing.

---

## Recommended Mitigations

- Enforce strict rate limiting on verification attempts.
- Lock or temporarily suspend verification after multiple failed attempts.
- Generate short-lived, unpredictable verification codes.
- Monitor and alert on repeated failed 2FA attempts.
- Require re-authentication after excessive verification failures.

---

## References

- PortSwigger Web Security Academy
- OWASP Authentication Cheat Sheet
- OWASP Top 10 – Identification and Authentication Failures

---

## Disclaimer

This lab was completed within the controlled environment provided by the PortSwigger Web Security Academy. All testing activities were performed solely for educational purposes on intentionally vulnerable applications.
