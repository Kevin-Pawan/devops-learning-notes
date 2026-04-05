# Days 01–04 Catchup — April 7-10, 2026

## What I Covered
- Lectures 1–39 completed
- Course: Decoding DevOps by Imran Teli

## Sections Completed
- DevOps Introduction (What is DevOps, CI, CD)
- Tools Setup (Chocolatey, software installation, signups)
- AWS Account Setup
- Virtualization and Vagrant (VM setup on Windows)
- Complete Linux Section (Lectures 23–39)

## Key Linux Commands I Learned

# Navigation
pwd                    — show current directory
ls / ls -la            — list files
cd dirname             — change directory
cd ..                  — go one level up
cd ~                   — go to home directory

# File Operations
mkdir dirname          — create folder
touch filename         — create empty file
cp file1 file2         — copy file
mv file1 file2         — move or rename
rm filename            — delete file

# Viewing Files
cat filename           — print file content
head -5 filename       — first 5 lines
tail -10 filename      — last 10 lines

# Filters
grep "word" filename   — search in file
grep -i "word" file    — case insensitive search
grep -R "word" dir     — search in all files in folder

# Redirections
command > file         — write output to file
command >> file        — append output to file
command | command      — pipe output to next command

# Users and Groups
useradd username       — create user
passwd username        — set password
groupadd groupname     — create group
usermod -aG group user — add user to group
cat /etc/passwd        — list all users

# File Permissions
chmod 755 filename     — change permissions
chown user:group file  — change owner
ls -la                 — view permissions

# Package Management
yum install package    — install on CentOS
apt install package    — install on Ubuntu
yum remove package     — remove package

# Services
systemctl start service    — start service
systemctl stop service     — stop service
systemctl status service   — check status
systemctl enable service   — start on boot

# Processes
ps aux                 — list all processes
kill PID               — kill process
top                    — live process monitor

# Archiving
tar -czvf file.tar.gz dirname   — create archive
tar -xzvf file.tar.gz           — extract archive

## What I Understood About DevOps
DevOps is about breaking the wall between Development
and Operations teams. CI means automatically building
and testing code every time someone pushes changes.
CD means automatically deploying that tested code.

## What Confused Me
Vim modes were confusing at first — kept getting stuck
in normal mode and couldn't type. Fixed by remembering:
press i to type, press Esc to stop, :wq to save and quit.

## Interview Questions I Can Now Answer
1. What is the difference between CI and CD?
2. How do you check running processes in Linux?
3. What does chmod 755 mean?
4. How do you search for a word inside a file in Linux?
5. What is the difference between yum and apt?
6. How do you create a user and add them to a group?

## Tomorrow's Plan
- Start Git section (Lectures 40–47)
- Practice git init, clone, add, commit, push
- Set up GitHub Copilot (Lecture 46)
