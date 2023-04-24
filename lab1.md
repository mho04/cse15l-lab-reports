# SET UP
You will need three things. 
- open visual studio code
- download [git](https://gitforwindows.org/) 
- set up [bash](https://stackoverflow.com/questions/42606837/how-do-i-use-bash-on-windows-from-the-visual-studio-code-integrated-terminal/50527994#50527994) 

**Visual Studio** is the program that you will be coding in. If you do not already have VS code installed. You can download it [here](https://code.visualstudio.com/). They have a tutorial to follow on their website.

Once downloaded and opened, VS should look like this.
![opening vs](https://user-images.githubusercontent.com/130100567/231044468-eaebf2ce-fad5-4a48-b61a-fce639a1424d.png)

Before being able to even log in, you will need **Git** installed as well. Only windows devices need to download this. 
After downloading Git, you will need to set up **Bash**, click on the link provided above for the tutorial on how to do this.

---
# GETTING LOG IN INFO
To log into a server remotely, you will need the log in info for your cs15L account
find your cs15L username [here](https://sdacs.ucsd.edu/~icc/index.php)
1. enter ucsd username (without @ucsd.edu)
2. enter student id (A########)

once you log in, this is were you will find your CS15L account username under 

Additional Accounts
---
![account pw reset](https://user-images.githubusercontent.com/130100567/233898563-215728ca-744f-4ff1-b5aa-2e5f3a22d111.png)
---
 
You need to make a password for this account.
Make your password by clicking the *UC San Diego Active Directory (AD) Password Change Tool* Link

---
# LOGGING INTO REMOTE SERVER
![logging in](https://user-images.githubusercontent.com/130100567/231045093-4f1ebeb7-51a2-45e3-afd5-b1c0b7ae68e0.png)

after finishing all the set up and getting log in info
1. make sure you're not on an opened file 
2. open the terminal
3. enter ssh cs15lsp23`yourusername`@ieng6@ucsd.edu
4. enter the password you just made

---
# TEST SOME COMMANDS
![commands to test](https://user-images.githubusercontent.com/130100567/231048096-5d6c3fc3-9315-4987-b673-ac51394f63bf.png)


what they do (for the given path following it):
cd - stands for "change directory" switches to that given path from the current working directory

ls - list all the files and folders in that path
  
cat - allows you to display multiple files at a time
  
cp - stands for "Class Path", makes the program look for the given path

example of what testing a commmand should look like
current command being ran: ls -lat
![testing commands](https://user-images.githubusercontent.com/130100567/231048161-c9946463-ef2a-480b-bb2b-e8adac6d6d0b.png)

---
# LOGGING OUT
To leave the remote server:

press Ctrl D

then enter into your terminal "exit"
