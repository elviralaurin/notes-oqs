# Fundamentals
On this page, we start off with the basics of quantum mechanics (QM). As discussed on the [Reflections page](reflections.md), we will be a little loose with our definitions at first, but hopefully we'll be able to become more rigorous as we get a better understanding for what we're doing.

## State vectors and Hilbert space
The state of a closed physical system can be described by a *state vector* or *wave function* which is an element of some Hilbert space $\mathcal{H}$.

Throughout these notes and in most other QM resources available, state vectors are written in *Dirac notation* and are then called *kets*. A ket is written with a vertical bar (`|`), followed by the name or label of the ket (often a Greek letter like $\psi$(1) or $\phi$(2)), followed by a right-angle bracket (`>`). The following is a ket: $\ket{\psi}$.
{ .annotate }

1.    pronounced "sy", "psy", "see", or "psee", depending on who you ask
2.    pronounced "fy" or "fee", depending on who you ask

$\mathcal{H}$ can be *infinite-dimensional*. If we think of vectors as an ordered list of numbers, this means that the list can be infinitely long. An equivalent way to think about it is that we might need an infinite number of basis vectors to represent a given vector in $\mathcal{H}$.

Another important thing to remember about $\mathcal{H}$ is that whenever we talk about scalars, we mean complex scalars. In other words, vector components are complex, and the scalars we scale vectors with are complex, and so on. Always assume that the numbers we work with are complex, i.e. can include an imaginary term, **unless otherwise specified**.

!!! info "State vector? Ket? Wave function?"
    What is really the difference between a state vector, a ket, and a wave function?

    A **state vector** is a vector in Hilbert space that is associated with a physical state that the system can be in(1).
    { .annotate }
    
    1.    Note that this does **not** mean that the state of the system necessarily corresponds to that exact vector. In other words, a state vector $\bar{v}$ corresponds to one specific physical state $V$ ($\bar{v} \rightarrow V$), but a physical state does not necessarily correspond to that same vector ($V \nrightarrow \bar{v})$. More on this later.

    A **ket** is a state vector in Dirac notation.

    A **wave function** is a complex-valued function that is a mathematical description of a quantum system. It is a different way of representing the state of a quantum system. It is less general than that of the vector representation, as it implicitly chooses a basis.

## The inner product
Just like we can take the dot product of two vectors in Euclidian space, we can take what's called the *inner product* of two kets $\ket{\psi}$ and $\ket{\phi}$ in Hilbert space. The inner product of $\ket{\psi}$ and $\ket{\phi}$ is written $\braket{\psi | \phi}$, and results in a scalar:

$$
\text{inner_prod}(\ket{\psi}, \ket{\phi}) = \braket{\psi | \phi} = c,\quad\quad c \in \mathbb{C}.
$$

Typographically, taking the inner product looks like flipping the first ket and sticking it together with the second ket:

$$
\ket{\psi} \ket{\phi} \rightarrow \bra{\psi} \ket{\phi} \rightarrow \braket{\psi | \phi}
$$

This is no accident. That "flipped ket" $\bra{\phi}$ is called a *bra*, and sticking it together with a ket produces a *bra-ket* &mdash; a bracket. This is all part of Dirac notation, and this idea of brackets is why Dirac notation is also commonly called *bra-ket notation*.

!!!info "Properties of the inner product"
    The inner product $\braket{\psi | \phi}$ of kets $\ket{\psi}, \ket{\phi} \in \mathcal{H}$ has the following properties:
    
    **Conjugation**

    We can invert the order of the arguments by taking the **complex conjugate** of the whole thing: $\braket{\psi | \phi} = (\braket{\phi | \psi})^*$, which is usually just written $\braket{\phi | \psi}^*$.

    **Linearity in the second argument**

    If we multiply the inner product with a scalar $a$, we can "move the scalar in" to the **second argument** like so:

    $$
    a\braket{\psi | \phi} = \bra{\psi} a(\ket{\phi}).
    $$

    Furthermore, if the **second argument** of the inner product is a sum of two kets, say $\ket{\phi} = \ket{\phi_1} + \ket{\phi_2}$, we can "distribute" the inner product like so:

    $$
    \bra{\psi} \Bigl(\ket{\phi_1} + \ket{\phi_2}\Bigr) = \braket{\psi | \phi_1} + \braket{\psi | \phi_2}.
    $$

    As you can see from my choice of words above, I like thinking about this property as corresponding to distributing over parentheses in "regular algebra":
    
    ![Distribution of a scalar over a parenthesis, a bracket, and of a bra over a sum of kets](images/inprod-distr-comp1.png){ width="300" loading=lazy }

## Dual vectors and the adjoint space
!!! quote " "
    "To every ket, there corresponds a bra" &mdash; *Professor M does Science*[[1]](#prof-m-dirac)

Just like the kets live in state space $\mathcal{H}$, the bras live in a space we denote $\mathcal{H}^*$. This space is commonly called the *dual space*.

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

The reason why we have to take the complex conjugate of any scalars when finding the corresponding bra to a ket comes from the definition of the inner product.
<!-- ## Closed vs. open physical systems
A physical system is *closed* if a given quantity of the system, such as matter, stays constant within the system. Nothing enters, nothing exits.

The opposite of a closed physical system is an *open* physical system. As you can probably guess, a physical system is open if the system exchanges a given quantity with its environment. Humans are open physical systems &mdash; we constantly exchange energy and matter with our environment.

Sometimes a system can be closed on one level, and open on another, or it can be closed to a certain quantity, and open to another. It's word that depends on the perspective. -->

<!-- The mathematics of quantum mechanics is done in a special type of vector space we'll call **quantum state space**, or just **state space** [[1]](#prof-m-dirac).

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
-->
## References
<!-- <span id="griffiths">[1]</span> D. J. Griffiths, D. F. Schroeter, *Introduction to Quantum Mechanics*, 3rd ed. Cambridge, U.K.: Cambridge Univ. Press, 2018, [doi: 10.1017/9781316995433](https://doi.org/10.1017/9781316995433). -->
<span id="prof-m-dirac">[1]</span> Professor M does Science, Cambridge, U.K. *Dirac Notation: State Space And Dual Space*. (May 23, 2020). Accessed: Jul. 3, 2024. [Online Video]. Available: [https://www.youtube.com/watch?v=hJoWM9jf0gU](https://www.youtube.com/watch?v=hJoWM9jf0gU).
<!-- <span id="von-neumann">[3]</span> J. von Neumann, *Mathematical Foundations of Quantum Mechanics*, N. A. Wheeler, Ed., 2018 ed. Princeton, NJ, USA: Princeton Univ. Press, 2018, [doi: 10.1017/9781316995433](https://doi.org/10.1017/9781316995433).   -->