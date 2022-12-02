# Lab Report 4
## Introduction

In this lab report, we practiced using VIM and finding the shortest possible navigation/edit methods in files. We also compared the speed of using VIM vs. SCP'ing a file.

***

## Part I: Changing the `main` method to take a command-line argument

The keystrokes that our group came up with, in the shortest sequence, is this:
`/tec<Enter>n3hd2w3xi"args[1]"<Esc>:wq<Enter>`
Which is 28 keystrokes total.

The behavior of the keystrokes are below:
`/tec<Enter>`
> ![Image](Screenshot18.png)

`n`
> ![Image](Screenshot19.png)

`3h`
> ![Image](Screenshot20.png)

`d2w`
> ![Image](Screenshot21.png)

`3x`
> ![Image](Screenshot22.png)

`i"args[1]"`
> ![Image](Screenshot23.png)

`<Esc>`
> ![Image](Screenshot24.png)

`:wq`
> ![Image](Screenshot25.png)

`<Enter>`
> ![Image](Screenshot26.png)


***

## Part II: Comparing VIM and SCP

In this part of the lab report, I timed myself performing an edit (which was the edit above this part) in Visual Studio Code, using `scp` to move the file to the remote server and run it there to confirm it works using `bash test.sh`. Even having the `scp` command in my history made me perform all of this in **38 seconds.**

I then timed myself already logged into a `ssh` session, and then made the same edit in VIM, exited, and then ran `bash test.sh`. However, this only took **14 seconds.**

The first method took longer due to the time `scp` took to move files, even if the command was already copied. I also had to log in remotely which also took more time, resulting in the extra time taken. On the other hand, using VIM was exceptionally fast and easy, as I could make direct edits without having `scp` or login using `ssh`.

I prefer using **VIM** when having to work on a program that I was running remotely due to the speed I can accomplish edits, as using `scp` for every edit/file is extremely frustrating. It is a lot more faster and easier (less typing) to accomplish the same thing that `scp` does. 

However, if the project or task I am working on requires many lines of codes to be created or I am not debugging, I would prefer `scp`. This is because Visual Studio Code would allow me to click around easily and scroll fast, which is especially convenient when the file is very long. And this type of coding does not require minor edits and constant running of the program (i.e. debugging), so although VIM may be faster in terms of minor edits, I prefer `scp` for anything else.


End.