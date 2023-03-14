# Lab Report 7

## Step 4:

![Image](https://media.discordapp.net/attachments/1085046811267448832/1085046857400594454/Screen_Shot_2023-03-13_at_8.48.05_PM.png?width=1870&height=1084)
I have previously used the ssh command line in my local computer to enter into the ieng6 server, so I back searched by using the command `Ctrl + r`
then following by typing ssh, to find the command line `ssh cs15lwi23anq@ieng6.ucsd.edu` once it popped up through the back search I hit `<enter>`. 
The reason it did not ask me for my password, is due to the fact that I had previously an ssh key gen. Now I have successfully logged into ieng6.

## Step 5:

![Image](https://media.discordapp.net/attachments/1085046811267448832/1085048956834295819/Screen_Shot_2023-03-13_at_8.56.44_PM.png?width=1904&height=406)
I had previously made a ssh keygen in class, so I took the fork that I had made of lab7 and copied the ssh key, and then in the terminal, I typed in,
`git clone ` followed by `<command + v>` to paste in my ssh key. Then I hit `<enter>` to run the command line.

## Step 6:

![Image](https://media.discordapp.net/attachments/1085046811267448832/1085050436773478420/Screen_Shot_2023-03-13_at_9.02.27_PM.png?width=1808&height=1084)
Before I had started this step I had the CSE15L week 3 github opened. I change directories by typing `cd lab7` and clicking `<enter>` to change into the 
lab7 repository I just made. Then to compile the testers I copied the compiler line from week 3, and then in the terminal I used the paste command which is
`<command + v>`. Then I copied the command to run it up until the end of "JUnitCore". Then I pasted this using `<command + v>` again, followed by `<space>` and then 
typed in `ListExamplesTests`. Then I hit `<enter>`.

## Step 7:

![Image](https://media.discordapp.net/attachments/1085046811267448832/1085051261642092594/Screen_Shot_2023-03-13_at_9.05.46_PM.png?width=1722&height=1084)
In order to fix the mistakes in the code. I first typed in the command `nano L <tab> .j <tab>` and then `<enter>` The command line should result in
"nano ListExamples.java". I then hit the `<down>` arrow 42 times, then the `<right>` arrow 12 times. Then `<delete>` and then the key `<2>`. This changes
the 1 to a 2. Then I typed `<control + o>` then `<enter>` to save. Then `control + x` to exit nano. 

## Step 8:

![Image](https://media.discordapp.net/attachments/1085046811267448832/1085051628111020062/Screen_Shot_2023-03-13_at_9.07.12_PM.png?width=1904&height=482)
In order to rerun the tests, I typed `<up>` 3 times to get to the line where I previously ran the compiler. Then hit `<enter>`. I then typed `<up>` 3 times 
again to get to the line that ran the testers then hit `<enter>`.

## Step 9:

![Image](https://media.discordapp.net/attachments/1085046811267448832/1085051628111020062/Screen_Shot_2023-03-13_at_9.07.12_PM.png?width=1904&height=482)
To commit and push changes I typed out the command `git add L<tab>.j<tab>` in that order and then hit `<enter>`. I then typed out `git commit - m "Updated"`
with "Updated" to mark as the updated commit, then I hit `<enter>`. Then i typed `git push` and then `<enter>`. The previously made ssh key allows pushing 
and committing to be much easier this way.
