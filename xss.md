# Cross-Site Scripting (XSS)

## Objective

The objective was to determine whether DVWA improperly processes user-controlled input as executable browser-side script.

## Security Level

Low

## Reflected XSS

A normal input was first submitted to establish baseline behavior.

A harmless JavaScript alert payload was then submitted:

<script>alert('XSS Test')</script>

## Observation

The application processed the input as executable JavaScript, demonstrating reflected XSS behavior.

## Stored XSS

A harmless message was submitted to the stored XSS functionality.

The following test payload was used:

<script>alert('Stored XSS Test')</script>

The application stored and subsequently rendered the input as executable script.

## Security Impact

XSS can allow attacker-controlled JavaScript to execute in a victim's browser. Depending on the application context, this can affect page content, user actions, and information accessible to client-side scripts.

## Recommended Mitigation

- Encode untrusted output.
- Validate input appropriately.
- Use context-aware escaping.
- Implement Content Security Policy.
- Avoid unsafe DOM manipulation.
- Use secure cookie attributes.

