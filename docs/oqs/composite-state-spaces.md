# Composite state spaces
In order for us to be able to talk about more complex quantum behaviour, we'll need to introduce composite state spaces. We use these to describe systems involving two or more quantum subsystems, which means that we could for example describe a quantum system of two or more particles.

Composite state spaces are realized through the use of the tensor product of the component state spaces, resulting in a tensor space. Exploring this notion of tensor spaces will eventually lead us to the phenomenon of entanglement.

## Tensor product
Say we have two Hilbert spaces $\mathcal{H}_1$ and $\mathcal{H}_2$. We can construct another Hilbert space $H$ that is a composition of $\mathcal{H}_1$ and $\mathcal{H}_2$ by taking the *tensor product* ($\otimes$) of the spaces:

$$
\mathcal{H} = \mathcal{H}_1 \otimes \mathcal{H}_2.
$$

If $\mathcal{H}_1$ is spanned by $n$ basis vectors $\{a_1, a_2, \dots, a_n\}$ and $\mathcal{H}_2$ is spanned by $m$ basis vectors $\{\ket{b_1}, \ket{b_2}, \dots, \ket{b_m}\}$, then the tensor product space $\mathcal{H} = \mathcal{H}_1 \otimes \mathcal{H}_2$ is spanned by the following $mn$ basis vectors:

$$
\{\ket{a_1} \otimes \ket{b_1}, \ket{a_1} \otimes \ket{b_2}, \dots, \ket{b_1} \otimes \ket{a_1}, \ket{b_1} \otimes \ket{a_2}, \dots \ket{a_n} \otimes \ket{b_m}\}
$$

So in other words, if $\mathcal{H}_1$ is $n$-dimensional and $\mathcal{H}_2$ is $m$-dimensional, then $\mathcal{H} = \mathcal{H}_1 \otimes \mathcal{H}_2$ is $mn$-dimensional.

!!! info "Properties of the tensor product"
    Say we have two state vectors $\ket{u_1}$ and $\ket{u_2}$ from a Hilbert space $U$, and two state vectors $\ket{v_1}$ and $\ket{v_2}$ from another Hilbert space $V$. Then, for a tensor space $\mathcal{H} = U \otimes V$:
    
    - **Distribution to the right**: $\ket{u_1} \otimes (\ket{v_1} + \ket{v_2}) = \ket{u_1} \otimes \ket{v_1} + \ket{u_1} \otimes \ket{v_2}$
    - **Distribution to the left**: $(\ket{u_1} + \ket{u_2}) \otimes \ket{v_1} = \ket{u_1} \otimes \ket{v_1} + \ket{u_2} \otimes \ket{v_1}$
    - **Scalars move freely**: $(\alpha\ket{u_1}) \otimes \ket{v_1} = \alpha(\ket{u_1} \otimes \ket{v_1}) = \ket{u_1} \otimes (\alpha \ket{v_1})$

Now, let's say we have two qubits, $\mathcal{H}_1, \mathcal{H}_2 \in \mathbb{C}^2$, and we want to describe the composite system $\mathcal{H}_1 \otimes \mathcal{H}_2$.

We denote the basis vectors of $\mathcal{H}_1$ as $\ket{0}_1$ and $\ket{1}_1$, and the basis vectors of $\mathcal{H}_2$ as $\ket{0}_2$ and $\ket{1}_2$. The basis vectors of $\mathcal{H}_1 \otimes \mathcal{H}_2$ are then:

$$
\{\ket{0}_1 \otimes \ket{0}_2, \ket{0}_1 \otimes \ket{1}_2, \ket{1}_1 \otimes \ket{0}_2, \ket{1}_1 \otimes \ket{1}_2 \}
$$

When we use tensor products in conjunction with bra-ket notation, it is very common to completely omit the $\otimes$-symbol and just write $\ket{\psi} \otimes \ket{\phi} = \ket{\psi}\ket{\phi}$. Furthermore, it is also very common to write these into one ket as $\ket{\psi} \otimes \ket{\phi} = \ket{\psi\phi}$, especially when dealing with qubits. Therefore we will rewrite the basis of $\mathcal{H}_1 \otimes \mathcal{H}_2$ as:

$$
\{\ket{00}, \ket{01}, \ket{10}, \ket{11}\}.
$$

Note that the order of the 1s and 0s tells us which of the two qubits are in which state, e.g. in state $\ket{01}$, the first qubit $\mathcal{H}_1$ is in state $\ket{0}$ and the second qubit $\mathcal{H}_2$ is in state $\ket{1}$.


