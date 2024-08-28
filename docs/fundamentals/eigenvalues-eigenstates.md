# Eigenstates and eigenvalues

!!! info "The eigenvalue equation"
    Let $\hat{A}$ be an operator. The eigenstates $\ket{\lambda}$ and eigenvalues $\lambda$ of $\hat{A}$ are such that they obey the **eigenvalue equation**:

    $$
    \hat{A}\ket{\lambda} = \lambda\ket{\lambda}.
    $$

    Note that $\ket{\lambda}$ is a **state vector**, while $\lambda$ is a **complex number**.

    The set of eigenvalues $\{\lambda_i\}$ is called the **spectrum** of $\hat{A}$.


## Eigenstates are only defined up to a constant
Let's say we have an operator $\hat{A}$ with eigenvalue equation $\hat{A}\ket{\lambda} = \lambda\ket{\lambda}$. Now, let's see what happens if we scale the eigenstate with a factor $\alpha \in \mathbb{C}$:

$$
\begin{align}
    &\hat{A}\ket{\lambda} = \lambda\ket{\lambda},\\
    &\ket{\lambda'} = \alpha\ket{\lambda}, \alpha \in \mathbb{C}.\\
    &\Rightarrow\\
    &\hat{A}\ket{\lambda'} = \hat{A}(\alpha\ket{\lambda}) = \alpha\hat{A}\ket{\lambda} = \alpha(\lambda\ket{\lambda}) = \alpha\lambda\ket{\lambda} = \lambda(\alpha\ket{\lambda}) = \lambda\ket{\lambda'}\\
    &\Leftrightarrow\\
    &\hat{A}\ket{\lambda'} = \lambda\ket{\lambda'}.
\end{align}
$$

This is just the same eigenvalue equation for the operator $\hat{A}$ again, with the same eigenvalue $\lambda$. In other words, if you find an eigenstate $\ket{\lambda}$, any multiple $\alpha\ket{\lambda}$ of the eigenstate will also be an eigenstate. This demonstrates that **eigenstates are only defined up to a constant** &mdash; they only really tell us about a direction in $\mathcal{H}$, and any state vector in that direction will also be an eigenstate.

When we talk about eigenstates without acknowledging this fact, what we tend to mean is the **normalized eigenstate**. The corresponding eigenvalue will then be the factor $\alpha$ that makes $\braket{\lambda | \lambda} = 1$.

## Global phase factor
!!! quote " "
    "Quantum mechanics is independent of a global phase" - *B. Monserrat*[[2]](#prof-m-eigen)

Since we are dealing with complex vector spaces, there is another fact that we have to keep in mind.

Let's say we have an eigenstate $\ket{\lambda}$ that is normalized: $\braket{\lambda | \lambda} = 1$, and we scale it by a factor $\alpha = e^{i\theta}$(1).
{ .annotate }

1.    Recall that a complex number $c \in \mathbb{C}$ can be written in polar coordinates as $c = re^{i\theta}$, where $r$ is the magnitude and $\theta$ is the phase in radians.

Note that when scaling it by this factor, we're not actually changing the magnitude of $\ket{\lambda}$, we're only shifting it by some phase $\theta$. We get:

$$
\begin{align}
    \ket{\lambda'} = e^{i\theta}\ket{\lambda} \Rightarrow\\
    \braket{\lambda' | \lambda '} = \Bigl(e^{-i\theta}\bra{\lambda}\Bigr)\Bigl(e^{i\theta}\ket{\lambda}\Bigr) = e^{-i\theta}e^{i\theta}\braket{\lambda | \lambda} = \braket{\lambda | \lambda} = 1.
\end{align}
$$

The magnitude of the phase-shifted eigenstate is the same as the original eigenstate. The phase-shifting had no impact on the defining property of the eigenstate.

!!! info "Differentiating eigenstates"
    Two eigenstates $\ket{\lambda_1}$ and $\ket{\lambda_2}$ are equivalent to each other if:

    - one is a multiple of the other: $\ket{\lambda_1} = \alpha\ket{\lambda_2}$,
    - one is phase-shifted from the other: $\ket{\lambda_1} = e^{i\theta}\ket{\lambda_2}$.

    In other words, you can multiply an eigenstate by any complex number $c = re^{i\theta} \in \mathbb{C}$, and it will still correspond to the same eigenstate.

## Eigenvalues of Hermitian operators
Perhaps you have been wondering what's so special about Hermitian operators for them to represent observables.

Here is your answer: observables are represented by Hermitian operators because all Hermitian operators have **real eigenvalues**. Furthermore, Hermitian operators have **orthogonal eigenstates**, which we can normalize, letting us use them to form an **orthonormal basis for the state space**.

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

## Eigenvalues and eigenstates of unitary operators
Given a unitary (but not necesarily Hermitian) operator $\hat{U}$, consider the eigenvalue equation:

$$
\hat{U}\ket{\lambda} = \lambda\ket{\lambda}.
$$

The eigenvalues $\lambda_n$ of a unitary operator $\hat{U}$ obey $|\lambda_n| = 1$, and can therefore be written in the form:

$$
\lambda_n = e^{i\phi_n},\quad\quad\phi_n \in \mathbb{R},
$$

??? abstract "Proof: The eigenvalues of a unitary operator have unit magnitude"
    Consider the norm:
    
    $$
    \begin{align}
        \|\hat{U}\ket{\lambda}\|^2 = && \\
        \|\lambda\ket{\lambda}\|^2 = && \\
        \Bigl(\lambda^*\bra{\lambda}\Bigr)\Bigl( \lambda\ket{\lambda} \Bigr) = && \tiny{\text{with $\|\psi\|^2 = \braket{\psi | \psi}$}}\\
        \lambda^*\lambda\braket{\lambda | \lambda} = && \\
        \lambda^*\lambda = && \tiny{\text{assuming $\ket{\lambda}$ is normalized}}\\
        |\lambda|^2. &&
    \end{align}
    $$
    
    Now, consider the norm again:

    $$
    \begin{align}
        \|\hat{U}\ket{\lambda}\|^2 = && \\
        \Bigl(\bra{\lambda}\hat{U}^\dagger\Bigr) \Bigl(\hat{U}\ket{\lambda}\Bigr) = && \\
        \bra{\lambda}\hat{U}^\dagger\hat{U}\ket{\lambda} = && \\
        \bra{\lambda}\mathbb{I}\ket{\lambda} = && \\
        \braket{\lambda | \lambda} = && \\
        1. &&
    \end{align}
    $$
    
    Given the above, we find that $|\lambda|^2 = 1$.

This means that the norm of the eigenvalues of a unitary operator is always equal to one, which can be described by all points on the radius of a unit circle in the complex plane.

!!! info "Bra version of the eigenvalue equation"
    For a unitary operator $\hat{U}$, we can write the eigenvalue equation in dual space in a really straight-forward way:

    $$
    \begin{align}
        \hat{U}\ket{\lambda} = \lambda\ket{\lambda} \Rightarrow\\
        \bra{\lambda}\hat{U} = \lambda\bra{\lambda}.
    \end{align}
    $$

If we have a unitary operator with two **distinct** eigenvalues $\lambda$ and $\mu$, the corresponding eigenstates $\ket{\lambda}$ and $\ket{\mu}$ are orthogonal.