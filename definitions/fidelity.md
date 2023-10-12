Let $\rho$ and $\sigma$ be two density operators on a register $A$ and $\ket{\Psi}$, $\ket{\Phi}$ be purifications of these states over an extra register $B$. Then the fidelity of states $\rho$ and $\sigma$ is defined as 
- $F(\rho, \sigma) := \text{Tr}\sqrt{\rho^{1/2}\sigma\rho^{1/2}}$
- $F(\rho, \sigma) := \max_{\ket{\Psi}, \ket{\Phi} \text{ Purif.}} |\braket{\Psi|\Phi}|$ 
- $F(\rho, \sigma) := \max_{U_B} |\braket{\Psi|(I_A \otimes U_B)|\Phi}|$ 
	- See [[Uhlmann's theorem]] 