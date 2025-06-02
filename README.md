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

Challenge 3: crackme0x02
 ![Image Alt](https://github.com/Deekshith2023/Reverse-Engineering/blob/main/ScreenShots/crackme02.png?raw=true)

This challenge is almost same to previous challenge password is in Hexadecimal format 0x52b24 after converting them the password will be 338724.

Challenge 4: crackme0x03
 ![Image Alt](https://github.com/Deekshith2023/Reverse-Engineering/blob/main/ScreenShots/crackme03.png?raw=true)
This challenge is a bit tricky after analsying the main function we can see that there is a “test” function. The test function reveals that the output after running the input from user is encrypted.
But if we observe closely the output stored it is using Ceaser cipher (Shift Cipher). So basically after shifting the value most likely -3 for decryption of the encrypted output we can see the original output. The Password after converting from hexadecimal to decimal is 338724.
  
Challenge 5: crackme0x04


 ![Image Alt](https://github.com/Deekshith2023/Reverse-Engineering/blob/main/ScreenShots/crackme0x05.png?raw=true)
After analysing the main function, Check function was present. It is checking the input of users. Inside the check function there is a logic built where my input should be in total of 15. For example, to achieve 15 in total 8+7=15 or 6+9=15. In general, Input should be 2 number which should indirectly points to 15 after adding that 2 numbers.
This logic is implemented in order to build the complexity of the program and to waste their time who so ever is Reverse Engineering it.

Challenge 6: crackme0x05
As pervious challenge 5 logic on check function is slight different that the result should be sum of 16 when it matches 16 then it is time to call the Parallel function. 
In the parallel function, it checks the sum of the input plus 1 is giving 0 (zero) if it satisfies the condition it prints “Password ok” status else it will escape and prints “Password incorrect”.
Example for “Password ok” : 4,4,8 






NOTE: The files that i have uploaded are not mine but owned by their respective owners and i have took inspiration from "stryker2k2" Youtube Channel.
