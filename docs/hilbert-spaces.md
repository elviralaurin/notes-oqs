# Hilbert spaces
The mathematics of quantum mechanics is done in a special type of vector space called a **Hilbert space**.

The following is an incomplete description of what Hilbert spaces actually are, as the complete formalism is (so far) out of scope for what we're trying to accomplish. Whenever we say "Hilbert space" throughout these pages, we actually mean the $L^2$ space (the set of all square-integrable functions; see 3.1 of [\[1\]](#griffiths)). We will denote this space with $\mathcal{H}$, and it's the properties of this space that we're talking about below.

## Vectors in Hilbert space
As mentioned in the section about [abstract vector spaces](abstract-vector-spaces.md), the vectors of $\mathcal{H}$ aren't the familiar list-of-numbers we learn about in our basic linear algebra courses. Instead, they are **complex functions**, usually denoted by the uppercase Greek letter $\Psi$ (pronounced "psi") that map **real scalars** to **complex scalars**.

By the way, from now on, whenever we mention "scalars", we mean **complex** scalars. Also, remember that the real numbers are a subset of the complex numbers. In other words, just because something is a complex number, it doesn't mean that it for sure contains $i$.

Quantum mechanics is &mdash; suprise, surprise &mdash; a branch of physics. We therefore generally want for the symbols we use to have real, physical interpretations. The objects or entities we will talk about tend to be particles, or rather, the state of particles.

Now, repeat after me:

!!! info "Quantum states"
    The **state of a quantum particle**, i.e. a **quantum state**, is a **ray in complex Hilbert space**.

In order to explain what that means, we'll start off by being sloppy. Incorrectly, we could say that a vector in $\mathcal{H}$ is a quantum state, and usually we would denote such a thing as $\ket{\psi}$.(1)
{ .annotate }

1.    Don't worry about the wonky notation just yet; it's called *Bra-Ket notation* and we'll talk about that in the [next section](bra-ket-notation.md).

However, for reasons we have yet to get in to, if we take a scalar $\lambda$ (remember, scalars are complex from now on), and multiply that with the state $\ket{\psi}$:

$$
\lambda\ket{\psi},
$$

that expression has absolutely **no physically observable difference** to the original state $\ket{\psi}$. Therefore, a single quantum state can be represented by an infinitude of different vectors, as long as the difference between those vectors is just a scalar factor $\lambda$.

The reason this matters is because if you were to answer the question "what is a quantum state" with "a vector in Hilbert space", that would be comparable to answering the question "what is a line" with "that dot over there". Well, not really, because a vector has a direction too, but the point remains.

## Inner products
We are used to being able to take the dot product of any two vectors in the context of "normal" vector spaces. In $\mathcal{H}$, the corresponding operation is the *inner product*.

"A Hilbert space is a **vector space** equipped with an **inner product** such that the norm, which is defined as $|f| = \sqrt{f \cdot f}$, turns the space into a **complete metric space**"

## References
<span id="griffiths">[1]</span> D. J. Griffiths, D. F. Schroeter, *Introduction to Quantum Mechanics*, 3rd ed. Cambridge, U.K.: Cambridge Univ. Press, 2018, [doi: 10.1017/9781316995433](https://doi.org/10.1017/9781316995433).