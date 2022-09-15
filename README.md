# LinearSystemSolver

## Summary
This project takes an input file that contains the data of a valid linear system and outputs a file displaying the results of that system.

## Input
The program accepts a .lin file in the following format:

3        <-- The system Size <br />
3 4 3    <-- Coefficients of first equation <br />
1 5 -1   <-- Coefficients of second equation <br />
6 3 7    <-- Coefficients of third equation <br />
10 7 15  <-- Answers to each equation in respective order <br />

This input can be visualized as follows:

3x + 4y + 3z = 10 <br />
x + 5y - z = 7 <br />
6x + 3y + 7z = 15 <br />

## Command Line
This program takes a minimum of one command line argument, being the name of the input file. Doing so solves the linear system by its default method, which is the Naive Gaussian Method.

ex: ./LinearSystemSolver.exe SampleInput.lin

Alternatively, the program accepts the --spp tag before the file name to indicate that the program should solve the linear system using Scaled Partial Pivoting.

ex: ./LinearSystemSolver.exe --spp SampleInput.lin

## Output
After it is finished inputing the data and calculating the answers, the program will output a file by the same name of the input file with the .sol type. The value of each variable will be given in respective order that they were taken. Using the example above, the default expected output file will look as follows:

2 1 0

This output can be visualized as follows:

x = 2
y = 1
z = 0
