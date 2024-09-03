# Projection operators
When we start talking about the collapse of the wave function and what happens to a quantum state after it is measured, we'll inevitebly encounter the concept of projection operators. Like the name implies, the projection operator projects one state onto another, allowing us to mathematically describe the collapse of a state at measurement.

## Outer product
We've previously talked about the inner product, introducing the notion of a bracket $\braket{\psi | \phi}$.

So if we have "bra-kets", is it possible to have a "ket-bra"? The answer is yes, and it's written like $\ket{\phi}\bra{\psi}$(1).
{ .annotate }

1.    In handwriting, we usually write the left and right angle brackets without the space in the middle, a bit like a cross: $|\phi \times \psi |$. To avoid confusion though, I will stick to $\ket{\phi}\bra{\psi}$.

We call this operation $\ket{\phi}\bra{\psi}$ the *outer product*, and in contrast to the inner product, the result of this is an operator.

!!! info "Inner vs. outer product, result type"
    Let $\ket{\psi}$ and $\ket{\phi}$ be two state vectors in $\mathcal{H}$.

    - The **inner product** $\braket{\psi | \phi} = a \in \mathbb{C}$ results in a complex number.
    - The **outer product** $\ket{\phi} \bra{\psi} = \hat{A} \in \mathbb{C}^{n \times n}$ results in an operator, which can be written as a matrix.

## Projection operators as outer products
Say we have a normalized state vector $\ket{\psi}$, such that $\braket{\psi | \psi} = 1$. We define the *projection operator* $\hat{P}_\psi$ as the outer product of the state with itself:

$$
\hat{P}_\psi = \ket{\psi}\bra{\psi}.
$$

As $\hat{P}_\psi$ is an operator, we can begin by investigating its effect on a state vector $\ket{\phi}$:

$$
\hat{P}_\psi\ket{\phi} = \bigl(\ket{\psi}\bra{\psi}\bigr)\ket{\phi} = \ket{\psi}\braket{\psi | \phi} = \braket{\psi | \phi}\ket{\psi}.
$$

We know $\braket{\psi | \phi}$ is a complex scalar, so the result of acting on $\ket{\phi}$ with $\hat{P}_\psi$ results in a state vector **in the direction of $\ket{\psi}$**, scaled with some number $\braket{\psi | \phi}$.

!!! info "Properties of the projection operator"
    The projection operator $\hat{P}_\psi = \ket{\psi}\bra{\psi}$ has the following properties:
    
    - **Idempotency**: $\hat{P}_\psi^2 = \hat{P}_\psi$
    - **Hermiticity**: $\hat{P}_\psi^\dagger = \hat{P}_\psi$

## References
<span id="prof-m-projection">[1]</span> Professor M does Science, Cambridge, U.K. *Projection operators in quantum mechanics*. (Aug. 6, 2020). Accessed: Sep. 3, 2024. [Online Video]. Available: [https://youtu.be/M9V4hhqyrKQ?si=9LA79kCxyBuuVE3G](https://youtu.be/M9V4hhqyrKQ?si=9LA79kCxyBuuVE3G).