# Definition
We define a state sequence $\Psi_{UHLMANN} = (\ket{\psi_x})_{x\in\{0, 1\}^*}$ as follows: for all $x \in \{0, 1\}^*$, 
$$\ket{\psi_x} = \cases{\ket{C} & if $x = (1^n, C, D)$ is a valid Uhlmann instance\\0&otherwise.}$$
Then, the **distributional $(\kappa, \eta)$-Uhlmann transformation problem** is the [[distributional unitary synthesis problem]] $DISTUHLMANN_{\kappa, \eta} = (UHLMANN_{\kappa, \eta}, \Psi_{UHLMANN})$. 

Analogously, we define the state family  $\Psi_{SUCCINCTUHLMANN} = (\ket{\psi_x})_{x\in\{0, 1\}^*}$ as follows: for all $x \in \{0, 1\}^*$, 
$$\ket{\psi_x} = \cases{\ket{C} & if $x = (1^n, \hat{C}, \hat{D})$ is a valid Uhlmann instance\\0&otherwise.}$$
The **distributional $(\kappa, \eta)$-succinct Uhlmann transformation problem** is the [[distributional unitary synthesis problem]] $DISTSUCCINCTUHLMANN_{\kappa, \eta} = (SUCCINTUHLMANN_{\kappa, \eta}, \Psi_{SUCCINTUHLMANN})$. 