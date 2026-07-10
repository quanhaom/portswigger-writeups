# Lab: SQL Injection Attack, Listing the Database Contents on Non-Oracle Databases

## Category

SQL Injection

## Difficulty

Practitioner

## Overview

This lab demonstrates how a SQL Injection vulnerability can expose information about database structure, including available tables and stored data.

## Root Cause

User-controlled input is incorporated into database queries without secure parameterization, allowing unintended interaction with database metadata and application data.

## Key Concepts

* Database enumeration
* Metadata exposure
* Information disclosure
* Database structure discovery

## Impact

Potential consequences include:

* Exposure of database schema information
* Discovery of sensitive tables
* Increased effectiveness of follow-up attacks
* Potential disclosure of sensitive records

## Detection Summary

Assessment activities indicated that database metadata could be accessed through vulnerable query functionality.

## Remediation

* Parameterized queries
* Principle of least privilege
* Restrict metadata access where possible
* Secure database architecture

## Lessons Learned

* Database schema information can be highly sensitive.
* Metadata disclosure increases attack surface.
* SQL Injection frequently enables broader reconnaissance activities.

## OWASP Mapping

* A03:2021 – Injection

## CWE Mapping

* CWE-89

## Status

Completed
