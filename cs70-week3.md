# Kimberley Rangel
## Week 3 Reading

## Chapter 2
### 2.1 Linear functions
$$f : \mathbb{R}^n \rightarrow \mathbb{R}$$
- This notation means that $f$ is a function that maps realn $n$-vectors to real numbers.
In $f(x)$ $x$ is referred to the argument of the function and $(x)$ is the value of the function $f$
Ex: 
![Example f(x)](/img/Week3_1.png)
- The inner product function gives the inner product of its *n*-vector argument *x* with some (fixed) *n*-vector *a*. *f* can also be thought of as forming a weighted sum of the elements of *x*

- Superposition and linearity
    - Superposition property is defined as follows:
    ![Superposition](/img/Week3_2.png)
    - A function that satisifes the superposition property is called *linear*. (inner product is a linear function)
    - If a function f is linear, superposition extends to linear combinations of any number of vectors:
    ![Extension](/img/Week3_3.png)
    - The superposition equality can be broken down into two properties: 
    ![Two properties](/img/Week3_4.png)
    - If a function is linear, then it can be expressed as the inner product of its argument with some fixed vector.
    - The representation of a linear function f as $f(x) = a^T x$ is unique, which means that there is only one vector a for which $f(x) = a^T x $holds for all x.
    ![Examples](/img/Week3_5.png)

    - Affine functions:
        - A linear function plus a constant is called an affine function. A function $f:\mathbb{R}^n \rightarrow \mathbb{R} $ is affine if and only if it can be expressed as $f(x) = a^T x + b$ for some n-vector a and scalar b, which is sometimes called the offset.

        - For linear functions, superposition holds for any coeffcients $\alpha$ and $\beta$; for affine functions, it holds when the coeffcients sum to one (i.e., when the argument is an affine combination).
        - We find vectors x, y, and numbers alpha and beta with
        $\alpha + \beta = 1$, and verify that $f(\alpha x+\beta y) \neq \alpha f(x)+\beta f(y)$. This shows that f cannot be affine.
        - The converse is true: Any scalar-valued function that satisfies the restricted superposition property is affine. 
    - Civil engineering example showing real-life application of inner product use (predicting a measurement)
### 2.2 Taylor approximation
- "In many applications, scalar-valued functions of n variables, or relations between n variables and a scalar one, can be approximated as linear or affine functions. In these cases we sometimes refer to the linear or affine function relating the variables and the scalar variable as a model, to remind us that the relation is only an approximation, and not exact" (35).
    - The first-order Taylor approximation $\hat{f}(x)$ is a very good approximation of f(x) when all $x_i$ are near the associated $z_i$. So, $\hat{f}$ is an affine function of x
    - Example is given where $f: \mathbb{R}^2 \rightarrow \mathbb{R}$
### 2.3 Regression model
$$\hat{y} = x^T\beta + v$$ is an affine function called a regression model where beta is an n-vector and v is a scalar. 
- In this context, the entries of x are called the regressors, and ^y is called the prediction, since the regression model is typically an approximation or prediction of some true value y,which is called the dependent variable, outcome, or label.
- \beta and v are called the parameters in the model
- The entries in the weight vector have a simple interpretation: $\beta_i$ is the amount by which ^y increases (if $\beta_i$ > 0) when feature i increases by one (with all other features the same). If $\beta_i$ is small, the prediction ^y doesn't depend too strongly on feature i. The offset v is the value of ^y when all features have the value 0.
- Simplified regression model notation
- House price regression model

## Chapter 5
### 5.1 Linear dependence
- A collection of n-vectors are linearly dependent if we can form the zero vector as a linar combination of the n-vectors, with coefficients that are not all zero. Order doesn't matter when determining linear dependence
- When a collection of vectors is linearly dependent, at least one of the vectors can be expressed as a linear combination of the other vectors. The converse is true.
- A collection of n-vectors are linearly independent if the only linear combination of the vectors that equals the zero vector is the linear combination with all coefficients zero
- Examples of both are given
- A list of vectors is linearly independent if and only if for any linear
combination of them, we can infer or deduce the associated coecients.
- Supersets and subsets
### 5.2 Basis
- Independence-dimension inquality: If the n-vectors $a_1,...,a_k$$ are linearly independent, then k <= n.
- Any collection of n + 1 or more n-vectors is linearly dependent.
- **Definition of basis**: A collection of n linearly independent n-vectors (i.e., a collection of linearly
independent vectors of the maximum possible size) is called a basis.
- If the n-vectors $a_1,...,a_n$$ are a basis, then any n-vector b can be written as a linear combination
of them
- Any n-vector b can be written in a unique way as a linear combination of a basis  $a_1,...,a_n$$
- Expansion in a basis
- Examples
    - Cash flows and single period loans
- Proof of independence-dimension inequality
### 5.3 Orthonormal vectors

## Chapter 7
### 7.1 Geometric transformations
- Scaling
- Dilation
- Rotation
- Reflection
![Transformation Examples](/img/Week3_6.png)
- Projection onto a line
- Change of coordinates
    - In many applications multiple coordinate systems are used to describe locations or positions in 2-D or 3-D.
### 7.2 Selectors
![Define Selector matrices](/img/Week3_7.png)
Examples:
- Down-sampling
- Image cropping
- Permutation matrices
### 7.3 Incidence matrix
- Directed graph
A directed graph can also be described by its adjacency matrix (an n X m incidence matrix)
- Networks
    - Flow Conservation
    - Sources
    - Flow conservation with sources
    - Node potentials
    - Dirichlet energy
        - Definition: The sum of the squares of the potential dierences of v across all edges in the graph.
        - The Dirichlet energy is used as a measure the non-smoothness (roughness) of a set of node potentials on a graph. A set of node potentials with small Dirichlet energy can be thought of as smoothly varying across the graph. Conversely, a set of potentials with large Dirichlet energy can be thought of as non-smooth or rough.
    - Chain graph
### 7.4 Convolution
