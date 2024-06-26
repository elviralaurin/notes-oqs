# Abstract vector spaces
!!! info "Why is this relevant?"

    The language of quantum mechanics is linear algebra, and everything we do is done in special vector spaces called Hilbert spaces. Hilbert spaces can be infinite-dimensional (don't worry, we'll get there), and the "vectors" we work with aren't really vectors in the sense you'd learn about in a basic linear algebra course. Instead, they are functions.

Abstract linear algebra is what happens when we do normal linear algebra, but we stop caring about the details of what a vector "actually" is. Instead, we just formulate a set of definitions (the same ones as in normal linear algebra, in fact), and base all our logic on those definitions. In other words, we take the findings of normal linear algebra and abstract them so that we are able to apply them to a wider range of objects and topics.

For example, consider the vector space $R^3$. It contains any vector in any direction you can literally think of. You can add any two (or more) vectors, stretch or shrink them by multiplying them with scalars, all to your heart's content. Also, you can condense the information of a vector space into just a set of basis vectors, which you can then use as a kind of common language to express any vector in the space. The basis vectors can be arbitrarily chosen, as long as there is at least one representative of each direction of the space, which in math is called linear independence.

If we play around with vectors like this for a while, we will start noticing certain properties that any vector space has to have in order to actually be a vector space. Formally, there are eight such properties, and we'll use them as axioms for defining what a vector space actually is.[^smits]

!!! note "Vector spaces"

    A **vector space** is a set $V$, that has an **addition operation** ($+$) and a **scalar multiplication operation** ($\cdot$), for which the following eight axioms hold (assume that all symbols with an arrow (e.g. $\vec{v}$) are elements of $V$, and all lowercase symbols without an arrow (e.g. $a$), are scalars):

    1. When adding elements, the order of the arguments doesn't matter: $\vec{v} + \vec{u} = \vec{u} + \vec{v}$
    2. When adding more than two arguments, it doesn't matter which two arguments we add together first: $(\vec{u} + \vec{v}) + \vec{w} = \vec{u} + (\vec{v} + \vec{w})$
    3. There is a special element $0 \in V$ that, when added to any other element $\vec{v} \in V$, leaves $\vec{v}$ unchanged: $\vec{v} + 0 = \vec{v}$
    4. Every single elements $\vec{v} \in V$ has an opposite $-\vec{v} \in V$, so that when you add them together, you get $0$: $\vec{v} + (-\vec{v}) = 0$
    5. When multiplying $1$ with any element $\vec{v}$, that element remains unchanged: $1 \cdot \vec{v} = \vec{v}$
    6. There is a distributive rule for sums of scalars like so: $(a + b)\cdot\vec{v} = a \cdot \vec{v} + b \cdot \vec{v}$
    7. When multiplying scalars and elements of $V$, the order doesn't matter: $(a \cdot b) \cdot \vec{v} = a \cdot (b \cdot \vec{v})$
    8. There is a distributive rule for sums of vectors like so: $a \cdot (\vec{v} + \vec{u}) = a \cdot \vec{v} + a \cdot \vec{u}$

I'm playing a little fast and loose with the term "scalar" here. At this point, just assume that a scalar is a real number.

All of these properties probably feel quite trivial. There are some interesting things to note though. First, the way we've written it, whenever we use scalar multiplication we always write the scalar on the left and the element of $V$ on the right.

Now, let's consider the set of all polynomials $\mathcal{P}(x)$.

Say we have two polynomials $p_1(x)$ and $p_2(x)$. No matter what $p_1(x)$ and $p_2(x)$ actually are, the result will always be another polynomial, with the same degree as whichever of $p_1(x)$ or $p_2(x)$ had the highest degree. We can multiply a polynomial by a scalar.

## References
[^smits]:
    T. Smits. (2023). Abstract Linear Algebra [Online]. Available: [https://www.math.ucla.edu/~tsmits/115coursenotes.pdf](https://www.math.ucla.edu/~tsmits/115coursenotes.pdf)