# Bandit Level 6 Writeup

## Chapter Zero: The Objective

### To get the password for the next level that is stored in a file somewhere under the *inhere* directory and has all of the following properties: human-readable, 1033 bytes in size, not executable

## Chapter One: The Adventure

Firstly I logged into the game using **ssh** command and the password I got by completing the last level. Then I made *inhere* my cwd (current working directory) using the **cd** command. It was now time to search for the file that had the password to the next level, for this task I decided to use the **find** command. And boom, it gave me the path to the file that had the password and then I used the **cat** command to read the contents of that file, and there it was, the password to the next level.

## Chapter Two: Reflecting on my journey

During this adventure, I used the **find** command for the first time and learnt how can I search for a file whose properties are known to me.
Now I have one more tool to tackle whatever lies in the further levels of this game.

## Chaper Three: My exact action sequence

1. ssh `bandit5@bandit.labs.overthewire.org` -p 2220
2. cd inhere
3. find -type f -size 1033c ! -executable
4. cat ./maybehere07/.file2
