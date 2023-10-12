# Definition
Consider a local Hamiltonian system $H = \sum_i H_i$ on a 1D chain, together with a cut between particles $i^*$ and $i^* + 1$ that bi-partitions the system. We say that an operator $K$ is a **$(D, \Delta)$-Approximate Ground Space Projection** (with respect to the cut) if the following holds: 
- **Ground space invariance**: for any ground state $\ket{\Omega}$, $K\ket{\Omega} = \ket{\Omega}$. 
- **Shrinking**: for any state $\ket{\Omega^\perp} \in \mathcal{H}^\perp$, also $K\ket{\Omega^\perp} \in \mathcal{H}^\perp$, and $||K|\ket{\Omega^\perp}||^2 \leq \Delta$. 
- **Entangling**: for any state $\ket{\phi}$, $SR(K\ket{\phi}) \leq D \cdot SR(\phi)$, where $SR(\cdot)$ is evaluated with respect to the bi-partitioning. 