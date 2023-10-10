# Variation of Parameters Example

$$
\vec{y}(x) = \Psi(x) \Psi^{-1}(x_0)\vec{y_0} + \Psi(x)\int_{x_0}^x \Psi^{-1}(s)\vec{g}(x)ds
$$

As confusing as this formula looks its actually pretty straightforward. For example take this:
$$
A= \begin{bmatrix} 2 & 1 \\ 0 & 4 \end{bmatrix}\\
f= \begin{bmatrix} e^x \\ e^{3x} \end{bmatrix}\\
$$
The complementary solution is very normal and should be the exact same formula as complementary & particular below:
$$
C_1 e^{\lambda_1x} \begin{bmatrix} \vec{V_1} \end{bmatrix} + C_2 e^{\lambda_2 x} \begin{bmatrix} \vec{V_2} \end{bmatrix}
$$


The particular solution is the stuff on the other end of the addition sign. In this example 
$$
\Psi(x)\int_{x_0}^x \Psi^{-1}(s)\vec{g}(x)ds = \begin{bmatrix} e^{2x} & e^{4x} \\ 0 & 2e^{4x} \end{bmatrix}\int\begin{bmatrix} e^{2x} & e^{4x} \\ 0 & 2e^{4x} \end{bmatrix}^{-1} \begin{bmatrix} e^x \\ e^{3x} \end{bmatrix} ds = \begin{bmatrix} -e^x-3e^x \\ -e^{3x} \end{bmatrix}
$$
Then you just add them to the solution:
$$
\vec{y}(x) = C_1 e^{2x}\begin{bmatrix} 1 \\ 0 \end{bmatrix} + C_2 e^{4x} + \begin{bmatrix} 1 \\ 2 \end{bmatrix} +\begin{bmatrix} -e^x-3e^x \\ -e^{3x} \end{bmatrix}
$$

# Complementary & Particular Solutions Example

Complementary & Particular solutions are reasonably straightforward to find - consisting of just finding the eigenpair and then solving a simple system:

1. Take this example $\frac{d}{dx} \vec{y} = \begin{bmatrix} 2 &4\\ 4 & 2 \end{bmatrix}\vec{y} - \begin{bmatrix} 26\\22 \end{bmatrix}$
2. Find a solution that looks like $C_1 e^{\lambda_1x} \begin{bmatrix} \vec{V_1} \end{bmatrix} + C_2 e^{\lambda_2 x} \begin{bmatrix} \vec{V_2} \end{bmatrix}$ by paying attention to only the first $2\times 2$ matrix. This just means finding the eigenvalues and then eigenvectors & then plugging them into the formula above.
3. Find the particular by setting the $2 \times 2 = 0$ and add in the given particular section:
   1. $\begin{bmatrix} 0\\0 \end{bmatrix} = \begin{bmatrix} 2 &4\\ 4 & 2 \end{bmatrix}\begin{bmatrix} a_1\\a_2 \end{bmatrix} - \begin{bmatrix} 26\\22 \end{bmatrix}$
   2. This solves to $a_1 = 3$ and $a_2 = 5$.
4. Then just add that back to the original and and plug everything in:
   1. $y(x) = C_1 e^{\lambda_1x} \begin{bmatrix} \vec{V_1} \end{bmatrix} + C_2 e^{\lambda_2 x} \begin{bmatrix} \vec{V_2} \end{bmatrix} + \begin{bmatrix} 3\\5 \end{bmatrix}$
   2. Solution: $y(x) = C_1 e^{6x} \begin{bmatrix} 1\\1 \end{bmatrix} + C_2 e^{-2 x} \begin{bmatrix} -1\\1 \end{bmatrix} + \begin{bmatrix} 3\\5 \end{bmatrix}$

# An Imaginary Root Gives Two Real-Valued Solutions

Take eigenvalue $\lambda_2 = 2+3i$ with an eigenvector $\begin{bmatrix} -5+3i \\ 3+3i\\ 2 \end{bmatrix}$.

The eigenvalue can be turned into $e^{(2+3i)x}$ which can be decomposed into $e^{2x}e^{3ix}$ which using Euler's formula can be turned into $e^{2x}(\cos(3x)+i\sin(3x))$. You then can foil the decomposed eigenvalue with the the values in the eigenvector. I will show the first one as an example:
$$
e^{2x}(-5\cos(3x)+3i\cos(3x)-5i\sin(3x)-3\sin(3x))\\
e^{2x}(-5\cos(3x)-3\sin(3x))+ie^{2x}(3\cos(3x)-5\sin(3x))
$$
Or as the top row of the vector:
$$
\begin{bmatrix} e^{2x}(-5\cos(3x)-3\sin(3x)) & ie^{2x}(3\cos(3x)-5\sin(3x)) \end{bmatrix}
$$
If the eigenvalues are purely imaginary there might be no $e^x$ terms.

# Stability

Suppose *P* is a real invertible $2\times 2$ matrix. Then $\frac{d}{dx} \vec{y} = P\vec{y}$ has a unique equilibrium point $\vec{y}e = \vec{0}$ which is:

1. Asymptotically stable if all the eigenvalues of *P* have negative real parts
2. Non-asymptotically stable if the eigenvalues of *P*. Are purely imaginary
3. Unstable if at least one of the eigenvalues has positive real part

# Defective Matrix

1. This is a $2\times 2$ matrix example. First solve for the eigenvalues - if you get only one eigenvalue with algebraic multiplicity 2
2. Find the corresponding eigenvector
3. Solve this: $\begin{bmatrix} a_1-\lambda & b_1\\ a_2 & b_2-\lambda\end{bmatrix} =  \begin{bmatrix} \text{The eigenvector it corresponds to} \end{bmatrix}$
4. Lets call the solution to that $\vec{c}$
5. Then the general solution is $\vec{y}(x) = C_1 e^{\lambda x}  \begin{bmatrix} \vec{\text{Original Eigenvector}} \end{bmatrix} + C_2(xe^{\lambda x} \begin{bmatrix} \vec{\text{Original Eigenvector}} \end{bmatrix} + e^{\lambda x} \begin{bmatrix} \vec{c} \end{bmatrix})$

# Linearization

Very simple: Just the Jacobian matrix $\times$ some linearization factor:
$$
\text{For} \begin{bmatrix} xy+x-y^2-y\\xy-4x+2y-8\end{bmatrix} \ \ J(x,y) = \begin{bmatrix} y+1 & x-2y-1\\ y-4 & x+2\end{bmatrix}\\
\\
\text{At (-2,-1): } \frac{d}{dt}\begin{bmatrix} x+2\\x+1 \end{bmatrix}=\begin{bmatrix} 0 & -1\\-5 & 0 \end{bmatrix}\begin{bmatrix} x+2\\y+1 \end{bmatrix}
$$
