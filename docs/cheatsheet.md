# Cheatsheet for Quantum Mechanics
This page originally acted as an intermediary for my own knowledge &mdash; writing down what I learn as I learn it &mdash; so that I could try to explain stuff in my own words later in the form of the rest of the notes on this website.

## State vectors
Let $\ket{\psi}$ and $\ket{\phi}$ be two state vectors in a Hilbert space $\mathcal{H}$.

!!! info "Inner product of kets"
    The inner product of $\ket{\psi}$ and $\ket{\phi}$ is written $\braket{\psi|\phi}$. The result of the inner product is a complex number $c \in \mathbb{C}$.

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