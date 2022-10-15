# Lab Report 1
## Tutorial Introduction 
This is a tutorial on how to install VS code, connect remotely to another computer, move files with SCP, set an SSH key, and optimize remote running. 




## Installing VS Code
Although I currently already have VS Code installed, I will still show how to download it.

First, head to the [VS Code](https://code.visualstudio.com/download) website.

Second, click on whichever option is compatible with your computer (i.e. if you have a Windows operating system, click on the Windows installer).

![Image](Screenshot1.png) 

Third, open the installer and follow the prompts given. 

Fourth, after it's finished downloading, launch VS Code to make sure it's working.



## Remotely Connecting
*After finally getting my remote login working, I have updated the following below.*

First, open the terminal in VS Code using the button "Terminal" on the top left of the application, or with the keyboard shortcut CTRL + `. 

![Image](Screenshot2.png)

Second, type `ssh cs15lfa22XX@ieng6.ucsd.edu` into the terminal, replacing XX with the two letters that are part of your personal CS account.

Third, once prompted, type in your password. Although there is no feedback, it will be recording your keystrokes. Once you're done, press enter. 
> If the password is wrong and/or denied for another reason, it will prompt you again afterwards. 

![Image](Screenshot3.png) 

Fourth, after entering your password correctly, it should pull up several lines of code before saying you have successfully logged in remotely.



## Trying Some Commands
Now that you are remotely connected, some commands to try out are:
* `cd ~` --> changes the current directory to the home directory
* `cd (directory name)` --> changes the current directory to the designated one
* `pwd` --> prints the working directory
* `cp /home/linux/ieng6/cs15lfa22/public/hello.txt ~/` --> changes directory to the specified one on the remote computer
* `cat /home/linux/ieng6/cs15lfa22/public/hello.txt` --> prints out the contents of `hello.txt`

![Image](Screenshot4.png)



## Moving Files With SCP
Here are the steps to move a file with `scp`.

First, type `scp (file name) cs15lfa22XX@ieng6.ucsd.edu:~/`, replacing XX with your personal account letters.

Second, once prompted, type in your SSH account password.

Third, lines of code will print afterwards, showing the progress of the file copying. The file has been successfully copied once it reaches 100%.

Fourth, after that (to test if it worked), connect remotely using `ssh cs15lfa22XX@ieng6.ucsd.edu` and type in your password.

Fifth, compile the file you moved over and run it using the commands `javac (file name)` and `java (file name)`, the last one without the suffix.

![Image](Screenshot5.png)


## Setting an SSH Key
Here are the steps to set an SSH key, which will make logging in remotely much easier!

First, type `ssh-keygen` into the terminal. Once prompted, save a passphrase into a folder on your computer (it should already give you one), and then press enter again to set the default path.
> If your operating system is on Windows, there is an additional step to saving an ssh, although it is mostly for security reasons.

![Image](Screenshot6.png)

Second, login to your remote computer using your login.

Third, once logged in, type `mkdir .ssh`, and then type `exit` to logout.

Fourth, use the SCP method to copy the PUBLIC key folder (should end with id_rsa.pub), but the end of the codeline should be `cs15lfa22XX@ieng6.ucsd.edu:~/.ssh/authorized_keys`.

Fifth, you should be able to login to `ssh` and `scp` using the passphrase now! To know it worked, it will prompt you with asking for the passphrase rather than the password, as seen in the image below.

![Image](Screenshot7.png)



## Optimizing Remote Running
This section of the tutorial is to let you know the most efficient way to make a local edit to a file and copy it over using `scp`.

The most efficient way for me, so far, is to combine all the commands into a couple lines rather than multiple. This reduces the typing and processing time. By utilizing the arrow keys, you can also reduce the keystrokes to less than 10 if you have previously typed out the commands. I reduced mine to 6 keystrokes, not counting the passphrase keystrokes.

![Image](Screenshot8.png)





End.