# Intel Vtune Assignment

## Problem Statement

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
#### Constraints
- You are not allowed to use the c library functions strlen and memcmp are needed to implement a custom optimized version of the same.
- Do not modify the decryption scheme as well as the representation used to hold the required keys and password. In addition you are not expected to modify the order in which passwords or generated as well as the keys held. i.e, the value of any global data structure must be preserved at the end of execution.
- Do not modify any line of code following the marker `// DO NOT MODIFY ANY CODE BELOW`
- Note that any optimizations not following the flowchart will be directly awarded 0.

#### Flowchart

#### Report
- Submit a screenshot of the final output obtained along with the series of optimizations performed and the intuition/reason behind them in the report. You will have to defend every optimization performed.
- Pro Tip: Always try to optimize the common case and the largest hotspot first.

#### Bonus
Improving the password cracker by performing threading without changing the order of passwords being tested would be awarded a bonus score.

## Resources
- [Installation and basic usage of Intel Vtune](https://github.com/CS232-Labs/Lab-5---Resources/tree/main/intel-vtune)
- [Stable benchmarking of binaries in modern machines](https://easyperf.net/blog/2019/08/02/Perf-measurement-environment-on-Linux)
