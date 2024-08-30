# The Schrödinger equation
The Schrödinger equation describes the time evolution of a quantum state. It can be compared to Newton's second law in classical mechanics, which describes how a classical system behaves over time.

!!! info "The Schrödinger equation"
    The Schrödinger equation:

    $$
    i\hbar\frac{d}{dt}\ket{\psi(t)} = \hat{H}(t)\ket{\psi(t)},
    $$

    **deterministically** describes how a quantum state evolves over time. This is one of the postulates of quantum mechanics.

    Here, $\hat{H}(t)$ is the Hamiltonian, which is an operator corresponding to the total energy of the system, and $\hbar$ is called the reduced Planck constant (which is equal to Planck's constant over $2\pi$: $\hbar = h/2\pi$).

Note that we have now started writing the ket as a function of time: $\ket{\psi(t)}$.

The Schrödinger equation is a first order differential equation, which means that we can find a definite solution by finding a general solution and combining it with an initial condition.