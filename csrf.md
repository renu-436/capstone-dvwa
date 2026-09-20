# Cross-Site Request Forgery (CSRF)

## Objective

The objective was to understand whether DVWA's password-change functionality properly protects state-changing requests against Cross-Site Request Forgery.

## Security Level

Low

## Normal Test

A password-change request was performed using a lab-only test password.

## Observation

The request was inspected using the browser's developer tools.

At the Low security level, the application demonstrates insufficient CSRF protection and does not use a strong anti-CSRF token to validate the request.

## Security Impact

CSRF can cause an authenticated user's browser to perform an unintended action when an application does not adequately verify the origin and authenticity of state-changing requests.

Potential impact depends on the functionality exposed by the application.

## Recommended Mitigation

- Implement unpredictable anti-CSRF tokens.
- Validate CSRF tokens on the server.
- Use SameSite cookie protections.
- Validate Origin or Referer headers where appropriate.
- Require re-authentication for sensitive operations.

## Evidence

screenshots/task5_csrf_normal.png

screenshots/task5_csrf_request.png
