# Lab: SQL Injection UNION Attack, Retrieving Multiple Values in a Single Column

## Category

SQL Injection

## Difficulty

Practitioner

## Overview

This lab highlights how database query results may be combined and processed within an application. It demonstrates the importance of understanding data representation and output handling in SQL Injection scenarios.

## Root Cause

User-controlled input is incorporated into database queries without proper separation from SQL instructions, allowing query behavior to be modified.

## Key Concepts

* UNION-based SQL Injection
* Data aggregation
* Result set processing
* Application output handling

## Security Significance

Applications often display only a subset of available data. Understanding how information is formatted and returned can influence the impact of a SQL Injection vulnerability.

## Impact

Potential consequences include:

* Exposure of sensitive information
* Increased effectiveness of reconnaissance activities
* Enhanced visibility into application data structures
* Support for further compromise efforts

## Detection Summary

Testing demonstrated that application output behavior could reveal information about how database results were processed and presented.

## Remediation

* Parameterized queries
* Secure coding standards
* Database least privilege
* Security-focused code review practices

## Lessons Learned

* Data presentation logic influences security outcomes.
* Information disclosure often results from multiple design weaknesses.
* SQL Injection remains one of the most impactful application vulnerabilities.

## Professional Takeaway

Understanding the relationship between backend databases and frontend presentation layers is essential for effective application security assessment.

## OWASP Mapping

* A03:2021 – Injection

## CWE Mapping

* CWE-89

## Status

Completed
