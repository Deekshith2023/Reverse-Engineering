# Reverse-Engineering

Reverse Engineering is a process of taking a piece of code (complied code) and trying to understand the working of software. By Reverse Engineering it we can find Bugs like Buffer over flow, Heap, memory corruption etc.

In this Section i will be walking through some Code Analysis by using GHIDRA tool.

Challenge-1: crackme0X00

 ![Image Alt](https://github.com/Deekshith2023/Reverse-Engineering/blob/c094f50fe27d4532e4dcd6798b7ea4fbab5e93eb/ScreenShots/crackme0x00%20pic-1.png)

So, from the above screen shot Navigate to Main function from Symbol Tree and select main function by double clicking it, post that Main function can be seen left side.

EXPLANATION

* we can see that it is very straight Password validation check. I have renamed some variable to my needs for my Better understanding.
* The program takes some input from the User using Strcmp function it checks for the stored password i.e, 250382 and validates it.
* The file is in ELF (Executable and Linkable Format) which can be run in Linux OS or WSL (Windows Subsystem for linux) if it can be installed in Windows OS you can run through CMD directly.

Challenge-2: crackme0x01 
 ![Image Alt](https://github.com/Deekshith2023/Reverse-Engineering/blob/main/ScreenShots/crackme01.png?raw=true)
 For this challenge if we can see above it is almost the same as the 1st Challenge one but the password is in Hexadecimal format after converting that the password will be “5274” from 0x149a. It is simple challenge.









NOTE: The files that i have uploaded are not mine but owned by their respective owners and i have took inspiration from "stryker2k2" Youtube Channel.
