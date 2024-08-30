# Density operator
The density operator is part of another way of doing quantum mechanics than the state vector-centered one we have been using so far.

There are two main interpretations of the density operator, which turn out to be mathematically indistinguishable.

The first is as a way of including the notion of *mixed states* in the theory, through the lense of classical uncertainty. So we might have a situation where we have a quantum system that is in a superpositioned state, e.g. $\ket{\psi} = c_1\ket{\psi_1} + c_2\ket{\psi_2}$. Quantum mechancis teaches us that there is a probabilistic aspect of this situation, in that when we measure the system, we'll get one of the eigenvalues of the observable we measured with a certain probability given by the Born rule. However, there might also be additional uncertainty which is introduced if we only have *partial information* about the system. In that case, we might not even know what state we're dealing with in the first place, but we might know that it must be one of a set of states. If so, there is an additional classical probabilistic aspect to the system. We call such states mixed states.

The other interpretation is that we actually have two systems that are interacting with each other, such as is the case when a quantum system is *open* and is interacting with its environment.

We will first focus on the first interpretation, as that seems to me to be the more common one.

## Density operator for pure states
A pure state is a state for which we have **full information**. We can represent it with a ket $\ket{\psi}$, for which we can predict the time evolution using the Schrödinger equation.

As seen before, even if we have full information about the state, there is still a probabilistic aspect which comes from the act of performing a measurement of the state.