# Authentication / Brute Force Testing

## Objective

The objective of this test was to evaluate the authentication mechanism of DVWA and demonstrate the risk of repeated login attempts.

## Target

- Application: Damn Vulnerable Web Application (DVWA)
- Environment: Local authorized lab
- Target: 127.0.0.1
- Security Level: Low

## Normal Authentication Test

A normal authentication attempt was performed using the configured DVWA lab credentials.

The successful authentication demonstrated that the login functionality was working normally.

Screenshot:

![Normal Authentication](screenshots/task5_auth_normal.png)

## Brute Force Testing

A small password list was used to perform a controlled authentication test against the local DVWA application.

The test demonstrated that multiple authentication attempts could be made without effective rate limiting or account lockout at the selected Low security level.

Screenshot:

![Brute Force Testing](screenshots/task5_auth_bruteforce.png)

## Security Impact

Weak authentication controls can allow attackers to repeatedly guess passwords.

Potential impacts include:

- Account compromise
- Password guessing
- Unauthorized access
- Increased risk from weak passwords

## Recommended Mitigations

1. Implement rate limiting.
2. Use temporary account lockout after repeated failures.
3. Require strong passwords.
4. Implement multi-factor authentication (MFA).
5. Monitor and log failed authentication attempts.
6. Use secure password hashing algorithms.
7. Use generic authentication error messages.
8. Consider CAPTCHA or other anti-automation controls where appropriate.

## Conclusion

The controlled DVWA test demonstrated the importance of protecting authentication mechanisms against repeated login attempts. Rate limiting, strong passwords, MFA, monitoring, and appropriate account protection can significantly reduce brute-force risk.
