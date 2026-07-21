# Lab 04 – Broken Brute-Force Protection, IP Block

## Overview

This lab demonstrates an authentication vulnerability where an application's brute-force protection mechanism is improperly implemented. Although the application attempts to restrict repeated login attempts using IP-based blocking, the protection can be bypassed, allowing continued password guessing against a valid user account.

---

## Objective

Evaluate the effectiveness of the application's brute-force protection mechanism and identify a technique to bypass the implemented IP-based restriction.

---

## Lab Information

| Property | Value |
|----------|-------|
| Platform | PortSwigger Web Security Academy |
| Category | Authentication |
| Difficulty | Practitioner |
| Vulnerability | Broken Brute-Force Protection |
| Tools Used | Burp Suite Professional, Mozilla Firefox |

---

## Vulnerability Description

The application relies on IP-based restrictions to defend against brute-force attacks. However, the implementation does not adequately prevent automated authentication attempts, enabling an attacker to continue testing credentials despite the intended protection.

---

## Attack Methodology

1. Intercept the authentication request using Burp Suite.
2. Analyze the application's brute-force protection mechanism.
3. Configure Burp Intruder to automate authentication attempts.
4. Bypass the IP-based restriction.
5. Identify the valid credentials.
6. Authenticate successfully and complete the lab.

---

## Outcome

The IP-based brute-force protection was successfully bypassed, allowing continued authentication attempts until valid credentials were identified.

---

## Security Impact

Weak brute-force protection significantly increases the risk of unauthorized account access. Attackers can exploit ineffective rate-limiting mechanisms to perform automated password guessing and credential-based attacks.

---

## Recommended Mitigations

- Implement account-based and IP-based rate limiting.
- Enforce progressive account lockout after repeated failed login attempts.
- Deploy Multi-Factor Authentication (MFA).
- Detect and block distributed brute-force attacks.
- Monitor authentication logs for abnormal login activity.
- Introduce CAPTCHA or adaptive authentication after multiple failed attempts.

---

## References

- PortSwigger Web Security Academy
- OWASP Authentication Cheat Sheet
- OWASP Top 10 – Identification and Authentication Failures

---

## Disclaimer

This lab was completed within the controlled environment provided by the PortSwigger Web Security Academy. All testing activities were performed for educational purposes on intentionally vulnerable applications.
