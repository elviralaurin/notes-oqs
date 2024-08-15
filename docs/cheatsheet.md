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