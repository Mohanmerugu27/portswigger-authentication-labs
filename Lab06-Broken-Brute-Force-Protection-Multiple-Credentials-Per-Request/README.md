
# Lab 06 – Broken Brute-Force Protection, Multiple Credentials per Request

## Overview

This lab demonstrates an authentication vulnerability where the application's brute-force protection can be bypassed by submitting multiple credential pairs within a single HTTP request. The flawed implementation allows attackers to perform password guessing while avoiding the intended rate-limiting or request-based restrictions.

---

## Objective

Evaluate the application's brute-force protection mechanism and identify a method to bypass it by submitting multiple credentials in a single authentication request.

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

The application enforces brute-force protection on a per-request basis instead of validating each authentication attempt individually. As a result, multiple username and password combinations can be included in a single request, allowing attackers to bypass request-based security controls.

---

## Attack Methodology

1. Intercept the authentication request using Burp Suite.
2. Analyze the request structure and brute-force protection mechanism.
3. Modify the request to include multiple credential pairs.
4. Submit the modified request.
5. Identify the valid credentials from the server response.
6. Authenticate successfully and complete the lab.

---

## Outcome

The application's brute-force protection was successfully bypassed by submitting multiple authentication attempts within a single HTTP request, resulting in successful account authentication.

---

## Security Impact

Ineffective brute-force protection significantly increases the risk of credential guessing attacks. Attackers can exploit request-handling flaws to test numerous credential combinations while avoiding request-based security controls.

---

## Recommended Mitigations

- Validate every authentication attempt individually.
- Apply rate limiting per authentication attempt rather than per HTTP request.
- Implement account lockout after repeated failed logins.
- Deploy Multi-Factor Authentication (MFA).
- Monitor and detect abnormal authentication patterns.

---

## References

- PortSwigger Web Security Academy
- OWASP Authentication Cheat Sheet
- OWASP Top 10 – Identification and Authentication Failures

---

## Disclaimer

This lab was completed within the controlled environment provided by the PortSwigger Web Security Academy. All testing activities were performed solely for educational purposes on intentionally vulnerable applications.
