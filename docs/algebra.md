# The Algebraic Rules of Quantum Mechanics
This page contains all the algebraic rules I have been able to identify so far.

## State vectors
Let $\ket{\psi}$ and $\ket{\phi}$ be two state vectors in a Hilbert space $\mathcal{H}$.

### Inner product
The inner product of $\ket{\psi}$ and $\ket{\phi}$ is written $\braket{\psi|\phi}$. The result of the inner product is a complex number $c \in \mathbb{C}$.

## Operators
A measurable, physical property $\mathcal{A}$ is called an observable and is described by an operator $\hat{A}$ acting on the state space $\mathcal{H}$.

The result of $\hat{A}$ acting on a ket $\ket{\psi}$ is another ket $\ket{\psi'}$, which is also in the state space:

$$
\hat{A}\ket{\psi} = \ket{\psi'}, \in \mathcal{H}.
$$

Let $\hat{A}$, $\hat{B}$, and $\hat{C}$ be linear operators acting on $\mathcal{H}$.

### Addition
Operator addition is:

- associative: $(\hat{A} + \hat{B}) + \hat{C} = \hat{A} + (\hat{B} + \hat{C})$;
- commutative: $\hat{A} + \hat{B} = \hat{B} + \hat{A}$.

### Multiplication
Operator multiplication is defined by how operators act on kets:

$$
(\hat{A}\hat{B})\ket{\psi} = \hat{A}(\hat{B}\ket{\psi}) = \hat{A}\ket{\psi'}
$$

Operator multiplication is therefore:

- associative: $\hat{A}(\hat{B}\hat{C}) = (\hat{A}\hat{B})\hat{C}$;
- but **NOT** necessarily commutative: $\hat{A}\hat{B} \neq \hat{B}\hat{A}$.