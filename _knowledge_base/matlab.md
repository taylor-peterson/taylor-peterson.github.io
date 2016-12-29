---
title: MATLAB
---

HMC AE E59 MATLAB Tutorial v1.0, Fall 2012

The built in help (type help \<command\>, or doc \<command\> for even more information) is quite good, and you can also use the function browser to learn about new commands.

Basic Matlab Syntax and Commands

Entering a matrix

Matlab basically has one data type: complex-valued matrices. Real matrices, integer matrices, vectors and scalars are all treated as special cases. In this document only real and integer values are used for simplicity. To enter a matrix A, type

\>\> A = [1 2 3; 4 5 6; 7 8 9]

and Matlab will echo

A =

1 2 3

4 5 6

7 8 9

If you do not want to see the results of your commands echoed, type a semicolon afterwards:

\>\> A = [1 2 3; 4 5 6; 7 8 9];

Note that matrices are indicated by square brackets, elements are separated by spaces (or commas) and rows separated by semicolons. Elements of a matrix are specified using parentheses and can be assigned and manipulated individually. For example, an element of A can be changed by typing

\>\> A(3,1) = 10.6;

If the semicolon were left off of the line above, Matlab would echo the new version of the complete matrix.

An apostrophe is used to designate the transpose of a matrix. Thus

\>\> Aâ€™

now gives the output

ans =

1 4 10.6

2 5 8

3 6 9

Note that the matrix A remains unchanged, its transpose was simply reported. The output was given as ans since the command Aâ€™ is not an assignment. B = Aâ€™ would have assigned the above matrix to a variable B.

The apostrophe can also be used to enter a matrix, for example

\>\> C = [1 2 3]â€™

results in

C =

1

2

3

The colon is also useful for defining matrices. A colon indicates an increment with a default of 1, so that

\>\> D = [1:6]

produces

D =

1 2 3 4 5 6

But the increment does not have to be 1,

\>\> E = [12:-2:4]

results in

E =

12 10 8 6 4

A colon can also be used to designate certain rows or columns of a matrix. For example, using the matrix A above,

\>\> a = A(:, 2:3)

would produce the result

a =

2 3

5 6

8 9

which is all of the rows (indicated by the colon on its own before the comma) and the second through third columns of A.

Another row could be attached to a by typing

\>\> a = [a;[43 0]]

which gives

a =

2 3

5 6

8 9

43 0

Comments in MATLAB

%          comments a line of code (shortcut: ctrl + R)

Variables and expressions

Matlab is case-sensitive, so that A and a are different variables. To clear all variables that you have assigned type clear. Some variable names are already assigned, such as pi and Inf (infinity).

The elements of a matrix can be expressions, e.g.

\>\> F = [-1.4e2, sqrt(-3.4), (1+4)/3.]

Matrix operations

A careful distinction must be made between matrix operations and array operations.

The matrix operations are:

addition A+B         A and B must be the same size

subtraction Aâ€"B      A and B must be the same size

multiplication A\*B     the number of columns in A must equal the number of rows in B

power A^n         A is multiplied by A n times. A must be a square matrix.

left division A\B      solves Ax = B (see below)

If B is replaced by a scalar in the above matrix relations, the scalar is added, multiplied, etc. to each element in A.

The array operators include dots and have different meanings from the matrix operators:

multiplication A.\*B         each element in A is multiplied by corresponding element in B

power A.^B              each element in A is raised to the power of the corresponding element in B.

power with a scalar A.^n     each element of A is raised to the power n

division A./B             each element in A is divided by corresponding element in

Below is a list of some other mathematical operators that you may find useful. Each is followed by an argument in parentheses. Type help followed by the command name for details.

abs sign real imag exp log log10

cos sin tan acos asin atan atan2

More useful commands

This is only a partial list. Consult help for lots more.

det(X)     the determinant of square matrix X

eig(X)     a vector containing the eigenvalues of a square matrix X

rank(X)    the rank of matrix X

eye(n)     the n-n identity matrix

zeros(m,n) an m-n matrix of zeros

ones(m,n)  an m-n matrix of ones

inv(X)     the inverse of a square matrix X \*\*see note below\*\*

max(X)     the largest/smallest element in the vector X or, for matrices, a row

or min(X)  vector containing the largest/smallest element from each column of X

size(X)    returns the dimensions of matrix X

length(V)  returns the length of vector V

Basic plotting in Matlab

The basic two-dimensional, linear (as opposed to log) plot command is

plot(X,Y)

which plots vector Y versus vector X. Various line types, plot symbols and colors may be obtained with

plot(X,Y,S)

For the options for â€œSâ€ type help plot.

Other plot formatting commands that you may find useful are

figure     hold       grid       axis

title      xlabel     ylabel     subplot

semilogx   semilogy   loglog

figure(x)       % creates a new figure, â€œfigure x,â€ where x is an

% integer

subplot(m,n,x)  % creates a plot on a grid with m (row) x n (column)

% subplots. x refers to the x-th subplot, counting

% across then down

Pro Tips

1) atan vs. atan2

atan calculates the arctangent of a complex number defined between â€"p/2 to + p/2.

atan2 calculates the arctangent of a complex number for all 4 quadrantsâ€"by automatically unwrapping the phase angle. Very useful when plotting phase vs. frequency.

atan2(X,Y) % for the fraction X/Y, use atan2 in the form shown.

2) Clearing the command window, clearing the workspace, clearing figures

clc        % clears your command window so itâ€™s nice and white

clear all  % clears all variables in the workspace

clf        % clears the active figure

close all  % closes (and clears) all open figures

These clearing commands are useful to have on the very top of functions or scripts, unless, of course, your function/script requires the use of previously stored variables!

Reference:

Prof. Bassman and Prof. Yongâ€™s notes from E72 (Spring 2011)
