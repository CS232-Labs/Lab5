# Intel Vtune Assignment

## Problem Statement

### Note (Constraints)
- Perform non-algorithmic optimisations i.e The provided flowchart must be followed
- Don't change code in areas marked appropriately by comments

### Part1

### Part2

#### Intro
- You are givent the c code for a [password cracking](link_to_code) application which you are required to optimize.
#### Compilation
A [Makefile](link_to_makefile) is provided in the same folder with the required optimization flags you will be evaluated on. The following command can be used to compile the application generating the binary cracker.o
```
make
``` 
- The number of passwords that are tested can be configured via the compile time parameter ITER. This is provided in the code in the following manner:
```
#define ITER 10000
```
#### Running Instructions
No other parameters or arguments are required to run the password cracker. The command used to execute it is as follows:
```
./cracker.o
```
#### Output Format
```
= = = VTune profiling demo = = =
=================================
memory malloc		+OK
initializing from		built-in data
memory malloc		+OK
max iter		100000
===
try search... wait!
Password per sec:       250 
```
The beginning section of the output can be used to verify if the initialization process completes successfully along with the value of the parameter ITER. The application in addition prints the number of passwords cracker per second. Note that this value is empirical and is affected by system noise, value of ITER and the resolution of the clock in use.
#### Objective
You are expected to use the vtune tool to detect hotspots and remove them preserving the algorithm used. The number of passwords cracked per second will be used to determine the grade.

- Idea to reduce analysis jitter (for analysing your result when running on your terminal)

#### Flowchart

#### Report

#### Submission Format

#### Grading Scheme

#### Bonus
Can add threading to improve performance

## Resources
- [Installation and basic usage of Intel Vtune](https://github.com/CS232-Labs/Lab-5---Resources/tree/main/intel-vtune)
- Point to resources on some optimisations
