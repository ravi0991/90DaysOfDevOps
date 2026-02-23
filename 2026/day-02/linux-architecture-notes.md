# Linux Architecture, Processes, and systemd

## Core Parts of Linux

Linux system mainly has 3 parts:

**Kernel**
- It is the core of Linux OS
- Directly talks to hardware (CPU, memory, disk)
- Manages processes and resources

**User Space**
- Where normal programs run
- Example: nginx, ssh, docker, shell
- Users interact with system here

**systemd (init)**
- First process started by kernel (PID 1)
- Starts all services during boot
- Controls background services

---

## How Processes Work in Linux

- Every running program = process
- Each process has PID
- New process created from parent process
- Kernel gives CPU time to processes
- systemd manages service processes

Example flow:
systemd → sshd → bash → top

---

## Process States

- **R (Running)** → using CPU
- **S (Sleeping)** → waiting (most common)
- **T (Stopped)** → paused
- **Z (Zombie)** → finished but not cleaned
- **D (I/O wait)** → waiting for disk/network

Zombie shows as `<defunct>` in ps.

---

## What systemd Does

systemd is service manager in Linux.

It:
- Starts services at boot
- Stops/restarts services
- Keeps services running
- Maintains logs
- Handles dependencies

Why important:
Most production services run via systemd.

---

## Daily Commands I Use

- `ps -ef` → see processes
- `top` → CPU/memory usage
- `systemctl status nginx` → service state
- `journalctl -u nginx` → logs
- `kill PID` → stop process

---

## Key Points

- Kernel controls hardware
- Programs run as processes
- systemd manages services
- Process states help in troubleshooting
