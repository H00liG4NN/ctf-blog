---
title: Nmap Cheatsheet
parent: Tools & Notes
nav_order: 1
---

# Nmap Cheatsheet

## Basic Scans

```bash
# Full port scan
nmap -p- --min-rate 5000 -oN nmap/full 10.10.10.x

# Service + script scan
nmap -sC -sV -p 22,80,443 -oN nmap/targeted 10.10.10.x

# UDP scan
nmap -sU --top-ports 20 10.10.10.x
```

## Output Formats

```bash
nmap -oA output_all  # saves .nmap, .xml, .gnmap
```
