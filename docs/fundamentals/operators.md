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

## Hermitian operators

!!! info "Observables = Hermitian operators"
    In QM, all operators are observables &mdash; they are measurable properties of physical systems. In order for this to be true, the operators we deal with are all **equal to their own adjoints**:

    $$
    \hat{A} = \hat{A}^\dagger.
    $$

    An operator that obeys this property is called a **Hermitian operator**.

Observables are represented by Hermitian operators because all Hermitian operators have **real eigenvalues**. Furthermore, Hermitian operators have **orthogonal eigenstates**, which we can normalize, letting us use them to form an **orthonormal basis for the state space**.

??? abstract "Proof: Hermitian operators have real eigenvalues"
    Let $\hat{A}$ be a Hermitian operator. The eigenvalue equation gives

    $$
    \begin{align}
        \hat{A}\ket{\lambda} = \lambda\ket{\lambda} \Leftrightarrow && \tiny{\text{[multiply with $\bra{\lambda}$ from left]}}\\
        \bra{\lambda}\hat{A}\ket{\lambda} = \lambda\braket{\lambda | \lambda}. && 
    \end{align}
    $$

    The corresponding bra to $\lambda\ket{\lambda}$ is $\lambda^*\bra{\lambda}$, and the corresponding bra to $\hat{A}\ket{\lambda}$ is $\bra{\lambda}\hat{A}^\dagger$. The eigenvalue equation $\hat{A}\ket{\lambda} = \lambda\ket{\lambda}$ can thus be written as $\bra{\lambda}\hat{A}^\dagger = \lambda^*\bra{\lambda}$
    
    Given that $\hat{A}$ is Hermitian, $\hat{A} = \hat{A}^\dagger$, we get:

    $$
    \begin{align}
        \bra{\lambda}\hat{A}\ket{\lambda} = \lambda\braket{\lambda | \lambda} \Leftrightarrow && \\
        \bra{\lambda}\hat{A}^\dagger\ket{\lambda} = \lambda\braket{\lambda | \lambda} \Leftrightarrow && \\
        \lambda^*\braket{\lambda | \lambda} = \lambda\braket{\lambda | \lambda} \Rightarrow && \tiny{\text{[from eigenvalue eq., bra version]}}\\
        \lambda^* = \lambda. && \tiny{\text{[assuming $\ket{\lambda} \neq \ket{\text{null}}$]}}\\
    \end{align}
    $$

    There is only one way for a complex number $c \in \mathbb{C}$ to be equal to its own complex conjugate: it cannot have an imaginary component, so it is real. QED.

??? abstract "Proof: Hermitian operators have eigenstates that form an orthonormal basis for $\mathcal{H}$"
    Say we have an operator $\hat{A}$ with two different eigenvalues $\lambda$ and $\mu$ and their associated eigenvectors $\ket{\lambda}$ and $\ket{\mu}$ like so:

    $$
    \begin{align}
        \hat{A}\ket{\lambda} = \lambda\ket{\lambda},\tag{1}\\
        \hat{A}\ket{\mu} = \mu\ket{\mu}\tag{2}.
    \end{align}
    $$

    We modify equation (1) to get:

    $$
    \begin{align}
        \hat{A}\ket{\lambda} = \lambda\ket{\lambda} \Leftrightarrow && \tiny{\text{multiply with $\bra{\mu}$ from left}}\\
        \bra{\mu}\hat{A}\ket{\lambda} = \lambda\braket{\mu | \lambda}. &&
    \end{align}
    $$

    We now modify equation (2) to get:

    $$
    \begin{align}
        \hat{A}\ket{\mu} = \mu\ket{\mu} \Leftrightarrow && \tiny{\text{rewrite to dual space}}\\
        \bra{\mu}\hat{A}^\dagger = \mu^*\bra{\mu} \Leftrightarrow && \tiny{\text{$\hat{A}$ is Hermitian and $\mu$ is real}}\\
        \bra{\mu}\hat{A} = \mu\bra{\mu} \Leftrightarrow && \tiny{\text{multiply with $\ket{\lambda}$ from right}}\\
        \bra{\mu}\hat{A}\ket{\lambda} = \mu\braket{\mu | \lambda}. &&
    \end{align}
    $$

    Since the left-hand sides of both equations are equal, we can equate the right-hand sides to get:

    $$
    \begin{align}
        \lambda\braket{\mu | \lambda} = \mu\braket{\mu | \lambda} \Leftrightarrow && \\
        \lambda\braket{\mu | \lambda} - \mu\braket{\mu | \lambda} = 0 \Leftrightarrow && \\
        \braket{\mu | \lambda}(\lambda - \mu) = 0.
    \end{align}
    $$

    Since $\lambda \neq \mu$, the only way this can be true is if $\braket{\mu | \lambda} = 0$, which means that $\ket{\lambda}$ and $\ket{\mu}$ are orthogonal. QED.

## Compatibility of observables
Two observables

!!! info "Compatible operators"
    Two operators $\hat{A}$ and $\hat{B}$ are compatible if they commute:

    $$
    \hat{A}\hat{B} = \hat{B}\hat{A}.
    $$

## Unitary operators

!!! info "Unitary operators"
    Another important subset of operators are the **unitary operators**. An operator is unitary if **its inverse is equal to its adjoint**:

    $$
    \hat{A}^{-1} = \hat{A}^\dagger.
    $$