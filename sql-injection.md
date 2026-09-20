# SQL Injection

## Objective

The objective was to test whether user-controlled input could alter the SQL query processed by the DVWA application.

## Security Level

Low

## Normal Input

1

The normal input was tested first to establish baseline application behavior.

## Test Input

1' OR '1'='1

## Observation

The application processed the injected input and returned multiple records, demonstrating that user input was being interpreted as part of the SQL query.

## Security Impact

Improper SQL query construction can allow an attacker to manipulate database queries and potentially access unauthorized information.

The actual impact depends on the application's database privileges and implementation.

## Recommended Mitigation

- Use prepared statements.
- Use parameterized SQL queries.
- Validate and sanitize input appropriately.
- Apply least-privilege database permissions.
- Avoid constructing SQL queries through direct string concatenation.

