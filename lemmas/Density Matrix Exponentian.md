# Statement (Due to [[@bostanci+2023]])
Let $t \in \mathbb{R}$. There exists a quantum polynomial-time algorithm DME that takes as input registers $\sc{A}\sc{C}_{[m]}$ and outputs register $\sc{A}$ with the following guarantee:
	if the input registers are in state $\tau_{\sc{A}\sc{B}} \otimes \rho_{\sc{C}_[m]}^{\otimes k}$, where $\sc{B}$ is an arbitrary purifying register on which the algorithm does not act and $\rho$ is an $n$-qubit mixed state, then the output state $\sigma_{\sc{A}\sc{B}}$ of the algorithm satisfies
$$\text{td}(\sigma_{\sc{A}\sc{B}}, (W_\sc{A} \otimes \text{id}_\sc{B})\tau_{\sc{A}\sc{B}}(W_\sc{A}^\dagger \otimes \text{id}_\sc{B})) \leq O(t^2/k), \text{ where } W = e^{2\pi i \cdot t \cdot \rho}.$$

First introduced in [[@lloyd+2014]]