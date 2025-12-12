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
	$$
	\begin{aligned}
	\frac{\sigma_1}{\sigma_{X_t}} \text{or} \frac{\sigma_1}{\sigma_{X_c}} &= 1 \\ 
	\text{or} \\  
	$\frac{\sigma_2}{\sigma_{Y_t}}$ or $\frac{\sigma_2}{\sigma_{Y_c}} &= 1  
	\text{or} \\  
  	$\frac{|\sigma_6|}{\sigma_Q} &= 1
	\end{aligned}
	$$
  2. Tsai-Hill
  3. Tsai-Wu
  4. Hashin



	</div>
  3. Tsai-Hill
  4. Tsai-Wu
  5. Hashin

