# Kimberley Rangel
## Week 2 Reading

I'm really glad we read the VMLS textbook first because otherwise this chapter would have been harder to follow.

### Chapter 1.1
- Key Terms:
    - Elimination
    - Back-substitution
    - **Determinants** Not sure if I understand what this means, but can be used to solve linear system
    ![Ratio of Determinants](/img/Week2_1.png)
    - *Gaussian Elimination*:
        - Solves large systems of equations
        - It is faster than using the determinant formula
    - Variables to keep in mind for the rest of the Ch:
        - The coefficient matrix A, the matrices E for elimination and P for row exchanges, and the final factors L and U
- Main Ideas Covered in Ch 1:
    1. Linear equations lead to *geometry of planes*
    2. Matrix notation
    3. In exceptional cases elimination will *break down*. Singular case has no solution. Other singular cases have infinitely many solutions.
    4. We need a rough count of the **number of eliminaiton steps** required to solve a system of size *n*. Computing cost often determines the accuracy in the model.

### Chapter 1.2 - Geometry of Linear Equations
- Linear systems can be looked at by rows or by columns:
    ![Linear system](/img/Week2_4.png)
    - Row pic: Intersection of planes
    ![Row pic](/img/Week2_2.png)
    - Col pic: Combination of columns
    ![Col pic](/img/Week2_3.png)
- Every point in 3D space is matched to a vector, and vice versa (Descartes).
- Equations in the linear system ask for a **linear combination of the *n* columns that equals b**
- The singular case:
    - Equations can be inconsistent, meaning that $$l \neq r$$, so no solution
    - Equations can have an infinity of solutions
- Visualizations of singular cases both in row and column pictures:
![Row](/img/Week2_5.png)
![Column](/img/Week2_6.png)
Note: If the n planes have no point in common, or infinitely many points, then the n columns lie in the same plane.
### Chapter 1.3 - Example of Gaussian Elimination
![Step 1](/img/Week2_7.png)
![Step 2](/img/Week2_8.png)
![Step 3](/img/Week2_9.png)
- Forward elimination produced the pivots 2, -8, 1. It subtracted multiples of each row from the rows beneath, It reached the “triangular” system (3), which is solved in reverse order: Substitute each newly computed value into the equations that
are waiting.
- If a zero appears in a pivot position, elimination has to stop—either temporarily or permanently. The system might or might not be singular.
- Roughly speaking, we do not know whether a zero will appear until we try going through the elimination process
- The cost of elimination (left side):
$$ \frac{1}{3}(n^3 - n) $$
If n is large, a good estimate for the # of operations is
$$ \frac{1}{3}n^3$$
- The cost of elimination (right side):
$$n^2$$
### Chapter 1.4 - Matrix Notation and Matrix Multiplication
- Multiplication of a Matrix and a Vector:
![Linear System](/img/Week2_10.png)
![Matrix Representation](/img/Week2_11.png)
![By Row](/img/Week2_12.png)
![By Col](/img/Week2_13.png)
    - Every product Ax can be found using whole columns as in equation (5). Therefore Ax is a combination of the columns of A. The coefficients are the components of x.
- Matrix Form of One Elimination Step:
    First step of the system we have in the first image was: 2 times the first component of b was subtracted from the second component.
     ![Right-side](/img/Week2_18.png)
     - Need to review this because I don't quite get it:
     ![Right-side](/img/Week2_19.png)

### Chapter 1.5 - Triangular Factors and Row Exchanges
- One Linear System = Two Triangular Systems
    - Steps of good elimination code
    1. Factor (from A find its factors L and U).
    2. Solve (from L and U and b find the solution x).

- Row Exchanges and Permutation Matrices
    We can use permuation matrix to exchange a row
    - Ex of 3 by 3 permutations
    ![Permuations](/img/Week2_20.png)
- Elimination in a Nutshell: PA = LU
    - "In the nonsingular case, there is a permutation matrix P that reorders the rows of A to avoid zeros in the pivot positions. Then Ax = b has a unique solution and with the rows reordered in advance, PA can be factored into LU" (Strang 43)
### Chapter 1.6 - Inverses and Transposes
- Inverse:
![Inverse](/img/Week2_14.png)
- Had a little trouble following Gauss-Jordan Method
- Tranpose Matrix
![Tranpose](/img/Week2_15.png)
    - Essential formulas:
    ![Formulas](/img/Week2_16.png)
    Examples:
    ![Examples](/img/Week2_17.png)
- Symmetric Matrices

### Chapter 1.7 - Special Matrices and Applications