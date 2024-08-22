# Measurement
The measurement of a quantum system and what happens to the system after a measurement has been done is at the core of the strangeness most people associate with quantum mechanics.

What we will find is that it is **impossible** to predict the outcome of a measurement of a quantum system.

This is quite a bold statement. All physical laws we are aware of in the world of classical mechanics are deterministic &mdash; every event has a cause and an effect. If you know *everything* about the state of something at any point in time (i.e. complete, perfect knowledge, if such a thing could exist), it is possible to retrace all past states, and to predict all future states.

When we say that it is impossible to predict the outcome of a quantum measurement, it implies that some things don't have a clear cause and effect. Note that we aren't saying that we just simply don't know how to predict the outcome, we are making the stronger claim of it physically not being possible.

Here, we will try to make some sense of this seemingly insane claim.

!!! quote " "
    "Richard Feynman, one of the big figures in physics, used to say 'No one understands quantum mechanics.' So in some sense, the pressure is off for you guys, because I don't get it and you don't get it and Feynman doesn't get it. The point is, here is my goal: right now, I am the only one who doesn't understand quantum mechanics. In about seven days, all of you will be unable to understand quantum mechanics." &mdash; *R. Shankar*[[1]](#shankar-l1)

## Eigenstates and eigenvalues
Say you have a quantum system of some kind, and you want to measure one of its physical properties. That physical property corresponds to a particular Hermitian operator $\hat{A}$, and the result of you measuring this property of the system will be one of the **eigenvalues** of $\hat{A}$.

!!! info "The eigenvalue equation"
    Let $\hat{A}$ be an operator. The eigenstates $\ket{\lambda}$ and eigenvalues $\lambda$ of $\hat{A}$ are such that they obey the **eigenvalue equation**:

    $$
    \hat{A}\ket{\lambda} = \lambda\ket{\lambda}.
    $$

    Note that $\ket{\lambda}$ is a **state vector**, while $\lambda$ is a **complex number**.

    The set of eigenvalues $\{\lambda_i\}$ is called the **spectrum** of $\hat{A}$.


### Normalizing the eigenstate
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

This is just the same eigenvalue equation for the operator $\hat{A}$ again, with the same eigenvalue $\lambda$. In other words, if you find an eigenstate $\ket{\lambda}$, any multiple $\alpha\ket{\lambda}$ of the eigenstate will also be an eigenstate. This demonstrates that **eigenstates are only really defined up to a constant** &mdash; they only really tell us about a direction in $\mathcal{H}$, and any state vector in that direction will also be an eigenstate.

When we talk about eigenstates without acknowledging this fact, what we tend to mean is the **normalized eigenstate**. The corresponding eigenvalue will then be the factor $\alpha$ that makes $\braket{\lambda | \lambda} = 1$.

### Global phase factor
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

## References
<span id="shankar-l1">[1]</span> YaleCourses, Yale Univ. Press, New Haven, CT, USA. *19. Quantum Mechanics I: The key experiments and wave-particle duality*. (March 24, 2011). Accessed: Aug. 22, 2024. [Online Video]. Available: [https://youtu.be/uK2eFv7ne_Q?feature=shared](https://youtu.be/uK2eFv7ne_Q?feature=shared).

<span id="prof-m-eigen">[2]</span> Professor M does Science, Cambridge, U.K. *Eigenvalues and eigenstates in quantum mechanics*. (July 1, 2020). Accessed: Aug. 21, 2024. [Online Video]. Available: [https://youtu.be/p1zg-c1nvwQ?feature=shared](https://youtu.be/p1zg-c1nvwQ?feature=shared).