# SQL Injection: Authentication Bypass

## Overview
A practical write-up demonstrating an **Authentication Bypass** vulnerability via In-band SQL Injection on a vulnerable login form (OWASP Juice Shop)[cite: 1].

## Target & Vulnerability
* **Application:** OWASP Juice Shop[cite: 1]
* **Endpoint:** `/rest/user/login`
* **Vulnerability Type:** In-band SQL Injection (Authentication Bypass)

## Technical Mechanism
The vulnerable backend constructs queries using unsafe string concatenation:
```sql
SELECT * FROM Users WHERE email = 'USER_INPUT' AND password = 'PASSWORD_INPUT' AND deletedAt IS NULL;
