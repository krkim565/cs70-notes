# Kimberley Rangel
## Week 5 Reading

## Strang Chapter 3 3.2-3.4
### Ch. 3.2 Cosines and Projections onto Lines
- Key Idea: Vectors with x^T(y)=0 are orthogonal (perpendicular)
  - The line connecting *b* to *p* (the dotted line in Fig 3.5) is perpendicular to *a*. The same logic extends to finding the *p* on a subspace
  ![Projection of b](/img/Week5_1.png)
  - The **least-squares solution to an overdetermined system** is finding the projection *p*
- Inner products and cosines
    - The cosine of the angle is directly related to inner products.
    ![Finding theta by using inner products](/img/Week5_2.png)
    ![Cosine of theta](/img/Week5_3.png)
    
- Projection onto a Line
    - The projection point *p* is the some multiple p = x_hat * a of a given vector *a* (every point on the line is a multiple of a).
    ![Projection onto a line](/img/Week5_4.png)
    ![Schwarz Inequality](/img/Week5_5.png)

- Projection Matrix of Rank 1
    - ![Projection Matrix](/img/Week5_5.png)
    - Properties:
        1. P is a symmetric matrix
        2. Its square is itself: P^2 = P
    - The column space consists of the line through a = (1;1;1).
    - The nullspace consists of the plane perpendicular to a.
    -  The rank is r = 1
    - Remark on scaling The projection matrix aa^T=a^Ta is the same if a is doubled
    - To project b onto a, multiply by the projection matrix P: p = Pb.
- Transposes from Inner Products
    - ![Transpose Property](/img/Week5_5.png)
    - (AB)^T = B^T(A^T)
    - (A^-1)^T = (A^T)^-1
### Ch. 3.2 Projections and Least Squares
- Key Idea: Given an inconsistent system Ax=b, we want to choose the x that minimizes an average error R in the 
m equations. 
- ![Sum of Squares](/img/Week5_6.png)
- The error vector e connecting *b* to *p* must be perpendicular to *a* 
- Least Squares Problems with Several Variables
    - Problem: Projecting *b* onto a subspace
    - The error is E = ||Ax - b||, and this is exactly the distance from b to the point Ax in the column space.
    - Searching for the least-squares solution bx, which minimizes E, is the same as locating the point p = Abx that is closer to b than any other point in the column space.
    - The equations A^TA(x_hat) = (A^T)b are known in statistics as the normal equations.
    ![Projection onto a plane](/img/Week5_7.png)
    ![Remark 4](/img/Week5_8.png)
    ![Remark 5](/img/Week5_9.png)
    ![Remark 6](/img/Week5_10.png)
- Cross-Product Matrix (A^T)A
    - (A^T)A has the same nullspace as A.
    - If A has independent columns, then A^TA is square, symmetric, and invertible.
- Projection Matrices
    ![Projection Matrix Rank>1](/img/Week5_11.png)
    - Properties:
    ![Projection properties](/img/Week5_12.png)
- Least-Squares Fitting of Data
- Weighted Least Squares
    ![Example Weighted](/img/Week5_13.png)
    - Now suppose the two observations are not trusted to the same degree. The value x = b1 may be obtained from a more accurate scale—or, in a statistical problem, from a larger sample—than x = b2.
    ![Weighted error](/img/Week5_14.png)

### Ch. 3.4 Orthogonal Bases and Gram-Schmidt
- Orthogonal Matrices
- Rectangular Matrices with Orthgonal Columns
- The Gram-Schmidt Process
- The Factorization A = QR
- Function Spaces and Fourier Series

## VMLS Chapter 12
- Least Squares Problem
    - The problem of finding an n-vector x_hat that minimizes ||Ax - b||^2, over all possible choices of x, is called the least squares problem. A and b are data given and x is what we want to find.
    - It is very important to understand that a least squares approximate solution x_hat of Ax = b need not satisfy the equations Ax_hat = b; it simply makes the norm of the residual as small as it can be.
    - Col View Ex given
    - Row View Ex given
- Solution
    - Deriving the solution of the least squares problem is done under the assumption that the columns of A are linearly independent.
    - Calculus Derivation shown
    - Normal equation! (A^T)A(x_hat) = A^T(b)
    - Gram matrix (A^T)A is invertible if the columns of A are linearly independent. Its invertibleness implies that x_hat is the only solution of the normal equations.
    - Psuedo-inverse of matrix A! (A^TA)^-1(A^T)
    - Thus, x_hat = A^+(b) and this formula shows us that the solution x_hat of the least squares problem is a linear function of b.
    - Direct verification of least squares solution (w/ out calculus)
    - Row form: The formula for the least squares approximate solution can be expressed in a useful form in terms of the rows a^T_i of the matrix A. In this formula we express the n X n Gram matrix A^TA as a sum of m outer products, and the n-vector A^T b as a sum of m n-vectors.
    ![Orthogonality Principle](/img/Week5_15.png)
- Solving Least Squares Problems
    - Using QR factorization to compute the least squares approximate solution (algorithm given)
    - Complexity of algo
    - Sparse least squares
    - Matrix least squares problem - extension of the least squares problem
        - Choose n x k matrix *X* to minimize ||AX-B||^2
        - Solution: *X_hat*  = A^+(B)
- Examples
    - Advertising purchases
    - Illumination

## VMLS Chapter 13
- Least Squares Data Fitting
- Regression
- Log transform of dependent variable
- 13.2 Validation
- 13.3 Feature engineering
- Transforming features
- Creating new features
- Advanced feature generation methods
    - Custom mappings
    - Predictions from other models
    - Distance to cluster representatives
    - Random features
    - Neural network features
- Summary
- House price prediction

