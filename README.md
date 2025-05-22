# Reverse-Engineering

Reverse Engineering is a process of taking a piece of code (complied code) and trying to understand the working of software. By Reverse Engineering it we can find Bugs like Buffer over flow, Heap, memory corruption etc.

In this Section i will be walking through some Code Analysis by using GHIDRA tool.

crackme0X00

 ![Image Alt]()

So, from the above screen shot Navigate to Main function from Symbol Tree and select main function by double clicking it, post that Main function can be seen left side.

EXPLANATION

* we can see that it is very straight Password validation check. I have renamed some variable to my needs for my Better understanding.
* The program takes some input from the User using Strcmp function it checks for the stored password i.e, 250382 and validates it.
* The file is in ELF (Executable and Linkable Format) which can be run in Linux OS or WSL (Windows Subsystem for linux) if it can be installed in Windows OS you can run through CMD directly.












NOTE: The files that i have uploaded are not mine but owned by their respective owners and i have took inspiration from "stryker2k2" Youtube Channel.
