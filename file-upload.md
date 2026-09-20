# File Upload Security Testing

## Objective

The objective was to determine whether the DVWA application properly validates uploaded files.

## Security Level

Low

## Normal Test

A harmless image file was uploaded through the DVWA File Upload functionality.

## Validation Test

A harmless text file was created and submitted to determine whether the application restricted unexpected file types.

Test file:

test.txt

Content:

DVWA file upload security test

## Observation

The application was tested to determine whether its upload functionality properly restricted file types.

At the Low security level, DVWA is intentionally configured with weak security controls.

## Security Impact

Weak file-upload validation can allow unauthorized or potentially dangerous files to be stored on a server. Depending on server configuration, this may lead to further security issues.

## Recommended Mitigation

- Use an allowlist of permitted file types.
- Validate actual file content.
- Restrict maximum file size.
- Generate safe filenames.
- Store uploads outside executable web directories.
- Disable script execution in upload directories.
- Apply least-privilege file permissions.

## Evidence

screenshots/task5_file_upload_normal.png

screenshots/task5_file_upload_validation.png
