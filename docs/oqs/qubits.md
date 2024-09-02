# Qubits
Consider a Hilbert space with two dimensions. We'll call this space $\mathcal{H}_2$.

This space is called a *qubit*, *2-level system*, or *2-state system*

Since $\mathcal{H}_2$ has two dimensions, we need two basis vectors to describe it. We'll call the two basis vectors $\ket{0}$ and $\ket{1}$. So, we can now describe any state $\ket{\psi}$ of $\mathcal{H}_2$ in terms of the basis states:

$$
\ket{\psi} = \alpha\ket{0} + \beta\ket{1}.
$$

These basis states, $\ket{0}$ and $\ket{1}$, are commonly called the Up and Down states. However, there is no overwhelming consensus on which of the two is Up and which is Down, so to avoid confusion, physicists will sometimes use $\ket{\uparrow}$ and $\ket{\downarrow}$ instead.

In these notes, we'll stick to the $\ket{0}$-$\ket{1}$ notation, and use this definition(1):
{ .annotate }

1.    If you get confused over the order ("why does $\ket{0}$ have a 1 as its first element?"), just think of the basis vectors of any Euclidean space: the **first** basis vector is $[1, 0, 0, \dots]$, the **second** $[0, 1, 0, \dots]$, and so on, and then we're just using zero-indexing.

$$
\begin{align}
    &\ket{0} = \begin{bmatrix}1 \\ 0\end{bmatrix},\\
    &\ket{1} = \begin{bmatrix}0 \\ 1\end{bmatrix}.
\end{align}
$$

## The Pauli matrices
The Pauli matrices are a set of $2 \times 2$ matrices that have been found to be fundamental for 2-level systems.

There are three Pauli matrices, all denoted by the Greek letter $\sigma$(1):
{ .annotate }

1.    pronouced "sigma"

$$
\begin{align}
    \sigma_x =
    \begin{bmatrix}
        0 & 1\\
        1 & 0
    \end{bmatrix},\\
    \sigma_y =
    \begin{bmatrix}
        0 & -i\\
        i & 0
    \end{bmatrix},\\
    \sigma_y =
    \begin{bmatrix}
        1 & 0\\
        0 & -1
    \end{bmatrix}.
\end{align}
$$

Sometimes, people will use $\{1, 2, 3\}$ as subindices instead of $\{x, y, z\}$, so that $\sigma_x = \sigma_1$, $\sigma_y = \sigma_2$, and $\sigma_z = \sigma_3$.

!!! info "Properties of the Pauli matrices"
    The Pauli matrices $\sigma_k$ where $k \in \{x, y, z\}$ obey the following properties:

    1. **Hermiticity:** $\sigma_k = (\sigma_k)^\dagger$;
    2. **Involutarity:** $\sigma_k = (\sigma_k)^{-1}$;
    3. $\text{det}(\sigma_k) = -1$;
    4. **Tracelessness:** $\text{tr}(\sigma_k) = 0$.
    
    The first two properties imply that the Pauli matrices are **unitary**: $(\sigma_k)^\dagger = (\sigma_k)^{-1}$.

All Pauli matrices have the same two eigenvalues each, positive and negative one, but they have different eigenvectors associated with their eigenvalues:

$$
\begin{align}
    \sigma_x&: &&
    \lambda_1 = +1, \ket{\lambda_1} = \frac{1}{\sqrt{2}}\begin{bmatrix} 1 \\ 1 \end{bmatrix}, &&
    \lambda_2 = -1, \ket{\lambda_2} = \frac{1}{\sqrt{2}}\begin{bmatrix} 1 \\ -1 \end{bmatrix}.\\
    \sigma_y&: &&
    \lambda_1 = +1, \ket{\lambda_1} = \frac{1}{\sqrt{2}}\begin{bmatrix} 1 \\ i \end{bmatrix}, &&
    \lambda_2 = -1, \ket{\lambda_2} = \frac{1}{\sqrt{2}}\begin{bmatrix} 1 \\ -i \end{bmatrix}.\\
    \sigma_z&: &&
    \lambda_1 = +1, \ket{\lambda_1} = \begin{bmatrix} 1 \\ 0 \end{bmatrix}, &&
    \lambda_2 = -1, \ket{\lambda_2} = \begin{bmatrix} 0 \\ 1 \end{bmatrix}.\\
\end{align}
$$

Now, why are the Pauli matrices so important? Well, **we can write all $2 \times 2$ operators in terms of the Pauli matrices and the identity matrix**. In other words, the Pauli matrices together with the identity matrix form a basis for the space of $2 \times 2$ operators.

In QM, we are generally only interested in the subset of operators that are Hermitian, since those have real eigenvalues and can therefore correspond to measurable, physical quantities. As you should know by now, we call those operators observables.

So now that we have a formula for all $2 \times 2$ operators, we can investigate what subset of these are Hermitian in order to find out the set of observables.

Assuming a $2 \times 2$ Hermitian operator $\hat{A}$, we have:

$$
\begin{align}
    &\hat{A} = \hat{A}^\dagger\\
    &\Leftrightarrow\\
    &\begin{bmatrix}
        A_{11} & A_{12}\\
        A_{21} & A_{22}\\
    \end{bmatrix} =
    \begin{bmatrix}
        A_{11} & A_{12}\\
        A_{21} & A_{22}\\
    \end{bmatrix}^\dagger\\
    &\Leftrightarrow\\
    &\begin{bmatrix}
        A_{11} & A_{12}\\
        A_{21} & A_{22}\\
    \end{bmatrix} =
    \begin{bmatrix}
        A_{11}^* & A_{21}^*\\
        A_{12}^* & A_{22}^*\\
    \end{bmatrix}\\
    &\Rightarrow\\
    &\begin{cases}
        A_{11} = A_{11}^* \\
        A_{12} = A_{21}^* \\
        A_{21} = A_{12}^* \\
        A_{22} = A_{22}^*
    \end{cases}\\
    &\Rightarrow\\
    &\begin{cases}
        A_{11}, A_{22} \in \mathbb{R} \\
        A_{12} = A_{21}^*
    \end{cases}
\end{align}
$$

From this, we can conclude that all $2 \times 2$ observables will have real numbers along the main diagonal, and the off-diagonal elements will be the complex conjugate of each other.