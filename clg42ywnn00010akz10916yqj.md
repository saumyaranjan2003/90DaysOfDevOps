---
title: "#Day5 Task: Advanced Linux Shell Scripting for DevOps Engineers with User management"
datePublished: Wed Apr 05 2023 19:26:55 GMT+0000 (Coordinated Universal Time)
cuid: clg42ywnn00010akz10916yqj
slug: day5-task-advanced-linux-shell-scripting-for-devops-engineers-with-user-management
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1679674515486/bc09ffc9-d9e2-4db5-a653-c14bcdae5676.png
tags: linux, aws, bash, devops, shell-scripting

---

### Q) Creating n number of directories using a script?

Ans:-

`mkdir assg`

`cd assg`

`vim` [`asg5.sh`](http://asg5.sh)

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680712674369/4dc10427-783f-41ce-92a5-57e3e359930c.png align="center")

`chmod 770` [`asg5.sh`](http://asg5.sh)

`./`[`asg5.sh`](http://asg5.sh)

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680712611569/d8495add-c065-4dd3-a83c-4610797f6168.png align="center")

`ls`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680712650546/e1c488f0-3c0a-440c-bcb6-3cead1e08ef1.png align="center")

### Q) Create a Script to back up all your work done till now. ?

Ans:-

#!/bin/bash

**#set the backup directory**

BACKUP\_DIR=/path/to/backup/directory

**#create the backup directory if it doesn't exist**

if \[ ! -d "$BACKUP\_DIR" \]; then

mkdir -p $BACKUP\_DIR

fi

**#set the filename of the backup**

BACKUP\_FILE=work\_backup\_$(date +%Y%m%d\_%H%M%S).tar.gz

**#create the backup archive**

tar czvf $BACKUP\_DIR/$BACKUP\_FILE /path/to/your/work

**#print a message confirming the backup**

echo "Backup of your work has been created: $BACKUP\_DIR/$BACKUP\_FILE"

### Q) Cron and Crontab, to automate the backup Script?

Ans:- Let's First See How to Use Crontab

to see some details about Crontab `cat /etc/crontab`

`mkdir crontab`

`cd crontab`

`crontab -l` &lt;- it will show the list if any crontab is active or not.

`crontab -e` &lt;- to create crontab

if you are a first-time user so it will display which crontab you want to use. 1)nano 2)vi 3)vim so choose according to your preferences.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680715197470/755f84d6-3644-43fa-8059-991c0662d870.png align="center")

so I have written a command that 8 17 \* echo "this is my first cron job" &gt; /home/ubuntu/crontab/test.txt

Which Means that at a time of 8 min 17hr, it will run and show the message in the .txt file

(Crontab varies in 12hr and 24-hour formats so set your time according to it)

after writing the command it will show like this **crontab: installing new crontab**

after it reaches that time it will do that work according to the command you have written, in my case, it shows like this

`ls`

`test.txt`

`cat test.txt`

`this is my first cron job`

**Cron - &gt;** It is Mainly Used in Scheduling Work/Used in Automation. It is the Service/utility which allows to Schedule/Automation of the Work.

**Crontab -&gt;** It is the File That Includes a set of commands where it states when to execute, what to execute, and at which time to execute.

We Should Remember The 5 Things in **Crontab that Are**

**MIN HOUR DAY-OF-MONTH MONTH DAY-OF-WEEK**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680716987806/2aa86f46-d21e-4a31-afdc-4f55d71c22db.png align="center")

one thing is to remember that whenever that particular day will come in the calendar according to your command it will work on that day it may vary in 12 hr format or 24-hour format and also your server time format(if you are using services like AWS, Azure, GCP) if the date not exist, not there in the calendar or not come so it will not work.

### Q) User Management Short Note!

Ans:- **User Administration** is the process of managing different user accounts and their respective permissions in an operating system. **User administration** in Linux involves **creating, modifying, and deleting user accounts, managing user passwords, assigning permissions, and managing user groups.**

In Linux, there are **three types** of user accounts:

1. **Superuser or root user account:** The superuser or root user account is the **administrative account** that has **full access to the system**. The root account has the highest level of privileges and can perform any system-level task, including creating and modifying user accounts, installing and configuring software, and modifying system settings. ***It is important to use the root account only when necessary, as any mistake can cause serious damage to the system.***
    
2. **Regular user accounts:** Regular user accounts are created for **normal users** who do not require administrative privileges. These accounts are limited in their capabilities and are meant for performing day-to-day tasks such as accessing files, running applications, and browsing the internet. Regular user accounts are typically created using the `adduser` command and can be modified or deleted using the `usermod` and `userdel` commands, respectively.
    
3. **Service accounts**: Service accounts are special-purpose accounts used by **system services and daemons(System Users)**. This is the type of account that is created only for a specific purpose or software. For example, a mail account.
    
    It is important to properly manage service accounts to ensure the security and stability of the system.
    

there is also the concept of "***guest***" accounts in some Linux distributions, which allow users to log in with ***limited privileges to perform basic tasks without having to create a full user account***. ***Guest accounts are typically temporary and are deleted when the user logs out.***

### **Groups**

In Linux, we can form **groups** of users’ accounts. Groups are used to manage the user accounts collectively. We can manage the access permissions for the entire group. ***A single user can be a part of multiple groups, and a group can have multiple users.***

### Q) Create 2 users and just display their Usernames

Ans:- `cd /`

`/$ sudo useradd -m test1user`

`/$ sudo useradd -m test2user`

`/$ sudo cat /etc/passwd`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680721181029/d2097928-9aca-4b70-989c-985231209d38.png align="center")

`id test1user`

**uid=1008(test1user) gid=1012(test1user) groups=1012(test1user)**

`id test2user`

**uid=1009(test2user) gid=1013(test2user) groups=1013(test2)**

ThankYou\_So\_Much For Reading ❤️😅

Saumya Ranjan Mohapatra