# GitHub-Backup-Script
Shell script (Linux) that automatically backups my repositories to my external hard drive

## Setup
Fill in the variables in the file:

GITHUB_USERNAME="[YOUR GITHUB USERNAME]" e.g.: "TomTruyen" <br/>
GITHUB_TOKEN="[ACCESS TOKEN HERE]" e.g.: "abcdefghij123456798" <br/>
OUTPUT_PATH="[YOUR OUTPUT_PATH HERE]" e.g.: "~/Desktop/Backups" <br/>

## Run
1) cd to the directory of the script <br/>
2) ./github_backup_script.sh <br/>

## Automate Backups
#### Crontab
1) crontab -e (opens crontab file for user)
2) 00 00 * * * bash /path/to/github_backup_script.sh

In this example the backup will be made daily at midnight

## Bad Interpretor Error Fix
#### bash: ./github_backup_script.sh: /usr/bin/bash^M: bad interpreter: No such file or directory
Fix: 
1) Install dos2unix (sudo apt-get install dos2unix)
2) Convert the shell script to unix (dos2unix -k -o github_backup_script.sh)
3) Run the script again. It should work now.
