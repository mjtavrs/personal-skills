---
name: secure-backend-review
description: Use this skill when creating or changing endpoints, authentication, authorization, queries, file uploads, external integrations, or any business logic that touches sensitive or user-controlled data.
---

# Secure Backend Review

## Goal
Review backend code and decisions with a strict security-first mindset.

## When to use
Use this skill for:
- new endpoints
- endpoint changes
- authentication or authorization logic
- file upload flows
- database queries
- external API integrations
- business rules involving user identity, permissions, or sensitive data

Do not use this skill for purely visual UI changes with no data or security impact.

## Mandatory mindset
Assume inputs are hostile until validated.
Assume users may try to access resources they do not own.
Assume sensitive data can leak unless intentionally protected.
Prefer deny-by-default behavior.

## Always verify
- authentication exists where required
- authorization is checked at the correct layer
- resource ownership is verified
- user input is validated and sanitized
- output does not expose sensitive fields
- internal errors are not leaked to clients
- logs do not contain secrets or sensitive personal data
- queries are safe against injection
- business rules cannot be bypassed from the client
- abusive scenarios are considered

## Common risks to look for
- IDOR / access to resources from other users
- missing authorization checks
- trusting frontend flags or roles
- overposting / mass assignment
- insecure default values
- excessive data in API responses
- unsafe file upload handling
- weak error handling
- unsafe query construction
- inconsistent permission checks between endpoints

## Code expectations
- never trust client-side validation alone
- validate request body, params, query, and headers when relevant
- keep permission logic explicit
- prefer small, testable functions
- isolate security-critical decisions in clear places
- reject ambiguous access rather than allowing it

## Output format
Always provide:
1. Security findings
2. Severity level for each finding
3. Exact correction proposed
4. Brief implementation impact
5. Plain-language summary for non-technical readers