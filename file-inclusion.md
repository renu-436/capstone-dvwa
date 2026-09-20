# File Inclusion

## Objective

The objective was to determine whether the DVWA application allowed user-controlled file paths to be used for local file inclusion.

## Security Level

Low

## Normal Test

A normal DVWA file was selected through the File Inclusion interface.

## Test

The page parameter was modified to reference a local system file:

../../../../etc/passwd

## Observation

The application processed the modified path and exposed contents of a local system file.

## Vulnerability

This demonstrates Local File Inclusion / path traversal behavior caused by insufficient validation of the user-controlled file path.

## Security Impact

A vulnerable application may expose sensitive local files and application information. The actual impact depends on server permissions and application configuration.

## Recommended Mitigation

- Use an allowlist of permitted files.
- Do not accept arbitrary file paths from users.
- Validate and canonicalize file paths.
- Prevent directory traversal.
- Apply least-privilege permissions.
- Avoid directly passing user-controlled paths to file inclusion functions.

