# Project 5 — First-ply Failure of a Composite Plate

This project evaluates failure initiation in a composite laminate under uniaxial loading using classical failure theories.

## Contents
- Geometry setup
  - Plate dimensions: 300 mm × 300 mm
  - Shell modelling (S8R5 elements)
  - Number of ply: 24
  - Ply thickness: 0.1397 mm 
- Material properties  
  **Graphite/epoxy T300/5208**  

  | Property | Value | Strength type | Value |  
  |:---:|:---:|:---:|:---:|  
  | $E_1$ (GPa) | 181.0 | $\sigma_1^T$ | 1500 |  
  | $E_2$ (GPa) | 10.3 | $\sigma_1^C$ | -1500 |  
  | $G_{12}$ (GPa) | 7,17 | $\sigma_2^T$ | 40 |  
  | $\nu_{12}$ | 0.28 | $\sigma_2^C$ | -246 |  
  | | | $\tau_{12}$ | 68 |  

- Layup  

  | Design | Stacking Sequence |  $\psi^\circ$,  $\phi^\circ$ |  
  |:---:|:---:|:---:|  
  | a | [  $\psi$/  $\psi$/ $-\phi$/  $\phi$/  $\phi$/ $-\phi$/  $\phi$/ $-\phi$/ $-\phi$/  $\phi$/ $-\psi$/  $\psi$/ $-\psi$/  $\psi$/  $\phi$/ $-\phi$/ $-\phi$/  $\phi$/ $-\phi$/  $\phi$/  $\phi$/ $-\phi$/  $\psi$/ $-\psi$]<sub>T</sub> | 63.78, 17.44 |  
  | b | [ $\psi$/- $\psi$/- $\phi$/- $\phi$/- $\phi$/ $\phi$/- $\phi$/ $\phi$/- $\psi$/ $\psi$/ $\phi$/- $\phi$/ $\phi$/- $\phi$/- $\psi$/ $\psi$/- $\phi$/ $\phi$/- $\phi$/ $\phi$/ $\phi$/- $\phi$/ $\psi$/- $\psi$]<sub>T</sub> | 65.08, 19.58 |  
  | c | [ $\psi$/- $\psi$/- $\phi$/ $\phi$/ $\phi$/- $\phi$/- $\psi$/ $\psi$/ $\phi$/- $\phi$/- $\phi$/ $\phi$/ $\phi$/- $\phi$/- $\phi$/ $\phi$/- $\psi$/ $\psi$/- $\phi$/ $\phi$/ $\phi$/- $\phi$/ $\psi$/- $\psi$]<sub>T</sub> | 68.08, 23.04 |  
  | d | [ $\psi$/- $\psi$/- $\phi$/ $\phi$/- $\psi$/ $\psi$/ $\phi$/- $\phi$/ $\phi$/- $\phi$/ $\phi$/- $\phi$/- $\phi$/ $\phi$/- $\phi$/ $\phi$/- $\phi$/ $\phi$/- $\psi$/ $\psi$/ $\phi$/- $\phi$/ $\psi$/- $\psi$]<sub>T</sub> | 74.28, 27.06 |  
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
  
  <!--
  4. Hashin-Rotem
  The Hashin-Rotem failure criterion considers the matrix and fibre failure modes separately. Interactions between the various stress components are also considered.  

  <div align="center">

  $$
  \begin{align}
		\text{Fibre failure:} \; \frac{\sigma_1}{X} &= 1	\\	
		\text{Matrix failure:} \; (\frac{\sigma_2}{Y})^2+(\frac{\sigma_6}{Q})^2 &= 1	
	\end{align}
  $$

  </div>

  5. Hashin  
  The Hashin failure criterion is a modification of Hashin-Rotem criterion, which involves the interactions between the stresses for both fibre and matrix failure.  
  <div align="center">

  $$
  \begin{align}
    \text{Fibre failure in tension:} \; (\frac{\sigma_1}{X_t})^2+(\frac{\sigma_6}{Q})^2 &= 1	\\	
	  \text{Fibre failure in compression:} \; \frac{\sigma_1}{X_t} &= 1	\\
	  \text{Matrix failure:} \; (\frac{\sigma_2}{Y_t})^2+(\frac{\sigma_6}{Q})^2 &= 1
  \end{align}
  $$

	</div>
  -->

  4. Tsai-Wu  
  Compared to the independent and partially-interactive criteria, the Tsai-Wu criterion gives a more comprehensive prediction by considering the interaction between the compressive and tensile strengths. However, the criterion does not indicate whether the laminate failure occurs in the fibre or matrix material. Like the previously mentioned criteria, the Tsai-Wu criterion is predicted using a single expression. Moreover, assumptions are made to generalise the von Mises criterion, giving the A\textsubscript{12} term.  
  
  <div align="center">

  $$
  F_{1}\sigma_1+2F_{2}\sigma_2+F_{11}\sigma_1^2+F_{22}\sigma_2^2+F_{66}\tau_{12}^2-\sqrt{F_{11}F_{22}}\sigma_1\sigma_2 = 1
  $$

  </div>


  5. Tsai-Hill  
  Similar to the Tsai-Wu criterion, the Tsai-Hill criterion determines the strength with one single expression, without indicating whether the failure occurs in the fibre or matrix material. The Tsai-Hill criteria is applicable to the case of a single homogeneous orthotropic layer.  
  
  <div align="center">

  $$
  (\frac{\sigma_1}{X})^2-\frac{\sigma_1\sigma_2}{X^2}+(\frac{\sigma_2}{Y})^2+(\frac{\sigma_6}{Q})^2 = 1
  $$

  </div>

  6. Puppo-Evensen Criterion  
  The Puppo-Evensen criterion is proposed to carry out strength assessment for an entire laminate, although it can also be utilized for a single layer. The criterion considers a more thorough interaction between the tensile and compressive stress than the Tsai-Hill criterion and requires simpler testing requirements than the Tsai-Wu criterion. However, adjustments are needed according to the sign of the stresses, which makes it more cumbersome to use than the Tsai-Wu failure criterion.
  
  <div align="center">

  $$
  (\frac{\sigma_1}{X})^2-\phi\frac{X\sigma_1\sigma_2}{X^2Y}+\phi(\frac{\sigma_2}{Y})^2+(\frac{\sigma_6}{Q})^2 = 1 \\  
  \text{where} \\  
  \phi = \frac{3Q^2}{X_tY_t}
  $$

  </div>

- Results  
  * Failure Index Plots    
  ![FPFcompare](https://github.com/jasonleehs1018/Design-Portfolio/blob/main/Project_5-First-ply-Failure/FPFComparison.png?raw=true)