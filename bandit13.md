# Bandit level 13 writeup

## Chapter Zero: The Objective

To extract the password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed.

## Chapter One: The Adventure

Firstly I logged into the game using **ssh** command and the password I got by completing the last level. Then I made a temporary directory using the **mktemp** command with *-d* option to specify that a directory has to be created. I then copied the file data.txt using the **cp** command and then reversed the hexdump back into binary format using the **xxd** command with *-r* option and then stored the binary data in a new file named *zoro.bin*. Then I used the **file** command to determine the type of the file *zoro.bin* and got to know that it had gzip compressed data. To decompress that I used the **gunzip command** and then again checked the type of the resulting file using the **file** command, which made me aware of the fact that it now had bzip2 compressed data. To decompress that I used the **bunzip2** command and then the resulatnt file was archived in tar format and the I used the **tar** command with *-xvf* option to unarchive the file and this process of unarchiving and decompressing continued until I obtained the password to the next level.

## Chapter Two: Reflecting On My Journey

I learnt how to convert hexdump to binary, decompress gzip and bzip2 compressed data, and unarchiving tar.

## Chapter Three: My Exact Action Sequence

1. ssh `bandit12@bandit.labs.overthewire.org` -p 2220
2. mktemp -d
3. cp data.txt /temp/temp.ULbAfJbQ43
4. cd /temp/temp.ULbAfJbQ43
5. xxd -r data.txt > zoro.bin
6. file zoro.bin
7. mv zoro.bin zoro.gz
8. gunzip zoro.gz
9. file zoro
10. mv zoro zoro.bz2
11. bunzip zoro.bz2
12. file zoro
13. mv zoro zoro.tar
14. tar -xvf zoro.tar
15. And so on.......
