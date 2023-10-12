Let $\ket{\psi}_{AB}$ and $\ket{\varphi}_{AB}$  denote pure states on registers $A$, $B$. Let $\rho$ and $\sigma$ denote the reduced density matrices on register $A$ of $\ket{\psi}$ and $\ket{\varphi}$, respectively. Define the operator 
$$W = \text{sgn}(\text{Tr}_A(\ket{\psi}\bra{\varphi}))$$
acting on register $B$. Then $W$ is a partial isometry satisfying 
$$F(\rho, \sigma) = \bra{\psi}(I_A\otimes W)\ket{\varphi}.$$
where $F$ is the [[fidelity]] function. 

This Uhlmann transformation is *minimal* in the sense that any other partial isometry $\tilde{W}$ that achieves the same guarantee satisfies $W^\dagger W \leq \tilde{W}^\dagger \tilde{W}$. 



