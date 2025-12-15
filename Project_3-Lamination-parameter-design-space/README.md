# Project 01 — Linear Buckling of a Composite Plate

This project studies the lamination parameter design space of standard quad finite length plates.

## Contents
- BUCKLING PERFORMANCE OF FINITE LENGTH PLATES
    - To assess the vast number of designs contained in the laminate database, a closed form solution of compression buckling is necessary. 

    <div align="center">

    $$
	N_x = \pi^2 [D_{11} (\frac{m}{a})^2 + 2(D_{11} + 2D_{66})(\frac{n^2}{b^2}) +D_{22}(\frac{n^4}{b^4})(\frac{a}{m})^2]
    $$

    </div>

from knowledge of the bending stiffness, $D_{ij}$, plate length, $a$, and width, $b$, and the buckling half-wave parameter, $m$ (= 1, 2, 3, ...), which produces the lowest critical force resultant N\textsubscript{x}. 

- CONTOUR MAPPING FOR COMPRESSION BUCKLING
    - For orthotropic laminates, the following buckling equation, represented by a 2-dimensional, 4\textsuperscript{th} order polynomial, can be solved estimated using buckling loads obtained from the exact closed form buckling solution at 15 equally spaced points across the lamination parameter design space, as illustrated by the example cross section in Fig. \ref{figure:New3DSpace_NoPts}, when $\xi_{11}$ = 0:

    <div align="center">

    $$
    \begin{align}
	k_x &= c_{1} +c_{2}\xi_{9} +c_{3}\xi_{10} +c_{4}\xi_{9}^2 +c_{5}\xi_{10}^2 +c_{6}\xi_{9}\xi_{10} +c_{7}\xi_{9}^{3} +c_{8}\xi_{10}^{3} +c_{9}\xi_{9}\xi_{10}^{2}  
	& +c_{10}\xi_{9}^{2}\xi_{10} +c_{11}\xi_{9}^{4} +c_{12} \xi_{10}^{4} +c_{13}\xi_{9}\xi_{10}^{3} +c_{14}\xi_{9}^{2}\xi_{10}^{2} +c_{15}\xi_{9}^{3}\xi_{10}  
    \end{align}   
    $$

    </div>
    where $k_x$ is defined by:  

    <div align="center">
    $k_x=\frac{N_xb^2}{\pi^2D_{Iso}}$  
    </div>
    
    This normalization ensures that buckling factor results are comparable across the design space, since the relative change in buckling factor, $k_x$, is the same as the relative change in the critical force resultant, $N_x$.  In this study, IM7/8552 carbon-fibre/epoxy material is used, with Young’s moduli $E_1$ = 161.0 GPa and $E_2$ = 11.38 GPa, shear modulus $G_{12}$ = 5.17 GPa and Poisson ratio $\nu_{12}$ = 0.38.  