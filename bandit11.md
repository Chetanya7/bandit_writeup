# Bandit Level 11 Writeup

## Chapter Zero: The Objective

To extract the password for the next level that is stored in the file data.txt, which contains base64 encoded data

## Chapter One: The Adventure

Firstly I logged into the game using **ssh** command and the password I got by completing the last level. Now, I needed to decode the base64 data present in the file data.txt, for which I used the **base64** with -d option(to decode).

## Chapter Two: Reflecting on my journey

I used the **base64** command for the first time. I learnt how to decode a data that is encoded using base64.

## Chapter Three: My Exact Action Sequence

1. ssh `bandit10@bandit.labs.overthewire.org` -p 2220
2. base64 -d data.txt
