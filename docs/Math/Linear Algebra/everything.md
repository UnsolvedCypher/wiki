# Linear algebra super cheat-sheet

## Systems of equations

Assuming equations in form $ax + by = c$

Two equations are the same if an equation can be multiplied by a constant to get another (infinitely many solutions).

Two equations are parallel if a and b can be multiplied by a constant from one equation to the other, but c is different (no solutions).

Otherwise, the two equations intersect at one point (one solution).

**Consistent** means that there is at least one solution.

## Augmented Matrices

An augmented matrix uses a line to divide off the last number in each column. It means that for every item $i$ in a row, $i_0 + i_1 + ... + i_n = z$ where z is on the augmented side. Note that if you have a row full of zeroes that equals a non-zero value, no solutions exist.


## Matrix forms

REF (row echelon form): every row is either all zeroes or starts with a one, and the leading 1 of the row must be further right than in the above row. All rows completely of zeroes must be at the bottom.

RREF (reduced row echelon form): matrix must be in REF, but every row with a leading one must have zeroes everywhere else in the column.

**a leading one is called a pivot**

## Matrix operations

A matrix row can be scaled by a constant, or added to or subtracted from another row, and the augmented matrix still holds true. You can solve augmented matrices by putting them in RREF so each one corresponds to the solution for the variable.

## Free variables

Any variable that doesn't have its own pivot column is considered a free variable. 


## Span

A if there is a group of vectors $G$ and vector $W$ is in the span of this group, then $W$ can be found by multiplying each vector by a constant and then adding together. To find the constants to multiply by, make a matrix out of $G$ and augment with $W$, then solve.

**expressing a vector as other vectors multiplied by constants is called a linear combination**

## Linear dependence and independence and rank

The rank of a matrix is the number of linearly independent rows in the matrix, or linearly independent columns (this is the same thing). To see how many independent rows a matrix contains, simply put it into RREF and the number of non-zero columns is the number of linearly independent matrices.

## Matrix multiplication

To be able to multiply, the number of columns in the first matrix must equal to the number of rows in the second. The resulting matrix will have as many rows as the first matrix, and as many columns as the second.

Every column in the second matrix should be turned sideways and each element should be multiplied by the corresponding element in the row and added together to make the new element. This should happen for every row.

## $Ax$

Given matrix $A$ and vector $x$, $Ax$ is the linear combination, where each row of $x$ is multiplied by the corresponding column of $A$ and the resulting vectors are added together. 


### Homogenous equations

$Ax=0$ is the homogenous equation. It always has a trivial solution, which is $x=0$.

## Solving a system

First, put into RREF. Then, for every $x_n$, express it in terms of the other variables (remember to flip the sign of anything crossing the equals sign/augmentation line). Then, group together each $x_n$ and put into a vector, and you have your group of vectors!

## Solving a chemical equation

Make a matrix with one row for each element and one column for each element grouping. In each cell, write the number of times the given element occurs in the current grouping, remembering to negate anything on the other side of the equals sign. Augment the matrix with zero, and solve.

## Transformations

A $m * n$ matrix can define a transformation from $RR^n$ to $RR^m$. To perform the transformation, multiply the vector by the matrix and you have a resulting vector. This is called the image.

### Properties

Linear transformations 










































## Misc

Column space: the vectors that make up the columns of the vector

Row space: the vectors that make up the rows of a vector

Issues: 2.9