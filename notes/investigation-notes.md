# Investigation Notes

## Lab Summary

This investigation focused on analyzing Linux authentication, user privileges, scheduled tasks, file permissions, and system activity using native Linux utilities.

The investigation reconstructed user activity by correlating authentication logs, Cron configuration, user information, and system metadata.

---

## Analyst Methodology

The investigation followed a structured workflow:

1. Enumerate current user.
2. Review user privileges.
3. Validate file ownership.
4. Examine Linux user database.
5. Review scheduled Cron jobs.
6. Analyze authentication logs.
7. Correlate evidence.
8. Document findings.

---

## Investigation Scenario

A Linux workstation required investigation to validate user privileges, authentication activity, scheduled tasks, and file ownership.

The investigation aimed to determine:

- Which user was active.
- What privileges the user possessed.
- Whether scheduled tasks existed.
- Whether authentication activity could be reconstructed.

---

## Evidence Collected

### Evidence 1 – User Information

Commands Used

```bash
whoami
id
groups
```

Finding

Confirmed the active user and verified assigned privilege groups.

---

### Evidence 2 – File Permissions

Commands Used

```bash
ls -la
stat investigation.txt
```

Finding

Validated ownership, permissions, and file metadata.

---

### Evidence 3 – User Database

Commands Used

```bash
cat /etc/passwd
cat /etc/group
getent passwd
```

Finding

Verified local user accounts and group information.

---

### Evidence 4 – Scheduled Tasks

Commands Used

```bash
cat /etc/crontab
crontab -l
ls -la /etc/cron.*
```

Finding

Reviewed scheduled Cron jobs and confirmed system scheduling configuration.

---

### Evidence 5 – Authentication Logs

Commands Used

```bash
cat /var/log/auth.log
journalctl
```

Finding

Validated authentication events and reconstructed system activity.

---

## Investigation Analysis

Evidence collected from authentication logs, Cron configuration, file permissions, and user information consistently reconstructed Linux user activity.

Multiple independent sources validated system configuration and user privileges.

---

## MITRE ATT&CK Mapping

| Tactic | Technique | ID |
|---------|-----------|----|
| Persistence | Scheduled Task / Cron | T1053.003 |
| Privilege Escalation | Valid Accounts | T1078 |
| Discovery | Account Discovery | T1087 |

---

## Analyst Observations

- Linux authentication logs provide valuable investigative evidence.
- Cron configuration should always be reviewed.
- User privilege validation is essential.
- File metadata assists in ownership verification.
- Multiple evidence sources improve investigation reliability.

---

## Conclusion

The investigation successfully reconstructed Linux authentication and user activity using native Linux utilities. Correlating user information, authentication logs, Cron configuration, and file metadata demonstrated how Linux system activity can be investigated effectively.
