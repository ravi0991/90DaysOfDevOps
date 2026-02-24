# Day 06 – File Read/Write Practice

Practiced basic file creation, writing, appending and reading using Linux commands.

---

touch notes.txt  
→ created an empty file  

echo "Hello world" > notes.txt  
→ wrote first line (overwrite mode)  

echo "Welcome to this course" >> notes.txt  
→ appended second line  

echo "bye bye" >> notes.txt  
→ appended third line  

cat notes.txt  
→ displayed full file content  

head -n 2 notes.txt  
→ showed first 2 lines  

tail -n 2 notes.txt  
→ showed last 2 lines  

echo "thanks to all" | tee -a notes.txt  
→ appended line and displayed output  

![File IO Practice](file-io.png)

---

Final file content:
Hello world  
Welcome to this course  
bye bye  
thanks to all  

---

Learning:
> creates/overwrites file  
>> appends to file  
tee writes and prints simultaneously  
cat/head/tail help read files quickly
