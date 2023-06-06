---
title: "Day 3 Task: Basic Linux Commands"
datePublished: Thu Mar 23 2023 16:34:04 GMT+0000 (Coordinated Universal Time)
cuid: clflc2j5v000309l4hz7a2utp
slug: day-3-task-basic-linux-commands
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1679508681515/ec35dea1-bd51-4b39-bef9-57f09e10597c.jpeg
tags: linux, aws, devops, jira, ci-cd

---

## *Task: What is the Linux command to*

1. To view what's written in a file. ?
    
    Ans: - `cat` Cat(concatenate) command is very frequently used in Linux. ***It reads data from the file and gives its content as output***.
    
    Ex- `cat filename` -&gt; hello dosto
    
    ![](https://infolinux.com/wp-content/uploads/2019/08/cat-newfile.png align="center")
    
2. To change the access permissions of files. ?
    
    Ans: - The `chmod` command is used to change the access permissions of files. For example, to give the owner of a file read, write, and execute permissions and everyone else only read and execute permissions, run the following command
    
    `chmod 755 filename`
    
3. To check which commands you have run till now. ?
    
    Ans:- `history` history command is ***used to display the history of the commands executed by the user****.*
    
    ![](https://linuxways.net/wp-content/uploads/2021/07/word-image-312.png align="center")
    
4. To remove a directory/ Folder. ?
    
    Ans:- **Case 1)** if dir does not include any file inside it mean empty dir. So Command will be `rmdir xyzfoldername` .
    
    **Case 2)** if dir contains files so `rmdir` will not work, so the command will be
    
    `rm -r xyzfoldername` (it will remove dir including the contents inside it).
    
    ![](https://infolinux.com/wp-content/uploads/2019/08/rmdir.png align="center")
    
5. To create a fruits.txt file and to view the content.?
    
    Ans:-
    
    `touch fruits.txt`
    
    `echo "fruits are good for health" > fruits.txt`
    
    `cat fruits.txt`
    
    `fruits are good for health`
    
6. Add content in devops.txt (One in each line) - Apple, Mango, Banana, Cherry, Kiwi, Orange, Guava. ?
    
    Ans:-
    
    `echo "Apple" >> devops.txt`
    
    `echo "Mango" >> devops.txt`
    
    `echo "Banana" >> devops.txt`
    
    `echo "Cherry" >> devops.txt`
    
    `echo "Kiwi" >> devops.txt`
    
    `echo "Orange" >> devops.txt`
    
    `echo "Guava" >> devops.txt`
    
    `cat devops.txt`
    
    `Apple`
    
    `Mango`
    
    `Banana`
    
    `Cherry`
    
    `Kiwi`
    
    `Orange`
    
    `Guava`
    
7. Show only the top three fruits from the file.?
    
    Ans:- `head -n 3 devops.txt`
    
    `Apple`
    
    `Mango`
    
    `Banana`
    
8. To Show only the bottom three fruits from the file. ?
    
    Ans:- `tail -n 3 devops.txt`
    
    `Kiwi`
    
    `Orange`
    
    `Guava`
    
9. To create another file Colors.txt and to view the content.?
    
    Ans:- `touch Colors.txt`
    
    `"cat colors.txt"`
    
10. Add content in Colors.txt (One in each line) - Red, Pink, White, Black, Blue, Orange, Purple, Grey.?
    
    Ans:- `nano Colors.txt`
    
    `Red`
    
    `Pink`
    
    `White`
    
    `Black`
    
    `Blue`
    
    `Orange`
    
    `Purple`
    
    `Grey`
    
    Once you have added all the lines, save the file by pressing `Ctrl+O` and then exit the editor by pressing `Ctrl+X`
    
    `cat Colors.txt`
    
    *Output*
    
    `Red`
    
    `Pink`
    
    `White`
    
    `Black`
    
    `Blue`
    
    `Orange`
    
    `Purple`
    
    `Grey`
    
11. To find the difference between fruits.txt and Colors.txt files. ?
    

Ans:- To find the difference between two files in Linux, you can use the `diff` command. The `diff` command compares two files line by line and shows the differences between them.

`diff fruits.txt Colors.txt`

`output`

![](https://lh3.googleusercontent.com/4rlhERm-nXlP3TB3QHs5SXZOJYhwRhjGknG-FAUfr4cKG14NS0DTkkKSa22yyyA-z2atJELY7SFzUbO9aSdKmYznu0uiqHdX97QGyoJige-TCscjDi_cXRHvKCSaquSMo4lxYoUTCq1ke6cd8lTRaEI9QTqn9byq_ko8R6qQXBmUCgmnazD2aowTSqf307TH10TJE5ndw0QnJtATfds9NUTyvt--3FXwTUYlXlF15hs13OlibItHHl-Rr5zuLTQ0shup6WCXbnNUx2yfyV29cyXEuo4AlomaHQHf58er0l64UR9xG1NzpVHlSaB3DpKRplbxnin3_4Rp3z7MXjQrBPA-o_cL0dgbEx3K7-tT0uSSCPWMMqLkXVoxysAOxXhrd6ETWzO1RjDLd34t-HclohSX4vIH544lK6luniK-WupFFnhNVAMi5vn0kPb9bsLinkVSlLnP8nv2dR_0b6NqcVMpGT5PT6IYxhoqdArvAYPnA-yQVR3NrB64X8PtEjWK50xqQpnKe6GTsz-h7oIHjPER-nz5xIx0uvOYnVn7zww_ZCE5fb06vmkLnImwbFfFMfcKC7e36XkbkMw0ZWNFRHLyxDiRNkelTk8gUug_jaiU9S9dHb1wnWhyIcUfNz2Hn08OyjcKyqcYQSBmD9ZiqBBnJ9i1YvQQviWFyMgmKNxXMKU-GCGzc0iOrRn__8b5kkPKZ9_5BNY69AtP-937c_DfNbNu-T9XakVIipBIbA8_ptvJAa9LVOc_NUiTjjbL_0JzjqhM6UBgWZN9C-5j1ODUvx6Qovol4uo54ixDZNV_orZi7s7qLg3lXk49fIg96ihWgLIxlBwWwnxsSgs6A0a-PYJQYU5HdVkBsuwdUiQ8AoRl2fjvPEq4FG_1TEByDx5ms4eRN6oi_oUpfIo_8xGoUTPubd1Gn5etS6EtJrZuxfL9kg=w164-h933-no?authuser=0 align="left")

This output shows that the first line of `fruits.txt` (`Apple`) is different from the first line of `Colors.txt` (`Red`). Similarly, lines 3, 5, and 7 have differences as well. The `<` symbol indicates the line from the first file (`fruits.txt`), while the `>` symbol indicates the line from the second file (`Colors.txt`). The `c` and `a` character indicate whether a line was changed (`c`) or added (`a`).

Thank You So Much For Reading 🐧

Saumya Ranjan Mohapatra😁🚀