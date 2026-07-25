# Troubleshooting Notes

## Issue 1 — Authentication Log Not Found

### Cause

Some Linux distributions store authentication events using systemd journal instead of `/var/log/auth.log`.

### Resolution

Use:

```bash
journalctl
```

or

```bash
journalctl | grep sudo
```

---

## Issue 2 — "stat: missing operand"

### Cause

The `stat` command was executed without specifying a file.

### Resolution

Provide the filename:

```bash
stat investigation.txt
```

---

## Issue 3 — No User Crontab Found

### Cause

The current user or root user has no personal scheduled Cron jobs configured.

### Resolution

Verify the system-wide Cron configuration:

```bash
cat /etc/crontab
```

and inspect:

```bash
ls -la /etc/cron.*
```

---

## Issue 4 — Permission Denied

### Cause

The current user lacks permission to access protected system files.

### Resolution

Run the command with elevated privileges:

```bash
sudo <command>
```

---

## Issue 5 — Authentication Events Missing

### Cause

Authentication activity may not have occurred recently or logs may have rotated.

### Resolution

Review older logs using:

```bash
journalctl
```

or archived log files if available.

---

# Lessons Learned

- Native Linux commands provide comprehensive investigative evidence.
- Authentication logs are valuable for reconstructing user activity.
- Cron jobs should always be reviewed for persistence.
- File permissions help validate ownership and privilege.
- Correlating multiple evidence sources strengthens investigation accuracy.
