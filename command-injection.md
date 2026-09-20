# Command Injection

## Objective

The objective was to determine whether user-controlled input could be used to execute additional operating-system commands through the DVWA application.

## Security Level

Low

## Normal Test

Input:

127.0.0.1

The application executed the expected ping operation.

## Command Injection Test

Input:

127.0.0.1; whoami

## Observation

The application processed the additional command and returned its output, demonstrating that user-controlled input was being passed to a system command without sufficient protection.

## Security Impact

Command injection may allow an attacker to execute unauthorized operating-system commands with the privileges of the application process.

Potential impact can include unauthorized access to files, information disclosure, modification of system resources, or further compromise.

## Recommended Mitigation

- Avoid passing user input directly to operating-system shells.
- Use safe APIs instead of shell execution where possible.
- Validate input using an allowlist.
- Restrict accepted characters and formats.
- Run applications with the minimum required privileges.
- Apply appropriate operating-system security controls.

## Evidence

screenshots/task5_command_normal.png

screenshots/task5_command_injection.png
