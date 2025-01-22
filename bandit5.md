# Bandit Level 5 writeup

## Chapter Zero: The Objective

### To get the password for the next level that is stored in the only human-readable file in the *inhere* directory

## Chapter One: The Adventure

Firstly I logged into the game using **ssh** command and the password I got by completing the last level. I then saw the the contents of the home directory using the **ls** command and found that it had only one sub-directory that was named *inhere* which (according to the intel I got) is the directory that has the file I am searching for. I then made *inhere* my cwd (current working directory) using the **cd** command so that I could see it's contents using the **ls** command. There were nine files in there. Now I had to identify the file which was human-readable. For that I used the **file** command for each file and when I used it for -file07 the output came out to be *ASCII text* which meant that this file was the *CHOSEN ONE*. Now, there was only thing left to do to reach my goal, that was to read the file and for that I obviously used the **cat** command. And there it was, the password to the next level.

## Chapter Two: Reflecting on my journey

I used the **file** command for the first time and learnt how to differeniate between a non-human-readable file and a human-readable file using this command.
Now I have one more tool to tackle whatever lies in the further levels of this game.

## Chaper Three: My exact action sequence

1. ssh `bandit4@bandit.labs.overthewire.org` -p 2220
2. ls
3. cd inhere
4. ls
5. file ~/inhere/-file0x (here x=0 to 7)
6. cat ~/inhere/-file07
