# Lab Report 1
## Installing VScode
To download VScode, you would need to go to their [website](https://code.visualstudio.com/download) where you would choose one to download based on the operating system of your computer. After it is downloaded, run the installer and follow the steps on it, you should be set when the process is over.
![Image](Screenshot%2022-04-17%230823.png)
***
## Remotely Connecting
Now that you have VScode installed, open a terminal by pressing ``Ctrl + ` ``, then enter the command `ssh cs15lsp22zz@ieng6.ucsd.edu` where the "zzz" will be replaced by the letters in your course-specific account (you can find yours [here](https://sdacs.ucsd.edu/~icc/index.php)). Then you should get a message asking if you want to continue connecting, type `yes` and press enter. You would then asked to enter your password, after it is entered, you are now logeed in to a remote computer!
> Message you should get when you are successfully logged in </br>
> ![Image](Screenshot%2022-04-17%233143.png)
***
## Trying Some Commands
Now that you are connected to a remote computer, you can now run some commands on both your own computer and the remote computer. Below are some useful ones for you to try:
- `cd ~` : go back to the home directory
- `cd` : change between directories, typing the directory you want to go to after it.
- `ls `: list the names of the files within the directory
- `cat <filepath>` : output the content of the files
- `mkdir` : create a new directory
> If you try to access the directory which you have no permission for, it will deny your request. </br>
![Image](Screenshot%2022-04-18%221013.png)
***
## Moving Files with scp
What you just did was all completed on one computer, now, we are going to move files between a remote and a local computers.
First, create a file wiht the name `WhereAmI.java`, with the contents being: 
> class WhereAmI { </br>
>  public static void main(String[] args) {</br>
>    System.out.println(System.getProperty("os.name"));</br>
>    System.out.println(System.getProperty("user.name"));</br>
>    System.out.println(System.getProperty("user.home"));</br>
>    System.out.println(System.getProperty("user.dir"));</br> 
}</br>
> }

After have the file saved, enter the command `scp WhereAmI.java cs15lsp22zz@ieng6.ucsd.edu:~/` from the directory the file is in, and remember to change `zzz` with your username. Then you should be asked for your password
![Image](Screenshot%2022-04-18%222655.png)

***
## Setting an SSH Key
***
## Optimizing Remote Running

![Image](Screenshot%202022-04-08%20131534.png)