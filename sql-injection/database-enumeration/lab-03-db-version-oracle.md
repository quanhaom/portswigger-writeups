# Lab: SQL Injection Attack, Querying the Database Type and Version on Oracle

## Category

SQL Injection

## Difficulty

Practitioner

## Overview

This lab focuses on database fingerprinting through a SQL Injection vulnerability. Understanding the database platform is often an important step in assessing security risk and determining defensive requirements.

## Root Cause

The application exposes a SQL Injection point that allows interaction with backend database functionality. Insufficient separation between user input and database queries enables unintended query behavior.

## Key Concepts

* Database fingerprinting
* Oracle database characteristics
* Information disclosure through SQL Injection

## Impact

Potential consequences include:

* Disclosure of backend technology information
* Improved attacker understanding of the environment
* Increased effectiveness of follow-up attacks

## Detection Summary

Testing revealed that user-controlled input could influence database interactions and expose characteristics of the underlying database platform.

## Remediation

* Parameterized queries
* Minimize database information disclosure
* Secure error handling
* Database hardening practices

## Lessons Learned

* Technology disclosure can increase risk.
* Database fingerprinting is often an early assessment objective.
* SQL Injection can expose more than application data.

## OWASP Mapping

* A03:2021 – Injection

## CWE Mapping

* CWE-89

## Status

Completed
