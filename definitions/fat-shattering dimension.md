# Definition 
Let $S$ be a [[p-concept class]] over $\{0, 1\}^n$ and $\epsilon > 0$ be a real number. We say the set $A \subseteq \{0, 1\}^n$ is *$\epsilon$-shattered* by $S$ if there exists a function $r : A \rightarrow [0, 1]$ such that for all $2^{|A|}$ Boolean functions $g : A \rightarrow \{0, 1\}$, there exists a $p$-concept $f \in S$ such that for all $x \in A$, we have $f(x) \leq r(x) - \epsilon$ whenever $g(x) = 0$ and $f(x) \geq r(x) + \epsilon$ whenever $g(x) = 1$. Then the *$\epsilon$-fat-shattering dimension* of $S$, denoted $\text{fat}_\epsilon(S)$, is the size of the largest set $\epsilon$-shattered by $S$. 
We say $S$ is *bounded-dimensional* if $\text{fat}_\epsilon(S) \leq \text{poly}(n, 1/\epsilon)$ for all $\epsilon > 0$. 

# Intuition 
Think of the set $A$ as a subset of points to be colored (binary coloring with gradients). The shattering dimension roughly captures the intuition that any assigned coloring of these points (which is the role of $g$) can be approximately realized by a function $f$ in the [[p-concept class]] $S$. 

We say that $S$ **shatters** $A$ if $S$ can realize any labeling on $A$. 

# References
- Andrew Ng [Learning theory lecture notes](http://cs229.stanford.edu/notes_archive/cs229-notes4.pdf)
- 