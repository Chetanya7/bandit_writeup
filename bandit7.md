# Bandit Level 7 Writeup

## Chapter Zero: The Objective

### To get the password for the next level that is stored somewhere on the server and has all of the following properties: owned by user bandit7, owned by group bandit6, 33 bytes in size

## Chaper One: The Adventure

Firstly I logged into the game using **ssh** command and the password I got by completing the last level. Then I used the **find** command to search the whole filesystem by specifying the properties of the file that had the password within it, in order to obtain the path to that file. I then used the **cat** command to obtain the password from the file.

## Chapter Two: Reflecting on my journey

I learnt how to redirect the error messages to the null device so that I can keep the output of the **file** command clean.

## Chapter Three: My exact action sequence

1. ssh `bandit6@bandit.labs.overthewire.org` -p 2220
2. find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
3. cat /var/lib/dpkg/info/bandit7.password
