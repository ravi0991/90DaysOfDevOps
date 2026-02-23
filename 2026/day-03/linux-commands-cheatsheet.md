# Linux Commands Cheat Sheet

## Process Management

- ps -ef → see all running processes
- ps -ef | grep nginx → see a particular process
- top → live CPU & memory usage  
- htop → interactive process view  
- pgrep nginx → find PID by name  
- kill PID → stop process  
- kill -9 PID → force kill a process
- systemctl start nginx → start a service 
- systemctl status nginx → check service state  
- systemctl restart nginx → restart a service
- systemctl stop nginx → stop a service

---

## File System

- ls -lh → list files with size  
- df -h → disk usage  
- du -sh /dir1 → check a directory size  
- cd /path → change directory
- touch file1  → craete a file
- cp file1 file2 → copy file  
- mv devops devops2 → move/rename a file or directory
- mkdir dir1 → make a directory
- rm -rf dir → delete a directory  
- find / -name file_name → search a file by file name
- chmod 644 file1 → change permission of a file 
- chown user:grp file → Change ownership of a file  

---

## Networking

- ip addr → check IP address of a server 
- ip route → check routing  
- ping host → check connectivity of a server
- ss -tulnp → ports/services 
- curl http://host → test web  
- dig domain → DNS lookup
- nslookup domain → DNS lookup
- traceroute host → check network path  

---

## Logs & System

- journalctl -u nginx → check service logs  
- journalctl -xe → check system errors  
- tail -f logfile → check live logs  
- free -h → check memory usage 
- uptime → Check load average and uptime  

---

## Quick Troubleshooting Steps

1. systemctl status nginx  
2. ss -tulnp | grep 80  
3. journalctl -u nginx  
4. df -h
5. free -h  
6. ping server_ip
7. telnet server_ip port 
