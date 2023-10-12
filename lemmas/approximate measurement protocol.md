# Statement
Let $\Psi = (\ket{\psi_x})_x$ be a $\sc{stateQIP}$ family of states. Then for all polynomials $p(n)$, there exists a polynomial-time quantum verifier $V$ that takes as input register $\sc{A}$, and outputs an accept/reject flag, a measurement outcome bit $b$, and a register $\sc{A}$ such that the following properties hold: 

1. **Completeness**: There exists an honest prover $P^*$ such that for all input state $\tau_A$ 
$$\text{Pr}[V(\tau_A)\leftrightarrow P^* \text{ accepts }] = 1.$$
	Furthermore, given input state $\ket{\psi_x}\bra{\psi_x}$ in register $\sc{A}$, the verifier outputs $b = 1$ with overwhelming probability:
$$\text{Pr}[V(\ket{\psi_x}\bra{\psi_x}) \leftrightarrow P^* \text{ outputs 1}] \geq 1 - 2^{-|x|}.$$
2. **Soundness**: For all input state $\tau_{AR}$ (where $R$ is an arbitrary external register not touches by the verifier or prover) and for all provers $P$ such that $V(\tau_{AR}) \leftrightarrow P$ accepts with probability at least 1/2, 
$$\left| \text{Pr}[V \text{ outputs } b = 1 | V \text{ accepts}] - \text{Tr}\left( \ket{\psi_x}\bra{\psi_x}_A \tau_A \right) \right| \leq \frac{1}{p(|x|)},$$
	where the events "outputs $b = 1$" and "accepts" are with respect to the interaction $V(\tau_{AR}) \leftrightarrow P$. If additionally $\text{Tr}\left( \ket{\psi_x}\bra{\psi_x}_A \tau_A \right) \geq 1/2$, then the final state $(\tau_{acc})_{AR}$ at the end of the protocol conditioned on acceptance and conditioned on measurement outcome bit $b=1$ satisfies 
$$\text{td}(\tau_{acc}, \tau|_{\psi_x \otimes \text{id}}) \leq \frac{1}{p(|x|)},$$
	where $\tau|_{\psi_x\otimes \text{id}}$ denotes the post-measurement state of $\tau_{AR}$ conditioned on projecting the $A$ register onto the state $\ket{\psi_x}$. Let $1/p(n)$ be the **closeness** of the verifier. 