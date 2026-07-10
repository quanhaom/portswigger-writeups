# Lab: SQL Injection Vulnerability Allowing Login Bypass

## Summary

This lab demonstrates how insecure handling of user-controlled input within an authentication workflow can lead to a SQL Injection vulnerability. The issue allows the application's authentication logic to be manipulated, resulting in unauthorized access.

## Category

* SQL Injection
* Authentication Security

## Difficulty

Apprentice

## OWASP Mapping

* A03:2021 – Injection

## CWE Mapping

* CWE-89: Improper Neutralization of Special Elements used in an SQL Command

## Scenario

The application contains a login functionality backed by a database. User credentials are processed by a server-side query that does not adequately separate user input from query logic.

As a result, the authentication mechanism can be influenced by crafted input.

## Root Cause Analysis

The vulnerability exists because user-controlled data is incorporated into a database query without proper parameterization.

Instead of treating input strictly as data, the database interpreter may process portions of the input as query instructions, altering the intended logic.

## Security Impact

Potential impacts include:

* Unauthorized access
* Account compromise
* Privilege escalation
* Exposure of restricted functionality
* Further compromise of application resources

## Detection Indicators

The following indicators suggested a possible SQL Injection issue:

* Authentication behavior changed unexpectedly when input values were modified.
* Input appeared to influence backend query processing.
* Access control decisions were affected by malformed or specially crafted input.

## Remediation

Recommended mitigations:

* Use parameterized queries (prepared statements).
* Avoid dynamic SQL query construction.
* Implement secure authentication design.
* Apply least-privilege permissions for database accounts.
* Perform security testing on all authentication-related features.

### Vulnerable Pattern

```python
query = "SELECT * FROM users WHERE username = '" + username + "'"
```

### Secure Pattern

```python
cursor.execute(
    "SELECT * FROM users WHERE username = ?",
    (username,)
)
```

## Lessons Learned

* Authentication systems are high-value targets.
* User input must never be trusted.
* Parameterized queries are essential.
* SQL Injection remains one of the most critical web application risks.

## References

* OWASP Top 10 2021
* CWE-89
* PortSwigger Web Security Academy

## Status

Completed
