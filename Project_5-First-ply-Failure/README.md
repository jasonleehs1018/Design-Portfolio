# Project 5 — First-ply Failure of a Composite Plate

This project evaluates failure initiation in a composite laminate under uniaxial loading using classical failure theories.

## Contents
- Geometry setup
  - Plate dimensions: 300 mm × 300 mm
  - Shell modelling (S8R5 elements)
  - Number of ply: 24
  - Ply thickness: 0.1397 mm 
- Material properties
  Graphite/epoxy T300/5208
  | Property | Value | Strength type | Value |
  | :---: | :---: | :---: | :---: |
  | $E_1$ (GPa) | 181.0 | $\sigma_1^T$ | 1500 | 
  | $E_2$ (GPa) | 10.3 | $\sigma_1^C$ | -1500 | 
  | $G_{12}$ (GPa) | 7,17 | $\sigma_2^T$ | 40 | 
  | $\nu_{12}$ | 0.28 | $\sigma_2^C$ | -246 | 
  | | | $\tau_{12}$ | 68 | 
- Layup
  | Design | Stacking Sequence |  $\psi^\circ$,  $\phi^\circ$ |
  | :---: | :---: | :---: | 
  | a | [  $\psi$/  $\psi$/ $-\phi$/  $\phi$/  $\phi$/ $-\phi$/  $\phi$/ $-\phi$/ $-\phi$/  $\phi$/ $-\psi$/  $\psi$/ $-\psi$/  $\psi$/  $\phi$/ $-\phi$/ $-\phi$/  $\phi$/ $-\phi$/  $\phi$/  $\phi$/ $-\phi$/  $\psi$/ $-\psi$]<sub>T</sub> | 63.78, 17.44 |
  | b |  [ $\psi$/- $\psi$/- $\phi$/- $\phi$/- $\phi$/ $\phi$/- $\phi$/ $\phi$/- $\psi$/ $\psi$/ $\phi$/- $\phi$/ $\phi$/- $\phi$/- $\psi$/ $\psi$/- $\phi$/ $\phi$/- $\phi$/ $\phi$/ $\phi$/- $\phi$/ $\psi$/- $\psi$]<sub>T</sub> | 65.08, 19.58 |
  | c | [ $\psi$/- $\psi$/- $\phi$/ $\phi$/ $\phi$/- $\phi$/- $\psi$/ $\psi$/ $\phi$/- $\phi$/- $\phi$/ $\phi$/ $\phi$/- $\phi$/- $\phi$/ $\phi$/- $\psi$/ $\psi$/- $\phi$/ $\phi$/ $\phi$/- $\phi$/ $\psi$/- $\psi$]<sub>T</sub> | 68.08, 23.04 |
  | d |[ $\psi$/- $\psi$/- $\phi$/ $\phi$/- $\psi$/ $\psi$/ $\phi$/- $\phi$/ $\phi$/- $\phi$/ $\phi$/- $\phi$/- $\phi$/ $\phi$/- $\phi$/ $\phi$/- $\phi$/ $\phi$/- $\psi$/ $\psi$/ $\phi$/- $\phi$/ $\psi$/- $\psi$]<sub>T</sub> | 74.28, 27.06 |
  | e | [ $\psi$/- $\psi$/ $\phi$/- $\phi$/- $\phi$/ $\phi$/ $\psi$/- $\psi$/- $\psi$/ $\psi$/- $\psi$/ $\psi$/- $\psi$/ $\psi$/- $\psi$/ $\psi$/ $\psi$/- $\psi$/- $\phi$/ $\phi$/ $\phi$/- $\phi$/ $\psi$/- $\psi$]<sub>T</sub> | 70.46, 24.95 |
  | f | [ $\psi$/- $\psi$/ $\phi$/- $\phi$/ $\psi$/- $\psi$/- $\phi$/ $\phi$/- $\psi$/ $\psi$/- $\psi$/ $\psi$/- $\psi$/ $\psi$/- $\psi$/- $\phi$/ $\phi$/ $\psi$/- $\psi$/ $\phi$/- $\phi$/ $\psi$/- $\psi$]<sub>T</sub> | 78.64, 28.59 |
  
- Loading & Boundary conditions
  - Axial compression 
  - Simply supported
- Failure Criteria
  1. Max stress  
  The maximum stress criterion predicts the failure of a laminate by looking into the stresses individually, interactions between the tension and compressive stresses are ignored. 

  <div align="center">

	$$
	\begin{aligned}
	  \frac{\sigma_1}{\sigma_{X_t}} \text{or} \frac{\sigma_1}{\sigma_{X_c}} &= 1 \\ 
	  \text{or} \\  
	  \frac{\sigma_2}{\sigma_{Y_t}} or \frac{\sigma_2}{\sigma_{Y_c}} &= 1  \\
	  \text{or} \\  
  	\frac{|\sigma_6|}{\sigma_Q} &= 1
	\end{aligned}
	$$

  </div>

  2. Max Strain  
  The maximum strain criterion function is similar to the maximum stress criterion, but instead of stresses, this approach uses strains to predict the failure strength of a laminate.

  <div align="center">

  $$
  \begin{align}
			\frac{\varepsilon_1}{\varepsilon_{X_t}} \; \text{or} \; \frac{\varepsilon_1}{\varepsilon_{X_c}} &= 1 \\
			\text{or}	\\
			\frac{\varepsilon_2}{\varepsilon_{Y_t}} \; \text{or} \; \frac{\varepsilon_2}{\varepsilon_{Y_c}} &= 1	\\
			\text{or}	 \\
			\frac{|\varepsilon_6|}{\varepsilon_Q} &= 1	
		\end{align}
  $$

  </div>

  3. Puck-Modified  
  The Puck-modified criterion is an updated version of the simple Puck criterion. The modified version considers interactions between the stress in compression and in tension, normal to the fibre direction.

  <div align="center">

  $$
  \begin{align}
			\frac{\sigma_1}{X_t} \; \text{or} \; \frac{\sigma_1}{X_c}	&= 1 \\
			\text{or} \\
			\frac{\sigma_2^2}{Y_tY_c}+\sigma_2(\frac{1}{Y_t}-\frac{1}{Y_c})+(\frac{\sigma_6}{Q})^2 &= 1
		\end{align}
  $$

  </div>
  4. Tsai-Hill  
  5. Tsai-Wu  
  6. Hashin  



	</div>


