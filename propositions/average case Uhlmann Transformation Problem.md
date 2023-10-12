The following provides a justification on the definition of the [[distributional Uhlmann transformation problem]] and show that being able to solve the problem in the average case coincides with being able to perform the [[Uhlmann transformation problem|Uhlmann transformation]] corresponding to a pair of (succinctly or non-succinctly described) states. 

# Proposition 
Let $M = (M_x)_x$ be a [[uniform circuit family|quantum algorithm]] where for each valid fidelity-$\kappa(n)$ Uhlmann (resp. Succinct Uhlmann) instance $x = (1^n, C, D)$ (resp. $x = (1^n, \hat{C}, \hat{D})$), 
$$F\left( (\text{id}\otimes M_x)(\ketbra{C}{C}, \ketbra{D}{D}) \right) \geq \kappa(n) - \delta(n)$$
for some error function $\delta(n)$, where $M_x$ acts on the second $n$ qubits of $\ket{C}$. Then $M$ implements $\sc{DIST}\sc{UHLMANN}_{\kappa, 0}$ (resp. $\sc{DIST}\sc{SUCCINCT}\sc{UHLMANN}_{\kappa, 0}$) with average-case error $6\sqrt{1 - \kappa(n)} + \sqrt{\delta(n)}$. 

Conversely, suppose that a (uniform or nonuniform) quantum algorithm $M = (M_x)_x$ implements $\sc{DIST}\sc{UHLMANN}_{\kappa, 0}$ (resp. $\sc{DIST}\sc{SUCCINCT}\sc{UHLMANN}_{\kappa, 0}$) with average-case error $\delta$. Then for all valid fidelity-$\kappa(n)$ Uhlmann (resp. Succinct Uhlmann) instances $x = (1^n, C, D)$ (resp. $x = (1^n, \hat{C}, \hat{D})$), the following holds: 

_$$F\left( (\text{id}\otimes M_x)(\ketbra{C}{C}, \ketbra{D}{D}) \right) \geq \left( 1 - \delta(n) - 5\sqrt{1 - \kappa(n)} \right)^2.$$