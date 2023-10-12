---
related: [[swap test]]
---

# Definition [[@gilyen+2022]]
Given identical copies of a state $\ket{\psi}$ and a unitary $U$, repeat the following circuit
![[Hadamard test.png]]
$4\log \left(\frac{4}{\delta}\right)/\xi^2$ many times with parameters $\xi \in (0, 1)$ and $\delta \in (0, 1)$ to approximate $z = \braket{\psi|U|\psi}$ as $\text{Re}\braket{\psi|U|\psi}$ and $\text{Im}\braket{\psi|U|\psi}$, each within an additive error of $\xi/\sqrt{2}$ with probability $1 - \delta/2$. 
By the union bound, an estimate $\tilde{z}$ with $|\tilde{z} - z| \leq \xi$ is obtained with probability $1 - \delta$. 

# References
- Introduced in [[@Buhrmann+2001]]