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

Since the result of the inner product of two kets in general is a scalar $c \in \mathbb{C}\$, the above must of course also result in a scalar $c \in \mathbb{C}$.

The expression $\bra{\psi} \bigl(\hat{A}\ket{\phi}\bigr)$ is by definition equivalent to $\bigl(\bra{\psi}\hat{A}\bigr)\ket{\phi}$ &mdash; i.e. we can interpret it as either the operator $\hat{A}$ acting on the ket $\ket{\psi}$, or as $\hat{A}$ acting on the bra $\bra{\phi}$.

!!! info "Matrix element"
    The following two expressions are equivalent:
    
    $$
    \bra{\psi} \bigl(\hat{A}\ket{\phi}\bigr) \Leftrightarrow \bigl(\bra{\psi}\hat{A}\bigr)\ket{\phi}.
    $$

    This structure is called a **matrix element** and is usually written without parentheses, as $\bra{\psi}\hat{A}\ket{\phi}$. Specifically, we would call this example the matrix element of the operator $\hat{A}$ with respect to $\ket{\psi}$ and $\ket{\phi}$.

We know that an operator $\hat{A}$ acts on a ket to produce another ket: $\hat{A}\ket{\psi} = \ket{\psi'}$. However, we don't yet have a corresponding way of talking about how operators act on bras to produce other bras.

!!! info "Adjoint operator"
    Let $\ket{\psi'} = \hat{A}\ket{\psi}$ be a ket in state space $\mathcal{H}$. Then, $\bra{\psi'} = \hat{A}^\dagger\bra{\psi}$ is the corresponding bra in dual space $\mathcal{H}^*$.
    
    $\hat{A}^\dagger$ is called the **adjoint operator**, and just like other operators in QM, it is **linear**. With $\bra{\psi} = a_1\bra{\psi_1} + a_2\bra{\psi_2}$, we can distribute $\hat{A}^\dagger$ to the left onto bras within parentheses like so:

    $$
    \bra{\psi}\hat{A}^\dagger = \bigl(a_1\bra{\psi_1} + a_2\bra{\psi_2}\bigr)\hat{A}^\dagger = a_1\bra{\psi_1}\hat{A}^\dagger + a_2\bra{\psi_2}\hat{A}^\dagger
    $$

!!! info "Observables = Hermitian operators"
    In QM, all operators are observables &mdash; they are measurable properties of physical systems. In order for this to be true, the operators we deal with are all **equal to their own adjoints**:

    $$
    \hat{A} = \hat{A}^\dagger.
    $$

    An operator that obeys this property is called a **Hermitian operator**.

!!! info "Unitary operators"
    Another important subset of operators are the **unitary operators**. An operator is unitary if **its inverse is equal to its adjoint**:

    $$
    \hat{A}^{-1} = \hat{A}^\dagger.
    $$