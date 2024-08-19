# Cheatsheet for Quantum Mechanics
This page originally acted as an intermediary for my own knowledge &mdash; writing down what I learn as I learn it &mdash; so that I could try to explain stuff in my own words later in the form of the rest of the notes on this website.

## Bras, kets, and the inner product
Let $\ket{\psi}$ and $\ket{\phi}$ be two state vectors in a Hilbert space $\mathcal{H}$.

!!! info "Properties of the inner product"
    $$
    \begin{align}
        &\braket{\psi | \phi} = c, c \in \mathbb{C},\\\\
        &\braket{\psi | \phi} = \bigl(\braket{\phi | \psi}\bigr)^* = \braket{\phi | \psi}^*,\\\\
        &\bra{\psi} \Bigl(a\ket{\phi_1} + b\ket{\phi_2}\Bigr) = a\braket{\psi | \phi_1} + b\braket{\psi | \phi_2},\\\\
        &\Bigl(a\bra{\psi_1} + b\bra{\psi_2}\Bigr)\ket{\phi} = a^*\braket{\psi_1 | \phi} + b^*\braket{\psi_2 | \phi}.
    \end{align}
    $$

!!! info "Inner product of a ket with itself"
    $$
    \begin{align}
        &\braket{\psi | \psi} = r, \text{ where }r \in \mathbb{R} \text{ and } r \geq 0,\text{ and}\\
        &\braket{\psi | \psi} = 0, \text{ iff } \ket{\psi} = \ket{\text{null}}.
    \end{align}
    $$

## Operators
A measurable, physical property $\mathcal{A}$ is called an observable and is described by an operator $\hat{A}$ acting on the state space $\mathcal{H}$.

The result of $\hat{A}$ acting on a ket $\ket{\psi}$ is another ket $\ket{\psi'}$, which is also in the state space:

$$
\hat{A}\ket{\psi} = \ket{\psi'},\quad\quad\ket{\psi'} \in \mathcal{H}.
$$

Let $\hat{A}$, $\hat{B}$, and $\hat{C}$ be linear operators acting on $\mathcal{H}$.

!!! info "Operator addition"
    Operator addition is:

    - associative: $(\hat{A} + \hat{B}) + \hat{C} = \hat{A} + (\hat{B} + \hat{C})$;
    - commutative: $\hat{A} + \hat{B} = \hat{B} + \hat{A}$.

!!! info "Operator multiplication"
    Operator multiplication is defined by how operators act on kets:
    
    $$
    (\hat{A}\hat{B})\ket{\psi} = \hat{A}(\hat{B}\ket{\psi}) = \hat{A}\ket{\psi'}
    $$

    Operator multiplication is therefore:
    
    - associative: $\hat{A}(\hat{B}\hat{C}) = (\hat{A}\hat{B})\hat{C}$;
    - **NOT** necessarily commutative: $\hat{A}\hat{B} \neq \hat{B}\hat{A}$.

!!! info "Conjugation of the matrix element"
    For a matrix element $\bra{\psi} \hat{A} \ket{\phi} \in \mathbb{C}$, it is the case that:

    $$
    \bra{\psi} \hat{A} \ket{\phi} = \bra{\phi} \hat{A}^\dagger \ket{\psi}^*
    $$

!!! info "Inverse operators"
    The **inverse** $\hat{A}^{-1}$ of an operator $\hat{A}$ is defined by:

    $$
    \hat{A}^{-1}\hat{A} = \hat{A}\hat{A}^{-1} = \mathbb{1},
    $$

    where $\mathbb{1}$ is the identity matrix.

!!! info "Hermitian operators"
    An operator $\hat{A}$ is **Hermitian** if it is equal to its adjoint:

    $$
    \hat{A} = \hat{A}^\dagger.
    $$

!!! info "Unitary operators"
    An operator $\hat{U}$ is **unitary** if it is equal to its inverse:

    $$
    \hat{U} = \hat{U}^{-1},
    $$

    or, equivalently,

    $$
    \hat{U}^\dagger\hat{U} = \hat{U}\hat{U}^\dagger = \mathbb{1},
    $$

!!! info "Adjoint operator"
    For two operators $\hat{A}$ and $\hat{B}$, the following are true:

    $$
    \begin{align}
        (\hat{A}^\dagger)^\dagger = \hat{A},\\
        (a\hat{A})^\dagger = a^*\hat{A}^\dagger,\\
        (\hat{A} + \hat{B})^\dagger = \hat{A}^\dagger + \hat{B}^\dagger,\\
        (\hat{A}\hat{B})^\dagger = \hat{B}^\dagger\hat{A}^\dagger.
    \end{align}
    $$

!!! info "Finding the expansion coefficients of a state"
    The expansion coefficients $c_i$ of a state vector $\ket{\psi}$ in an orthonormal basis $\{u_i\}$ can be found by projecting $\ket{\psi}$ onto the basis:

    $$
    \braket{u_j | \psi} = c_i.
    $$