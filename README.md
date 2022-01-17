# Description

This assembly language program (written in Microsoft Assembler, aka **MASM**) reads 10 user-provided strings representing integer values and then displays sum and (floor division rounded) mean of these values.

Internally the string representaion of each integer is converted to a 32-bit signed integer and stored in an array that is used by function `computeSumAndMean`. The code required to execute the simple computation represents only ~10% of the total program.

The majority of the code and compute time is consumed by reading user input, converting string representations to / from integers for computation / output, and managing / cleaning / restoring data in the stack and registers.

While most operations are done "the hard way," *ReadString* and *WriteSting* macros from the Irvine library were used to convert keyboard input to strings, and strings to terminal-displayed characters.

<br>
<br>

![screenshot](/images/run_demo.PNG)
