# SQL Injection: UNION-based Data Exfiltration

## Overview
A technical analysis and documentation of **UNION-based SQL Injection**, focusing on how the `UNION` operator can be leveraged to extract hidden database contents from vulnerable endpoints.

## Target & Vulnerability
* **Application:** OWASP Juice Shop
* **Vulnerability Type:** In-band SQL Injection (UNION-based)
* **Objective:** Data Exfiltration (Retrieving unauthorized data such as user credentials, PII, or internal tables).

---

## Technical Mechanism & Concepts

### 1. How UNION Works in SQL
The `UNION` operator is used to combine the result sets of two or more `SELECT` statements into a single result set displayed directly on the application page.

### 2. Attack Methodology
To successfully execute a UNION-based attack, an attacker must satisfy two strict database constraints:
1. **Matching Column Count:** The injected query must return the exact same number of columns as the original application query.
2. **Compatible Data Types:** The data types in the corresponding columns must match.

---

## Step-by-Step Payload Construction

### Step 1: Determining Column Count (The Probe)
Using `NULL` values safely bypasses data type mismatch errors while testing column counts:
```sql
') UNION SELECT NULL, NULL, NULL, NULL, NULL, NULL, NULL --
