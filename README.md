# Low Level IO and Mean Calculation (in MASM)

## Description

This assembly language program (written in Microsoft Assembler, aka **MASM**) was the final project for an undergraduate Computer Architecture and Assembly course in March 2020.

The program reads 10 user-provided strings representing integer values and then displays sum and (floor division rounded) mean of these values Internally the string representaion of each integer is converted to a 32-bit signed integer and stored in an array that is used by function `computeSumAndMean`. The code required to execute the simple computation represents only ~10% of the total program.

The majority of the code and compute time is consumed by reading user input, converting string representations to / from integers for computation / output, and managing / cleaning / restoring data in the stack and registers.

While conversions between integers and strings were "the hard way," (i.e. without the aid of any libraries) `ReadString` and `WriteSting` macros from the [Irvine library](https://asmirvine.com/) were used to convert keyboard input to strings, and strings to terminal-displayed characters.

<br>

## Running the code

If you are running Windows and would like test the program, you can download file `main.asm` and follow [these instructions](https://asmirvine.com/gettingStartedVS2019/index.htm) to set up an environment for 32-bit MASM programs in Visual Studio. 

NOTES:

1. If you follow the instructions exactly and unzip the file `Irvine.zip` file [from this link](https://asmirvine.com/gettingStartedVS2019/Irvine.zip) to your C Drive, you will likely end up with the directory structure: `C:\Irvine\irvine\...`. The lowercase "i" `irvine` folder contains the `Irvine32.Lib` and other files needed for the Irvine Library. In order to match the library path in Visual Studio Project template [available at this link](https://asmirvine.com/gettingStartedVS2019/Project32_VS2019.zip.txt), you will need move the contents of the `irvine` folder up one directory into the uppercase "I" `Irvine` folder.

2. When you reach the **Adding a File to a Project**, this is where you will add file `main.asm` to your project. At this point, you should also remove any other `.asm` files from your project by right-clicking on the file name in the project and selecting `Remove`.

3. 






<br>
<br>

![screenshot](/images/run_demo.PNG)
