# Lab 07 – 2FA Simple Bypass

## Overview

This lab demonstrates an authentication vulnerability where the application fails to properly enforce two-factor authentication (2FA). By manipulating the authentication workflow, an attacker can gain access to a user account without successfully completing the second authentication factor.

---

## Objective

Assess the authentication workflow and identify a method to bypass the application's two-factor authentication mechanism.

---

## Lab Information

| Property | Value |
|----------|-------|
| Platform | PortSwigger Web Security Academy |
| Category | Authentication |
| Difficulty | Practitioner |
| Vulnerability | 2FA Bypass |
| Tools Used | Burp Suite Professional, Mozilla Firefox |

---

## Vulnerability Description

The application does not properly validate whether the second authentication factor has been successfully completed before granting access to protected resources. This allows an attacker to bypass the 2FA process and access authenticated functionality.

---

## Attack Methodology

1. Authenticate using valid user credentials.
2. Intercept the authentication workflow with Burp Suite.
3. Analyze the 2FA verification process.
4. Manipulate the authentication flow to bypass the second verification step.
5. Access the authenticated application.
6. Successfully complete the lab.

---

## Outcome

The authentication workflow was successfully bypassed, allowing access to the application without completing the second authentication factor.

---

## Security Impact

Improper enforcement of two-factor authentication significantly weakens account security. Attackers with valid credentials can bypass the additional verification layer and gain unauthorized access.

---

## Recommended Mitigations

- Enforce server-side validation of the 2FA process.
- Bind authenticated sessions to successful 2FA completion.
- Prevent direct access to protected resources before verification.
- Invalidate incomplete authentication sessions.
- Log and monitor suspicious authentication events.

---

## References

- PortSwigger Web Security Academy
- OWASP Authentication Cheat Sheet
- OWASP Top 10 – Identification and Authentication Failures

---

## Disclaimer

This lab was completed within the controlled environment provided by the PortSwigger Web Security Academy. All testing activities were performed solely for educational purposes on intentionally vulnerable applications.
