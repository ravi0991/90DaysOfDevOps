# Day 09 – Linux User & Group Management Challenge

## Users & Groups Created

**Users created:**
- tokyo  
- berlin  
- professor  
- nairobi  

**Groups created:**
- developers  
- admins  
- project-team  

### Verification

cat /etc/passwd | tail -n 5

**Observed:**

tokyo, berlin, professor users created with /home directories

login shell: /bin/bash

ls -l /home


**Observed:**

/home/tokyo

/home/berlin

/home/professor

---------------------------------------------------------------------------

## Group Assignments

**Assignments done:**

tokyo → developers

berlin → developers, admins

professor → admins

nairobi → project-team

tokyo → project-team

**Verification:**

groups tokyo
groups berlin
groups nairobi

**Observed:**

tokyo: tokyo developers project-team

berlin: berlin developers admins

nairobi: nairobi project-team

------------------------------------------------------------------------

## Directories Created

### Dev Project Directory

**Created:**

mkdir -p /opt/dev-project
chgrp developers /opt/dev-project
chmod 775 /opt/dev-project

**Verification:**

ls -ld /opt/dev-project

**Observed:**

drwxrwxr-x root developers /opt/dev-project


**Testing Access**

su tokyo

touch /opt/dev-project/file1

touch /opt/dev-project/file2

exit


su berlin

touch /opt/dev-project/file3

touch /opt/dev-project/file4

exit


**Result:**

Both users successfully created files

Group access working

------------------------------------------------------------------------

## Team Workspace Directory

**Created:**

mkdir -p /opt/team-workspace

chgrp -R project-team /opt/team-workspace

chmod 775 /opt/team-workspace


**Verification:**

ls -ld /opt/team-workspace


**Observed:**

drwxrwxr-x root project-team /opt/team-workspace


**Testing Access**

su nairobi

cd /opt/team-workspace

touch new-file.txt

exit


**Result:**

nairobi successfully created file

------------------------------------------------------------------------

## Shared workspace working

**Commands Used**

useradd -m tokyo
useradd -m berlin
useradd -m professor
useradd -m nairobi

passwd tokyo
passwd berlin
passwd professor
passwd nairobi

groupadd developers
groupadd admins
groupadd project-team

usermod -aG developers tokyo
usermod -aG developers berlin
usermod -aG admins berlin
usermod -aG admins professor
usermod -aG project-team tokyo
usermod -aG project-team nairobi

mkdir -p /opt/dev-project
mkdir -p /opt/team-workspace

chgrp developers /opt/dev-project
chgrp project-team /opt/team-workspace

chmod 775 /opt/dev-project
chmod 775 /opt/team-workspace

groups username
ls -ld directory
su username
touch file

**What I Learned**

Users and groups control access in Linux systems

Shared directories require correct group ownership and permissions

775 permissions allow team collaboration safely

usermod -aG adds users to multiple groups

Always verify using groups and ls -ld
