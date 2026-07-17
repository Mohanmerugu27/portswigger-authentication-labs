# Lab 03 – Username Enumeration via Response Timing

## Overview

This lab demonstrates a username enumeration vulnerability caused by measurable differences in authentication response times. Although the application returns identical error messages, variations in processing time allow an attacker to identify valid usernames.

---

## Objective

Identify a valid username by analyzing authentication response times and complete the login process.

---

## Technical Summary

| Property | Value |
|----------|-------|
| Platform | PortSwigger Web Security Academy |
| Category | Authentication |
| Difficulty | Practitioner |
| Tools | Burp Suite Professional, Mozilla Firefox |

---

## Vulnerability Description

The authentication mechanism processes requests for valid usernames differently from invalid usernames. This results in observable timing discrepancies that can be exploited to enumerate existing accounts.

---

## Attack Methodology

1. Intercept the authentication request using Burp Suite.
2. Forward the request to Burp Repeater.
3. Submit multiple authentication requests with different usernames while keeping the password constant.
4. Compare the response times for each request.
5. Identify the valid username based on the timing variation.
6. Authenticate successfully and complete the lab.

---

## Outcome

A valid username was successfully identified through response timing analysis, allowing the authentication process to be completed.

---

## Security Impact

Username enumeration significantly improves the success rate of password brute-force and credential stuffing attacks by allowing attackers to focus on valid user accounts.

---

## Recommended Mitigations

- Ensure authentication requests execute in consistent time.
- Return identical authentication responses for valid and invalid usernames.
- Implement rate limiting and account lockout mechanisms.
- Monitor authentication logs for enumeration attempts.

---

## References

- PortSwigger Web Security Academy
- OWASP Authentication Cheat Sheet
