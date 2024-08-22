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

!!! question "Observable vs. operator"
    What is the difference between an observable and an operator?

    ??? success "Answer"
        An operator is a mathematical object which maps a set of states onto another set of states.

        An observable is a measurable physical property of some system. It is not a mathematical object.

        Observables are represented in QM by (Hermitian) operators.