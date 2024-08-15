# Operators
Physical, measurable quantities such as energy, position, and momentum are called **observables** and are represented by **operators**, which in QM are **complex square matrices**.

These quantities correspond to properties of **quantum systems**, such as atoms or subatomic particles.

!!! note "Common operators"
    Some common operators are the position operator $\hat{x}$, the momentum operator $\hat{p}$, and the energy operator $\hat{H}$. The energy operator $\hat{H}$ is called the **Hamiltonian**, and corresponds to the total energy of the given system.

A physical quantity $\mathcal{A}$ is described by an operator $\hat{A}$, which **acts on state vectors to produce another state vector**:

$$
\hat{A}\ket{\psi} = \ket{\psi'}.
$$

!!! info "Operators are linear in QM"
    Algebraically, operators in QM distribute over superpositions just as you'd expect:

    $$
    \hat{A}\Bigl(a\ket{\psi} + b\ket{\phi}\Bigr) = a\hat{A}\ket{\psi} + b\hat{A}\ket{\phi}
    $$

    The reason is that **all operators in QM are linear**.

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