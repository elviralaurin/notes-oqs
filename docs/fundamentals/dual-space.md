# Dual space
!!! quote " "
    "To every ket, there corresponds a bra" &mdash; *B. Monserrat*[[1]](#prof-m-dirac)

Just like the kets live in state space $\mathcal{H}$, the bras(1) live in a space we denote $\mathcal{H}^*$. This space is commonly called the *dual space*(2).
{ .annotate }

1.    If this is term is unfamiliar to you, you should check out the notes on the [inner product](inner-product.md) first.
2.    It's actually a bit misleading to call it *the* dual space, as all vector spaces has a dual space. When we talk about dual spaces in QM, at least in these notes, what we mean is really just the space of all bras, i.e. the *linear functionals* to the kets. Search for the "Riesz representation theorem" for more information.

!!! note
    The dual space $\mathcal{H}^*$ is also a Hilbert space!

Recall that in Euclidean space, the dot product of two vectors $\bar{u}$ and $\bar{v}$ can be thought of as multiplying the corresponding components and adding up the result:

$$
\bar{u} \cdot \bar{v} = [u_1, u_2, \dots, u_n] \cdot [v_1, v_2, \dots, v_n] = \sum_{i=1}^n{u_iv_i}.
$$

However, we can also think about it as a matrix multiplication where the first factor is a row vector and the second a column vector:

$$
\bar{u} \cdot \bar{v} =
\begin{bmatrix}
    u_1 & u_2 & \dots & u_n
\end{bmatrix}
\begin{bmatrix}
    v_1\\
    v_2\\
    \vdots\\
    v_n
\end{bmatrix} = \sum_{i=1}^n{u_iv_i}.
$$

If vectors are thought of as column vectors by default, we can say that we "flipped" the first vector to turn it into a row vector in order to calculate the dot product. Mathematically, this "flipping" of column vectors to row vectors is done by taking the *transpose* of the vector. In other words, a column vector $\bar{v}$ has a corresponding row vector which is found by taking the transpose of the original vector: $\bar{v}^T$.

The relationship between row and column vectors is similar to that of bras and kets, with one additional difference:

!!! info "Column vs. row vector, ket vs. bra"
    Let $a_r \in \mathbb{R}$ and $a_c \in \mathbb{C}$ be scalars.

    In Euclidean space, given a column vector $a_r\bar{v} \in \mathbb{R}^n$, the corresponding row vector is given by $a_r\bar{v}^T \in \mathbb{R}^{1 \times n}$. When going from column vector to row vector, we leave the scalar unchanged.

    In state space, given a ket $a_c\ket{\psi} \in \mathcal{H}$, the corresponding bra is given by $a_c^*\bra{\psi} \in \mathcal{H}^*$. When going from ket to bra, we have to take the **complex conjugate** of the scalar: $a_c$ becomes $a_c^*$.

The reason why we have to take the complex conjugate of any scalars when finding the corresponding bra to a ket comes from the definition of the inner product(1).
{ .annotate }

1.    For more information on why this is, check out [Professor M does Science's video on YouTube](https://www.youtube.com/watch?v=hJoWM9jf0gU) from timestamp 10:05 onwards.

## References
<span id="prof-m-dirac">[1]</span> Professor M does Science, Cambridge, U.K. *Dirac Notation: State Space And Dual Space*. (May 23, 2020). Accessed: Jul. 3, 2024. [Online Video]. Available: [https://www.youtube.com/watch?v=hJoWM9jf0gU](https://www.youtube.com/watch?v=hJoWM9jf0gU).