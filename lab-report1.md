# CSE 15L Lab Report 1
**In the following tutorial, you will learn how to remotely connect to cse servers with your course specific account**

## Step 1: Finding your course specific account for CSE 15L

Use this link to search for your course-specific account for CSE 15L:

[Link](https://sdacs.ucsd.edu/~icc/index.php)

This is the weboage that should pop up:
![Image](https://ibb.co/Z2sddDN)

- You will then input your UCSD username, as well as your pid underneath account lookup as shown
  - Then you will click the blue button that says "submit"

A new page should open like the following image:
![Image](https://ibb.co/pnBqySr)

- Make sure that all the information is correct to you
  - Then on your page you will have a greyed out box under "additional accounts" (where the image above points at) that has "cse15L" followed by the current quarter and year as well as your own personal last few digits
  - The account you have clicked on is your current cse15L specific account
- A similar page should pop up, except now you are under your cse15L account
- There will be blue text that says "change your password" click on it and we will proceed to changing your account password

This is the following webpage that should open up:
![Image](https://ibb.co/nrYB001)

- You will then have to retype username and pid once again under the following inputs, then click the submit button

This is the new webpage that should pop up, except without the annotations in red:
![Image](https://ibb.co/FwSfPLT)

- Enter your UCSD account password underneath "current password"
- Then for your new password, make sure that it is complicated with a combination of different types of characters
- Look at the annotations on the screeshot and follow it carefully after inputting your current and new password
  - If you submit, and it pulls to a new page saying that the password reset failed, it could be because of your new password being not too complicated. Go back to the previous page and keep trying to make a complicated password
- A new page may pop up after you click enter, saying the password change was a success that means you are finished

*Note: There may be a chance that the new password you created has changed your whole UCSD account password, so make sure that you keep this password in mind*

## Step 2: Downloading VSCode

*Note: This step may be skipped if you have previously downloaded vscode on your computer*

Open the link to download vscode below:
[Link](https://ibb.co/JtZScQb)

This is the webpage that should pop up:
![Image](https://ibb.co/JtZScQb)

- VSCode can be downloaded amongst the operating systems such as: Linux, MacOS, or Windows
- To choose your specific operating system, click the blue drop down arrow, and click on your designated operating system

![Image](https://ibb.co/TR8Cpw5)

- You will then be prompted with instructions to download vscode on your computer, make sure to follow them correctly

After you have successfully installed vscode, you may open it up and this is how it should look like (it may appear different on your screen as I have used vscode previously):
![Image](https://ibb.co/Wy4DKLF)

## Step 3: Remotely connecting

If you are on windows please follow these steps to install the following on your computer

- Follow the following link to install git for windows: [Link](https://gitforwindows.org/)
- After you have installed git, click on the following link for instructions to use git bash on vscode: [Link](https://stackoverflow.com/questions/42606837/how-do-i-use-bash-on-windows-from-the-visual-studio-code-integrated-terminal/50527994#50527994)

Now we will try sshing in the terminal through vscode

- In order to open a terminal you can do either of the following (Ctrl or Command + , or click on the "terminal" tab on the top and then click "new terminal" )
- After you click new terminal this should pop up on your screen: 

![Image](https://ibb.co/d6xG085)

-You will then type the following command inside of the terminal and then click enter: (**your course-specific account username** *can be found in step 1 if you forgot* **@ieng6.ucsd.edu**)

This is an example of what yours may look like:

![Image](https://ibb.co/LpxWcYH)

- If it is your first time connecting to this server the terminal will then return text, asking "Are you sure you want to continue connecting?"
  - Simply type yes in the terminal and then hit enter
- Then the terminal will return text saying "Password: ", this is where you will enter in your new password you made previously in step 1

*Note: The terminal will not show you typing in the password on screen due to privacy reason, treat it as if you were typing in your password normally just be extra careful since you cannot see it, and then click enter*

  - If you typed in the password incorrectly, then it will re-return "Password: " again for you to type it in again
- Once you successfully typed your password in, the following text will be returned: 

![Image](https://ibb.co/KyWgqCw)

## Step 4: Running commands

Once you have successfully logged into the remote server, you may type in the commands such as "cd" , "ls , "pwd" , "mkdir" , "cp" in several different ways

Some command lines you may test out are:

- cd ~
- cd
- cd ..
- ls -lat
- ls -a
- ls <directory> where <directory> is /home/linux/ieng6/cs15lwi23/cs15lwi23abc, where the abc is one of the other group members’ username
- cp /home/linux/ieng6/cs15lwi23/public/hello.txt ~/
- cat /home/linux/ieng6/cs15lwi23/public/hello.txt
  
Try creating a new directory with these steps!
  
- mkdir "new directory name"
- cd "new directory name"
  
You can exit out of the server doing the commands (Ctrl + D or typing exit)
