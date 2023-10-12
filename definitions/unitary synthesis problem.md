# Definition
A **unitary synthesis problem** is a sequence $\mathcal{U} = (U_x)_{x\in\{0, 1\}^*}$ of partial isometries. 

Suppose we have a unitary synthesis problem $\mathcal{U}$ and a let $\delta : \mathbb{N} \rightarrow \mathbb{R}$ be a function. Let $C = (C_x)_{x\in \{0, 1\}^*}$ denote a (not necessarily uniform) family of quantum circuits, where $C_x$ implements a channel whose input and output registers are the same as those of $U_x$. We say that $C$ *implements* $\mathcal{U}$ with **worst-case error** $\delta$ if for all $x \in \{0, 1\}^*$, there exists a channel completion $\Phi_x$ of $U_x$ such that 
$$||C_x - \Phi_x||_\diamond \leq \delta(|x|),$$
where $|| \;\cdot\;||_\diamond$ denotes the diamond norm. 

# Examples
- [[Uhlmann transformation problem]]


# Ref
- [[@bostanci+2023]]