# Definition
We say that a pair $(\mathcal{U}, \Psi)$ is a **distributional unitary synthesis problem** if $\mathcal{U} = (U_x)_x$ is a [[unitary synthesis problem]] with $U_x \in L(A_x, B_x)$ for some registers $A_x$, $B_x$, and $\Psi = (\ket{\psi_x})_x$ is a family of bipartite pure states on registers $A_xR_x$. We call $\ket{\psi_x}$ the **distribution state** with target register $A_x$ and ancilla register $R_x$. 

Let $(\mathcal{U}, \Psi)$ denote a distributional unitary synthesis problem, where $\mathcal{U} = (U_x)_x$ and $\Psi = (\ket{\psi_x})_x$, and let $\delta : \mathbb{N} \rightarrow \mathbb{R}$ be a function. Let $C = (C_x)_x$ denote a family of quantum circuits, where $C_x$ implements a channel whose input and output registers are the same as those of $U_x$. We say that $C$ *implements* $(\mathcal{U}, \Psi)$ with **average-case error** $\delta$ if for all $x \in \{0, 1\}^*$, there exists a channel completion $\Phi_x$ of $U_x$ such that 
$$\text{td}\big( (C_x \otimes \text{id})(\psi_x), (\Phi_x \otimes \text{id})(\psi_x) \big) \leq \delta(|x|),$$
where the identity channel acts on the ancilla register of $\psi_x$. 