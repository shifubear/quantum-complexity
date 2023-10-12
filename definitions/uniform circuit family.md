---
aliases: 
	- polynomial time quantum algorithm
	- polynomial space quantum algorithm
	- time-uniform circuit family
	- space-uniform circuit family
---

# Definition 
A family of general quantum circuits $\mathcal{C} = (C_x)_{x\in\{0,1\}^*}$ is called **time-uniform** (or simply **uniform**) if $\mathcal{C}$ is polynomial-size and there exists a classical polynomial-time Turing machine that on input $x$ outputs the description of $C_x$. 

Similarly, a family of general quantum circuits $\mathcal{C} = (C_x)_{x\in\{0,1\}^*}$ is called **space-uniform** if $\mathcal{C}$ is polynomial-space and there exists a classical polynomial-space Turing machine that on input $(x, i)$ outputs the $i$'th gate of $C_x$. 

For brevity, we also call a time-uniform (resp. space-uniform) family of quantum circuits a polynomial time (resp. polynomial space) quantum algorithm. 

# Refs 
- [[@metger+2023]]
- [[@bostanci+2023]]