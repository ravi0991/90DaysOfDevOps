# Day 21 – Shell Scripting Cheat Sheet (My Personal Reference)

## Quick Reference Table

| Topic | Key Syntax | Example |
|------|-----------|---------|
| Variable | VAR="value" | NAME="DevOps" |
| Argument | $1, $2 | ./script.sh arg1 |
| If | if [ cond ]; then | if [ -f file ]; then |
| For loop | for i in list; do | for i in 1 2 3; do |
| Function | name() { } | greet() { echo "Hi"; } |
| Grep | grep pattern file | grep -i "error" log.txt |
| Awk | awk '{print $1}' | awk -F: '{print $1}' /etc/passwd |
| Sed | sed 's/a/b/g' | sed -i 's/foo/bar/g' conf |

---

# Basics

**Shebang**  
Tells system which interpreter to use.  
```bash
#!/bin/bash
```

**Run Script**  
```bash
chmod +x script.sh
./script.sh
bash script.sh
```

**Comments**  
```bash
# single line
echo "Hi"  # inline comment
```

**Variables**  
```bash
NAME="Ravi"
echo $NAME
echo "$NAME"
echo '$NAME'
```

**User Input (read)**  
```bash
read -p "Enter name: " NAME
```

**Arguments**  
```bash
$0 script name
$1 first arg
$# count
$@ all args
$? last exit
```

---

# Operators & Conditionals

**String**  
```bash
[ "$a" = "$b" ]
[ -z "$var" ]
[ -n "$var" ]
```

**Integer**  
```bash
[ $a -eq $b ]
[ $a -gt 5 ]
```

**File Tests**  
```bash
-f file
-d dir
-r file
-w file
-x file
-s file
```

**If Else**  
```bash
if [ -f file ]; then
  echo "exists"
elif [ -d file ]; then
  echo "dir"
else
  echo "no"
fi
```

**Logical**  
```bash
cmd && echo ok
cmd || echo fail
! cmd
```

**Case**  
```bash
case $var in
  start) echo "start";;
  stop) echo "stop";;
  *) echo "other";;
esac
```

---

# Loops

**For**  
```bash
for i in 1 2 3; do
  echo $i
done
```

**C-style**  
```bash
for ((i=0;i<5;i++)); do
  echo $i
done
```

**While**  
```bash
while read line; do
  echo $line
done < file.txt
```

**Until**  
```bash
until ping -c1 host; do
  sleep 1
done
```

**Control**  
```bash
break
continue
```

**Files Loop**  
```bash
for f in *.log; do
  echo $f
done
```

---

# Functions

**Define & Call**  
```bash
greet() {
  echo "Hello $1"
}
greet Ravi
```

**Return vs Echo**  
```bash
sum() { echo $(($1+$2)); }
result=$(sum 2 3)
```

**Local Variable**  
```bash
func() {
  local x=5
}
```

---

# Text Processing

**grep**  
```bash
grep -i error log
grep -r warn /var/log
grep -c fail log
```

**awk**  
```bash
awk '{print $1}'
awk -F: '{print $1}' /etc/passwd
```

**sed**  
```bash
sed 's/old/new/g' file
sed -i '/delete/d' file
```

**cut**  
```bash
cut -d: -f1 /etc/passwd
```

**sort / uniq**  
```bash
sort file
sort -nr nums
uniq -c file
```

**tr**  
```bash
tr 'a-z' 'A-Z'
```

**wc**  
```bash
wc -l file
```

**head / tail**  
```bash
head -n 5 file
tail -f log
```

---

# Useful One‑Liners

**Delete files older than 7 days**  
```bash
find /path -type f -mtime +7 -delete
```

**Count lines in logs**  
```bash
wc -l *.log
```

**Replace text in many files**  
```bash
sed -i 's/old/new/g' *.conf
```

**Check service running**  
```bash
systemctl is-active nginx
```

**Disk usage alert**  
```bash
df -h | awk '$5>80'
```

**Tail errors live**  
```bash
tail -f app.log | grep ERROR
```

---

# Error Handling & Debugging

**Exit Codes**  
```bash
echo $?
exit 1
```

**Strict Mode**  
```bash
set -e
set -u
set -o pipefail
```

**Debug**  
```bash
set -x
```

**Trap**  
```bash
trap 'echo cleanup' EXIT
```

---

# What I Learned

- Shell scripting syntax and patterns consolidated in one place  
- Text processing tools are extremely powerful for automation  
- Strict mode and checks make scripts production‑safe  