### Separable vs. entangled states
Say we have a Hilbert space $\mathcal{H}_1$ with an orthonormal basis $\{\ket{e_i}\}$, and another Hilbert space $\mathcal{H}_2$ with an orthonormal basis $\{\ket{f_j}\}$.

We can write an arbitrary state vector in either of the spaces in terms of the basis vectors of the space. So, if we have a ket $\ket{\psi_1} \in \mathcal{H}_1$, we can write it as:

$$
\ket{\psi_1} = \sum_i{c_i \ket{e_i}}, \quad\quad c_i = \braket{e_i | \psi_1}.
$$

Likewise, we can write a ket $\ket{\psi_2} \in \mathcal{H}_2$ as:

$$
\ket{\psi_2} = \sum_j{c_j \ket{f_j}}, \quad\quad c_j = \braket{f_j | \psi_2}.
$$

If we form the tensor space $\mathcal{H}_1 \otimes \mathcal{H}_2$, we can then write an arbitrary ket $\ket{\psi} \in \mathcal{H}_1 \otimes \mathcal{H}_2$ like this:

$$
\begin{align}
    \ket{\psi} = \ket{\psi_1} \otimes \ket{\psi_2} \Leftrightarrow\\
    \ket{\psi} = \Bigl(\sum_i{c_i \ket{e_i}}\Bigr) \otimes \Bigl(\sum_j{c_j \ket{f_j}}\Bigr) \Leftrightarrow\\
    \ket{\psi} = \sum_{i,j}{c_i c_j \Bigl(\ket{e_i} \otimes \ket{f_j}\Bigr)}.
\end{align}
$$

Since $c_i \in \mathbb{C}$ and $c_j \in \mathbb{C}$ are complex scalars, the product $c_i c_j$ is also a complex scalar, so we can write it as $c_i c_j = c_{ij} \in \mathbb{C}$, arriving at the final expression:

$$
\ket{\psi} = \sum_{i,j}{c_{ij} \Bigl(\ket{e_i} \otimes \ket{f_j}\Bigr)}.
$$

So we can write any state in the tensor space in terms of the basis vectors of the respective component spaces.

!!! info "Separable states"
    A state $\ket{\psi} \in \mathcal{H}_1 \otimes \mathcal{H}_2$ is separable if it consists of a single tensor product where one of the component vectors is from the first space, and the other component vector is from the second space.
    
    In other words, $\ket{\psi} \in \mathcal{H}_1 \otimes \mathcal{H}_2$ is separable if:

    $$
    \ket{\psi} = \ket{\psi_1} \otimes \ket{\psi_2}, \quad\quad \ket{\psi_1} \in \mathcal{H}_1, \ket{\psi_2} \in \mathcal{H}_2,
    $$

    or

    $$
    \ket{\psi} = \ket{\psi_2} \otimes \ket{\psi_1}, \quad\quad \ket{\psi_1} \in \mathcal{H}_1, \ket{\psi_2} \in \mathcal{H}_2.
    $$

Obviously, only a subset of all possible states of $\mathcal{H}_1 \otimes \mathcal{H}_2$ are separable.

Consider a general state of a system of two qubits, $\ket{\psi} \in \mathcal{H}_1 \otimes \mathcal{H}_2$:

$$
\ket{\psi} = c_{00}\ket{00} + c_{01}\ket{01} + c_{10}\ket{10} + c_{11}\ket{11}.
$$

This state is separable if we can write it as a pure tensor. If we let $\ket{0_1}$ and $\ket{1_1}$ be the orthonormal basis vectors for $\mathcal{H}_1$, and $\ket{0_2}$ and $\ket{1_2}$ the orthonormal basis vectors for $\mathcal{H}_2$, we can express this condition as:

$$
c_{00}\ket{00} + c_{01}\ket{01} + c_{10}\ket{10} + c_{11}\ket{11} = \Bigl(\alpha\ket{0_1} + \beta\ket{1_1}\Bigr) \otimes \Bigl(\gamma\ket{0_2} + \delta\ket{1_2}\Bigr).
$$

We can rewrite the right-hand side:

$$
\begin{align}
    \Bigl(\alpha\ket{0_1} + \beta\ket{1_1}\Bigr) \otimes \Bigl(\gamma\ket{0_2} + \delta\ket{1_2}\Bigr) =\\
    (\alpha\ket{0_1}) \otimes (\gamma\ket{0_2}) + (\alpha\ket{0_1}) \otimes (\delta\ket{1_2}) + (\beta\ket{1_1}) \otimes (\gamma\ket{0_2}) + (\beta\ket{1_1}) \otimes (\delta\ket{1_2}) =\\
    \alpha\gamma(\ket{0_1} \otimes \ket{0_2}) + \alpha\delta(\ket{0_1} \otimes \ket{1_2}) + \beta\gamma(\ket{1_1} \otimes \ket{0_2}) + \beta\delta(\ket{1_1} \otimes \ket{1_2}) =\\
    \alpha\gamma\ket{00} + \alpha\delta\ket{01} + \beta\gamma\ket{10} + \beta\delta\ket{11}.
