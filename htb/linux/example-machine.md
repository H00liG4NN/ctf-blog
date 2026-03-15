---
title: Example Machine
parent: Linux Machines
grand_parent: HTB Writeups
nav_order: 1
---

# Example Machine

**Difficulty:** Easy | **OS:** Linux | **Points:** 20

---

## Recon

```bash
nmap -sC -sV -oN nmap/initial 10.10.10.x
```

## Foothold

Found a vulnerable service on port 80...

## Privilege Escalation

Found SUID binary...

## Flags

- **User:** `flag{example_user_flag}`
- **Root:** `flag{example_root_flag}`
