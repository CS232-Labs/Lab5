# Intel Vtune Assignment

## Problem Statement

### Note (Constraints)
- Perform non-algorithmic optimisations i.e The provided flowchart must be followed
- Don't change code in areas marked appropriately by comments

### Part1

### Part2

#### Intro
- You are to optimise the provided [password cracking c code](link_to_code) which doesn't take any command line arguments. 
- You are also provided with a [Makefile](link_to_makefile), run the command below 
to generate the executable on which you'll perform analysis using Vtune. Note that you must not modify the Makefile.
```
make
``` 
- You're allowed to change value of the macro **ITER** in the c code (see the codeblock below) as you deem necessary for your analysis, when evaluating we will ensure a uniform value.
```
#define ITER 10000
```
- Output format
- What is supposed to increase?
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