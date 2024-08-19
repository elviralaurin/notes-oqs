# Orthonormal bases
A state vector $\ket{\psi}$ can be written in terms of a set of basis vectors $\{\ket{u_i}\}$, which spans $\mathcal{H}$.

In the vast majority of cases, we'll be dealing with orthonormal bases:

!!! info "Orthonormal basis"
    A set of vectors $\{\ket{u_i}\}$ is an **orthonormal basis** to $\mathcal{H}$ if the vectors are mutually orthogonal ($\braket{u_i | u_j} = 0, i \neq j$) and all are normalized ($\braket{u_i | u_i} = 1$).

    We can summarize the properties of an orthonormal basis using the **Kroenecker delta** $\delta_{ij}$, which is defined as:

    $$
    \delta_{ij} =
    \begin{cases}
        1, i = j,\\
        0, i \neq j.
    \end{cases}
    $$

    Thus, a basis $\{\ket{u_i}\}$ is orthonormal if $\braket{u_i | u_j} = \delta_{ij}$.

Every ket $\ket{\psi} \in \mathcal{H}$ has a **unique** expansion of the basis vectors:

$$
\ket{\psi} = \sum_i{c_i \ket{u_i}},
$$

where $c_i$ is the expansion coefficient for the $i$th basis vector $\ket{u_i}$. This means that if the basis is known, we only need the set of expansion coefficients $c_i$ to uniquely identify a state vector.

!!! info "Determining the expansion coefficients"
    Given a basis $\{\ket{u_i}\}$ spanning $\mathcal{H}$, we can find the expansion coefficients of a state $\ket{\psi} \in \mathcal{H}$ as follows:

    $$
    \begin{align}
        \braket{u_j | \psi} =\\
        \bra{u_j} \Bigl(\sum_i{c_i \ket{u_i}}\Bigr) =\\
        \sum_i{c_i \braket{u_j | u_i}} =\\
        \sum_i{c_i \delta_{ij}} =\\
        c_i.
    \end{align}
    $$

    Note that in the second to last step, $\delta_{ij} = 0$ for every single term for which $i \neq j$. This leaves only one term in the sum: the one where $i = j$, which makes $\delta_{ij} = 1$, which results in $c_i\delta_{ij} = c_i \cdot 1 = c_i$.