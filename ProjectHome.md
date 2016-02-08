## Convert Folder into Executable ##

If you have one big folder with lots of scripts. You can convert this folder into one-click installer using this "Script" -- you need to have Nautilus for it. It is possible to create better cross-platform GUI for it but I do not have time to do it.

## Download ##

Download it --- http://code.google.com/p/convert-folder-into-executable/downloads/detail?name=Convert%20Folder%20into%20Executable.run

## What is This ?? ##

Many a time, I write some scripts or create software.. Installation or running these scripts is very easy for me but it become a trouble for me to teach other how to install or run the script because
1) Newbies do not know how to run terminal and its command like sudo ls space etc
2) Even If I tell him/her on phone , he/she will always mistake in spelling
3) Even If I create a installer script ,problem remain same, he/she have to do to terminal..
So what is the solution.. ???

A Solution would be a SOFTWARE who will compress whole folder into single executable file. User can click and run this executable from GUI too.  When User click on this file form GUI, It will automatically extract the file into /tmp directory and run a "initial starter script" from extracted directory.

So in nutshell, If you want to create or send Linux shell script packages then you can use this software.

Who Wrote this software ::-  NOT ME, there already exist a tool called  "makeself" , but makeself again a command mode tool, So I created a GUI for It.


## HOW TO CONVERT FOLDER INTO EXECUTABLE ? ##
**Install the package.** Just go a folder -> Right Click , Scripts -> Convert Folder into Executable

Now it will ask which shell file you want to run from that Folder.
Finally it will create a **FolderName.run** file.
You can share this file, now anybody copy to his/her linux box and just click to run it.

## Why I Created This ? ##
A month ago created a Keyboard Layout.  http://code.google.com/p/soni-hindi-phonetic-keyboard/ Which is basically a single file package
User have to download **hi-soni-phonetic.mim** file and copy into /usr/share/m17n directory.
I felt this even this is very difficult task for a newbies because he do not know how to copy a file into a area where normal user cannot write files.
so user have to go to terminal and need to write this command
sudo cp hi-soni-phonetic.mim /usr/share/m17n

It took me 20 minute to dictate this command on phone. This happen with many times.
So what I did is a new approach,
I create a folder and placed this hi-soni-phonetic.mim file inside it.

```
Soni-KeyLayout/
............../hi-soni-phonetic.mim
............../install.sh
```
I wrote a install.sh file too which is basically contain following lines

```
#!/bin/bash
sudo cp ./hi-soni-phonetic.mim /usr/share/m17n
exit 0
```

Now after this, made a Right Click -> Scripts -> Convert Folder into Executable
I selected **install.sh** , because I want to run this file.

So Finally I got a single file **Soni-KeyLayout.run** , Now I can send this .run file to anybody and all he need to click it to run it.

