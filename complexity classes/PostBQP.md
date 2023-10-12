# Definition
PostBQP is the class of languages $L \subseteq \{0, 1\}^*$ for which there exists a uniform family of polynomial-size quantum circuits $\{C_n\}_{n\geq 1}$ such that for all inputs $x$,
- After $C_n$ is applied to the state $\ket{0 \cdots 0}\otimes \ket{x}$, the first qubit has a nonzero probability of being measured to be $\ket{1}$. 
- If $x \in L$, then conditioned on the first qubit being $\ket{1}$, the second qubit is $\ket{1}$ with probability at least $2/3$. 
- If $x \not \in L$, then conditioned on the first qubit being $\ket{1}$, the second qubit is $\ket{1}$ with probability at most $1/3$. 

# Reference
- https://www.scottaaronson.com/papers/pp.pdf