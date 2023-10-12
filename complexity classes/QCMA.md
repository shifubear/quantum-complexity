# Definition 
$\sc{QMA}$ is the class of languages $L \subseteq \{0, 1\}^n$ for which there exists a polynomial-time quantum verifier $Q$ and a polynomial $p$ such that for all $x \in \{0, 1\}^n$: 
	(i) If $x \in L$ there exists a classical string $z \in \{0, 1\}^{p(n)}$ such that $Q$ accepts with probability at least 2/3 given $\ket{x}\ket{z}$ as input.
	(ii) If $x\not \in L$ then $Q$ accepts with probability at most 1/3 given $\ket{x}\ket{z}$ as input, for all classical proofs $\ket{z}$. 

# Known facts
- By the Solovay-Kitaev Theorem, the number of possible QCMA machines is only countably infinite. Mentioned in [[@Aaronson+2007]]. 