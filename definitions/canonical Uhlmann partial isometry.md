# Definition
The **canonical Uhlmann partial isometry with cutoff $\eta$** corresponding to a pair of pure states $(\ket{\psi}_{AB}, \ket{\phi}_{AB})$ is defined as 
$$W = \text{sgn}_\eta(\text{Tr}_A(\ket{\varphi}\bra{\psi})).$$
It is also referred to as the **canonical $\eta$-Uhlmann isometry**. 

Above, we define $\text{sgn}_\eta(K)$ to be the operator as follows: For $\eta \in \mathbb{R}$ and an operator $K$ with singular value decomposition $U\Sigma V^\dagger$, 
$$\text{sgn}_\eta(K) = U \text{sgn}_\eta(\Sigma) V^\dagger$$
where $\text{sgn}_\eta(\Sigma)$ denotes the projection onto the eigenvectors of $\Sigma$ with eigenvalue greater than $\eta$. 

# Properties
## Approximate Uhlmann transformation (Proposition 5.3)
The isometry $W$ approximately maps $\ket{\psi}$ to $\ket{\varphi}$, i.e., 
$$|\bra{\varphi}_{AB}(\text{id}_A \otimes W_B) \ket{\psi}_{AB}|^2 \geq F(\rho_A, \sigma_A) - 2\eta \dim(B).$$

## Minimality (Proposition 5.3)
For all partial isometries $R_B$ satisfying 
$$F(\rho_A, \sigma_A) = |\bra{\varphi}_{AB} (I_A \otimes R_B) \ket{\psi}_{AB}|^2,$$
we have $W^\dagger W \leq R^\dagger R$. 

# Notes
When $\eta = 0$, by the [[explicit Uhlmann unitary]] lemma $W$ is a unitary that exactly satisfies [[Uhlmann's theorem]]. However, this unitary is not robust in the sense that small differences in states could result in large changes in $W$ measured by the operator norm. The following two-qutrit example illuminates this issue
$$
\begin{align*}
\ket{\psi} &= \sqrt{1 - \epsilon}\ket{00} + \sqrt{\epsilon/2}\ket{11} + \sqrt{\epsilon/2}\ket{22}, \\ 
\ket{\tilde{\psi}} &= \sqrt{1 - \epsilon}\ket{00} + \sqrt{\epsilon/2}\ket{12} + \sqrt{\epsilon/2}\ket{21}, \\ 
\ket{\varphi} &= \ket{\psi}
\end{align*}
$$
The Uhlmann isometry corresponding to the pair $\ket{\varphi}$, $\ket{\psi}$ is the identity operator, but the isometry corresponding to the pair $\ket{\psi}$, $\ket{\tilde{\psi}}$ swaps qutrit states on the second qutrit. The difference in operator norm between these is at least 2, where as the states differ by at most $\epsilon$. 

# Ref
- [[@bostanci+2023]]
- 