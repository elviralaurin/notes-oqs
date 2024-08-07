# Quantum state space
The mathematics of quantum mechanics is done in a special type of vector space we'll call **quantum state space**, or just **state space** [[1]](#prof-m-dirac).

The details of the state space will differ depending on the situation. Not only that, but different people also seem to have quite different opinions on exactly what properties the state space has to have (or at least, which of those properties it is relevant to even mention).

In these notes, we will denote the state space with $\mathcal{H}$. What we generally mean when we refer to $\mathcal{H}$ here is a **complete**, **separable**, **complex**, possibly **infinite-dimensional** **Hilbert  
space**(1).
{ .annotate }

1.    For details on what all these terms mean, see chapter 2 of [[2]](#von-neumann).

If you're like me, that is a pretty hefty list of mathematical jargon, but the only word that really is relevant right now is **complex**. From now on, whenever we talk about numbers, we mean complex numbers, unless otherwise specified. That includes all scalars, vector components, etc.

## Vectors in state space
As mentioned in the section about [abstract vector spaces](abstract-vector-spaces.md), the vectors of $\mathcal{H}$ aren't the familiar list-of-numbers we learn about in our basic linear algebra courses. But, we'll get the practicalities out of the way first.

!!! info "Kets"
    The vectors of $\mathcal{H}$ are called *kets*, and are written using a pipe symbol (`|`), followed by the label of the ket, followed by a right angle bracket (`>`) [[1]](#prof-m-dirac):

    $$
    \ket{\psi} \in \mathcal{H}.
    $$

We will usually label our kets with Greek letters, such as with $\psi$ ("psi") or $\phi$ ("phi"), but no matter what, the labels are just that &mdash; labels. You can name them $\ket{\text{Erwin}}$ or $\ket{\text{Werner}}$ for all anyone cares.

!!! warning "Quantum states $\neq$ elements of $\mathcal{H}$"
    Even though we call $\mathcal{H}$ "quantum state space", the elements of $\mathcal{H}$ aren't quantum states, for reasons we'll get to later. For now we'll just say that the elements of state space are called kets, and simply ignore the physical interpretation &mdash; we'll get to that.

## Inner products
Just like we can take the dot product of two vectors in "normal"(1) vector spaces, there is a corresponding operation in state space.
{ .annotate }

1.    From now on, I'll stop writing "normal" and start writing what I actually mean: [Euclidean vector spaces](https://math.libretexts.org/Bookshelves/Calculus/Vector_Calculus_(Corral)/01%3A_Vectors_in_Euclidean_Space).

The operation is called **inner product**, and isn't specific to quantum mechanics. In linear algebra, the inner product of two vectors $\vec{u}$ and $\vec{v}$ of some vector space $V$ is usually written as $(\vec{u}, \vec{v})$.

In quantum mechanics, we use a special notation called **Dirac notation** or **Bra-Ket notation**(1).
{ .annotate }

1.    "Bra-Ket" from the word "bracket" &mdash; we have already met the *kets*, and will talk about the *bras* in a little bit.

!!! info "Inner product"
    The inner product of two kets $\ket{\psi}, \ket{\phi} \in \mathcal{H}$ is written as:

    $$
    (\ket{\psi}, \ket{\phi}) := \braket{\psi|\phi}
    $$

    The inner product **always results in a non-negative real number.**

This might look strange at first &mdash; I know it did to me &mdash; but there are some neat algebraic manipulation tricks that Bra-Ket notation allows us to use. It took some time for me to get used to it though, so I'll go slow in introducing it here.

Notice that when taking the inner product of two kets $\ket{\psi}$ and $\ket{\phi}$, we can look at it just in terms of the symbols as flipping the first ket (like $\bra{\psi}$), and smushing it together with the second ket (like $\bra{\psi}\ket{\phi}$), and finally removing one of the duplicate vertical bars in the middle (arriving at the notation for the inner product from above; $\braket{\psi|\phi}$).

That flipped ket, $\bra{\phi}$, has a name &mdash; it's a *bra*, the second part of the "bracket" of Bra-Ket notation &mdash; and we'll talk a little bit more about it later.

### Norm
Just as in Euclidean(1) vector spaces, the inner product raises the following question: can we take the inner product of a vector with itself, and what does that mean?
{ .annotate }

1.    See for example [Vectors in Euclidean Space on LibreTexts Mathematics](https://math.libretexts.org/Bookshelves/Calculus/Vector_Calculus_(Corral)/01%3A_Vectors_in_Euclidean_Space)

In Euclidean vector spaces, taking the inner (dot) product of a vector with itself results in a real number called the *norm* of the vector, which corresponds to its **length** or **magnitude**.

For vectors in $\mathcal{H}$, we don't have the luxury of such simple interpretations(1), but we can nevertheless still calculate the norm of kets.
{ .annotate }

1.    There is still a real, physical interpretation, but as it's slightly more confusing than just "length", we'll leave it at this for now.

!!! info "Norm of a ket"
    The *norm* of a ket $\ket{\psi} \in \mathcal{H}$ is defined as the result of taking the inner product of $\ket{\psi}$ with itself:

    $$
    \braket{\psi|\psi}
    $$

    Of course, since the inner product always results in a non-negative real number, the norm is a non-negative real number.

## References
<!-- <span id="griffiths">[1]</span> D. J. Griffiths, D. F. Schroeter, *Introduction to Quantum Mechanics*, 3rd ed. Cambridge, U.K.: Cambridge Univ. Press, 2018, [doi: 10.1017/9781316995433](https://doi.org/10.1017/9781316995433). -->
<span id="prof-m-dirac">[1]</span> Professor M does Science, Cambridge, U.K. *Dirac Notation: State Space And Dual Space*. (May 23, 2020). Accessed: Jul. 3, 2024. [Online Video]. Available: [https://www.youtube.com/watch?v=hJoWM9jf0gU](https://www.youtube.com/watch?v=hJoWM9jf0gU)  
<span id="von-neumann">[2]</span> J. von Neumann, *Mathematical Foundations of Quantum Mechanics*, N. A. Wheeler, Ed., 2018 ed. Princeton, NJ, USA: Princeton Univ. Press, 2018, [doi: 10.1017/9781316995433](https://doi.org/10.1017/9781316995433).  