# Bandit Level 9 Writeup

## Chapter Zero: The Objective

### To extract the password for the next level that is stored in the file data.txt and is the only line of text that occurs only once

## Chapter One: The Adventure

Firstly I logged into the game using **ssh** command and the password I got by completing the last level. Now, I needed to extract that line from data.txt that occured only once. For that I decided to use the **uniq** command with -u option as it would give only the unique line of text as an output. But there was a problem, **uniq** command only works when the duplicate lines are consecutive. so, to solve this problem, I used the **sort** command to sort the contents of the file and used the piping operator '|' to pass the output of **sort** as an input to **uniq**.

## Chapter Two: Reflecting on my journey

I used both the sort and uniq commands for the first time. I learnt how to sort a file and also to print the unique lines from a file filled with duplicates.
I also used the piping operator for the first time. I now have three more tools to help me navigate my way through the upcoming levels.

## Chapter Three: My Exact Action Sequence

1. ssh `bandit8@bandit.labs.overthewire.org` -p 2220
2. sort data.txt | uniq -u
