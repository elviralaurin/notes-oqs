# Outer product
We've previously talked about the inner product, introducing the notion of a bracket $\braket{\psi | \phi}$.

So is it possible to have a "ket-bra"? The answer is yes, and it's written like $\ket{\phi}\bra{\psi}$(1).
{ .annotate }

1.    In handwriting, we usually write the left and right angle brackets without the space in the middle, a bit like a cross: $|\phi \times \psi |$. To avoid confusion though, I will stick to $\ket{\phi}\bra{\psi}$.

The outer product $\ket{\phi}\bra{\psi}$ is another way of expressing an operator, as the result of executing the outer product results in an operator.

!!! info "Inner vs. outer product, result type"
    Let $\ket{\psi}$ and $\ket{\phi}$ be two state vectors in $\mathcal{H}$.

    - The **inner product** $\braket{\psi | \phi} = a \in \mathbb{C}$ results in a complex number.
    - The **outer product** $\ket{\phi} \bra{\psi} = \hat{A} \in \mathbb{C}^{n \times n}$ results in an operator, which can be written as a matrix.