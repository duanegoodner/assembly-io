# Assembly Language Low Level IO

This assembly language program (written in Microsoft Macro Assembler, aka **MASM**) was the final project for an undergraduate Computer Architecture and Assembly course in March 2020.

## Description

The program reads a series of user-provided ASCII strings representations of integers and performs data validation to identify inputs that can be represented as 32-bit signed integers. After converting a series of 10 valid string inputs to integer form, the program computes the sum and mean of these values, converts these results to strings, and outputs those strings to the terminal.

One takeaway from this project is that implementing conceptually simple tasks like the ones performed here can require a significant amount of assembly code (in this case, hundreds of lines). The sum and mean computations represent a small fraction of the total program. The majority of the code and compute time is spent reading and validating user input, converting string representations to / from integers, and managing data in the stack and registers.



## Requirements

Windows or a Linux/Mac system with [Wine](https://www.winehq.org/).



## Getting Started on Linux/Mac with Wine

Follow the instructions [here](https://reberhardt.com/blog/programming/2016/01/30/masm-on-mac-or-linux.html), and then follow the steps listed in the **Getting Started on Windows** section below.



## Getting Started on Windows

### 1. Clone this repository

```
$  git clone https://github.com/duanegoodner/lowlevel_io_meancalc.git
```

### 2. Download and install the 32 bit MASM SDK

Go to http://masm32.com/download.htm. Download and extract archive `masm32v11r.zip`. Run file `install.exe` located in the extracted folder to install the SDK.


### 3. Download the Irvine libraries

Go to https://github.com/surferkip/asmbook, and download `Irvine.zip`. Extract directory `irvine` from the archive. Save the `irvine` directory in `lowlevel_io_meancalc/lib`. 

### 4. Assemble the source code in to a object file
From directory `lowlevel_io_meancalc` run:

```
$ /masm32/bin/ml /Fo ./bin/main.obj /c /Zd /coff /I./lib/irvine ./src/main.asm
```

### 5. Run the linker to create the executable file 

```
$ \masm32\bin\Link /SUBSYSTEM:CONSOLE /OUT:./bin/main.exe /LIBPATH:./lib/irvine ./bin/main.obj
```



### 6. Run the program

From the `lowlevel_io_meancalc` directory, run:

```
$ ./bin/main.exe
```

Example interactive session:

```
Low-level I/O Procedures and Implementing Macros

Computer Architecture & Assembly Language Portfolio Project, March 2020


Please provide 10 signed decimal integers.
Each number needs to be small enough to fit inside a 32 bit register.
After you have finished inputting the raw numbers a list of the integers,
their sum, and their average value will be displayed.

Please enter a signed integer: 9
Please enter a signed integer: -84365
Please enter a signed integer: 4837623
Please enter a signed integer: -100000000
Please enter a signed integer: 2147483655
ERROR: You did not enter a signed number or your number was too big.
Please enter a signed integer: nine
ERROR: You did not enter a signed number or your number was too big.
Please enter a signed integer: 2587
Please enter a signed integer: -5642871
Please enter a signed integer: 4
Please enter a signed integer: -731946
Please enter a signed integer: 258
Please enter a signed integer: 456

You entered the following numbers:
9, -84365, 4837623, -100000000, 2587, -5642871, 4, -731946, 258, 456

The sum of these numbers is: -101618245

The rounded average (determined using floor division) is: -10161825
```
