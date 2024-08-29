# Unitary transformations
We have previously gone through the definition of a unitary operator, as well as explored some of the properties of the eigenvalues and eigenstates of unitary operators.

Now we're going to go through what the action of a unitary operator on a state vector, or on another operator, actually is and what that means physically. Such an action is called a unitary transformation.

## Unitary transformations conserve the inner product
Say we have the two following unitary transformations:

$$
\begin{align}
    \hat{U}\ket{\psi} = \ket{\psi'},\\
    \hat{U}\ket{\phi} = \ket{\phi'}.
\end{align}
$$

Consider the inner product of $\ket{\psi'}$ and $\ket{\phi'}$:

$$
\begin{align}
    \braket{\psi' | \phi'} = \\
    \bigl(\bra{\psi}\hat{U}^\dagger\bigr) \bigl(\hat{U}\ket{\phi}\bigr) = \\
    \bra{\psi}\hat{U}^\dagger\hat{U}\ket{\phi} = \\
    \bra{\psi}\mathbb{I}\ket{\phi} = \\
    \braket{\psi | \phi}.
\end{align}
$$

So, the inner product of two state vectors will be the same before and after a unitary transformation. This is the most important property of unitary operators, and is a big reason as to why they are so frequently used in QM.

This also means that the norm, which is defined as the inner product of a state vector with itself, is conserved as well. So if we have a state vector and normalize it, and then let it be subject to a unitary transformation, it will still be normalized afterwards.

## Unitary transformations of operators
Consider a basis of $\mathcal{H}$, and a unitary transformation of that basis:

$$
\{\ket{u_n}\} \rightarrow \{\ket{u_n'} = \hat{U}\ket{u_n}\}.
$$

We say that an operator $\hat{A}'$ is a unitary transformation of another operator $\hat{A}$ if the matrix elements of $\hat{A}'$ with respect to the basis $\{\ket{u_n'}\}$ are the same as the matrix element of $\hat{A}$ with respect to the basis $\{\ket{u_n}\}$:

$$
\bra{u_n'}\hat{A}'\ket{u_m'} = \bra{u_n}\hat{A}\ket{u_m}.
$$

There is another way to write this which is more convenient. Consider the matrix element again:

$$
\begin{align}
    \bra{u_n'}\hat{A}'\ket{u_m'} = && \\
    \bra{u_n}\hat{U}^\dagger\hat{A}'\hat{U}\ket{u_m} \Rightarrow && \\
    \hat{A} = \hat{U}^\dagger\hat{A}'\hat{U} \Leftrightarrow && \tiny{\text{mult. with $\hat{U}$ from left, and $\hat{U}^\dagger$ from right}}\\
    \hat{U}\hat{A}\hat{U}^\dagger = \hat{U}\hat{U}^\dagger\hat{A}'\hat{U}\hat{U}^\dagger \Leftrightarrow && \\
    \hat{U}\hat{A}\hat{U}^\dagger = \mathbb{I}\hat{A}'\mathbb{I} \Leftrightarrow && \\
    \hat{U}\hat{A}\hat{U}^\dagger = \hat{A}'. &&
\end{align}
$$

So far, this seems very abstract, but remember that this has just been definition up to this point.

Now for some properties:

!!! info "Properties of unitary transformations of operators"
    For a unitary transformation $\hat{A}'$ of an operator $\hat{A}$, $\hat{A}' = \hat{U}\hat{A}\hat{U}^\dagger$, the following is true:

    **If $\hat{A}$ is Hermitian, then so is its unitary transformation**

    $$
    \hat{A}^\dagger = \hat{A} \Rightarrow (\hat{A}')^\dagger = \hat{A}'.
    $$

    ??? abstract "Proof"
        $$
        \begin{align}
            (\hat{A}')^\dagger = \\
            (\hat{U}\hat{A}\hat{U}^\dagger)^\dagger = \\
            (\hat{U}^\dagger)^\dagger\hat{A}^\dagger\hat{U}^\dagger = \\
            \hat{U}\hat{A}^\dagger\hat{U}^\dagger = \\
            \hat{U}\hat{A}\hat{U}^\dagger = \\
            \hat{A}'.
        \end{align}
        $$

        QED.
    
    **Unitary transformations conserve eigenvalues**

    The eigenvalue equation for $\hat{A}$ is given by:

    $$
    \hat{A}\ket{\lambda} = \lambda\ket{\lambda}.
    $$

    With $\ket{\lambda'} = \hat{U}\ket{\lambda}$, the eigenvalue equation for the unitary transformation $\hat{A}'$ is then:

    $$
    \hat{A}'\ket{\lambda'} = \lambda\ket{\lambda'}.
    $$

    In other words, the eigenvalues of the two operators are the same.

    ??? abstract "Proof"
        Consider the eigenvalue equation of $\hat{A}'$:

        $$
        \begin{align}
            \hat{A}'\ket{\lambda'} = \\
            \hat{U}\hat{A}\hat{U}^\dagger\ket{\lambda'} = \\
            \hat{U}\hat{A}\hat{U}^\dagger\hat{U}\ket{\lambda} = \\
            \hat{U}\hat{A}\mathbb{I}\ket{\lambda} = \\
            \hat{U}\hat{A}\ket{\lambda} = \\
            \hat{U}\bigl(\lambda\ket{\lambda}\bigl) = \\
            \lambda\hat{U}\ket{\lambda} = \\
            \lambda\ket{\lambda'}.
        \end{align}
        $$
    
        QED.

## Relationship with Hermitian operators
Unitary and Hermitian operators have a special relationship which can be described in the following way:

!!! info "Unitary and Hermitian operators"
    Let $\hat{A}$ be a Hermitian operator, i.e. $\hat{A}^\dagger = \hat{A}$. The following operator $\hat{T}$ is then **unitary**(1):
    { .annotate }

    1.    See [[1]](#prof-m-unitary) for proof.

    $$
    \hat{T} = e^{i\hat{A}}.
    $$

## References
<span id="prof-m-unitary">[1]</span> Professor M does Science, Cambridge, U.K. *Unitary operators in quantum mechanics*. (Apr. 21, 2021). Accessed: Aug. 29, 2024. [Online Video]. Available: [https://youtu.be/baIT6HaaYuQ?si=c5Gp4ayfjHkYfx2z](https://youtu.be/baIT6HaaYuQ?si=c5Gp4ayfjHkYfx2z).