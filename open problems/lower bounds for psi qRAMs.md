Greg's thesis introduces the problem of trying to improve (our show that it can't be improved) the lowerbound for unitary synthesis relative to a Psi-qRAM instead of a U-qRAM. The lowerbound for the U-qRAM query complexity is achieved via reduction to implementing permutations, which has been shown to require $\Omega(2^{n/2})$ queries, whose lowerbound follows via a reduction to unique search. Since the dimensionality of the Psi-qRAM mapping is not $n$ to $n$ like it was for $U$-qRAM, a similar technique will probably not work directly.  

![[qRAMs#Psi-qRAM]]

Using $\Psi$-qRAMs, can we perform unitary synthesis with $o(2^{n/2})$ queries? 

The reduced density matrices of $\sum_x \ket{x}U\ket{x}$ and $\ket{0}\sum_x U\ket{x}$ are not the same, so we cannot use the Uhlmann PSPACE algorithm. The [[Renyi 2-entropy]] between the two states are not the same. 

It seems that morally the current known lowerbounds all follow from unique search. Is there a way to adapt the key insight in these lowerbounds for the unitary synthesis setting using a more geometric argument? What I have in mind is to try to derive some contradiction by using the space that the algorithm must traverse through the Hilbert space, and bounding how far it can travel in a single step. 
The goal is to get a type of "minimal assumption" statement for unitary synthesis, a self contained proof of the query lowerbounds without having to use lowerbounds for search. 

Consider the following unitary synthesis query model: 
Each query to the oracle produces the action outlined below, and the unitary operation simply rotates the first register to its closest standard basis state. 
$$\begin{align}1.  & \ket{x}\ket{0} \rightarrow \ket{x}U\ket{x} \\ 2. & \ket{x}\ket{y} \rightarrow\ket{x'}\ket{y'}& \\ 3. &\ket{\hat{x}}\ket{\hat{y}} \rightarrow \ket{0}U\ket{x} \end{align}$$ 
One reason I don't think reducing to complexity of decision problems captures the full picture, is that these problems don't require uncomputing of the control register in the way we want for unitary synthesis. This has to change the structure of the question being asked, and finding ways to match known lowerbounds without traversing this route may give new insights on how to work with unitary synthesis problems. 

## Guessing Lemma route
One construction of the Psi-qRAM is by appending the description of $U\ket{x}$ with some quantum state (perhaps a witness) that can be exploited to speed up the uncomputation of the first register. This could either be an advice type state (the same state for all $U\ket{x}$, or a witness that depends on $x$. This may not improve anything, as a new challenge is to uncompute this register as well. By the statement of the [[Guessing Lemma]], IF there exists a QMA protocol for unitary synthesis 



## Natural Proofs
Can a barrier for lower bounds for QMA, stateQMA, unitaryQMA problems analogous to the natural proof for NP separations be shown? 