# Lab Report 1
## Tutorial Introduction 
This is a tutorial on how to install VS code, connect remotely to another computer, move files with SCP, set an SSH key, and optimize remote running. 
> Although I was unable to login to my SSH account, I plan to update this lab report after I am able to get it working!



## Installing VS Code
Although I currently already have VS Code installed, I will still show how to download it.

First, head to the [VS Code](https://code.visualstudio.com/download) website.

Second, click on whichever option is compatible with your computer (i.e. if you have a Windows operating system, click on the Windows installer).

![Image](Screenshot1.png) 

Third, open the installer and follow the prompts given. 

Fourth, after it's finished downloading, launch VS Code to make sure it's working.



## Remotely Connecting
Unfortunately, I was unable to get my SSH login working, although I did use a TA account in our lab session. However, I will still write down the steps to login.

First, open the terminal in VS Code using the button "Terminal" on the top left of the application, or with the keyboard shortcut CTRL + `. 

![Image](Screenshot2.png)

Second, type `ssh cs15lfa22XX@ieng6.ucsd.edu` into the terminal, replacing XX with the two letters that are part of your personal CS account.

Third, once prompted, type in your password. Although there is no feedback, it will be recording your keystrokes. Once you're done, press enter. 
> If the password is wrong and/or denied for another reason, it will prompt you again afterwards. Unfortunately, this is what happened to my account so I was unable to have a screenshot of a successful login.

![Image](Screenshot3.png) 

Fourth, after entering your password correctly, it should pull up several lines of code before saying you have successfully logged in remotely.



## Trying Some Commands
Unfortunately, I cannot show any commands used while remotely connected, but some commands to try out are:
* cd ~ --> changes the current directory to the home directory
* cd (directory name) --> changes the current directory to the designated one
* pwd --> prints the working directory

![Image](Screenshot4.png)



## Moving Files With SCP
Again, I was unable to login to my SSH account, but I will still write the steps to move a file with SCP.

First, type `scp (file name) cs15lfa22XX@ieng6.ucsd.edu:~/`, replacing XX with your personal account letters.
> Again, I was unable to get my account working so I cannot show the full process.

![Image](Screenshot5.png)

Second, once prompted, type in your SSH account password.

Third, lines of code will print afterwards, showing the progress of the file copying. The file has been successfully copied once it reaches 100%.

Fourth, after that (to test if it worked), connect remotely using `ssh cs15lfa22XX@ieng6.ucsd.edu` and type in your password.

Fifth, compile the file you moved over and run it using the commands `javac (file name)` and `java (file name)`, the last one without the suffix.



## Setting an SSH Key
I was unable to login, I will update this part of the report as soon as I get my SSH login working. The general idea however, is to:

First, type `ssh-keygen` into the terminal. Once prompted, save a passphrase into a folder on your computer (it should already give you one), and then press enter again to set the default path.
> If your operating system is on Windows, there is an additional step to saving an ssh, although it is mostly for security reasons.

![Image](Screenshot6.png)

Second, login to your remote computer using your login.

Third, once logged in, type `mkdir .ssh`, and then type `exit` to logout.

Fourth, use the SCP method to copy the PUBLIC key folder (should end with id_rsa.pub), but the end of the codeline should be `cs15lfa22XX@ieng6.ucsd.edu:~/.ssh/authorized_keys`.

Fifth, you should be able to login to `ssh` and `scp` without using a password now!



## Optimizing Remote Running
Again, I was unable to get my SSH account working, so I am unable to provide any examples for this part. I will update this as soon as I get my account working. 

![Image](Screenshot3.png) 

This section of the tutorial is supposed to let you know the most efficient way to make a local edit to a file and copy it over using `scp`.

I will write the steps here once I am capable of doing so.





End.