# State vectors and Hilbert space
The state of a closed physical system can be described by a *state vector* or *wave function* which is an element of some Hilbert space $\mathcal{H}$.

Throughout these notes and in most other QM resources available, state vectors are written in *Dirac notation* and are then called *kets*. A ket is written with a vertical bar (`|`), followed by the name or label of the ket (often a Greek letter like $\psi$(1) or $\phi$(2)), followed by a right-angle bracket (`>`). The following is a ket: $\ket{\psi}$.
{ .annotate }

1.    pronounced "sy", "psy", "see", or "psee", depending on who you ask
2.    pronounced "fy" or "fee", depending on who you ask

$\mathcal{H}$ can be *infinite-dimensional*. If we think of vectors as an ordered list of numbers, this means that the list can be infinitely long. An equivalent way to think about it is that we might need an infinite number of basis vectors to represent a given vector in $\mathcal{H}$.

Another important thing to remember about $\mathcal{H}$ is that whenever we talk about scalars, we mean complex scalars. In other words, vector components are complex, and the scalars we scale vectors with are complex, and so on. Always assume that the numbers we work with are complex, i.e. can include an imaginary term, **unless otherwise specified**.

Just like with vectors in Euclidean space, we can scale state vectors by multiplying them with scalars. We can also add state vectors together, and the result will be another state vector.

If a state vector is written as a linear combination of other state vectors, we say that the former is a **superposition** of the latter. For example, if we have a state $\ket{\psi} = a\ket{\psi_1} + b\ket{\psi_2}$, we would say that $\ket{\psi}$ is a superposition of $\ket{\psi_1}$ and $\ket{\psi_2}$.

!!! info "State vector? Ket? Wave function?"
    What is really the difference between a state vector, a ket, and a wave function?

    A **state vector** is a vector in Hilbert space that is associated with a physical state that the system can be in(1).
    { .annotate }
    
    1.    Note that this does **not** mean that the state of the system necessarily corresponds to that exact vector. In other words, a state vector $\bar{v}$ corresponds to one specific physical state $V$ ($\bar{v} \rightarrow V$), but a physical state does not necessarily correspond to that same vector ($V \nrightarrow \bar{v})$. More on this later.

    A **ket** is a state vector in Dirac notation.

    A **wave function** is a complex-valued function that is a mathematical description of a quantum system. It is a different way of representing the state of a quantum system. It is less general than that of the vector representation, as it implicitly chooses a basis.

## References
<!-- <span id="griffiths">[1]</span> D. J. Griffiths, D. F. Schroeter, *Introduction to Quantum Mechanics*, 3rd ed. Cambridge, U.K.: Cambridge Univ. Press, 2018, [doi: 10.1017/9781316995433](https://doi.org/10.1017/9781316995433). -->
<span id="prof-m-dirac">[1]</span> Professor M does Science, Cambridge, U.K. *Dirac Notation: State Space And Dual Space*. (May 23, 2020). Accessed: Jul. 3, 2024. [Online Video]. Available: [https://www.youtube.com/watch?v=hJoWM9jf0gU](https://www.youtube.com/watch?v=hJoWM9jf0gU).
<!-- <span id="von-neumann">[3]</span> J. von Neumann, *Mathematical Foundations of Quantum Mechanics*, N. A. Wheeler, Ed., 2018 ed. Princeton, NJ, USA: Princeton Univ. Press, 2018, [doi: 10.1017/9781316995433](https://doi.org/10.1017/9781316995433).   -->