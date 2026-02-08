# 🐧 Linux File Permissions & Security Hardening

## 📌 Executive Summary
As a security analyst, ensuring that sensitive files are only accessible to authorized users is a critical defensive task. In this lab, I managed user and group permissions in a Linux environment to secure organizational data, specifically focusing on the `projects` directory and its contents.

---

## 🔍 Permission Analysis
I examined the initial state of the file system to identify security risks where unauthorized users (the "other" category) had excessive access to sensitive files.

### Initial File State:
* **Directory:** `projects`
* **Files:** `project_k.txt`, `project_m.txt`
* **Objective:** Ensure the `researcher2` user and the `research_team` group have appropriate access while removing permissions for all other users.

---

## 🛠️ Security Hardening Steps

### 1. Modifying Directory Permissions
The `projects` directory was initially accessible by all users. I restricted access so that only the owner and the group could access the directory, following the **Principle of Least Privilege**.
* **Command:** `chmod 750 projects`
* **Result:** The owner has full access (rwx), the group can read and execute (r-x), and others have no access (---).

### 2. Securing Sensitive Files
I updated the permissions for specific project files to ensure they were not world-readable.
* **File:** `project_m.txt`
* **Action:** Removed write permissions for the group and all permissions for others.
* **Command:** `chmod 640 project_m.txt`

### 3. Changing File Ownership
To ensure the correct users managed the files, I updated the ownership of `project_k.txt`.
* **Command:** `chown researcher2 project_k.txt`
* **Result:** `researcher2` became the official owner, allowing for individual accountability.

---

## 🧠 Key Takeaways
1. **Access Control:** Demonstrated proficiency in using `chmod` and `chown` to manage the **Authorization** aspect of security.
2. **Linux CLI:** Gained hands-on experience with the Linux terminal, a mandatory tool for security monitoring and server management.
3. **Data Integrity:** By restricting write access, I ensured that unauthorized users could not modify or delete critical project data.

---
**Source:** This file permissions lab scenario is provided by the **Google Cybersecurity Professional Certificate** curriculum on Coursera.
