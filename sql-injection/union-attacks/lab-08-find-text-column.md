# Lab: SQL Injection UNION Attack, Finding a Column Containing Text

## Category

SQL Injection

## Difficulty

Practitioner

## Overview

This lab explores data type compatibility within UNION-based SQL Injection scenarios. Understanding how application output maps to database result sets is an important aspect of vulnerability assessment.

## Root Cause

The application allows user input to affect database query execution without adequate safeguards. This creates opportunities for manipulating query output and database interactions.

## Key Concepts

* UNION attacks
* Data type compatibility
* Application response analysis
* Database output handling

## Security Significance

Database engines enforce compatibility requirements between combined result sets. Understanding these requirements helps assess the extent to which application functionality can be influenced through SQL Injection.

## Impact

Potential consequences include:

* Unauthorized data exposure
* Increased visibility into backend systems
* Enhanced effectiveness of follow-up attacks
* Discovery of sensitive application information

## Detection Summary

Application responses revealed indicators about how query results were processed and displayed within the application.

## Remediation

* Use prepared statements
* Apply least-privilege database permissions
* Limit unnecessary information exposure
* Conduct regular application security testing

## Lessons Learned

* Data type handling is a critical part of database security.
* Application output can reveal useful security information.
* SQL Injection extends beyond authentication and filtering flaws.

## Professional Takeaway

Assessing exploitability often requires understanding both database behavior and application presentation logic.

## OWASP Mapping

* A03:2021 – Injection

## CWE Mapping

* CWE-89

## Status

Completed
