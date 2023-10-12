## Definition 
Let $A$ and $B$ be two subsystems making up the composite system described by the density operator $\rho_{AB}$. The **partial trace over the $B$ subsystem**, denoted $\text{Tr}_B$, is defined as 
$$\text{Tr}_B[\rho_{AB}] := \sum_j (I_A \otimes \bra{j}_B)\rho_{AB}(I_A\otimes\ket{j}_B)$$
where $\{\ket{j}\}$ is any orthonormal basis over the Hilbert space $\mathcal{H}_B$ of subsystem $B$. 


## Alternate Definition
Let $A$ and $B$ be two subsystems making up the composite system described by the density operator $\rho_{AB}$. The **partial trace over the $B$ subsystem** is the linear function defined by 
$$\text{Tr}_B(\ket{a_1}\bra{a_2} \otimes \ket{b_1}\bra{b_2}) := \ket{a_1}\bra{a_2} \text{Tr}(\ket{b_1}\bra{b_2}).$$

Refs
- Definition 6.7 https://www.ryanlarose.com/uploads/1/1/5/8/115879647/quic06-states-trace.pdf
- QCQI (2.178)
