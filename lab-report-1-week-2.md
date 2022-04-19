# **Lab Report 1**
***
## Installing VScode
<p>To download VScode, you would need to go to their [website](https://code.visualstudio.com/download) where you would choose one to download based on the operating system of your computer. After it is downloaded, run the installer and follow the steps on it, you should be set when the process is over.</p>

![Image](Screenshot%202022-04-17%20230823.png)

***  

## Remotely Connecting
Now that you have VScode installed, open a terminal by pressing ``Ctrl + ` ``, then enter the command `ssh cs15lsp22zz@ieng6.ucsd.edu` where the "zzz" will be replaced by the letters in your course-specific account (you can find yours [here](https://sdacs.ucsd.edu/~icc/index.php)). Then you should get a message asking if you want to continue connecting, type `yes` and press enter. You would then asked to enter your password, after it is entered, you are now logeed in to a remote computer!
> Message you should get when you are successfully logged in. 
>
> ![Image](Screenshot%202022-04-17%20233143.png)
***
## Trying Some Commands
Now that you are connected to a remote computer, you can now run some commands on both your own computer and the remote computer. Below are some useful ones for you to try:
- `cd ~` : go back to the home directory
- `cd` : change between directories, typing the directory you want to go to after it.
- `ls `: list the names of the files within the directory
- `cat <filepath>` : output the content of the files
- `mkdir` : create a new directory
> If you try to access the directory which you have no permission for, it will deny your request. 
>
>![Image](Screenshot%202022-04-18%20221013.png)
***
## Moving Files with scp
<p>What you just did was all completed on one computer, now, we are going to move files between a remote and a local computers.
First, create a file wiht the name `WhereAmI.java`, with the contents being: </p>

> class WhereAmI {  
>  public static void main(String[] args) {    
>    System.out.println(System.getProperty("os.name"));    
>    System.out.println(System.getProperty("user.name"));   
>    System.out.println(System.getProperty("user.home"));   
>    System.out.println(System.getProperty("user.dir"));   
>}   
> }

<p>After have the file saved, enter the command `scp WhereAmI.java cs15lsp22zz@ieng6.ucsd.edu:~/` from the directory the file is in, and remember to change `zzz` with your username. Then you would be asked for your password to log into the remote computer. If every step is completed successfully, you should see the file in the directory with `ls` command and run the file with `java` or `javac` commands like the image below shown.</p>

![Image](Screenshot%202022-04-18%20222655.png)

***
## Setting an SSH Key
<p>Having to retype your password everytime you log in is ineffcient and annoying, so we would make the system to "remember you".
First, enter the command `ssh-keygen` in the terminal, you should get something similar like this: </p>

> Generating public/private rsa key pair.  
>Enter file in which to save the key   
> (/Users/user-name/.ssh/id_rsa): /Users/user-name/.ssh/id_rsa   
>Enter passphrase (empty for no passphrase): 

<p>Then just hit the enter key, you should get something like this: </p>

>Enter same passphrase again: 
>Your identification has been saved in /Users/<user-name>/.ssh/id_rsa.   
>
>Your public key has been saved in /Users/<user-name>/.ssh/id_rsa.pub.
>
>The key fingerprint is:   
SHA256:jZaZH6fI8E2I1D35hnvGeBePQ4ELOf2Ge+G0XknoXp0 
 <user-name>@<system>.local  
>
>The key's randomart image is:  
+---[RSA 3072]----+   
|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|   
|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;. . + .&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|   
|      . . B o .  |   
|     . . B * +.. |   
|      o S = *.B. |   
|       = = O.*.*+|   
|        + * *.BE+|   
|           +.+.o |   
|             ..  |   
+----[SHA256]-----+   


***
## Optimizing Remote Running

![Image](Screenshot%202022-04-08%20131534.png)