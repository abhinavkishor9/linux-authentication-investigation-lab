# linux-authentication-investigation-lab

## Overview

This Linux investigation lab demonstrates how native Linux commands and system logs can be used to investigate user activity, authentication events, scheduled tasks, permissions, and potential persistence mechanisms.

The investigation reconstructs system activity by correlating evidence collected from user accounts, authentication logs, cron jobs, file permissions, and privilege information.

---

# Executive Summary

This investigation demonstrates how Linux authentication and system activity can be reconstructed using native Linux utilities.

The investigation included:

- Enumerating user and group information
- Validating user privileges
- Investigating file ownership and permissions
- Reviewing scheduled Cron jobs
- Examining authentication logs
- Correlating evidence from multiple system sources
- Reconstructing investigation findings

---

# Learning Objectives

- Understand Linux user authentication
- Investigate user accounts and privileges
- Analyze Linux file ownership and permissions
- Examine Cron jobs and scheduled tasks
- Review Linux authentication logs
- Correlate multiple evidence sources
- Reconstruct user activity

---

# Skills Demonstrated

- Linux Administration
- Linux User Enumeration
- Privilege Analysis
- File Permission Analysis
- Cron Job Investigation
- Authentication Log Analysis
- System Log Investigation
- Evidence Correlation
- Timeline Reconstruction
- Investigation Documentation

---

# Tools Used

- Ubuntu Linux
- Bash Shell
- journalctl
- auth.log
- cron
- stat
- id
- groups
- whoami
- ls
- cat
- getent

---

# Lab Environment

| Component | Details |
|-----------|---------|
| Operating System | Ubuntu 24.04 LTS |
| Platform | WSL |
| Investigation Type | Linux System Investigation |
| Log Sources | auth.log, journalctl |
| Scheduler | Cron |
| User | abhinav |

---

# Investigation Scenario

A Linux workstation requires investigation to determine user privileges, authentication activity, scheduled tasks, and system permissions.

The investigation objectives are:

- Identify active users
- Verify user privileges
- Review authentication activity
- Examine scheduled tasks
- Validate file ownership
- Correlate collected evidence

---

# Investigation Workflow

1. Enumerate current user information.
2. Review user privileges.
3. Validate file permissions.
4. Examine Linux user database.
5. Review scheduled Cron jobs.
6. Analyze authentication logs.
7. Correlate collected evidence.
8. Document investigation findings.

---

# MITRE ATT&CK Mapping

| Tactic | Technique | ID |
|---------|-----------|----|
| Persistence | Scheduled Task / Cron | T1053.003 |
| Privilege Escalation | Valid Accounts | T1078 |
| Discovery | Account Discovery | T1087 |

### Why Linux Authentication Investigation Matters

Linux authentication records, user privileges, and scheduled tasks provide valuable evidence during security investigations. Reviewing these artifacts helps analysts identify unauthorized access, privilege misuse, persistence mechanisms, and abnormal system activity.

---

# Evidence Collected

- Current User Information
- User Privileges
- Group Membership
- File Permissions
- Cron Configuration
- Authentication Logs
- System Journal
- User Database

---

# Evidence Correlation

| Evidence Source | Information Obtained | Investigation Value |
|-----------------|---------------------|--------------------|
| whoami / id | Active user details | User identification |
| /etc/passwd | User accounts | Account verification |
| groups | Group membership | Privilege validation |
| stat | File ownership | Permission analysis |
| Cron | Scheduled jobs | Persistence review |
| auth.log | Authentication activity | Login verification |
| journalctl | System events | Activity correlation |

---

# Investigation Findings

- Active user successfully identified.
- User privilege membership verified.
- File ownership and permissions validated.
- Scheduled Cron configuration reviewed.
- Authentication logs confirmed user activity.
- Multiple evidence sources consistently reconstructed system activity.

---

# Key Takeaways

- Native Linux utilities provide valuable investigative evidence.
- Authentication logs help reconstruct user activity.
- Cron jobs should always be reviewed for persistence.
- File permissions assist in validating ownership and privilege.
- Correlating multiple evidence sources improves investigation accuracy.

---
