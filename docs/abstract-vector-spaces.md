# Abstract vector spaces
Abstract linear algebra is what happens when we do normal linear algebra, but we stop caring about the details of what a vector "actually" is. Instead, we just formulate a set of definitions (the same ones as in normal linear algebra, in fact), and base all our logic on those definitions. In other words, we take the findings of normal linear algebra and abstract them so that we are able to apply them to a wider range of objects and topics.

For example, consider the vector space $R^3$. It contains any vector in any direction you can literally think of. You can add any two (or more) vectors, stretch or shrink them by multiplying them with scalars, all to your heart's content. Also, you can condense the information of a vector space into just a set of basis vectors, which you can then use as a kind of common language to express any vector in the space. The basis vectors can be arbitrarily chosen, as long as there is at least one representative of each direction of the space, which in math is called linear independence.

!!! tip "Properties of vector spaces"

    **Addition**

    1. We can add two vectors to get a third: $\vec{v} + \vec{u} = \vec{w}$
    2. The order doesn't matter: $\vec{u} + \vec{v} = \vec{v} + \vec{u}$
    3. To actually perform a vector addition, we add component-wise: $(v_1, \dots, v_n) + (u_1, \dots, u_n) = (v_1 + u_1, \dots, v_n + u_n)$

    **Scalar multiplication**

    1. We can multiply a vector by a scalar, possibly complex, to get another vector: $\lambda\vec{v} = \vec{u}$
    2. Scalars can be moved around freely

Now, let's consider the set of all polynomials $\mathcal{P}(x)$.

Say we have two polynomials $p_1(x)$ and $p_2(x)$. No matter what $p_1(x)$ and $p_2(x)$ actually are, the result will always be another polynomial, with the same degree as whichever of $p_1(x)$ or $p_2(x)$ had the highest degree. We can multiply a polynomial by a scalar.