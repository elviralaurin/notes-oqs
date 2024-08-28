# Operators
Physical, measurable quantities such as energy, position, and momentum are called **observables** and are represented by **operators**, which in QM are **complex square matrices**.

These quantities correspond to properties of **quantum systems**, such as atoms or subatomic particles.

!!! note "Common operators"
    Some common operators are the position operator $\hat{x}$, the momentum operator $\hat{p}$, and the energy operator $\hat{H}$. The energy operator $\hat{H}$ is called the **Hamiltonian**, and corresponds to the total energy of the given system.

A physical quantity $\mathcal{A}$ is described by an operator $\hat{A}$, which **acts on state vectors to produce another state vector**:

$$
\hat{A}\ket{\psi} = \ket{\psi'}.
$$

!!! info "Operators in QM are linear"
    In QM, all operators are linear. Therefore, they distribute over superpositions just as you'd expect:

    $$
    \hat{A}\Bigl(a\ket{\psi} + b\ket{\phi}\Bigr) = a\hat{A}\ket{\psi} + b\hat{A}\ket{\phi}
    $$

!!! info "Operator addition"
    Addition of operators is:

    - associative: $\hat{A} + (\hat{B} + \hat{C}) = (\hat{A} + \hat{B}) + \hat{C}$, and
    - commutative: $\hat{A} + \hat{B} = \hat{B} + \hat{A}$.

!!! info "Operator multiplication"
    Multiplication of operators is defined through the way operators act on kets:

    $$
    (\hat{A}\hat{B})\ket{\psi} = \hat{A}\bigl(\hat{B}\ket{\psi}\bigr) = \hat{A}\ket{\psi'},
    $$

    if $\hat{B}\ket{\psi} = \ket{\psi'}$.

    Multiplication of operators is:

    - associative: $\hat{A}(\hat{B}\hat{C}) = (\hat{A}\hat{B})\hat{C}$, but
    - **NOT** necessarily commutative: $\hat{A}\hat{B} \neq \hat{B}\hat{A}$.

## Matrix elements
Let $\hat{A}\ket{\phi} = \ket{\phi'}$. If we take the inner product of a ket $\ket{\psi}$ with $\ket{\phi'}$, we end up with a structure that looks like the following:

$$
\braket{\psi | \phi'} = \bra{\psi} \bigl(\hat{A}\ket{\phi}\bigr).
$$

Since the result of the inner product of two kets in general is a scalar $c \in \mathbb{C}$, the above must of course also result in a scalar $c \in \mathbb{C}$.

The expression $\bra{\psi} \bigl(\hat{A}\ket{\phi}\bigr)$ is by definition equivalent to $\bigl(\bra{\psi}\hat{A}\bigr)\ket{\phi}$ &mdash; i.e. we can interpret it as either the operator $\hat{A}$ acting on the ket $\ket{\psi}$, or as $\hat{A}$ acting on the bra $\bra{\phi}$.

!!! info "Matrix element"
    The following two expressions are equivalent:
    
    $$
    \bra{\psi} \bigl(\hat{A}\ket{\phi}\bigr) \Leftrightarrow \bigl(\bra{\psi}\hat{A}\bigr)\ket{\phi}.
    $$

    This structure is called a **matrix element** and is usually written without parentheses, as $\bra{\psi}\hat{A}\ket{\phi}$. Specifically, we would call this example the matrix element of the operator $\hat{A}$ with respect to $\ket{\psi}$ and $\ket{\phi}$.

!!! info "Adjoint operator"
    Let $\ket{\psi'} = \hat{A}\ket{\psi}$ be a ket in state space $\mathcal{H}$. Then, $\bra{\psi'} = \bra{\psi}\hat{A}^\dagger$ is the corresponding bra in dual space $\mathcal{H}^*$.
    
    $\hat{A}^\dagger$ is called the **adjoint operator**, and it is defined by taking the transpose of original operator and then taking the complex conjugate of each of its elements.
    
    Just like other operators in QM, the adjoint operator is **linear**. With $\bra{\psi} = a_1\bra{\psi_1} + a_2\bra{\psi_2}$, we can distribute $\hat{A}^\dagger$ to the left onto bras within parentheses like so:

    $$
    \bra{\psi}\hat{A}^\dagger = \bigl(a_1\bra{\psi_1} + a_2\bra{\psi_2}\bigr)\hat{A}^\dagger = a_1\bra{\psi_1}\hat{A}^\dagger + a_2\bra{\psi_2}\hat{A}^\dagger
    $$

    Finally, the adjoint works on the product of two operators as follows:

    $$
    (\hat{A}\hat{B})^\dagger = \hat{B}^\dagger\hat{A}^\dagger.
    $$

## Hermitian operators

!!! info "Observables = Hermitian operators"
    In QM, all operators are observables &mdash; they are measurable properties of physical systems. In order for this to be true, the operators we deal with are all **equal to their own adjoints**:

    $$
    \hat{A} = \hat{A}^\dagger.
    $$

    An operator that obeys this property is called a **Hermitian operator**.

## Compatibility of observables
!!! info "Commutator"
    We define the **commutator** $[\hat{A}, \hat{B}]$ of two operators $\hat{A}$ and $\hat{B}$ as:

    $$
    [\hat{A}, \hat{B}] = \hat{A}\hat{B} - \hat{B}\hat{A}.
    $$

We say that two observables $\mathcal{A}$ and $\mathcal{B}$ are **compatible** if the corresponding operators $\hat{A}$ and $\hat{B}$ commute.

!!! info "Compatible operators"
    Two operators $\hat{A}$ and $\hat{B}$ are compatible if they commute:

    $$
    \hat{A}\hat{B} = \hat{B}\hat{A}.
    $$

    We can express this in terms of the commutator $[\hat{A}, \hat{B}]$ as:

    $$
    [\hat{A}, \hat{B}] = 0.
    $$

If we have two observables $\hat{A}$ and $\hat{B}$ that commute, $[\hat{A}, \hat{B}] = 0$, a key feature is that it is always possible to find a common set of eigenstates of $\hat{A}$ and $\hat{B}$ that form a basis in state space(1).
{ .annotate }

1.    See [[1]](#prof-m-compatible) for proof.

## Unitary operators
Another very important subset of operators are the **unitary operators**.

!!! info "Unitary operators"
    An operator $\hat{U}$ is unitary if **its inverse is equal to its adjoint**:

    $$
    \begin{align}
        \hat{U}^{-1} = \hat{U}^\dagger \Leftrightarrow\\
        \hat{U}^\dagger\hat{U} = \hat{U}\hat{U}^\dagger = \mathbb{I}.
    \end{align}
    $$

The product of two unitary operators $\hat{U}$ and $\hat{V}$ is also unitary.

## References
<span id="prof-m-compatible">[1]</span> Professor M does Science, Cambridge, U.K. *Compatible observables in quantum mechanics*. (Jul. 15, 2020). Accessed: Aug. 27, 2024. [Online Video]. Available: [https://youtu.be/IhJvX4H7xkA?si=gPwXJTg3_RRvY945](https://youtu.be/IhJvX4H7xkA?si=gPwXJTg3_RRvY945).