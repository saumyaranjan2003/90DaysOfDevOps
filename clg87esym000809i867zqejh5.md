---
title: "#Day6 Task: File Permissions and Access Control Lists"
datePublished: Sat Apr 08 2023 16:42:20 GMT+0000 (Coordinated Universal Time)
cuid: clg87esym000809i867zqejh5
slug: day6-task-file-permissions-and-access-control-lists
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1679804616137/54bf0f2b-0978-4ad0-b296-dd67cb343cfe.jpeg
tags: linux, docker, aws, github, devops

---

### Create a simple file and do `ls -ltr` to see the details of the files

`touch testing.txt`

`ls -ltr`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680965210569/99882885-b25e-4425-ad32-553eb4ef009b.png align="center")

### How do you view Linux file permissions?

`ls -l` The `ls` command along with its `-l` (for long listing) option will show you metadata about your Linux files, including the permissions set on the file.

Ex :- `ls -l`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680965433673/eb1bd5a3-8db2-48d5-a60b-1b320f9b94b5.png align="center")

* File type: `-` &lt;- file / `d` &lt;- dir
    
* Permission settings: `rw-r--r--`
    
* Extended attributes: dot (`.`)
    
* User owner: `ubuntu`
    
* Group owner: `ubuntu`
    

### How do you read file permissions?

Ex:-

```bash
rw-r--r–-
```

rw- **The first set of permissions applies to the owner/User of the file**

r-- **The second set of permissions applies to the user group that owns the file.**

r-- **The third set of permissions is generally referred to as "others."**

*All Linux files belong to an owner and a group.*

### **Symbolic Mode**

For users, `u` stands for user owner, `g` for the group owner, and `o` for others.

For permissions, `r` stands for read, `w` for write, and `x` for execution.

### What are octal values in **file permissions**?

When Linux file permissions are represented by numbers, it's called numeric mode. In numeric mode, a three-digit value represents specific file permissions (for example, 744.) These are called octal values. The first digit is for owner permissions, the second digit is for group permissions, and the third is for other users. Each permission has a numeric value assigned to it:

* r (read): 4
    
* w (write): 2
    
* x (execute): 1
    

| Num/Octal Values | Permissions Type | Symbols |
| --- | --- | --- |
| 0 | No Permissions | \--- |

<table><tbody><tr><td colspan="1" rowspan="1"><p>1</p></td><td colspan="1" rowspan="1"><p>Execute</p></td><td colspan="1" rowspan="1"><p>--X</p></td></tr><tr><td colspan="1" rowspan="1"><p>2</p></td><td colspan="1" rowspan="1"><p>Write</p></td><td colspan="1" rowspan="1"><p>-W-</p></td></tr><tr><td colspan="1" rowspan="1"><p>3</p></td><td colspan="1" rowspan="1"><p>Execute, Write</p></td><td colspan="1" rowspan="1"><p>-WX</p></td></tr><tr><td colspan="1" rowspan="1"><p>4</p></td><td colspan="1" rowspan="1"><p>Read</p></td><td colspan="1" rowspan="1"><p>R--</p></td></tr><tr><td colspan="1" rowspan="1"><p>5</p></td><td colspan="1" rowspan="1"><p>Read, Execute</p></td><td colspan="1" rowspan="1"><p>R-X</p></td></tr><tr><td colspan="1" rowspan="1"><p>6</p></td><td colspan="1" rowspan="1"><p>Read, Write</p></td><td colspan="1" rowspan="1"><p>RW-</p></td></tr><tr><td colspan="1" rowspan="1"><p>7</p></td><td colspan="1" rowspan="1"><p>Read, Write, Execute</p></td><td colspan="1" rowspan="1"><p>RWX</p></td></tr></tbody></table>

F/D(-) U(---) G(---) O(---)

For example, a file might have read, write, and execute permissions for its owner, and only read permission for all other users. That looks like this:

* Owner: rwx = 4+2+1 = 7
    
* Group: r-- = 4+0+0 = 4
    
* Others: r-- = 4+0+0 = 4
    

The results produce the three-digit value 744.

### What do Linux file permissions do?

### **Read (r)**

Read permission is used to access the file's contents. You can use a tool like

`cat filename` on the file to display the file contents. You could also use a text editor like Vi or `view` on the file to display the contents of the file. Read permission is required to make copies of a file because you need to access the file's contents to duplicate it.

### **Write (w)**

Write permission allows you to modify or change the contents of a file. Without written permission, changes to the file's contents are not permitted. for write you can use `vim filename`.

### **Execute (x)**

Execute permission allows you to execute the contents of a file. Typically, executables would be things like commands or compiled binary applications. However, execute permission also allows someone to run Bash shell scripts, Python programs, and a variety of interpreted languages.

`$ bash` [`script.sh`](http://script.sh) or `./filename.sh`

### chown

The **chown** command changes the owner of a file. the **chgrp** command changes the group. On Linux, only the **root** can use **chown** for changing the ownership of a file, but any user can change the group to another group he belongs to.

Ex:- **before**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680969885013/46891ec9-eb77-4c52-aaea-eb0bbb195656.png align="center")

`sudo chown -c student2 testing.txt`

changed ownership of 'testing.txt' from ubuntu to student2

**after**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680969943603/9dfc9ef6-ad1c-411a-94cb-c780c6c63eb1.png align="center")

In the above line, "student2" is the username of the user who created or owns the file "testing.txt". "ubuntu" refers to the group that the user "student2" belongs to. The file has read and writes permissions for the owner "student2" and the members of the "ubuntu" group, but only read permissions for all other users.

To break down the permissions, "rw-" means the owner "student2" has read and write permissions, "rw-" again means members of the "ubuntu" group also have read and write permissions, and "---" means all other users have no permissions (i.e., they can neither read nor write to the file).

### chgrp

The **chgrp** command in [**Linux**](https://linuxconfig.org/linux-download/) can change the group ownership of one or multiple files or directories. In Linux, every file has a few **permissions**: read, write, and execute. These permissions are assigned to specific users and groups to allow access to these operations

Ex :- before

`-rw-rw-r-- 1 student2 ubuntu 0 Apr 8 14:46 testing.txt`

after

`sudo chgrp -c student2 testing.txt`

changed group of 'testing.txt' from ubuntu to student2

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680970204533/e0587ead-4d8a-451c-9888-f925ea4bd8d7.png align="center")

### chmod task(change the user permissions of the file and note the changes after `ls -ltr)`

chmod" is used to change the other user's permissions of a file or directory

Ex:

`touch test.txt`

before

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680970579487/dfd09bf0-9feb-4814-9c12-ed23e9b12c65.png align="center")

`chmod 770 test.txt`

after

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680970645238/65198410-c0b9-40fa-b520-d78194a1fa5b.png align="center")

### Read about ACL and try out the commands `getfacl` and `setfacl`

It is the tool that helps to access control the lists from the file to see which access the file has and how to give access.

**Install**

`sudo apt-get install acl`

**to check acl**

`getfacl filname`

ex-

`getfcal testing`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680971397769/b41dceb4-f182-437a-966f-0fed42183ee7.png align="center")

**The syntax for setting an ACL looks like this**

`setfacl [option] [action/specification] file`

The 'action' would be `-m` (modify) or `-x` (remove), and the specification would be the user or group followed by the permissions we want to set. In this case, we would use the option `-d` (defaults)

ThankYou So Much For Reading

Saumya Ranjan Mohapatra❤️🐧😅