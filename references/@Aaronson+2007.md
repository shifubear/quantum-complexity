---
title: Quantum versus classical proofs and advice
authors: 
	- Scott Aaronson
	- Greg Kuperberg
year: 2007
url: https://arxiv.org/pdf/quant-ph/0604056.pdf
---

Presents three results towards answering the question of whether quantum proofs are more powerful than classical proofs (Is $QMA = QCMA$?). 
1. Any quantum algorithm needs $\Omega\left( \sqrt{\frac{2^n}{m+1}} \right)$ queries to find an $n$-qubit "marked state" $\ket{\psi}$, even if given an $m$-bit classical description of $\ket{\psi}$  together with a quantum black box that recognizes $\ket{\psi}$. 
2. An explicit QCMA protocol that nearly achieves this lower bound. 
3. QCMA protocol for verifying group non-membership (which was previously believed to require quantum advice). 

## Theorem 1.1.
There exists a quantum oracle $U$ such that $QMA^U \neq QCMA^U$. 

### Proof idea
Let $L$ be a unary language chosen uniformly at random. Define the oracle $U = \{U_n\}_{n\geq 1}$ as follows: 
1. if $0^n \in L$, then $U_n\ket{\psi_n} = -\ket{\psi_n}$ for some $n$-qubit marked state chosen uniformly at random, while $U_n\ket{\phi} = \ket{\phi}$ whenever $\braket{\phi|\psi_n} = 0$. 
2. Otherwise, $U = I$. 
The QMA machine with access to this oracle can decide $L$ with probability 1 given a quantum witness $\ket{\phi}$. Prepare the state $1/\sqrt{2} (\ket{0}\ket{\phi} + \ket{1}\ket{\phi})$ and apply the oracle to the second register. If $\phi$ is a witness in support of 1., then we accept with probability 1, and no other witness can make us accept with nonzero probability. 

For the QCMA machine, we use Theorem 3.3 combined with the fact that there are only countably infinite QCMA machines to show that the probability of success vanishes [Not super confident...]. If we fix a classical witness


## Theorem 3.3.
Suppose we are given oracle access to an $n$-qubit unitary $U$, and want to decide which of the following holds: 
1. There exists an $n$-qubit "quantum marked state" $\ket{\psi}$ such that $U\ket{\psi} = - \ket{\psi}$, but $U\ket{\phi} = \ket{\phi}$ whenever $\braket{\phi|\psi} = 0$; or 
2. $U = I$ is the identity operator. 
Then even if we have an $m$-bit classical witness $w$ in support of case 1., we still need $\Omega\left(\sqrt{\frac{2^n}{m+1}}\right)$ queries to verify the witness, with bounded probability of error. 

### Proof idea 
Uses a version of the [[hybrid method]]. Let $U_\psi$ be the oracle that corresponds to the case of 1, and $U = I$. Define possible states of the verifier $\ket{\Phi_t}$ for $t \in [T]$ as the verifier state after querying $t$ times to $U$, and then to $U_\psi$ for the remaining steps. If we are in case 1., the verifier will be in state $\ket{\Phi_0}$, and if in case 2., the state will be $\ket{\Phi_T}$. The objective is then to show that there can only be a small difference between $\ket{\Phi_t}$ and $\ket{\Phi_{t+1}}$. 