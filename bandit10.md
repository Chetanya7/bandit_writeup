# Bandit Level 10 Writeup

## Chapter Zero: The Objective

### To extract the password for the next level that is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters

## Chapter One: The Adventure

Firstly I logged into the game using **ssh** command and the password I got by completing the last level. Now, I needed to extract the human readable strings present in the file data.txt that are preceded by several '=' characters. For that I used the **strings** command and piped it's output to **grep** to filter the strings preceded by several '=' characters.

## Chapter Two: Reflecting on my journey

I used **strings** command for the first time. I learnt how to extract human-readable strings from a file.

## Chapter Three: My Exact Action Sequence

1. ssh `bandit9@bandit.labs.overthewire.org` -p 2220
2. strings data.txt | grep '=='
