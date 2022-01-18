# Low Level IO and Mean Calculation (in MASM)

## Description

This assembly language program (written in Microsoft Macro Assembler, aka **MASM**) was the final project for an undergraduate Computer Architecture and Assembly course in March 2020.

The program reads 10 user-provided strings representing integer values and then displays sum and (floor division rounded) mean of these values Internally the string representaion of each integer is converted to a 32-bit signed integer and stored in an array that is used by function `computeSumAndMean`.

The code required to execute the simple computation represents only a small fraction of the total program. The majority of the code and compute time is consumed by reading and validating user input, converting string representations to / from integers for computation / output, and managing data in the stack and registers.

While conversions between integers and strings were "the hard way," (i.e. without the aid of any libraries) `ReadString` and `WriteSting` macros from the [Irvine library](https://asmirvine.com/) were used to convert keyboard input to strings, and strings to terminal-displayed characters.

<br>

![screenshot](/images/run_demo.PNG)

<br>

## Downloading and running the executable

If you are running Windows and would like test the program, you can download file `bin/main.exe` and then enter `./main` at the command prompt from the folder where you have saved the file.

## Source code

If you would like to modify and/or recompile the source code in `/src/main` but do not have experience with MASM, [this link](https://asmirvine.com/gettingStartedVS2019/index.htm) from the Irvine website contains instructions on how to set up a MASM development environment in Microsoft Visual Studio.


