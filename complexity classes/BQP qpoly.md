# Definition
BQP/qpoly is the class of languages $L \subseteq \{0, 1\}^n$ for which there exists a polynomial time algorithm $Q$, together with a set of states $\{\ket{\psi_n}\}_{n\geq 1}$ (where $\ket{\psi_n}$ has size $p(n)$ for some polynomial $p$), such that for all $x \in \{0, 1\}^n$:
1. If $x \in L$ then $Q$ accepts with probability at least 2/3 given $\ket{x}\ket{\psi_n}$ as input. 
2. If $x \not \in L$ then $Q$ accepts with probability at most 1/3 given $\ket{x}\ket{\psi_n}$ as input. 