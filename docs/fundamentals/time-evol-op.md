# The time evolution operator
The Schrödinger equation (SE) describes how a state $\ket{\psi}$ evolves in time. However, the SE can be a bit clunky to work with, and so we can use that fact that it is linear to describe it just by using an operator $\hat{U}(t, t_0)$:

!!! info "The time evolution operator"
    The time evolution operator $\hat{U}(t, t_0)$ relates a state $\ket{\psi(t_0)}$ at a time $t_0$ with the same state $\ket{\psi(t)}$ at a later time $t$, which is the result of evolving the original state $\ket{\psi(t_0)}$ through time with the Schrödinger equation:

    $$
    \ket{\psi(t)} = \hat{U}(t, t_0)\ket{\psi(t_0)}.
    $$

If the start and end times are the same, i.e. $t = t_0$, we get:

$$
\ket{\psi(t_0)} = \hat{U}(t_0, t_0)\ket{\psi(t_0)} \Rightarrow \hat{U}(t, t_0) = \mathbb{I}.
$$

In other words, if the time doesn't change, the state doesn't change.

If the start and end times are different, i.e. $t \neq t_0$, we can use the SE to get:

$$
\begin{align}
    i\hbar\frac{d}{dt}\ket{\psi(t)} = \hat{H}(t)\ket{\psi(t)} \Leftrightarrow && \small{\text{with $\ket{\psi(t)} = \hat{U}(t, t_0)\ket{\psi(t_0)}$}}\\
    i\hbar\frac{d}{dt}\hat{U}(t, t_0)\ket{\psi(t_0)} = \hat{H}(t)\hat{U}(t, t_0)\ket{\psi(t_0)} \Leftrightarrow && \tiny{\text{$\ket{\psi(t_0)}$ not dependent on $t$, so move out of deriv.}}\\
    i\hbar\ket{\psi(t_0)}\frac{d}{dt}\hat{U}(t, t_0) = \hat{H}(t)\hat{U}(t, t_0)\ket{\psi(t_0)} \Leftrightarrow && \tiny{\text{div. with $\ket{\psi(t_0)}$ on both sides}}\\
    i\hbar\frac{d}{dt}\hat{U}(t, t_0) = \hat{H}(t)\hat{U}(t, t_0). && \\
\end{align}
$$

This is now a first-order differential equation which can be solved using the initial condition found earlier, $\hat{U}(t_0, t_0) = \mathbb{I}$.

So far, this is quite involved. Sure, we have found a way to find the time evolution operator, but to actually evaluate it seems to be tricky.

Luckily for us, the cases we will be dealing with almost always (as far as I know right now) have **time-independent Hamiltonians**. And for this special case, we can write the time evolution operator $\hat{U}(t, t_0)$