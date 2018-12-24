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

## Matrix addition and subtraction

This can only be done if matrices are the exact same size. If they are, you can just do the operation with each cell from the first matrix and the corresponding one from the second.

## Matrix multiplication

### By a constant

Just multiply every element by a constant!

### By a matrix

To be able to multiply, the number of columns in the first matrix must equal to the number of rows in the second. The resulting matrix will have as many rows as the first matrix, and as many columns as the second.

Every column in the second matrix should be turned sideways and each element should be multiplied by the corresponding element in the row and added together to make the new element. This should happen for every row.

## $Ax$

Given matrix $A$ and vector $x$, $Ax$ is the linear combination, where each row of $x$ is multiplied by the corresponding column of $A$ and the resulting vectors are added together. 


### Homogenous equation

$Ax=0$ is the homogenous equation. It always has a trivial solution, which is $x=0$.

## Solving a system

First, put into RREF. Then, for every $x_n$, express it in terms of the other variables (remember to flip the sign of anything crossing the equals sign/augmentation line). Then, group together each $x_n$ and put into a vector, and you have your group of vectors!

## Solving a chemical equation

Make a matrix with one row for each element and one column for each element grouping. In each cell, write the number of times the given element occurs in the current grouping, remembering to negate anything on the other side of the equals sign. Augment the matrix with zero, and solve.

## Transformations

A $m * n$ matrix can define a transformation from $RR^n$ to $RR^m$. To perform the transformation, multiply the vector by the matrix and you have a resulting vector. This is called the image.


### Properties

- Linear the image scales with the initial vector
- Transformations of the sum of two vectors are the same as the sum of the transformations of the vectors alone
- transformations can be one-to-one if they are from $R^n$ to $R^m$ where $m >= n$. They can be onto if $m <= n$.

### Transposes

A matrix $A$ can be written as $A^T$ or $A'$ to flip it over its diagonal (so columns are now rows, and rows are now columns).

## Determinants

Determinants are defined only for square matrices. For a 2x2 matrix, the determinant for $[[a, b], [c, d]]$ is $ad -bc$. 

For bigger matrices, just make everything below (or above)the diagonal zero and multiply the diagonals together


### Properties

- multiplying a row or column by a constant multiplies the determinant by that constant
- if any two rows or columns are equal then the determinant is zero
- adding rows to each other, even when rows are multiplied by a constant before adding
- switching two rows or columns changes the sign
- $A^T$ has the same determinant as $A$
- the inverse matrix has a determinant that's the inverse of the original one
- the matrix raised to any power has its determinant raised to the same power
- the determinant of two multiplied matrices is equal to the product of the determinants


## Inverse matrix

**an identity matrix is a matrix with all ones on the left-to-right downwards diagonal and zeroes elsewhere**

To find the inverse matrix $A^-1$, just augment $A$ with the identity matrix of the same size and get the identity matrix on the other side of the augmentation line. An inverse matrix doesn't always exist.

## $PP$ subspaces

In order to be in a $PP^n$ subspace with an appropriate n, a polynomial function must
- contain the zero vector
- be able to represent any sum of its outputs as an output
- be able to represent a scalar multiplication of an output as an output

## Basis

The basis is a minimal set of vectors that will span a subspace. To find the basis of a row space, simply reduce the matrix to REF and make vectors from the remaining rows. If you need to find the basis of the column space of a matrix, simply flip the matrix and perform the above procedure.

**the dimension of a subspace is the number of vectors needed to form the basis**


### Coordinates

A vector in the span of a basis is said to another vector which is made up of the coordinates of the first vector in the basis. This coordinate vector is made up of the coefficients needed to multiply each vector in the basis by in order to get the vector that's in the span. To find the coordinates, simply put the basis together to make a matrix and then augment it with the vector you want to find coordinates of, and put into RREF. The values in the augmented part of the vector are the coordinates.

## Rank and Null Space

The rank of a matrix is the number of linearly independent columns. The nullity, or the dimension of the null space, is the number of columns minus the rank. To find the null space, just find vector x where $Ax = 0$.

## Eigenvectors and eigenvalues

To find the eigenvalues, the equation $det(A - \lambda I) = 0$ is used, where $I$ is the identity matrix (all 1s diagonally). The resulting equation may need to be solved quadratically or otherwise.

To find eigenvectors, simply solve for $(A - \lambda I)v = 0$.

## $W^⊥$

To calculate the perp (orthogonal complement) of a vector, just calculate the null space of its transform.


## Orthogonal projection

The orthogonal projection of $\vec u$ onto $\vec b$ is $\frac{(\vec u \circ \vec b)}{|| \vec b ||^2} * b$

**Othogonal means dot product is equal to zero**

## Gram Schmidt Process

basis {$x_1, x_2, ... x_p$}
{$v_1, v_2, ..., v_n$}

$v_1 = x_1$

$v_2 = x_2 - \frac{x_2 \circ v_1}{v_1 \circ v_1} v_1$

$v_3 = x_3  - \frac{x_2 \circ v_1}{v_1 \circ v_1} v_1 - \frac{x_2 \circ v_1}{v_1 \circ v_1} v_1$


## Least Squares Problem

$(A^T A)x = A^T b$

## Angle between two vectors

$\cos{\theta} = \frac{\vec u \cdot \vec v}{||\vec u|| \cdot ||\vec v||}$