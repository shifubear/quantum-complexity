---
alias: other end of this line
hardness: 
	- PPAD
	- FPSPACE
---

# Statement
Let $G = (V, E)$ be a directed graph with $2^n$ vertices (indexed by $n$ bit strings). $G$ contains only directed paths, directed cycles, or isolated vertices. $G$ is given by two polynomial size classical circuits: $S$ (which computes the successor $S(u) = v$ of a node $u$ in $G$), and $P$ (which computes the predecessor, $P(v) = u$)). We are promised that $0^n$ has no predecessor; the problem is to find the end of the line that starts with $0^n$. 

# Comments
- An efficient algorithm for [[Hamiltonian fast-fowarding]] implies one for OEOTL, which is unlikely. 


# References
- Papadimitriou: On the complexity of the parity argument and other inefficient proofs of existence
- [[@Atia+2017]]