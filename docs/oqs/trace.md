# Trace
The following is all from [Wikipedia](https://en.wikipedia.org/w/index.php?title=Trace_(linear_algebra)&oldid=1235691329).

The trace of an operator (which we here will take to be a square matrix) is defined as the sum of its diagonal elements:

$$
\text{tr}(\hat{A}) = \sum_i{a_{ii}}.
$$

The trace is linear, which means that for two operators $\hat{A}$ and $\hat{B}$ as well as a scalar $c$, it is the case that:

$$
\begin{align}
    \mathbf{tr}(\hat{A} + \hat{B}) = \mathbf{tr}(\hat{A}) + \mathbf{tr}(\hat{B}),\\
    \mathbf{tr}(c\hat{A}) = c\mathbf{tr}(\hat{A}).
\end{align}
$$

Taking the trace of the product $\hat{A}\hat{B}$ is the same as taking the trace of the product $\hat{B}\hat{A}$:

$$
\mathbf{tr}(\hat{A}\hat{B}) = \mathbf{tr}(\hat{B}\hat{A}).
$$

The above can be further generalized in the **cyclic property** of the trace. If we have $n + 1$ different operators $\hat{A}_i, \hat{A}_{i+1}, \dots, \hat{A}_{i + n}$, it is the case that:

$$
\mathbf{tr}(\hat{A}_i\hat{A}_{i + 1}\dots\hat{A}_{i + n}) = \mathbf{tr}(\hat{A}_{i + 1}\dots\hat{A}_{i + n}\hat{A}_i).
$$

So for example, if we have operators $\hat{A}$, $\hat{B}$, $\hat{C}$, and $\hat{D}$, we have:

$$
\begin{align}
    &\mathbf{tr}(\hat{A}\hat{B}\hat{C}\hat{D}) =\\
    &\mathbf{tr}(\hat{B}\hat{C}\hat{D}\hat{A}) =\\
    &\mathbf{tr}(\hat{C}\hat{D}\hat{A}\hat{B}) =\\
    &\mathbf{tr}(\hat{D}\hat{A}\hat{B}\hat{C}).
\end{align}
$$

Taking the trace of a tensor product $\hat{A} \otimes \hat{B}$ is the same as taking the product of the individual traces:

$$
\mathbf{\hat{A} \otimes \hat{B}} = \mathbf{tr}(\hat{A}) \mathbf{tr}(\hat{B}).
$$

The trace of an operator $\hat{A}$ is also the sum of the eigenvalues of $\hat{A}$:

$$
\mathbf{tr}(\hat{A}) = \sum_i{\lambda_i},
$$

where $\{\lambda_i\}$ is the set of eigenvalues of $\hat{A}$. Compare this to the determinant of $\hat{A}$:

$$
\text{det}(\hat{A}) = \prod_i{\lambda_i}.
$$

We can write Born's rule in terms of the trace. Say we have a qubit with basis vectors $\{e_{0}, e_{1}\}$, whose (pure) state is represented as a density operator $\hat{\rho} = \ket{\psi}\bra{\psi}$, and we measure some observable $\hat{A}$ with orthonormal basis $$

$$
\begin{align}
    \mathbf{tr}\Bigl(\hat{\rho} \ket{e_0}\bra{e_0}\Bigr) =\\
    \mathbf{tr}\Bigl(\ket{\psi}\bra{\psi} \ket{e_0}\bra{e_0}\Bigr) =\\
    \mathbf{tr}\Bigl(\braket{\psi | e_0}\ket{\psi}\bra{e_0}\Bigr) =\\
    \braket{\psi | e_0}\mathbf{tr}\Bigl(\ket{\psi}\bra{e_0}\Bigr) =\\
    \braket{\psi | e_0} \Bigl(\bra{e_0} (\ket{\psi}\bra{e_0}) \ket{e_0} + \bra{e_1} (\ket{\psi}\bra{e_0}) \ket{e_1}\Bigr) =\\
    \braket{\psi | e_0} \Bigl(\braket{e_0 | \psi}\braket{e_0 | e_0} + \braket{e_1 | \psi}\braket{e_0 | e_1}\Bigr) =\\
    \braket{\psi | e_0} \Bigl(\braket{e_0 | \psi} \times 1 + \braket{e_1 | \psi} \times 0\Bigr) =\\
    \braket{\psi | e_0} \braket{e_0 | \psi} =\\
    |\braket{\psi | e_0}|^2.
\end{align}
$$

The trace is scalar-valued &mdash; it outputs a scalar.

Lastly, we can also express the expectation value of an operator $\hat{A}$ and a state vector $\ket{\psi}$ as:

$$
\braket{\hat{A}}_\psi = \braket{\psi | \hat{A} | \psi} = \mathbf{tr}(\hat{A}\ket{\psi}\bra{\psi}).
$$

## Partial trace and the partial density operator
Lorem ipsum