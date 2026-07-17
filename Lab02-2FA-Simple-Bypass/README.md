# Lab 02 – 2FA Simple Bypass

## Overview

This lab demonstrates an authentication flaw where the application fails to properly enforce two-factor authentication (2FA), allowing access to authenticated resources without completing the verification process.

---

## Objective

Assess the authentication workflow and identify a method to bypass the second authentication factor.

---

## Vulnerability

The application relies on client-side navigation rather than server-side validation to enforce the 2FA process. As a result, an authenticated user can directly access protected resources without successfully completing the second verification step.

---

## Environment

| Item | Details |
|------|---------|
| Platform | PortSwigger Web Security Academy |
| Category | Authentication |
| Difficulty | Apprentice |
| Tools | Burp Suite Professional, Mozilla Firefox |

---

## Methodology

1. Authenticate using valid user credentials.
2. Intercept the authentication flow using Burp Suite.
3. Analyze the 2FA verification request.
4. Modify the workflow to bypass the verification step.
5. Access the protected resource.
6. Successfully complete the lab.

---

## Result

The authentication mechanism was successfully bypassed by exploiting improper server-side validation of the two-factor authentication process.

---

## Security Impact

Improper enforcement of 2FA allows attackers with valid credentials to gain unauthorized access without completing the additional verification step, significantly reducing the effectiveness of multi-factor authentication.

---

## Mitigation

- Enforce 2FA validation on the server side.
- Bind user sessions to successful 2FA completion.
- Prevent direct access to protected resources before verification.
- Validate authentication state on every sensitive request.

---

## References

- PortSwigger Web Security Academy
- OWASP Authentication Cheat Sheet
