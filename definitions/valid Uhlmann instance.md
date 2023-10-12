# Definition
We say that a string $x \in \{0, 1\}^*$ is a **valid Uhlmann instance** if it encodes a tuple $(1^n, C, D)$ where $C$, $D$ are explicit descriptions of unitary circuits that each act on $2n$ qubits. 
We say that $x$ is a **valid succinct Uhlmann instance** if $x = (1^n, \hat{C}, \hat{D})$ is a succinct description of a pair $(C, D)$ of unitary circuits that each act on $2n$ qubits for some $n$.

We further say that a valid (possibly succinct) Uhlmann instance $x$ is a **fidelity-$\kappa$ instance** if the reduced states $\rho$, $\sigma$ of the states $\ket{C} = C\ket{0^{2n}}$, $\ket{D} = D\ket{0^{2n}}$ on the first $n$ qubits satisfy $F(\rho, \sigma) \geq \kappa$ where $F$ is the [[fidelity]] function. 