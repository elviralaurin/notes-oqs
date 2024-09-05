# Density operator
The density operator is part of another way of doing quantum mechanics than the state vector-centered one we have been using so far. In other words, even though density operators are commonly used to describe mixed states as we soon shall see, it is completely possible to describe pure states in terms of density operators as well.

## Two perspectives
There are two main perspectives of the density operator, which turn out to be mathematically indistinguishable.

The first is as a way of including the notion of *mixed states* in the theory, through the lense of classical uncertainty.

We can imagine a situation where we have a quantum system that is in a superpositioned state, e.g. $\ket{\psi} = c_1\ket{\psi_1} + c_2\ket{\psi_2}$. Quantum mechancis teaches us that there is a probabilistic aspect of this situation, in that when we measure the system, we'll get one of the eigenvalues of the observable we measured with a certain probability given by the Born rule.

However, there might also be additional uncertainty which is introduced if we only have *partial information* about the system. In that case, we might not even know what state we're dealing with in the first place, but we know that it must be one of a set of states. If so, there is an additional classical probabilistic aspect to the system. We call such states mixed states.

The second perspective of density operators is that we actually have two systems that are interacting with each other, such as is the case when a quantum system is *open* and is interacting with its environment.

We will first focus on the first interpretation, as that seems to me to be the more common one.

## Density operator as an expression of classical uncertainty
Assume we have a system that can be in any one out of $K$ different states. We denote each such state $\ket{\psi_k}, k \in [1, K]$. This situation is what people generally refer to as "mixed state".

For each state $\ket{\psi_k}$, there is an associated probability $p_k$ of the system being in that state. Since the system must be in exactly one of the states, the sum of the probabilities must be one:

$$
\sum_{k=1}^{K}{p_k} = 1.
$$

We now define the density operator $\hat{\rho}$ for a statistical mixture of states $\ket{\psi_k}$ as:

$$
\hat{\rho} = \ket{\psi_k}\bra{\psi_k}.
$$

If you've read the [fundamentals](../fundamentals/index.md), you'll immediately recognize this as a [projection operator](../fundamentals/projection-operators.md).

Now, say that we are measuring the system with respect to some observable $\hat{A}$. $\hat{A}$ has the eigenvalue equation:

$$
\hat{A}\ket{\lambda_n} = \lambda_n\ket{\lambda_n},
$$

and we know that once we measure the system, the result will be one of the eigenvalues $\lambda_n$.

So, given the mixed state, what is the probability $P(\lambda_n)$ of getting a particular eigenvalue $\lambda_n$ as the measurement outcome?

First, we have the probability associated with the quantum measurement that we have seen before:

$$
|\braket{\lambda_n | \psi_k}|^2.
$$

But we're not done here. We also have the classical probability associated with the fact that we have incomplete information about the system. So in total, the probability is:

$$
P(\lambda_n) = p_k|\braket{\lambda_n | \psi_k}|^2.
$$

Using the matrix formulation, we can write the [matrix elements](../fundamentals/operators.md#matrix-elements) of $\hat{\rho}$ in the $u$-basis as:

$$
\begin{align}
    \bra{u_i}\hat{\rho}\ket{u_j} =\\
    \bra{u_i}\bigl( \ket{\psi}\bra{\psi} \bigr)\ket{u_j} =\\
    \braket{u_i | \psi}\braket{\psi | u_j} =\\
    \braket{u_i | \psi}\braket{u_j | \psi}^* =\\
    c_i c_j^*.
\end{align}
$$