# Lab: SQL Injection Vulnerability in WHERE Clause Allowing Retrieval of Hidden Data

## Category

SQL Injection

## Difficulty

Apprentice

## Overview

This lab demonstrates a SQL Injection vulnerability affecting a database query used to retrieve product information. The application incorporates user-controlled input into a SQL query without sufficient validation or parameterization.

As a result, the database query logic can be altered, allowing unintended information to be returned by the application.

## Vulnerability Type

* OWASP Top 10 2021: A03 – Injection
* CWE-89: SQL Injection

## Root Cause

The application constructs SQL queries using untrusted user input.

When user-supplied data is processed directly within a database query, the intended filtering logic may be modified. This allows attackers to influence how the database interprets the query.

The primary cause is the absence of secure parameterized queries and proper input handling.

## Impact

Potential consequences include:

* Unauthorized access to hidden records
* Exposure of sensitive business data
* Authentication bypass in certain scenarios
* Data modification or deletion in more severe cases
* Increased attack surface for further exploitation

## Detection

The issue was identified during testing of application functionality that interacts with backend database queries.

Indicators included:

* User-controlled input influencing query results
* Unexpected data being returned
* Changes in application behavior when query parameters were manipulated

These observations suggested that database queries were not adequately protected from injection attacks.

## Remediation

Recommended mitigations include:

* Use parameterized queries (prepared statements)
* Avoid dynamic SQL construction using user input
* Apply server-side input validation
* Enforce least-privilege database permissions
* Implement secure error handling
* Conduct regular code reviews and security testing

### Example (Python SQLite)

Vulnerable approach:

```python
query = "SELECT * FROM products WHERE category = '" + category + "'"
```

Secure approach:

```python
cursor.execute(
    "SELECT * FROM products WHERE category = ?",
    (category,)
)
```

## Lessons Learned

* User input should never be trusted.
* Database queries must be parameterized.
* Even simple filtering functionality can introduce serious security risks.
* SQL Injection remains one of the most impactful web application vulnerabilities.

## References

* OWASP Top 10 2021
* CWE-89: SQL Injection
* PortSwigger Web Security Academy

## Status

Completed
