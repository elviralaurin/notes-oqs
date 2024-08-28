# Check yourself
!!! question "Dimensionality of composite systems"
    Assume you have a quantum system $\mathcal{H}$ consisting of one qubit (a 2D Hilbert space) and one qutrit (a 3D Hilbert space). What is the dimension of $\mathcal{H}$?

    ??? success "Answer"
        The qubit has two dimensions, and therefore has two basis vectors. The qutrit has three dimensions, and therefore has three dimensions.

        A composite system like $\mathcal{H}$ is formed as the tensor product of the component spaces. If the qubit has basis vectors $\{b_i\}$, and the qutrit basis vectors $\{t_j\}$, $\mathcal{H}$ has basis vectors of the form $\ket{b_i} \otimes \ket{t_j}$, where $i$ and $j$ are iterated over all possible combinations. So $\mathcal{H}$ has $2 \times 3 = 6$ basis vectors, resulting in it having 6 dimensions.

!!! question "Orthonormal basis representations"
    Write the following in the orthonormal basis $\{\ket{u_i}\}$:
    
    1. the ket $\ket{\psi}$
    2. the bra $\bra{\phi}$
    3. the operator $\hat{A}$
    
    ??? success "Answer"
        $$
        \begin{align}
            \ket{\psi} = \sum_i{c_i\ket{u_i}}, \quad\quad c_i = \braket{u_i | \psi},\\
            \bra{\phi} = \sum_i{c_i^*\bra{u_i}}, \quad\quad c_i^* = \braket{\phi | u_i},\\
            \hat{A} = \sum_{ij}{A_{ij}\ket{u_i}\bra{u_j}}, \quad\quad A_{ij} = \bra{u_i}\hat{A}\ket{u_j}.
        \end{align}
        $$

!!! question "The importance of Hermitian operators"
    What does it mean for an operator to be Hermitian? Why are all operators in QM Hermitian?

    ??? success "Answer"
        An operator $\hat{A}$ is Hermitian if it is equal to its adjoint:

        $$
        \hat{A} = \hat{A}^\dagger.
        $$

        Hermitian operators have two important properties: they have real eigenvalues, and their eigenstates are orthogonal.

        The result of a measurement of an observable will always be one of the corresponding operator's eigenvalues. In order for this to make sense for physical systems, this implies that the corresponding operator must have real eigenvalues.

        Furthermore, we need the eigenstates of the operators to be orthogonal because otherwise we allow for measurement outcomes which are linear combinations of other states, i.e. in a superposition. While systems can be in a superpositioned state before measurement, the act of measuring cannot resolve to a superpositioned state. Once we open the box containing Schrödinger's cat, the cat is either dead or alive, but not both.

        To ensure these properties, we represent physical observables with Hermitian operators.

!!! question "Result of the inner product"
    What can be said about:
    
    1. the result of the inner product of two different state vectors $\ket{\psi}$ and $\ket{\phi}$?
    2. the result of the inner product of a state vector $\ket{\psi}$ with itself?
    3. the state vector which, if you take the inner product of it with itself, results in 0?
    4. two different state vectors which, if you take the inner product of them, results in 0?

        ??? success "Answer"
            1\. The result of the inner product of two different state vectors is a complex number: $\braket{\psi | \phi} = c \in \mathbb{C}$.

            2\. The result of the inner product of a state vector with itself is a real, positive number: $\braket{\psi | \psi} = a \in \mathbb{R}_{\geq 0}$.

            3\. If the result of the inner product of a state vector with itself is 0, then that state vector is the null ket $\ket{\psi}$: $\braket{\psi | \psi} = 0 \Rightarrow \ket{\psi} = \ket{\text{null}}$

            4\. If the result of the inner product of two different state vectors is 0, then the two state vectors are orthogonal: $\braket{\psi | \phi} = 0 \land \ket{\psi} \neq \ket{\phi} \Rightarrow \ket{\psi} \perp \ket{\phi}$.

!!! question "Measuring a quantum system that is in an eigenstate"
    Say you want to measure some property with corresponding operator $\hat{A}$ of a system that is in state $\ket{\psi} = \ket{\lambda_0}$, where $\ket{\lambda_0}$ is one of the eigenstates of $\hat{A}$. What are the possible outcomes of this measurement? Assume normalized eigenstates.

    ??? success "Answer"
        The Born rule gives us:

        $$
        P(\lambda_n) = |\braket{\lambda_n | \psi}|^2,
        $$

        where $\ket{\psi}$ is the current state of the system. So if $\ket{\psi} = \ket{\lambda_0}$, we get:

        $$
        P(\lambda_0) = |\braket{\lambda_0 | \lambda_0}|^2 = |1|^2 = 1,
        $$

        since the eigenvectors are normalized.

        Since the probabilities of the total set of possible outcomes must sum to 1, this means that all other eigenstates have a zero probability.

!!! question "Example: probabilities and the expectation value"
    Say we measure the observable $\hat{A}$ of a system in state $\ket{\psi}$. $\hat{A}$ has two eigenvalues, $\lambda_+$ and $\ket{\lambda_-}$, such that the eigenvalue equations are given by:

    $$
    \begin{align}
        \hat{A}\ket{\lambda_+} = \ket{\lambda_+},\\
        \hat{A}\ket{\lambda_-} = -\ket{\lambda_-}.
    \end{align}
    $$

    The current state is given by $\ket{\psi} = \frac{1}{\sqrt{2}}(\ket{\lambda_+} + \ket{\lambda_-})$.

    Calculate the following:

    1. The probability of measuring $\lambda_+$
    2. The probability of measuring $\lambda_-$
    3. The expectation value $\braket{\hat{A}}_\psi$
    
    ??? success "Answer"
        We use the Born rule to find the probabilities:

        $$
        \begin{align}
            P(\lambda_+) = |\braket{\lambda_+ | \psi}|^2 = |\braket{\lambda_+ | \psi}|^2
        \end{align}
        $$

!!! question "Hermitian and unitary eigenvalues"
    What special properties do the eigenvalues of Hermitian operators have? What special properties do the eigenvalues of unitary operators have?
    
    ??? success "Answer"
        Hermitian operators have real eigenvalues, which is one of the main reasons why they are used to represent physical properties.

        Unitary operators have complex eigenvalues with magnitude 1.