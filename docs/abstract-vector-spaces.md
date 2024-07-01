# Abstract vector spaces
!!! info "Why is this relevant?"

    The language of quantum mechanics is linear algebra, and everything we do is done in special vector spaces called Hilbert spaces. Hilbert spaces can be infinite-dimensional (don't worry, we'll get there), and the "vectors" we work with aren't really vectors in the sense you'd learn about in a basic linear algebra course. Instead, they are functions.

## What we mean by "abstract"

Abstract linear algebra is what happens when we do normal linear algebra, but we stop caring about the details of what a vector "actually" is. Instead, we just formulate a set of definitions (the same ones as in normal linear algebra, in fact), and base all our logic on those definitions - we make no additional assumptions about the underlying mathematical objects. In other words, we take the findings of normal linear algebra and abstract them so that we are able to apply them to a wider range of objects and topics.

For example, consider the vector space $R^3$. It contains any vector in any direction you can literally think of. You can add any two (or more) vectors, stretch or shrink them by multiplying them with scalars, all to your heart's content. Also, you can condense the information of a vector space into just a set of basis vectors, which you can then use as a kind of common language to express any vector in the space. The basis vectors can be arbitrarily chosen, as long as there is at least one representative of each direction of the space, which in math is called linear independence.

If we play around with vectors like this for a while, we will start noticing certain properties that seem to be universal for all vector spaces. Formally, there are eight such properties, and we'll use them as axioms for defining what a vector space actually is.

## What makes a vector space?
!!! note "Vector spaces"

    A **vector space** is a set $V$, that has an **addition operation** ($+$) and a **scalar multiplication operation** ($\cdot$), for which the following eight axioms hold (assume that all symbols with an arrow &mdash; e.g. $\vec{v}$ &mdash; are elements of the set $V$, and all (lowercase) symbols without an arrow &mdash; e.g. $a$ &mdash; are scalars)[\[1\]](#smits):

    1. When adding elements, the order of the arguments doesn't matter: $\vec{v} + \vec{u} = \vec{u} + \vec{v}$
    2. When adding more than two arguments, it doesn't matter which two arguments we add together first: $(\vec{u} + \vec{v}) + \vec{w} = \vec{u} + (\vec{v} + \vec{w})$
    3. There is a special element $\vec{0} \in V$ that, when added to any other element $\vec{v}$, leaves $\vec{v}$ unchanged: $\vec{v} + \vec{0} = \vec{v}$
    4. Every single element $\vec{v}$ has an opposite $-\vec{v} \in V$, so that when you add them together, you get $\vec{0}$: $\vec{v} + (-\vec{v}) = \vec{0}$
    5. When multiplying the scalar $1$ with any element $\vec{v}$, that element remains unchanged: $1 \cdot \vec{v} = \vec{v}$
    6. There is a distributive rule for sums of scalars like so: $(a + b)\cdot\vec{v} = a \cdot \vec{v} + b \cdot \vec{v}$
    7. When multiplying multiple scalars with elements of $V$, the order doesn't matter: $(a \cdot b) \cdot \vec{v} = a \cdot (b \cdot \vec{v})$
    8. There is a distributive rule for sums of elements like so: $a \cdot (\vec{v} + \vec{u}) = a \cdot \vec{v} + a \cdot \vec{u}$

I'm playing a little fast and loose with the term "scalar" here. At this point, just assume that a scalar is a real number.

All of these properties probably feel quite trivial. There are some interesting things to note though. First, the way we've written it, whenever we use scalar multiplication we always write the scalar on the left and the element of $V$ on the right. Second &mdash; and most important &mdash; we're really not making any assumptions about the elements of $V$ at all. What this list of properties is really telling us are expectations about how the operations of addition and scalar multiplication behave. So what makes a vector space a vector space really isn't the vectors themselves; it's what we can do with them.

## *That's* a vector space?
Let's consider the set of all polynomials of degree $n \leq 2$. We'll denote this set as $\mathcal{P}^2$.

Let's grab three elements of $\mathcal{P}^2$; call them $p_1(x)$, $p_2(x)$, and $p_3(x)$.

Is $\mathcal{P}^2$ a vector space? Let's check:

1. Does the order matter when adding two elements, like $p_1(x) + p_2(x)$? No, so **check!**
2. If we add more than two elements together, does the order in which we do things matter? Nope, so **check!**
3. Is there a weird element that leaves other elements unchanged when adding it to them? With all coefficients equal to 0, we just get zero, so zero is technically a polynomial in the set, so **check!**
4. Does every polynomial have an opposite, so that if we add it with its opposite we get zero? If we take a polynomial, copy it, and reverse the signs of all coefficients of the copy, then we get exactly such an opposite. So **check!**
5. If we multiply any polynomial with the scalar 1, we get that same polynomial back. So **check!**
6. Does the distributive rule for sums of scalars work as expected? $(a + b)p_1(x) = ap_1(x) + bp_1(x)$, so yup, and **check!**
7. Does the order matter when multiplying with more than one scalar? $(ab)p_1(x) = abp_1(x) = a(bp_1(x))$ &mdash; it does not, so **check!**
8. Does the distributive rule for sums of elements work as expected? $a(p_1(x) + p_2(x)) = ap_1(x) + ap_2(x)$, so yes it does &mdash; **check!**

Why, look at that! It seems that our set is a vector space.

"Okay," you say. "So what?"

Well, now that we know that these polynomials really are just vector spaces in fancy outfits, we can apply all we know about "normal" vector spaces to them.

## References
<span id="smits">[1]</span> T. Smits. (2023). Abstract Linear Algebra [Online]. Available: [https://www.math.ucla.edu/~tsmits/115coursenotes.pdf](https://www.math.ucla.edu/~tsmits/115coursenotes.pdf)