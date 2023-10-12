Let $\rho$ be a mixed quantum state on system A. If $\ket{\psi}$ and $\ket{\phi}$ are two [[purification]]s of $\rho$ over a system B, then 
$$\ket{\phi}=(I_A\otimes U)\ket{\psi}$$
for some unitary $U$ that acts only on system B. 

*Pf*: By the [[Schmidt decomposition]], we can write $\ket{\psi}$ as 
$$\ket{\psi} = \sum_i \sqrt{p_i}\ket{\alpha_i}\ket{\beta_i}.$$
We can write the first register of $\ket{\phi}$ in the $\alpha_i$ basis as 
$$\ket{\phi} = \sum_i \ket{\alpha_i}\ket{\tilde{\gamma}_i}$$
for some unnormalized set of states $\ket{\tilde{\gamma}_i}$. 

Since these are purifications of the same state $\rho$, they should be equal when we take the [[partial trace]] over the $B$ system. 
$$
\begin{align*}
\text{Tr}_B(\ket{\psi}\bra{\psi}) &= \sum_{ijk}(I_A \otimes \bra{\beta_k})(\sqrt{p_i}\ket{\alpha_i}\bra{\alpha_j}\sqrt{p_j} \otimes \ket{\beta_i}\bra{\beta_j})(I_A \otimes \ket{\beta_k}) \\ 
&= \sum_{ijk}\sqrt{p_ip_j}\ket{\alpha_i}\bra{\alpha_j} \braket{\beta_k|\beta_i}\braket{\beta_j|\beta_k} \\
&=\sum_{ijk}\sqrt{p_ip_j}\ket{\alpha_i}\bra{\alpha_j}\delta_{ik}\delta_{jk}\\
&=\sum_{ij}\sqrt{p_ip_j}\ket{\alpha_i}\bra{\alpha_j}\delta_{ij}\\

\end{align*}
$$

$$
\begin{align*}
\text{Tr}_B(\ket{\phi}\bra{\phi}) &= \sum_{ij}\text{Tr}_B(\ket{\alpha_i}\bra{\alpha_j}\otimes \ket{\tilde{\gamma}_i}\bra{\tilde{\gamma}_j}) \\
&= \sum_{ij}\ket{\alpha_i}\bra{\alpha_j}\braket{\tilde{\gamma}_j|\tilde{\gamma}_i}
\end{align*}
$$
Since these two states are equivalent, we have 
$$\sqrt{p_ip_j}\delta_{ij} = \braket{\tilde{\gamma}_j|\tilde{\gamma}_i}$$
which implies that the states $\{\ket{\tilde{\gamma}_i\}}$ are pairwise orthogonal and $||\ket{\tilde{\gamma}_i}|| = \sqrt{p_i}$. It suffices now to define an orthonormal basis $\{\ket{\gamma_i}\}$ such that $\ket{\tilde{\gamma}_i} =\sqrt{p_i}\ket{\gamma_i}$. Then the unitary 
$$U=\sum_i \ket{\gamma_i}\bra{\beta_i}$$
is the unitary change of basis satisfying the theorem statement. 

Refs
- https://marozols.wordpress.com/2012/05/09/unitary-equivalence-of-purifications/
- 