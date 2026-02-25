# Day 12 – Revision Notes (Days 01–11)

Today I reviewed everything I learned from Day 01 to Day 11 to make sure I retain the Linux fundamentals before moving ahead.

---

##  Mindset & Plan Check (Day 01)

My goal is to become confident in Linux & DevOps fundamentals through daily hands-on practice.

Review:
- Plan is still correct 
- Hands-on practice is helping retention
- Need more speed in command usage

Improvement:
- Practice commands without notes
- Focus more on troubleshooting mindset

---

##  Processes & Services Review (Day 04–05)

Commands rerun:

ps aux | head  
systemctl status nginx  
journalctl -u nginx -n 10  

Observation:
- ps shows running processes and CPU usage
- systemctl shows service state (active/running)
- journalctl shows service logs and recent events

Learning:
Always check service status → then logs

---

##  File Skills Practice (Days 06–11)

Commands practiced:

echo "revision test" >> notes.txt  
chmod 640 notes.txt  
chown tokyo:developers devops-file.txt  
mkdir revision-dir  
ls -l  

Observation:
- echo >> appends content
- chmod controls access
- chown changes ownership
- ls -l verifies permissions

---

##  Cheat Sheet – Top 5 Commands (Day 03)

Commands I would use first in an incident:

1. ps aux  
   → check running processes  

2. top  
   → live CPU & memory usage  

3. systemctl status <service>  
   → check service health  

4. journalctl -u <service>  
   → check logs  

5. ls -l  
   → check permissions & ownership  

---

##  User & Ownership Sanity Check (Day 09 & 11)

Practice done:

useradd testuser  
id testuser  
touch testfile.txt  
chown testuser:testuser testfile.txt  
ls -l testfile.txt  

Verification:
- id shows user & groups
- ls -l shows ownership change

---

#  Mini Self-Check Answers

###  Which 3 commands save you the most time?

systemctl status  
→ instantly shows service health  

ps aux  
→ quick process inspection  

ls -l  
→ check permissions & ownership quickly  

---

###  How do you check if a service is healthy?

systemctl status nginx  
systemctl is-enabled nginx  
journalctl -u nginx -n 20  

---

###  How to safely change ownership & permissions?

Example:

chown tokyo:developers project.txt  
chmod 640 project.txt  

Reason:
- correct owner/group first
- then set permissions carefully

---

###  What will I improve in next 3 days?

- Faster troubleshooting flow
- More permission & ownership practice
- Service & log analysis confidence

---

#  Key Takeaways (Week 1–2)

- Linux troubleshooting follows a pattern
- Permissions & ownership are critical
- Services + logs are core DevOps skills
- Hands-on practice builds confidence
- I am now comfortable with basic Linux admin tasks

---

#  Revision Complete
Days 01–11 fundamentals reviewed and reinforced.
Ready to continue next phase 
