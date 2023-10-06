## Lab Report 1

**cd**

1.  <br>
![Image](cdNoArgs.png)

<p>The working directory when the command was run was /home/lecture1/messages . The output was the working directory was set to home, because no argument was indicated for cd. Nothing was printed. The output is not an error. </p>


2.  <br>
![Image](cdToDirectory.png)

<p>The working directory when the command was run was /home . The output of the command cd with a path to a directory, cd lecture1/messages was that the working directory was changed to the directory passed in as an argument, in this case, to the messages directory, nothing was printed. The output is not an error. </p>


3.  <br>
![Image](cdToFile.png)

<p>The working directory when the command was run was /home . The output of the command cd lecture1/messages/en-us.txt , the path to a file, was a bash message indicating the argument passed in was not a directory. This output is an error because cd changes the current working directory, it cannot change to a file. </p>


**ls**
1.  <br>
![Image](lsNoArgs.png)

<p>The working directory when the command was run was the home directory.
The output of the command ls with no args was lecture1 in bold blue. This is the output because the directories and/or files located within the home directory are lecture1. There is no error.</p>


2.  <br>
![Image](lsToDirectory.png)

<p>The working directory when the command was run was the lecture1 directory. The output of this command ls lecture1 was the files and directories within the lecture1 directory, the Hello.class, Hello.java, messages in a bold blue, and README. There is no error.</p>


3.  <br>
![Image](lsToFIle.png)

<p>The working directory when the command was run was the home directory. The output of the command ls lecture1/messages/en-us.txt was nothing because we were already located within a file, and files are the lowest in the unix hierarchy, meaning files are not located within files. There is no error.</p>

**cat**

1.   <br>
![Image](catNoArgs.png)

<p> The working directory when the command was run was the lecture1 directory. The output of the command cat with no args was a blank line where the user can enter input, because the cat command allows one to create or view a file. There is no error. </p>


2.  <br>
![Image](catToDirectory.png)

<p> The working directory when the command was run was the home directory. The resulting output of the command of cat lecture1 was an error stating that lecture1 is a directory. This is an error because cat takes in either a file to view or creates one, it does not work for directories. </p>


3.   <br>
![Image](catToFile.png)

<p> The working directory when the command was run was the home directory. The resulting output of the command cat lecture1/messages/en-us.txt was viewing the contents of the file, so "Hello World!" was printed. There is no error.
