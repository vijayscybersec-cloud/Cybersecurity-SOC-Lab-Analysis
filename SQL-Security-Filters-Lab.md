# 🔍 SQL Security Analysis: Filtering Database Queries

## 📌 Executive Summary
In this lab, I acted as a security analyst responsible for investigating potential security incidents and updating system information using **SQL**. I applied advanced filtering techniques to large datasets (the `log_in_attempts` and `employees` tables) to isolate suspicious login activity and identify machines requiring security updates.

---

## 🔍 Incident Investigation with SQL

### 1. Identifying After-Hours Failed Logins
A potential security incident occurred after business hours (18:00). I needed to isolate all failed login attempts during this period to identify brute force or unauthorized access attempts.

* **SQL Query:**
    ```sql
    SELECT * FROM log_in_attempts WHERE login_time > '18:00' AND success = FALSE;
    ```
* **Result:** This query filtered the database to show only unsuccessful entries that happened late at night, allowing the team to focus on high-risk events.

### 2. Investigating Specific Dates
A suspicious event was reported on **2022-05-09**. I expanded the search to include the day before to see if there were any "warm-up" activities by an attacker.

* **SQL Query:**
    ```sql
    SELECT * FROM log_in_attempts WHERE login_date = '2022-05-09' OR login_date = '2022-05-08';
    ```
---

## 🛠️ Security Hardening & Data Filtering

### 3. Locating Vulnerable Machines
I used the `LIKE` operator and wildcards (`%`) to find all computers located in the **Mexico** office that required a specific security patch.

* **SQL Query:**
    ```sql
    SELECT * FROM employees WHERE country LIKE 'MEX%';
    ```

### 4. Department-Specific Security Audits
I filtered for employees in the **Finance** and **Sales** departments to perform targeted identity and access audits.

* **SQL Query:**
    ```sql
    SELECT * FROM employees WHERE department = 'Finance' OR department = 'Sales';
    ```

### 5. Identifying Non-IT Assets
To verify that security protocols were being applied correctly outside the core technical team, I queried for all employees *not* in the **Information Technology** department.

* **SQL Query:**
    ```sql
    SELECT * FROM employees WHERE NOT department = 'Information Technology';
    ```

---

## 🧠 Key Learning Outcomes
1.  **Data Precision:** Mastered the use of `AND`, `OR`, and `NOT` operators to refine security searches and reduce "noise" in the logs.
2.  **Pattern Recognition:** Used the `LIKE` operator with percentage wildcards to search for regional or system-naming patterns.
3.  **SOC Readiness:** Demonstrated the ability to use SQL—a core tool for SIEM platforms like Splunk or Chronicle—to perform forensic investigations.

---
**Source:** This SQL filtering lab scenario and the database structures used are provided by the **Google Cybersecurity Professional Certificate** curriculum on Coursera.
