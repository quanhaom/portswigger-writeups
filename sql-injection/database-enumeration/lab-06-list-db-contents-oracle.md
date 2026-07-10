# Lab: SQL Injection Attack, Listing the Database Contents on Oracle

## Category

SQL Injection

## Difficulty

Practitioner

## Overview

This lab explores database enumeration techniques in Oracle environments. The exercise highlights how SQL Injection can expose information about database structure and stored information.

## Root Cause

The application fails to adequately separate user input from database query logic, enabling unintended interaction with Oracle database components.

## Key Concepts

* Oracle database enumeration
* Metadata exposure
* Information disclosure
* Database reconnaissance

## Impact

Potential consequences include:

* Exposure of database schema details
* Discovery of sensitive application data
* Improved attacker understanding of the environment
* Increased risk of data compromise

## Detection Summary

Testing revealed that database metadata and structural information were accessible through vulnerable query processing.

## Remediation

* Use prepared statements
* Limit access to metadata resources
* Implement least-privilege database permissions
* Perform regular security reviews

## Lessons Learned

* Database metadata is valuable information.
* Oracle environments require the same secure query practices as other DBMS platforms.
* SQL Injection often enables extensive information gathering activities.

## OWASP Mapping

* A03:2021 – Injection

## CWE Mapping

* CWE-89

## Status

Completed
