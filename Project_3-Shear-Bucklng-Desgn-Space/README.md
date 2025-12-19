# Project 03 — Lamination Parameter Design Space for shear bucklng

This project studies the lamination parameter design space of standard quad finite length plates for shear bucklng.

## Contents

Equations for shear loaded plates are obtained using the same procedure adopted for compression buckling.  However, the finite element analysis software ABAQUS must now be used for uncoupled as well as coupled designs to generate buckling factors. The plate axis system, positive shear load, positive fibre orientation with respect to the x-axis, and aspect ratio ($a/b$) are also defined in the thumbnail sketch in [Fig. 1](#Plate_axis_system).

<div align="center" id="Fig-Plate_axis_system">

<img src="Plate_axis_system.png" width="350"><br>

<em><strong>Figure 1.</strong> Illustration of the plate axis system, positive shear load, positive fibre orientation with respect to the x-axis, and aspect ratio ($a/b$).</em>

</div>

For the uncoupled laminates, positive and negative shear give identical buckling load factors. The shear buckling factors are obtained by substituting the calculated coefficients into Eqn. \ref{eq:bucklingCFS}. In this case, $k_{xy}$ is defined by: 


<div id="eq-kxy">

$$
K_{xy}=\frac{N_{xy}b^2}{\pi^2D_{Iso}}
\tag{Eqn. 1}
$$

</div>

<div align="center" id="Fig-ShearContour+ModeShape">

<img src="ShearContour+ModeShape.PNG"><br>

<em><strong>Figure 2.</strong> Positive and Negative Shear buckling factor contours, $k_{xy}(= N_{xy}b^2/\pi^2D_{Iso})$, for $\xi_{11}$ = 0.0 with: (a)  $a/b$ = 1.0; (b) $a/b$ = 1.5, and (c) $a/b$ = 2.0.</em>

</div>

<div id="Fig-NegativeShearContoursXi0_5AR1_0">
<table style="border:1px solid black; border-collapse:collapse;">
    <tr>
    <td align="center" style="border:1px solid black; padding:6px;">
      <a id="fig-NegativeShearContoursXi0_5AR1_0"></a>
      <img src="NegativeShearContoursXi0_5AR1_0.png" width="220"><br>
      <em>(a)</em>
    </td>
    <td align="center" style="border:1px solid black; padding:6px;">
      <a id="NegativeShearContoursXi0_5AR1_0"></a>
      <img src="NegativeShearContoursXi0_5AR1_5.png" width="220"><br>
      <em>(b)</em>
    </td>
    <td align="center" style="border:1px solid black; padding:6px;">
      <a id="fig-NegativeShearContoursXi0_5AR2_0"></a>
      <img src="NegativeShearContoursXi0_5AR2_0.png" width="220"><br>
      <em>(c)</em>
    </td>
    </tr>
</table>
    <em><strong>Figure 3.</strong> Negative Shear buckling contours $k_{xy}(=N_{xy}b^2/\pi^2D_{Iso})$ for $\xi_{11}$ = 0.0, with: $a/b$ = 1.0 (left); $a/b$ = 1.5 (middle) and; $a/b$ = 2.0 (right).</em>
</div>

<div id="Fig-PosShearContoursXi0_5AR1_0">
    <table style="border:1px solid black; border-collapse:collapse;">
    <tr>
    <td align="center" style="border:1px solid black; padding:6px;">
      <a id="fig-PositiveShearContoursXi0_5AR1_0"></a>
      <img src="PositiveShearContoursXi0_5AR1_0.png" width="220"><br>
      <em>(a)</em>
    </td>
    <td align="center" style="border:1px solid black; padding:6px;">
      <a id="PositiveShearContoursXi0_5AR1_0"></a>
      <img src="PositiveShearContoursXi0_5AR1_5.png" width="220"><br>
      <em>(b)</em>
    </td>
    <td align="center" style="border:1px solid black; padding:6px;">
      <a id="fig-PositiveShearContoursXi0_5AR2_0"></a>
      <img src="PositiveShearContoursXi0_5AR2_0.png" width="220"><br>
      <em>(c)</em>
    </td>
    </tr>
</table>
    <em><strong>Figure 4.</strong> Positive Shear buckling contours $k_{xy}(=N_{xy}b^2/\pi^2D_{Iso})$ for $\xi_{11}$ = 0.0, with: $a/b$ = 1.0 (left); $a/b$ = 1.5 (middle) and; $a/b$ = 2.0 (right).</em>

</div>

The resulting contour maps are presented in [Fig. 3(a)](#Fig-NegativeShearContoursXi0_5AR1_0) and [Fig. 4(c)](#Fig-PosShearContoursXi0_5AR1_0), showing isolines of constant buckling load factor across the lamination parameter design space for aspect ratios $a/b$ = 1.0, 1.5 and 2.0, respectively. Positive shear direction ($N_{xy}$) is defined together with positive fibre angle direction in [Fig. 1](#Plate_axis_system). For uncoupled rectangular plates, there is no difference in the shear buckling results for positive shear or negative shear loading.  However, for <em>Bend-Twist</em> coupled rectangular plates with $\xi_{11}$ = 0.5, [Figs. 3(a)](#NegativeShearContoursXi0_5) and [4(a)](#PositiveShearContoursXi0_5) demonstrate marked differences due to shear load reversal.  This can be appreciated by the fact that shear loading and \textit{Bend-Twist} coupling ($\xi_{11}\neq0$) both give rise to skewed nodal lines in the buckling mode shapes \cite{york&almeida2018bt}. [Figures 3](#Fig-NegativeShearContoursXi0_5AR1_0) and [4](#Fig-PosShearContoursXi0_5AR1_0) represent the equivalent series of negative and positive shear buckling factor contour maps, respectively. In both cases, minima and maxima are on the sloping boundary of the feasible design space, which often coincide with dotted lines indicating a change in buckling mode. The maximum negative shear buckling factors, $k_{xy}$ = 14.86 and 10.71, are both located at ($\xi_9$, $\xi_{10}$, $\xi_{11}$) = (0, -1, 0.5) for a/b = 1.0 and 1.5, whilst for $a/b$ = 2.0, ks = 9.89 at ($\xi_9$, $\xi_{10}$, $\xi_{11}$) = (-0.35, -0.31, 0.5).  By contrast, only the maximum positive shear buckling factor, $k_{xy}$ = 7.30, for coupled laminates with $a/b$ = 1.0, is located at ($\xi_9$, $\xi_{10}$, $\xi_{11}$) = (0, -1, 0.5).  For $a/b$ = 1.5 and 2.0, ($\xi_9$, $\xi_{10}$, $\xi_{11}$) = (0.41, -0.92, 0.5) and (-0.13, -0.74, 0.5), with $k_{xy}$ = 5.30 and 4.84, respectively. 

Shear buckling results from the literature \cite{Fukunaga1995} represent optimised lamination parameters for hypothetical or non-standard designs.  For aspect ratio a/b = 2.0 they correspond to ($\xi_9$, $\xi_{10}$) = (-0.39, -0.7) for orthotropic designs and ($\xi_9$, $\xi_{10}$, $\xi_{11}$, $\xi_{12}$) = (-0.42, -0.64, -0.91, 0.77) for \textit{Bend-Twist} coupled designs, representing buckling factor results, $k_{xy}$ = 7.94 and 12.51, respectively.  By contrast, the maximum shear buckling factor for practical designs corresponds to $k_{xy}$ = 7.52, at ($\xi_9$, $\xi_{10}$) = (-0.26, -0.49) on [Fig. 2(c)], for which stacking sequence [45/-45\textsubscript{2}/90/45/90\textsubscript{3}/0]<sub>S</sub>, with matching lamination parameter coordinates, is readily extracted from the laminate database.  Similarly, stacking sequence [45<sub>2</sub>/90<sub>2</sub>/-45/90/0/-45]<sub>S</sub> corresponds to the maximum shear buckling factor, $k_{xy}$ = 9.89, at ($\xi_9$, $\xi_{10}$, $\xi_{11}$) = (-0.35, -0.31, 0.5) on [Fig. 3(c)](#NegativeShearContoursXi0_5AR2_0).  Practical designs clearly offer more modest performance benefits than optimised solutions would suggest.

Note that the optimized lamination parameters for shear buckling, with $a/b$ = 1 and 2, were virtually the same for both simply supported and clamped conditions. The degrading influence of a <em>Bend-Twist</em> coupling on compression buckling load was also found to be similar for both simply supported and clamped boundary conditions \cite{York2017bt}.