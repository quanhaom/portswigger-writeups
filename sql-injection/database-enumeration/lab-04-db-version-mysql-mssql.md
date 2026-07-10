# Lab: SQL Injection Attack, Querying the Database Type and Version on MySQL and Microsoft SQL Server

## Category

SQL Injection

## Difficulty

Practitioner

## Overview

This lab focuses on identifying backend database technologies through a SQL Injection vulnerability. Understanding the database platform helps security professionals assess risk and understand technology-specific security considerations.

## Root Cause

The application allows user-controlled input to influence database queries without adequate separation between data and query logic.

## Key Concepts

* Database fingerprinting
* Information disclosure
* DBMS identification
* Technology exposure

## Impact

Potential consequences include:

* Disclosure of backend technology details
* Improved attacker reconnaissance
* Increased effectiveness of subsequent attacks
* Exposure of database version information

## Detection Summary

Testing revealed that application behavior exposed characteristics of the underlying database platform, indicating that database interactions were not sufficiently protected.

## Remediation

* Use parameterized queries
* Limit information disclosure
* Implement secure error handling
* Harden database configurations

## Lessons Learned

* Technology disclosure can significantly aid attackers.
* Database fingerprinting is a common assessment activity.
* SQL Injection can reveal infrastructure information in addition to application data.

## OWASP Mapping

* A03:2021 – Injection

## CWE Mapping

* CWE-89

## Status

Completed
