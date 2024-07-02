# Quantum state space
The mathematics of quantum mechanics is done in a special type of vector space we'll call **quantum state space**, or just **state space**.

Formally, the state space will be different depending on the situation. As such, there really is no "the" state space, just the one we happen to be talking about at the moment. We will denote the state space at hand by $\mathcal{H}$. Just remember that what $\mathcal{H}$ really is can be quite different depending on who you ask, and during what circumstances.

In these notes, we will try to be consistent in the use of $\mathcal{H}$. What we generally refer to here as a state space $\mathcal{H}$ is a **complete**, **separable**, **complex**, possibly **infinite-dimensional** **Hilbert  
space**(1).
{ .annotate }

1.    For details on what all these terms mean, see chapter 2 of [[1]](#von-neumann).

If you're like me, that is a pretty hefty list of mathematical jargon, but the only word that is really relevant at this moment is **complex**. From now on, whenever we talk about numbers, we mean complex numbers, unless otherwise specified. That includes all scalars, vector components, etc.

## Vectors in state space
As mentioned in the section about [abstract vector spaces](abstract-vector-spaces.md), the vectors of $\mathcal{H}$ aren't the familiar list-of-numbers we learn about in our basic linear algebra courses. But, we'll get the practicalities out of the way first.

!!! info "Kets"
    The vectors of $\mathcal{H}$ are called *kets*, and are written using a pipe symbol (`|`), followed by the label of the ket, followed by a right angle bracket (`>`):

    $$
    \ket{\psi} \in \mathcal{H}.
    $$

We will usually label our kets with Greek letters, such as with $\psi$ ("psi") or $\phi$ ("phi"), but no matter what, the labels are just that &mdash; labels. You can name them $\ket{\text{Erwin}}$ or $\ket{\text{Werner}}$ for all anyone cares.

!!! warning "Quantum states $\neq$ elements of $\mathcal{H}$"
    Even though we call $\mathcal{H}$ "quantum state space", the elements of $\mathcal{H}$ aren't quantum states, for reasons we'll get to later. For now we'll just say that the elements of state space are called kets, and get into the physical interpretation later.

## Inner products
Just like we can take the dot product of two vectors in "normal" vector spaces, there is a corresponding operation in state space.

The operation is called **inner product**, and isn't specific for quantum mechanics. In linear algebra, the inner product of two vectors $\vec{u}$ and $\vec{v}$ of some vector space $V$ is usually written as $(\vec{u}, \vec{v})$.

In quantum mechanics, we use a special notation called **Dirac notation** or **Bra-Ket notation**(1).
{ .annotate }

1.    "Bra-Ket" from the word "bracket" &mdash; we have already met the kets, and will talk about the bras in a little bit.

!!! info "Inner product"
    The inner product of two kets $\ket{\psi}, \ket{\phi} \in \mathcal{H}$ is written as:

    $$
    (\ket{\psi}, \ket{\phi}) := \braket{\psi|\phi}
    $$

### Norm

## References
<!-- <span id="griffiths">[1]</span> D. J. Griffiths, D. F. Schroeter, *Introduction to Quantum Mechanics*, 3rd ed. Cambridge, U.K.: Cambridge Univ. Press, 2018, [doi: 10.1017/9781316995433](https://doi.org/10.1017/9781316995433). -->
<span id="von-neumann">[1]</span> J. von Neumann, *Mathematical Foundations of Quantum Mechanics*, N. A. Wheeler, Ed., 2018 ed. Princeton, NJ, USA: Princeton Univ. Press, 2018, [doi: 10.1017/9781316995433](https://doi.org/10.1017/9781316995433).