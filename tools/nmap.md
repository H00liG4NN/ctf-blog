---
layout: default
title: Nmap Cheatsheet
description: Quick reference for Nmap scanning techniques
---

## Basic Scans

```bash
nmap -sV -sC -oN scan.txt <IP>       # Default scripts + version
nmap -p- --min-rate 5000 <IP>        # All ports fast
nmap -sU -top-ports 20 <IP>          # Top 20 UDP ports
```

## Service & Version Detection

```bash
nmap -sV --version-intensity 9 <IP>  # Max version detection
nmap -A <IP>                         # Aggressive (OS, version, scripts)
```

## NSE Scripts

```bash
nmap --script vuln <IP>              # Run vuln scripts
nmap --script smb-enum-shares <IP>   # SMB enumeration
nmap --script http-enum <IP>         # HTTP enumeration
```

## Output Formats

```bash
nmap -oN out.txt <IP>    # Normal
nmap -oX out.xml <IP>    # XML
nmap -oG out.gnmap <IP>  # Grepable
nmap -oA out <IP>        # All formats
```
