# SQL Injection: Error-based Data Extraction

## Overview
A technical analysis and documentation of **Error-based SQL Injection**, focusing on how verbose database error messages can be weaponized to leak internal database structures and sensitive data when standard output channels are unavailable.

## Target & Vulnerability
* **Application:** OWASP Juice Shop
* **Vulnerability Type:** Error-based SQL Injection
* **Objective:** Information Disclosure & Database Reconnaissance (forcing the database to reveal details via error outputs).

---

## Technical Mechanism & Concepts

### 1. What is Error-based SQLi?
In a standard application, detailed database error messages are hidden from users to maintain security. However, if a web application runs in a debug mode or lacks proper error handling, raw database exceptions are displayed on the screen.

### 2. Attack Methodology
An attacker deliberately injects malformed syntax or triggers specific database functions that result in a runtime error. If the database engine includes parts of the evaluated expression inside the error message, the attacker can use it as a side-channel to exfiltrate data.

---

## Practical Example & Concepts

### Triggering a Syntax/Runtime Error
Injecting unclosed quotes or invalid clauses into search or input fields:
```sql
' AND (SELECT 1/0) --
