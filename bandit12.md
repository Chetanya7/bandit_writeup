# Bandit Level 12 Writeup

## Chapter Zero: The Objective

To extract the password for the next level that is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

## Chapter One: The Adventure

Firstly I logged into the game using **ssh** command and the password I got by completing the last level. Now, I needed to decode ROT13, for that I used the **tr** (translate) command and using that I shifted the characters by 13 positions.

## Chapter Two: Reflecting on my journey

I used the **tr** command for the first time. I learnt hoe to decode ROT13 using that.

## Chapter Three: My Exact Action Sequence

1. ssh `bandit11@bandit.labs.overthewire.org` -p 2220
2. cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
