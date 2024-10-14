# Quantum states
A pure quantum state is a mathematical object that describes everything we can know about a quantum system at a given point in time.

A quantum state can be represented by a state vector, written $\ket{\psi}$. $\ket{\psi}$ lives in a complex, potentially infinite-dimensional vector space called a Hilbert space, which we will denote $\mathcal{H}$:

$$
\ket{\psi} \in \mathcal{H}.
$$

If $\mathcal{H}$ is a $d$-dimensional space, $\ket{\psi}$ has $d$ elements. As each element is a complex number, which we need two real numbers to describe (a magnitude and a phase), we need $2d$ real, independent parameters to describe a state vector.

## Inner product
If we have two state vectors $\ket{\psi}, \ket{\phi} \in \mathcal{H}$, we define the inner product of $\ket{\psi}$ and $\ket{\phi}$ to be $\braket{\psi | \phi}$. The result of the inner product is in general a complex scalar.

If $\text{dim}(\mathcal{H}) = d$, we can calculate the inner product $\braket{\psi | \phi}$ like so:

$$
\braket{\psi | \phi} = \sum_{i = 1}^d{\psi_i^* \phi_i},
$$

where $\psi_i$ are the elements of $\ket{\psi}$, $\phi_i$ are the elements of $\ket{\phi}$, and $*$ means taking the complex conjugate of the element.

!!! abstract "Example: Inner product"
    Let $\ket{\psi} = [1 + 2i, 3, -5 - i]$, and $\ket{\phi} = [-2, 3i, 4]$. Then the inner product $\braket{\psi | \phi}$ can be calculated like:

    $$
    \begin{align}
        &\braket{\psi | \phi} =\\
        &((1 + 2i)^*)(-2) + (3^*) (3i) + ((-5 - i)^*) (4) =\\
        &(1 - 2i)(-2) + 3(3i) + (-5 + i)(4) =\\
        &-2 + 4i + 9i - 20 + 4i =\\
        &-22 + 17i.
    \end{align}
    $$

If we take the square of the result of the inner product of two states, $\braket{\psi | \phi}^2$, we get the probability of finding a system which was previously in state $\ket{\phi}$, in state $\ket{\psi}$ upon measurement. Measurement is where things start to get messy in quantum mechanics as opposed to classical mechanics, so this notion might take some getting used to.