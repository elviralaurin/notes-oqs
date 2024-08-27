# Measurement
The measurement of a quantum system and what happens to the system after a measurement has been done is at the core of the strangeness most people associate with quantum mechanics.

What we will find is that it is **impossible** to predict the outcome of a measurement of a quantum system.

This is quite a bold statement. All physical laws we are aware of in the world of classical mechanics are deterministic &mdash; every event has a cause and an effect. If you know *everything* about the state of something at any point in time (i.e. complete, perfect knowledge, if such a thing could exist), it is possible to retrace all past states, and to predict all future states.

When we say that it is impossible to predict the outcome of a quantum measurement, it implies that some things don't have a clear cause and effect. Note that we aren't saying that we just simply don't know how to predict the outcome, we are making the stronger claim of it physically not being possible to know.

I don't know about you, but to me, this claim sounds absolutely insane. Hopefully, we'll be able to shed some light on why this is the best conclusion.

!!! quote " "
    "Richard Feynman, one of the big figures in physics, used to say 'No one understands quantum mechanics.' So in some sense, the pressure is off for you guys, because I don't get it and you don't get it and Feynman doesn't get it. The point is, here is my goal: right now, I am the only one who doesn't understand quantum mechanics. In about seven days, all of you will be unable to understand quantum mechanics." &mdash; *R. Shankar*[[1]](#shankar-l1)

## What happens when we measure a quantum system?
As stated before, one of the postulates of quantum mechanics is that the result of a measurement of a physical quantity is one of the eigenvalues of the associated observable. This is what the word "quantum" alludes to &mdash; the result of a measurement can only be one of a discrete set of outputs.

So we know that if we measure a physical quantity $\mathcal{A}$, it will result in one of the eigenvalues $\lambda_n$ of the corresponding operator $\hat{A}$. But how do we know which $\lambda_n$ we'll get?

!!! info "The Born rule"
    The measurement of $\mathcal{A}$ in a system in normalized state $\ket{\psi}$ gives eigenvalue $\lambda_n$ with probability:

    $$
    P(\lambda_n) = |\braket{\lambda_n | \psi}|^2,
    $$

    where $\ket{\lambda_n}$ is the eigenstate corresponding to eigenvalue $\lambda_n$[[3]](#prof-m-measure).

    This property is called the **Born rule** and is another one of the postulates of quantum mechanics. It's gotten its name from the German physicist Max Born, who formulated it in 1926[[4]](#born-rule).

??? aside "Reflections on the Born rule"
    The Born rule is *the* thing which introduces the probabilistic nature of quantum mechanics. And it has been demonstrated experimentally time and time again, but the obvious question to me is, how do we know that this isn't just an approximation of some deterministic rule or set of rules?
    
    After all, I can very well write a probabilistic model of the outcome of a dice roll and say that "each possible outcome of the roll of a 6-sided die has a 1 in 6 probability". And that model would be correct, and be possible to verify through experimentation. But it wouldn't tell the whole story.
    
    If I knew everything there was to know about the die: its weight, weight distribution, the exact way in which it was rolled, including its rotation speed and so on, I could use the classical laws of physics to create a deterministic model which could accurately predict the *exact* result of the roll, provided I had access to all the information. So how can we be so sure that the situation isn't the same in quantum mechanics?

So far, perhaps forever, the Born rule is the best we've got when it comes to the prediction of quantum measurements.

Now, since we can write a state $\ket{\psi}$ in terms of some basis to $\mathcal{H}$, and we know that the eigenstates of an operator $\hat{A}$ form such a basis, we can write $\ket{\psi}$ like so:

$$
\ket{\psi} = \sum_n{c_n\ket{\lambda_n}}, \quad\quad c_n = \braket{\lambda_n | \psi}.
$$

The Born rule then gives us:

$$
\begin{align}
    P(\lambda_n) = |\braket{\lambda_n | \psi}|^2 \Leftrightarrow\\
    P(\lambda_n) = |c_n|^2.
\end{align}
$$

So another way to express the Born rule is by using the expansion coefficients.

The Born rule gives us a means to find the probability distribution of the measurement outcome given a system in state $\ket{\psi}$. For each possible outcome, i.e. eigenvalue of the observable $\hat{A}$ in question, there is an associated probability given by the Born rule.

Now, what happens after a measurement has been done?

!!! info "State collapse"
    Let $\lambda_n$ be the eigenvalue that the measurement of property $\mathcal{A}$ of the system resulted in. Then, the system will be in state $\ket{\lambda_n}$ **immediately** after the measurement, where $\ket{\lambda_n}$ is the eigenstate associated with $\lambda_n$.

So if an isolated quantum system is in a state $\ket{\psi}$, the measurement of a physical property $\mathcal{A}$ of the system will result in one of the eigenvalues $\lambda_n$ of $\hat{A}$, where $\hat{A}$ is the corresponding Hermitian operator to $\mathcal{A}$. Once the system has been measured, its state will instantaneously become the eigenstate $\lambda_n$ to the corresponding eigenvalue $\lambda_n$.

## Expectation value
Just like in any other application of probability theory, there exists the notion of the **expectation value** in quantum mechanics as well.

!!! info "Expectation value"
    The expectation value $\braket{\hat{A}}_{\psi}$ of an observable $\hat{A}$ of a system in a normalized state $\ket{\psi}$ is the average value of the measurement outcomes:

    $$
    \braket{\hat{A}}_\psi = \sum_n{\lambda_n P(\lambda_n)} = \sum_n{\lambda_n |\braket{\lambda_n | \psi}|^2} = \sum_n{\lambda_n |c_n|^2}.
    $$

    There is also an alternative form of the expectation value that is very commonly used in quantum mechanics:

    $$
    \braket{\hat{A}}_\psi = \bra{\psi}\hat{A}\ket{\psi}.
    $$

    ??? abstract "Proof: Alternative form of the expectation value"
        $$
        \begin{align}
            \bra{\psi}\hat{A}\ket{\psi} = && \\
            \bra{\psi}\mathbb{I}\hat{A}\mathbb{I}\ket{\psi} = && \tiny{\text{insert resolution of id.}}\\
            \bra{\psi}\Bigl( \sum_n{\ket{\lambda_n}\bra{\lambda_n}} \Bigr)\hat{A}\Bigl( \sum_m{\ket{\lambda_m}\bra{\lambda_m}} \Bigr)\ket{\psi} = && \tiny{\text{move sums to beginning}}\\
            \sum_{n, m}{\braket{\psi | \lambda_n} \bra{\lambda_n}\hat{A}\ket{\lambda_m} \braket{\lambda_m | \psi}} = && \tiny{\text{eigenvalue eq. $\hat{A}\ket{\lambda_m} = \lambda_m\ket{\lambda_m}$}}\\
            \sum_{n, m}{\lambda_m\braket{\psi | \lambda_n} \braket{\lambda_n | \lambda_m} \braket{\lambda_m | \psi}} = && \tiny{\text{basis is orthonormal, $\braket{\lambda_n | \lambda_m} = \delta_{nm}$}}\\
            \sum_{n, m}{\delta_{nm} \lambda_m\braket{\psi | \lambda_n} \braket{\lambda_m | \psi}} = && \tiny{\text{only nonzero term is when $n = m \Rightarrow \delta_{nm} = 1$}}\\
            \sum_n{\lambda_n \braket{\psi | \lambda_n} \braket{\lambda_n | \psi}} = && \\
            \sum_n{\lambda_n \braket{\lambda_n | \psi}^* \braket{\lambda_n | \psi}} = && \tiny{\text{for $z \in \mathbb{C}$, $zz^* = |z|^2$}}\\
            \sum_n{\lambda_n |\braket{\lambda_n | \psi}|^2}. &&
        \end{align}
        $$

        Q.E.D.

    If we are **not** working with normalized states, the expectation value is simply given by:

    $$
    \braket{\hat{A}}_\psi = \frac{\bra{\psi} \hat{A} \ket{\psi}}{\braket{\psi | \psi}}.
    $$

The expectation value **does not** necessarily equal any actual measurement outcome, just as the expectation value in general probability theory doesn't necessarily equal any actual possible values. For example, the expectation value of a fair 6-sided die is 3.5, but you cannot roll that die and get 3.5.

## References
<span id="shankar-l1">[1]</span> YaleCourses, Yale Univ. Press, New Haven, CT, USA. *19. Quantum Mechanics I: The key experiments and wave-particle duality*. (March 24, 2011). Accessed: Aug. 22, 2024. [Online Video]. Available: [https://youtu.be/uK2eFv7ne_Q?feature=shared](https://youtu.be/uK2eFv7ne_Q?feature=shared).

<span id="prof-m-eigen">[2]</span> Professor M does Science, Cambridge, U.K. *Eigenvalues and eigenstates in quantum mechanics*. (July 1, 2020). Accessed: Aug. 21, 2024. [Online Video]. Available: [https://youtu.be/p1zg-c1nvwQ?feature=shared](https://youtu.be/p1zg-c1nvwQ?feature=shared).

<span id="prof-m-measure">[3]</span> Professor M does Science, Cambridge, U.K. *Measurements in quantum mechanics || Concepts*. (Nov. 11, 2020). Accessed: Aug. 23, 2024. [Online Video]. Available: [https://youtu.be/u1R3kRWh1ek?feature=shared](https://youtu.be/u1R3kRWh1ek?feature=shared).

<span id="born-rule">[4]</span> N. P. Landsman, "Born Rule and its Interpretation," in *Compendium of Quantum Physics*, D. Greenberger, K. Hentschel, F. Weinert, Ed., Berlin, Germany: Springer-Verlag, 2009, pp. 64-70.