# CSE 15L LAB REPORT 1: Remote Access and FileSystem

## Examples Using the cd Command:

Files and Folders used

cd command with no argument:

```
[user@sahara ~]$ pwd
/home
[user@sahara ~]$ cd
```
The working directory when run was home. The output did nothing as the cd command needs another directory or folder as an argument for the current directory to switch to the one stated in the argument. Therefore, running the cd command with no argument results in no change in the directory. 
There is no error, as the default move when cd is used with no argument is to move it to the home directory. 


cd command with a path to a directory as an argument:

```
[user@sahara ~]$ pwd
/home
[user@sahara ~]$ cd messages
[user@sahara ~/lecture1/messages]$
```
The working directory when run was home. This output was given because the diretory was succesfully changed to the directory titled "messages." Because this was a valid directory the correct output was given with no error.
The output is not an error. Messages directory was within the file system. 

cd command with a path to file as the argument:

```
[user@sahara ~/lecture1/messages]$ pwd
/home/lecture1/messages
[user@sahara ~/lecture1/messages]$ cd en-us.txt
bash: cd: en-us.txt: Not a directory
```

The working directory when run was messages. This output was given because the argument passed through the cd command was a path to an individual file and not a directory. The cd command is meant to change directories and if its passed through a path for a file it will return an error for the output.
The output was an error because a file was passed through the argument instead of a directory within the file system. Therefore, an error will be printed. 

## Examples Using the ls Command:

ls command with no argument:

```
[user@sahara ~]$ pwd
/home
[user@sahara ~]$ ls
lecture1
```

The working directory when run was home. This output was given because lecture1 is the folder within the home directory. Therefore, lecture1 is given as the output. This output is not an error. 

ls command with a path to directory as argument: 

```
[user@sahara ~]$ pwd
/home
[user@sahara ~]$ ls lecture1
Hello.class  Hello.java  messages  README
```

The working directory when run was home. This output was given because the files and folders under the lecture1 directory includes Hello.class, Hello.java, messages, and README. Therefore, those 4 are correctly given as the output. There is no error in this output.

ls command with a path to a file as the argument:

```
[user@sahara ~]$ pwd
/home
[user@sahara ~]$ ls en-us.txt
ls: cannot access 'en-us.txt': No such file or directory
```

The working directory when run was home. This output was given because this file does not exist within the home directory. There was no files in the home directory which is why the output is given as it is. This is an error as an output as this file does not exist within the home directory. 

## Examples Using the cat Command: 

cat command with no argument

```
[user@sahara ~]$ pwd
/home
[user@sahara ~]$ cat
hello
hello
```

The working directory when run was home. The output given when cat is ran with no argument is a blank output that lets the user input something into the terminal. Then, the input the user gives is outputted again by the terminal as shown in the code block above. This happens because the cat command is used to concatenate and display the contents of various files. However, with no argument the cat command resorts to to input from the keyboard from the user themselves. This is not an error within the output. 

cat command with a path to a directory as the argument:

```
[user@sahara ~]$ pwd
/home
[user@sahara ~]$ cat lecture1
cat: lecture1: Is a directory
[user@sahara ~]$ 
```

The working directory when run was home. The output was given as this error message because the cat command is designed to be used on individual files but not directories. As a result, the "Is a directory" error message is given as an output when the cat command is used on a directory. This is an error message given as an output because the cat command was used on a directory and not a file. 

cat command with a path to a file as the argument:

```
[user@sahara ~/lecture1/messages]$ pwd
/home/lecture1/messages
[user@sahara ~/lecture1/messages]$ cat en-us.txt es-mx.txt
Hello World!
¡Hola Mundo!
```

The working directory when run was messages. The output was given as it concatenated the 2 files given in the cat command's argument. The files en-us.txt and es-mx.txt contain "Hello World!" and "¡Hola Mundo!" which are then given as the output when the cat command uses these 2 files as arguments. There is no error message in this output. 







