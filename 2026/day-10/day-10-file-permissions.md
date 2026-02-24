# Day 10 Challenge

## Files Created

- devops.txt → empty file created using touch

- notes.txt → text file created using echo

- script.sh → shell script created using vim with content echo "Hello DevOps"

- project/ → directory created using mkdir

------------------------------------------------------------------------------

## Permission Changes

### script.sh

**Before**

-rw-r--r-- script.sh

**After**

-rwxr-xr-x script.sh

Action: Made executable using chmod +x
Result: Successfully executed with ./script.sh

------------------------------------------------------------------------------

### devops.txt

**Before**

-rw-r--r-- devops.txt

**After**

-r--r--r-- devops.txt

Action: Set to read-only using chmod 444
Result: File cannot be modified or executed

------------------------------------------------------------------------------

### notes.txt

**Before**

-rw-r--r-- notes.txt

**After**

-rw-r----- notes.txt

Action: Set to 640 using chmod 640
Result: Owner can read/write, group read-only, others no access

-----------------------------------------------------------------------------

### project directory

**Created with**

mkdir project
chmod 755 project

**Permissions**

drwxr-xr-x project

Result: Owner full access, others read & execute

----------------------------------------------------------------------------

## Commands Used

touch devops.txt

echo "hello all" > notes.txt
echo "this is devops tutorial" >> notes.txt
echo "welcome" >> notes.txt
echo "hello dosto" >> notes.txt

vim script.sh
cat script.sh

ls -l
chmod +x script.sh
./script.sh

chmod 444 devops.txt
chmod 640 notes.txt

mkdir project
chmod 755 project
ls -ld project

cat notes.txt
vim -R script.sh

head -n 5 /etc/passwd
tail -n 5 /etc/passwd

---------------------------------------------------------------------------

## What I Learned

Linux permissions follow owner-group-others model (rwx).

Scripts require execute permission to run.

chmod numeric modes (444, 640, 755) control access precisely.

Read-only files prevent modification.

Directory execute (x) allows entering/traversing directories.
