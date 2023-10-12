
# Definition [StatePP]
A family of quantum states $\{\ket{\psi_x}\}_{x\in L}$ is in $\sc{statePP}_\delta[\gamma(n)]$ if each $\ket{\psi_x}$ is an $n$-qubit state where $n := |x|$, and there exists a uniformly generated quantum circuit family $\{Q_x\}_{x\in L}$, which takes no inputs, such that for all $x \in L$:
- The circuit $Q_x$ outputs a (probably mixed) quantum state $\rho_x$ satisfying $\text{td}(\rho_x, \psi_x) \leq \delta(n)$ if $Q_x$ succeeds. Here, we define the success of circuit $Q_x$ as the measurement outcome of the designated output qubit being 1. 
- The success probability of $Q_x$ is at least $\gamma(n)$, which is a function that can depend on the input size. 
	- Note, the success probability has to be at least $1/\exp(n)$ to ensure that the probability can be written down. 


# Definition [StateALL]


# Notes
- Greg's algorithm requires query access to the Boolean function encoding the state we want to synthesize. Is it possible to have an advice state that encodes this? 