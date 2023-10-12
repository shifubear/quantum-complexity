# Definition
Let $c, s, \delta : \mathbb{N} \rightarrow [0, 1]$ be functions. The class $\sc{unitaryQIP}_{c, s, \delta}$ is the set of unitary synthesis problems $\mathcal{U} = (U_x)_x$ where there exists a polynomial-time quantum verifier $V = (V_x)_{x \in \{0, 1\}^*}$ satisfying, for all $x \in \{0, 1\}^*$ of sufficiently large length, 
- **Completeness**: There exists a quantum prover $P$ (called an *honest prover*) such that for all input states $\ket{\psi}$ in the support of $U_x$, 
$$\text{Pr}[V_x(\ket{\psi}) \leftrightarrow P \; \text{accepts}] \geq c(|x|)$$
- **Soundness**: For all input states $\ket{\psi}$ and for all quantum provers $P$, there exists a channel completion of $\Phi_x$ of $U_x$ such that 
$$\text{if  Pr}[V_x(\ket{\psi}) \leftrightarrow P \text{ accepts}] \geq s(|x|) \text{ then } \text{ td}(\sigma, \Phi_x(\psi)) \leq \delta(|x|),$$
   where $\sigma$ denotes the output of $V_x(\ket{\psi}) \leftrightarrow P$ conditioned on accepting. 

Here the probabilities are over the randomness of the interaction. 

Finally, define 
$$\sc{unitaryQIP}_\delta = \cup_{\epsilon(n)} \sc{unitaryQIP}_{1-\epsilon, \frac{1}{2}, \delta}$$
where the union is over all negligible functions $\epsilon(n)$, and define 
$$\sc{unitaryQIP} = \cap_{q(n)} \sc{unitaryQIP}_{1/q(n)}$$
where the intersection ranges over all polynomials $q(n)$. 

# Notes 
Intuitively, a unitary synthesis problem $\mathcal{U} = (U_x)_x$ has an interactive proof if a polynomial time verifier who receives a pair $(x, \ket{\psi})$ can interact with an all-powerful prover, and conditioned on accepting, output a state close to $U_x\ket{\psi}$. 

