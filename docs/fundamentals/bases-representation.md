# Bases and representation
A state vector $\ket{\psi}$ can be written in terms of a set of basis vectors $\{\ket{u_i}\}$, which spans $\mathcal{H}$.

In the vast majority of cases, we'll be dealing with orthonormal bases:

!!! info "Orthonormal basis"
    A set of vectors $\{\ket{u_i}\}$ is an **orthonormal basis** to $\mathcal{H}$ if the vectors are mutually orthogonal ($\braket{u_i | u_j} = 0, i \neq j$) and all are normalized ($\braket{u_i | u_i} = 1$).

    We can summarize the properties of an orthonormal basis using the **Kroenecker delta** $\delta_{ij}$, which is defined as(1):
    { .annotate }

    1.    I like to think about it as "equals" for the indices $i$ and $j$, returning 1 for "true" and 0 for "false": `i == j ? 1 : 0`

    $$
    \delta_{ij} =
    \begin{cases}
        1, i = j,\\
        0, i \neq j.
    \end{cases}
    $$

    Thus, a basis $\{\ket{u_i}\}$ is orthonormal if $\braket{u_i | u_j} = \delta_{ij}$.

    On this page, we will call this basis the u-basis.

Every ket $\ket{\psi} \in \mathcal{H}$ has a **unique** expansion of the basis vectors:

$$
\ket{\psi} = \sum_i{c_i \ket{u_i}},
$$

where $c_i$ is the expansion coefficient for the $i$th basis vector $\ket{u_i}$. This means that if the basis is known, we only need the set of expansion coefficients $c_i$ to uniquely identify a state vector.

We call $c_i$ the **representation** of $\ket{\psi}$ in the basis $\{\ket{u_i}\}$.

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

## Kets in the u-basis
Given a ket $\ket{\psi}$, we can write it in the $u$-basis, i.e. the orthonormal basis $\{\ket{u_i}\}$, like so:

$$
\ket{\psi} = \sum_i{c_i\ket{u_i}}, \quad\quad c_i = \braket{u_i | \psi}.
$$

## Bras in the u-basis

We now know how to represent a given ket in a specific basis. How about the bras?

Say we have a ket $\ket{\psi} = \sum_i{c_i\ket{u_i}} \in \mathcal{H}$, with expansion coefficients $c_i = \braket{u_i | \psi}$. The corresponding a bra $\bra{\psi} \in \mathcal{H}^*$ can then be written:

$$
\begin{align}
    \bra{\psi} &=\\
    \bra{\psi}\mathbb{I} &=\\
    \bra{\psi} \sum_i{\Bigl(\ket{u_i}\bra{u_i}\Bigr)} &=\\
    \sum_i{\Bigl(\braket{\psi | u_i}\bra{u_i}\Bigr)} &=\\
    \sum_i{\Bigl(\braket{u_i | \psi}^*\bra{u_i}\Bigr)} &=\\
    \sum_i{\Bigl(c_i^*\bra{u_i}\Bigr)}.
\end{align}
$$

## Operators in the u-basis
Finally, we want to be able to express operators in terms of a specific basis.

We can write an operator $\hat{A}\ket{\psi} = \ket{\psi'}$ in a particular orthonormal basis $\{\ket{u_i}\}$ like so(1):
{ .annotate }

1.    See [[1]](#prof-m-matrix) for proof.

$$
\hat{A} = \sum_{ij}{\ket{u_i}\bra{u_i}\hat{A}\ket{u_j}\bra{u_j}},
$$

which, if we let $A_{ij}$ be the matrix element $\bra{u_i}\hat{A}\ket{u_j}$, becomes:

$$
\hat{A} = \sum_{ij}{A_{ij}\ket{u_i}\bra{u_j}}.
$$

## References
<span id="prof-m-matrix">[1]</span> Professor M does Science, Cambridge, U.K. *Matrix formulation of quantum mechanics*. (June 24, 2020). Accessed: Aug. 20, 2024. [Online Video]. Available: [https://youtu.be/wIwnb1ldYTI](https://youtu.be/wIwnb1ldYTI).