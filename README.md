# LINUX

## What is Linux ?

[ALL ABOUT LINUX](https://www.linux.com/what-is-linux/)

In short, just like Windows, iOS, and Mac OS, Linux is an operating system. It is the best known and most used open source operating system. ( by open source we meand that the source code is freely available.)

Linux is the most used OS in the server World. Hence, the need for a DevOps Engineer to be familiar with it.

## Some Common Linux Commands

### The Echo Command
```
 echo
 ```

The echo command is used to print to screen
for example

```
echo Hello World
```
Output
> `Hello World`

So Hello World was the argument pass to echo and it prints it out. like Print in python.

### The ls Command
```
ls
```
The ls command is used to list all the elements of a directory. i.e All the files and folders in a particular location.

### The cd Command

The cd Command stands for change directory( in linux directory is the same thing as folder in windows) the cd command is used to navigate to new directories in a linux system.

```
cd /home/Damian/Documents
```
The above command changes the present working directory to Documents directory.

### The pwd Command
```
pwd 
```
Pwd command or the present working directory command is used to print the directory you are currently in.

For example if I'm in Documents directory of my Linux system and I used the pwd command it will output something like this.

> `/home/Damian/Documents`

Showing that I'm currently in the Documents directory.

### The mkdir command

mkdir is used to create a new directory. 

So if we currently in /home/Damian/Documents 
``` 
mkdir Africa
```
the command above creates a new directory/folder inside the Documents directory.
So if we run the ls command we will see the Africa directory among other files and directories that were in Documents directory.

## Flags ( or Options )
Flags are used to modify the behaviour of a command. There is always a dash (-) or two dashes before a flag. for example the ls command can view all the elements of a particular directory. But with the -a flag i.e
```
ls -a
```
you can also view all the hidden files in that particular directory.

Also if for example you want to make more than one directory at the same time, say you want to create Europe directory and then UK directory inside Europe directory. instead of using 
> `mkdir Europe`

Then changing to the directory using 
> `cd Europe`

and then 
> `mkdir UK`

We can easily use the -p flag like
```
mkdir Europe\UK
```
The above command will create both the Europe directory and the UK directory at the same time.

There are a ton of other flags that make our life easier.

## FILES
To create a new file in a linux system, we use the touch command.
```
touch first.txt
```

the above command creates a new text file called first but the new file will be empty.
To create a new file and put content in it we could use the cat> command
```
cat > second.txt
```

the above command will wait for you to type in the contents of second.txt we use the enter key to go to new line and use CTRL + D to exit and save.

To view the contents of the new files we have created we could use the cat command but this time without > i.e
```
cat second.txt
```
The above command prints the contents of second.txt for us.

### Copying Files

To copy file in a Linus System we use the cp command. The syntax for this is 
``` 
cp <source file path and name> < target file path and name>
```

So for example if we are in the Documents directory and we have a file name first.txt and we want to copy it to the same directory but with a different name we could use 
```
cp first.txt first_note.txt
```

So the above command makes a copy of the first.txt file with the name first_note.txt but if there already exist a first_note.txt it will be replaced.

Copying to another directory we could 
``` 
cp first.txt /home/Damian/Downloads
```
This copies first.txt to the downloads directory.
The above command can also be done like this 
``` 
cp /home/Damian/Documents/first.txt /home/Damian/Downloads/first.txt
```
The difference between the 2 commands above is the way we wrote the file path
There  2 ways of writing file paths Absolute and Relative path.

In Absolute path we list all the file path starting from the root directory the root directory is always specified by the first slash ( / ).

> `e.g /home/Damian/continent/Africa` 

The above is example of an absolute path. But suppose we are in the continent directory and want to go the Africa directory we simply do 

>`cd Africa`

we’ve used a relative path.


To copy directories(folders) the cp command will not work we need to add the -r flag.

``` 
cp -r /home/Damian/Documents/Europe/Nigeria /home/Damian/Documents/Africa
```
The above command copies the Nigeria directory to Africa.

### Moving Files

The command used for moving files is the mv command. It has the same same syntax as the cp command as explained above. The difference is that the mv commmand is used to cut and paste rather than copying like the cp command.
The mv command can also be used to rename files by just changing the name of the file in the target file path.
``` 
mv first.txt main.txt
```
The above command renames the text file from first to main.

### Removing fies / Directories
The rm command is used to remove or delete files in linux. you simply run
```
rm <file-name>
```
while to remove directories like in the case of copying you need the -r flag.
```
rm -r <directory-name>
```
