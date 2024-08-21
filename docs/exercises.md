# Exercises
So far, this page is just a template. Hopefully, content will be added to it over time.

!!! question "Exercise 1"
    Assume you have a quantum system $\mathcal{H}$ consisting of one qubit (a 2D Hilbert space) and one qutrit (a 3D Hilbert space). What is the dimension of $\mathcal{H}$?

    ??? success "Solution"
        The qubit has two dimensions, and therefore has two basis vectors. The qutrit has three dimensions, and therefore has three dimensions.

        A composite system like $\mathcal{H}$ is formed as the tensor product of the component spaces. If the qubit has basis vectors $\{b_i\}$, and the qutrit basis vectors $\{t_j\}$, $\mathcal{H}$ has basis vectors of the form $\ket{b_i} \otimes \ket{t_j}$, where $i$ and $j$ are iterated over all possible combinations. So $\mathcal{H}$ has $2 \times 3 = 6$ basis vectors, resulting in it having 6 dimensions.

        **Answer**: $\mathcal{H}$ has 6 dimensions.

!!! question "Exercise 2"
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