\end{align}
$$

Comparing this with the left-hand side of the expression we had before, we get that:

$$
\begin{cases}
    \alpha\gamma = c_{00},\\
    \alpha\delta = c_{01},\\
    \beta\gamma = c_{10},\\
    \beta\delta = c_{11}.
\end{cases}
$$

We'll assume here that $\alpha, \beta, \gamma, \delta$ are all nonzero. This makes this part a bit incomplete, but one can easily go through each case ($\alpha = 0$, $\beta = 0$, etc.) and see that $\ket{\psi}$ is separable for all those cases.

Solving the first two equations for $\gamma$ and $\delta$, we get:

$$
\begin{align}
    \alpha\gamma = c_{00} \Leftrightarrow \gamma = \frac{c_{00}}{\alpha},\\
    \alpha\delta = c_{01} \Leftrightarrow \delta = \frac{c_{01}}{\alpha}.\\
\end{align}
$$

We can insert these into the second two equations to get:

$$
\begin{align}
    \beta\gamma = c_{10} \Leftrightarrow \beta\Bigl(\frac{c_{00}}{\alpha}\Bigr) = c_{10} \Leftrightarrow \beta = \alpha \frac{c_{10}}{c_{00}}\\
    \beta\delta = c_{11} \Leftrightarrow \beta\Bigl(\frac{c_{01}}{\alpha}\Bigr) = c_{11} \Leftrightarrow \beta = \alpha \frac{c_{11}}{c_{01}}.
\end{align}
$$

Since we have two different expressions for $\beta$, we can set them equal to each other to get:

$$
\begin{align}
    \alpha \frac{c_{10}}{c_{00}} = \alpha \frac{c_{11}}{c_{01}} \Leftrightarrow\\
    \frac{c_{10}}{c_{00}} = \frac{c_{11}}{c_{01}} \Leftrightarrow\\
    c_{01}c_{10} = c_{00}c_{11} \Leftrightarrow\\
    c_{00}c_{11} - c_{01}c_{10} = 0.
\end{align}
$$

So what have we found? This is the condition that a two-qubit state needs to fulfil in order to be factorizable, i.e. separable. If $c_{00}c_{11} - c_{01}c_{10} \neq 0$, then the state is *entangled*.

## Operators
Operators on a composite state space, $\mathcal{H}_1 \otimes \mathcal{H}_2$, will be on the form $\hat{A} \otimes \hat{B}$, and act on pure tensors $\ket{\psi} \otimes \ket{\varphi}$ as follows:

$$
(\hat{A} \otimes \hat{B})(\ket{\psi} \otimes \ket{\varphi}) = \hat{A}\ket{\psi}\hat{B}\ket{\varphi}.
$$

So the two factors of an operator $\hat{A} \otimes \hat{B}$ can be thought of as acting on each corresponding factor of the tensor.

We can therefore write operators that only act on one of the components as either $\hat{A} \otimes \mathbb{I}$ or $\mathbb{I} \otimes \hat{A}$, depending on which component we want it to act on. The state vector corresponding to the identity operator $\mathbb{I}$ will be left unchanged.

Finally, we can combine the rules of tensor products introduced earlier to evaluate an expression like the following:

$$
\begin{align}
    \Bigl( \hat{A} \otimes \hat{B} + \hat{C} \otimes \hat{D} \Bigr)\bigl( \ket{\psi} \otimes \ket{\varphi} \bigr) =\\
    \Bigl( \hat{A} \otimes \hat{B} \Bigr) \Bigl(\ket{\psi} \otimes \ket{\varphi}\Bigr) + \Bigl(\hat{C} \otimes \hat{D}\Bigr)\Bigl(\ket{\psi} \otimes \ket{\varphi}\Bigr) =\\
    \hat{A}\ket{\psi} \otimes \hat{B}\ket{\varphi} + \hat{C}\ket{\psi} \otimes \hat{D}\ket{\varphi}.
\end{align}
$$

## Expectation value
If we describe the state of a system with a density operator $\hat{\rho}$, the expectation value of an operator $\hat{A} \otimes \hat{B}$ with the state:

$$
\braket{\hat{A} \otimes \hat{B}} = \mathbf{tr}\Bigl[\hat{\rho}(\hat{A} \otimes \hat{B})\Bigr].
$$