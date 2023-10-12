Attempts to define unitaryQMA and characterize it's power. I really think that the power of a single quantum state is extremely limited in describing a whole unitary. As an example, suppose that the witness state is a superposition over the image of our partial isometry. Then there are at least as many unitaries that can't be distinguished up to the number of permutation of basis states in this space. [Aaronson2011] seems to support this claim, and many of the lower bounds in that setting should work to rule out these unitaries to be in unitaryQMA. 

Maybe some property testing definition could work? 
	Synthesize a unitary that has property $P$. 
Not sure how interesting this is, but there are some known properties which have been studied, for example, in [She, Yuen]. 

The most natural place to start is defining unitaryQMA as [[unitaryQIP]] with 1 message from the prover to the verifier, giving rise to the following definition: 

A [[distributional unitary synthesis problem]] $(\mathcal{U}, \Psi)$ is in avgUnitaryQMA if there exists a polynomial time verifier $V_x$ such that the following is true:
- **Completeness**: There exists a "quantum witness state" $\ket{w}$ such that   $$\text{Pr}[V_x \text{ accepts } \ket{w} ] \geq c$$
- **Soundness**: For any quantum state $\ket{w}$, if $V_x$ accepts with probability greater than $s$, and the state $\tau_{acc}$ in register $A$ is close to 




- Aaronson2011 [Impossibility of Succinct Quantum Proofs for Collision-Freeness](https://arxiv.org/pdf/1101.0403.pdf) 
	- df
- She, Yuen [Unitary property testing lower bounds by polynomials](https://arxiv.org/pdf/2210.05885.pdf) 
	- 