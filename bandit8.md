# Bandit Level 8 Writeup

## Chapter Zero: The Objective

### To get the password for the next level that is stored in the file data.txt next to the word millionth

## Chapter One: The Adventure

Firstly I logged into the game using **ssh** command and the password I got by completing the last level. Then I used the **grep** command to find the line that had the word millionth in it and I found the password in the very same line.

## Chapter Two: Reflecting on my journey

I used the grep command for the first time and learnt how I can use it to find a specific line that contains a specific word or pattern.

## Chapter Three: My exact action sequence

1. ssh `bandit7@bandit.labs.overthewire.org` -p 2220
2. grep "millionth" data.txt
