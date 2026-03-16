# Day 28 -- Revision Day: Everything from Day 1 to Day 27

## Overview

Today was a **revision day** where I reviewed everything learned in the
first 27 days of the DevOps journey.\
The goal was to identify knowledge gaps, reinforce important concepts,
and ensure I can confidently explain the tools and techniques learned so
far.

------------------------------------------------------------------------

## What I Have Covered So Far

| Days | Topic | Key Concepts |
|-----|------|-------------|
| 1 | DevOps & Cloud Intro | What is DevOps, SDLC, Cloud basics |
| 2–7 | Linux Fundamentals | Architecture, commands, processes, systemd, filesystem hierarchy |
| 8 | Cloud Server Setup | Docker, Nginx, web deployment |
| 9–11 | Users, Permissions & Ownership | User/group management, file permissions, chown/chgrp |
| 12 | Revision Day 1 | Days 1–11 recap |
| 13 | Volume Management | LVM – physical volumes, volume groups, logical volumes |
| 14–15 | Networking | DNS, IP, subnets, ports, troubleshooting |
| 16–18 | Shell Scripting | Variables, loops, arguments, functions |
| 19–20 | Shell Scripting Projects | Backup scripts, log rotation, automation |
| 21 | Shell Scripting Cheat Sheet | Personal command reference guide |
| 22–25 | Git & GitHub | Init, branching, merge, rebase, stash, cherry-pick, reset, revert |
| 26 | GitHub CLI | Managing GitHub from the terminal |
| 27 | GitHub Profile | Profile README, repo organization, developer branding |

------------------------------------------------------------------------

# Task 1 -- Self Assessment

## Linux

✔ Navigate file systems and manage files\
✔ Manage processes using `ps`, `top`, `kill`\
✔ Manage services with `systemctl`\
✔ Edit files using `vi` / `vim`\
✔ Monitor CPU, memory and disk usage (`top`, `free`, `df`, `du`)\
✔ Understand Linux directory structure (`/etc`, `/var`, `/home`)\
✔ Create users and groups\
✔ Manage file permissions with `chmod`\
✔ Change ownership using `chown` and `chgrp`\
✔ Basic LVM understanding\
✔ Network troubleshooting using `ping`, `curl`, `ss`, `dig`

## Shell Scripting

✔ Write scripts using variables and arguments\
✔ Use `if`, `elif`, `case` statements\
✔ Implement loops (`for`, `while`)\
✔ Create functions in scripts\
✔ Process text using `grep`, `awk`, `sed`\
✔ Implement error handling (`set -e`, `set -u`, `pipefail`)\
✔ Automate scripts using `crontab`

## Git & GitHub

✔ Initialize repositories and commit changes\
✔ Create and manage branches\
✔ Push and pull from GitHub\
✔ Understand clone vs fork\
✔ Perform merge and rebase\
✔ Use git stash to temporarily save changes\
✔ Use cherry-pick to move commits between branches\
✔ Understand reset vs revert\
✔ Understand branching strategies (GitFlow, GitHub Flow)\
✔ Use GitHub CLI for repo and PR management

------------------------------------------------------------------------

# Task 2 -- Topics I Revisited

### 1. Git Rebase vs Merge

Revisited how rebasing rewrites commit history to create a cleaner
linear history, while merging preserves the branch history.

### 2. Shell Script Error Handling

Reviewed the importance of: - `set -e` - `set -u` - `set -o pipefail`

These help scripts fail fast and avoid unexpected behavior.

### 3. Linux Networking Tools

Practiced using: - `ss -tulnp` - `netstat` - `dig` - `curl`

These are essential for debugging connectivity issues.

------------------------------------------------------------------------

# Task 3 -- Quick Fire Answers

**What does chmod 755 script.sh do?**\
Gives read, write, execute to owner and read+execute to group and
others.

**Difference between a process and a service?**\
A process is a running program, while a service is a background process
managed by the system.

**How to find which process is using port 8080?**\
`ss -tulnp | grep 8080`

**What does set -euo pipefail do?**\
Makes a script exit on errors, undefined variables, and pipeline
failures.

**Difference between git reset --hard and git revert?**\
Reset rewrites history and discards commits, while revert creates a new
commit that undoes changes.

**Branching strategy for a small team shipping weekly?**\
GitHub Flow or Trunk-Based Development.

**What does git stash do?**\
Temporarily saves uncommitted changes so you can switch branches.

**How to schedule a script daily at 3 AM?**\
`0 3 * * * /path/script.sh`

**Difference between git fetch and git pull?**\
Fetch downloads changes without merging; pull fetches and merges.

**What is LVM?**\
Logical Volume Manager allows flexible disk management and resizing
volumes without repartitioning disks.

------------------------------------------------------------------------

# Task 4 -- Organizing Work

✔ Verified that all days (Day 1 -- Day 27) are committed and pushed\
✔ Checked `git-commands.md` for completeness\
✔ Updated shell scripting cheat sheet\
✔ Verified GitHub profile organization from Day 27

------------------------------------------------------------------------

# Task 5 -- Teaching Back

## Explaining File Permissions in Linux

Linux file permissions control who can read, write, or execute a file.\
Each file has three permission groups: **owner, group, and others**.

Permissions are represented as:

-   r → read
-   w → write
-   x → execute

Example:

`chmod 755 script.sh`

This allows the owner to read/write/execute while others can read and
execute.

Understanding permissions is essential for securing Linux systems and
controlling file access.

------------------------------------------------------------------------

# Summary

Revision is critical in DevOps learning.\
Today helped reinforce Linux fundamentals, scripting knowledge, and Git
workflows that will be used heavily in upcoming Docker and Kubernetes
topics.
