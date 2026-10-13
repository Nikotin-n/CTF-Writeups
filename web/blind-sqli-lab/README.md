# SQL Injection: Blind SQLi (Boolean & Time-based)

## Overview
A technical analysis and documentation of **Blind SQL Injection**, exploring how to extract information from a web application when the database does not return direct data or error messages (the application is "blind").

## Target & Vulnerability
* **Application:** OWASP Juice Shop (SQLite backend)
* **Vulnerability Type:** Inferential / Blind SQL Injection (Boolean-based & Time-based)
* **Objective:** Extracting data and validating conditions iteratively via application behavior or processing delays.

---

## Technical Mechanism & Concepts

### 1. What is Blind SQLi?
When an application is vulnerable to SQL injection but does not display query results or error messages on the page, attackers must rely on indirect feedback mechanisms:
* **Boolean-based Blind:** The application responds differently (e.g., standard page vs. empty/error page) based on whether an injected condition evaluates to `True` or `False`.
* **Time-based Blind:** The application pauses or delays its response if an injected condition is `True`, allowing the attacker to measure execution time.

---

## Attack Methodology & Payloads (SQLite Context)

### 1. Boolean-based Blind Technique
By asking binary (True/False) questions to the database and observing whether content loads:
```sql
' AND (SELECT length(email) FROM users WHERE id=1) = 25 --
