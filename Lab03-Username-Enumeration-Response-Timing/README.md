# Lab 03 – Username Enumeration via Response Timing

## Overview

This lab demonstrates how authentication response times can unintentionally reveal valid usernames. Even when the application returns identical error messages, measurable timing differences can allow attackers to enumerate existing accounts.

---

## Objective

Identify a valid username by analyzing the response time of authentication requests.

---

## Vulnerability

The application processes valid usernames differently from invalid usernames, resulting in noticeable response time variations. An attacker can exploit this behavior to determine whether a username exists.

---

## Environment

| Item | Details |
|------|---------|
| Platform | PortSwigger Web Security Academy |
| Category | Authentication |
| Difficulty | Practitioner |
| Tools Used | Burp Suite Professional, Mozilla Firefox |

---

## Methodology

1. Intercept the login request using Burp Suite Proxy.
2. Send the request to Burp Repeater.
3. Test multiple usernames while keeping the password constant.
4. Compare the response times for each request.
5. Identify the valid username based on the timing difference.
6. Continue the authentication process to complete the lab.

---

## Result

Successfully identified a valid username through response timing analysis and completed the lab.

---

## Security Impact

Timing-based username enumeration enables attackers to discover valid accounts, increasing the effectiveness of password brute-force and credential stuffing attacks.

---

## Mitigation

- Ensure authentication requests have consistent response times.
- Return generic authentication responses.
- Implement rate limiting and account lockout policies.
- Monitor and log suspicious authentication attempts.

---

## References

- PortSwigger Web Security Academy
- OWASP Authentication Cheat Sheet
