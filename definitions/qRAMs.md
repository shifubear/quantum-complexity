# U-qRAM
Given an $n$-qubit unitary $U$, call a unitary $A$ acting on $m \geq 2n$ qubits a $U$-qRAM if $A\ket{x, 0^{m-n}} = \ket{x} \otimes U\ket{x} \otimes \ket{0^{m-2n}}$ for all $x \in \{0, 1\}^n$. 

# Psi-qRAM
Given two functions $p(n), q(n) = \text{poly}(n)$ and a family of $q(n)$-qubit states $\Psi = (\ket{\psi_x})_{x\in\{0,1\}^{p(n)}}$, call a unitary $A$ acting on $m \geq p(n) + q(n)$ qubits a $\Psi$-qRAM if $A\ket{x, 0^{m-n}} = \ket{x} \otimes \ket{\psi_x} \otimes \ket{0}$ for all $x \in \{0, 1\}^{p(n)}$. 

