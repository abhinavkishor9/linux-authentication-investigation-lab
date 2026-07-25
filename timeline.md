# Investigation Timeline

| Time | Activity | Evidence |
|------|----------|----------|
| 09:00 | Enumerated current user | whoami, id |
| 09:03 | Verified user privileges | groups, sudo -l |
| 09:06 | Validated file ownership | stat, ls |
| 09:10 | Reviewed Linux user database | /etc/passwd |
| 09:15 | Investigated Cron configuration | /etc/crontab |
| 09:20 | Analyzed authentication logs | auth.log |
| 09:25 | Correlated collected evidence | journalctl |
| 09:30 | Completed investigation | Documentation |

---

# Investigation Flow

Investigation Started

↓

Identified Current User

↓

Validated User Privileges

↓

Verified File Ownership

↓

Reviewed User Database

↓

Investigated Cron Configuration

↓

Analyzed Authentication Logs

↓

Correlated Evidence

↓

Investigation Completed

---

# Summary

The investigation successfully reconstructed Linux user activity using native Linux commands and system logs. Evidence collected from user accounts, file permissions, authentication logs, Cron configuration, and system journals consistently validated user activity while demonstrating a structured Linux investigation workflow.
