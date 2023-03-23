Task: What is the Linux command to

To view what's written in a file. ?
Ans: - cat Cat(concatenate) command is very frequently used in Linux. It reads data from the file and gives its content as output.
Ex- cat filename -> hello dosto

To change the access permissions of files. ?
Ans: - The chmod command is used to change the access permissions of files. For example, to give the owner of a file read, write, and execute permissions and everyone else only read and execute permissions, run the following command
chmod 755 filename

To check which commands you have run till now. ?
Ans:- history history command is used to display the history of the commands executed by the user*.*

To remove a directory/ Folder. ?
Ans:- Case 1) if dir does not include any file inside it mean empty dir. So Command will be rmdir xyzfoldername .
Case 2) if dir contains files so rmdir will not work, so the command will be
rm -r xyzfoldername (it will remove dir including the contents inside it).

To create a fruits.txt file and to view the content.?
Ans:-
touch fruits.txt
echo "fruits are good for health" > fruits.txt
cat fruits.txt
fruits are good for health

Add content in devops.txt (One in each line) - Apple, Mango, Banana, Cherry, Kiwi, Orange, Guava. ?
Ans:-
echo "Apple" >> devops.txt
echo "Mango" >> devops.txt
echo "Banana" >> devops.txt
echo "Cherry" >> devops.txt
echo "Kiwi" >> devops.txt
echo "Orange" >> devops.txt
echo "Guava" >> devops.txt

cat devops.txt
Apple
Mango
Banana
Cherry
Kiwi
Orange
Guava

Show only the top three fruits from the file.?
Ans:- head -n 3 devops.txt
Apple
Mango
Banana

To Show only the bottom three fruits from the file. ?

Ans:- tail -n 3 devops.txt
Kiwi
Orange
Guava

To create another file Colors.txt and to view the content.?
Ans:- touch Colors.txt
"cat colors.txt"

Add content in Colors.txt (One in each line) - Red, Pink, White, Black, Blue, Orange, Purple, Grey.?
Ans:- nano Colors.txt
Red
Pink
White
Black
Blue
Orange
Purple
Grey

Once you have added all the lines, save the file by pressing Ctrl+O and then exit the editor by pressing Ctrl+X
cat Colors.txt
Output

Red
Pink
White
Black
Blue
Orange
Purple
Grey

To find the difference between fruits.txt and Colors.txt files. ?
Ans:- To find the difference between two files in Linux, you can use the diff command. The diff command compares two files line by line and shows the differences between them.
diff fruits.txt Colors.txt

This output shows that the first line of fruits.txt (Apple) is different from the first line of Colors.txt (Red). Similarly, lines 3, 5, and 7 have differences as well. The < symbol indicates the line from the first file (fruits.txt), while the > symbol indicates the line from the second file (Colors.txt). The c and a character indicate whether a line was changed (c) or added (a).

Thank You So Much For Reading 🐧

Saumya Ranjan Mohapatra😁🚀