# Project 03 — Lamination Parameter Design Space

This project studies the lamination parameter design space of standard quad finite length plates.

## Contents
- DESIGN SPACE INTERROGATION

    The database for Bend-Twist coupled designs with up to 21 plies is presented graphically in [Figure 1](#Fig-DesignSpaceDemo). [Figure 1(a)](#PlyPercentageExplaination) represents the lamination parameter design space for extensional stiffness ($\xi_{1}$, $\xi_{2}$) with ply percentage mapping of straight fibre ply orientation. $\xi_{1-4}$ represent the extensional stiffness, $\xi_{5-8}$ represent the coupling (in \& out of plane) stiffness and $\xi_{9-12}$ represent the bending stiffness, each set has its own feasible design region. The lamination parameter point cloud for extensional stiffness is illustrated by 112 points (grey circles) in [Fig. 1(a)](#PlyPercentageExplaination). Here exntensional $\xi_{3}$ = $\xi_{4}$ = 0, the coupling stiffness $\xi_{5-8}$ = 0, and the bending stiffness $\xi_{12}$ = 0, while $\xi_{9}$, $\xi_{10}$ and $\xi_{11}$ are all non-zero. Each of the 112 unique points represents many individual laminate designs sharing the same proportion of standard ply orientations, i.e. 0\textdegree, 90\textdegree and \textpm45\textdegree plies, but with different stacking sequences that result in different bending stiffnesses (i.e. different values of $\xi_{9}$, $\xi_{10}$ and $\xi_{11}$). The larger black triangle in Fig. \ref{figure:PlypercentageExplanation} represents the feasible region of the design space when the extensional stiffness is uncoupled (i.e. $A_{16}$ and $A_{26}$ are zero). Note that the 10\% rule has been applied, which means that each design consists of at least 10\% of each of the standard ply orientations, this defines a smaller triangle (a sub-region) within the uncoupled design space corresponding to this constraint. Ply contiguity further constrains the available design space, which is set to a maximum of 3 adjacent plies with the same orientation, as is now common design practice. Ply contiguity is used to prevent ‘ply blocking’, which refers to a large numbers of consecutive repeating plies with the same fibre angle, that would increase the likelihood of delamination occurring. This condition further shrinks the available design space. The smaller black triangle in [Fig. 1(a)](#PlyPercentageExplaination) is defined by the application of both these two types of constraint. The green grid lines represent constant ply percentage values for 0°, 90° and ±45° plies, ranging from 0 to 100\% in intervals of 10\%, where the top, left and right lines of the triangular design space represent purely 0\textdegree, 90\textdegree and \textpm45\textdegree plies respectively. 
    
    To give an example of how to read this graph, the blue point in [Fig. 1(a)](#PlyPercentageExplaination) at ($\xi_{1}$, $\xi_{2}$) = (-0.7, 0.8) contains (0/$\pm$45/90) ply percentages of (10/10/80), as indicated by the green grid lines. Typical locations of aircraft wing skins, spars and stiffeners in this design space are indicated by the red points in [Fig. 1(a)](#PlyPercentageExplaination). [Figure 1(b)](#3DDesignSpaceExplaination.PNG) shows 20 points in a three-dimensional design space for bending stiffness defined by $\xi_{9}$, $\xi_{10}$ and $\xi_{11}$. The points are randomly selected from all available designs correspond to the points shown in [Fig. 1(a)](#PlyPercentageExplaination). 

    Finally, [Fig. 1(c)](#New3DSpace_NoPts.png) shows the location of the planes defined by $\xi_{11}$ = 0 (bounded by the dashed line) and $\xi_{11}$ = 0.5 (bounded by the dashed-dotted line) in the bending stiffness design space. These 2-D cross-sections are used later in later projects, where a 15-point grid of sample points is used to develop closed-form bucking equations. $\xi_{11}$ represents the out-of-plane coupling, with 0.5 being the most extreme value for this type of coupling used by industry. By using this value, the knock-down in buckling performance due to out-of-plane coupling can be assessed, while the size of the design space is reduced, making the optimisation more feasible.

    <div id="Fig-DesignSpaceDemo">

    <table style="border:1px solid black; border-collapse:collapse;">
    <tr>
    <td colspan="2" align="center" style="border:1px solid black; padding:8px;">
    <a id="PlyPercentageExplaination"></a>
    <img src="PlyPercentageExplaination.png" width="350"><br>
      <em>(a)</em>
        </td>
     </tr>
    <tr>
    <td align="center" style="border:1px solid black; padding:8px;">
     <a id="3DDesignSpaceExplaination"></a>
      <img src="3DDesignSpaceExplaination.PNG" width="280"><br>
      <em>(b)</em>
    </td>
       <td align="center" style="border:1px solid black; padding:8px;">
        <a id="New3DSpace_NoPts"></a>
      <img src="New3DSpace_NoPts.png" width="280"><br>
        <em>(c)</em>
    </td>
    </tr>
    </table>

    <em><strong>Figure 1.</strong> Lamination design space and corresponding geometric mappings.</em>

    </div>

- BUCKLING PERFORMANCE OF FINITE LENGTH PLATES
    - To assess the vast number of designs contained in the laminate database, a closed form solution of compression buckling is necessary. 

    <div align="center">

    $$
	N_x = \pi^2 [D_{11} (\frac{m}{a})^2 + 2(D_{11} + 2D_{66})(\frac{n^2}{b^2}) +D_{22}(\frac{n^4}{b^4})(\frac{a}{m})^2]
    $$

    </div>

from knowledge of the bending stiffness, $D_{ij}$, plate length, $a$, and width, $b$, and the buckling half-wave parameter, $m$ (= 1, 2, 3, ...), which produces the lowest critical force resultant N\textsubscript{x}. 

- CONTOUR MAPPING FOR COMPRESSION BUCKLING
    - For orthotropic laminates, the following buckling equation, represented by a 2-dimensional, 4\textsuperscript{th} order polynomial, can be solved estimated using buckling loads obtained from the exact closed form buckling solution at 15 equally spaced points across the lamination parameter design space, as illustrated by the example cross section in [Fig. 1(c)](#New3DSpace_NoPts.png), when $\xi_{11}$ = 0:

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

    Mode changes complicate the contour maps for finite length plates. Hence the closed form buckling soluton is no longer a continuous function across the design space. The mode change boundaries must therefore first be determined, and separate equations must be derived for each mode region. To help further understand the buckling mode changes across the lamination parameter design space, classical Garland curves are first presented across a range of aspect ratios ($a/b$) in Fig. \ref{figure:compressioncurve}  Garland curves show the relationship between buckling factor and the aspect ratios of laminates. These correspond to simply supported plates subject to uniaxial compression.  Here, the solid black lines represent the buckling load factor of uncoupled laminate designs, whilst the broken black lines represent the buckling load factor when $\xi_{11}$ = 0.5 (corresponding to the limit for practical designs), comparison of the two sets of lines illustrates the effect of introducing a \textit{Bend-Twist} coupling. The individual curves of Fig. \ref{figure:compressioncurve}, with circled labels 1 – 5, and 11 - 15 represent discrete coordinate points along the boundary of the $\xi_{9}$, $\xi_{10}$ lamination parameter design space, while curves 6-10 represent points along the middle line of the $\xi_{9}$, $\xi_{10}$ design space, as indicated by the corresponding label locations in Fig. \ref{figure:CompressionContour+ModeShape}. Points on the same curve also represent points with the same location on design spaces across a range of aspect ratios ($a/b$) from 0.5 to 2.5, the coordinates of the points on the design spaces are indicated by the coordinates under each curve. For example, the lowest curve, curve 1, in Fig. \ref{figure:CompressiveCurvePt1-5} represents the buckling factor of laminates with lamination parameters ($\xi_{9}$, $\xi_{10}$) = (-1, 1), in which the $a/b$ = 1.0 case is shown on Fig. \ref{figure:CompressionContour+ModeShapeA}. The curves are split into 3 separate graphs in Fig. \ref{figure:compressioncurve} to avoid confusion that might be caused by crowding overlapping curves.  Fine dotted black lines connect the cusps on the uncoupled ($\xi_{11}$ = 0) and coupled ($\xi_{11}$ = 0.5) curves demonstrate the effect of coupling on the location of mode change in terms of aspect ratio. Only 3 coupled curves with $\xi_{11}$ = 0.5 are presented in Fig. \ref{figure:CompressionContour+ModeShapeA} - \ref{figure:CompressionContour+ModeShapeC} because the design space shrinks as the value of $\xi_{11}$ increases, therefore no feasible data points are available for points located with $\xi_{10}$ > 0 for $\xi_{11}$ = 0.5.

    <div id="fig-garland">

    <table style="border:1px solid black; border-collapse:collapse;">
    <tr>
    <td align="center" style="border:1px solid black; padding:6px;">
      <a id="fig-garland-a"></a>
      <img src="GarlandCurvePt1-5.png" width="220"><br>
      <em>(a)</em>
    </td>
    <td align="center" style="border:1px solid black; padding:6px;">
      <a id="fig-garland-b"></a>
      <img src="GarlandCurvePt6-10.png" width="220"><br>
      <em>(b)</em>
    </td>
    <td align="center" style="border:1px solid black; padding:6px;">
      <a id="fig-garland-c"></a>
      <img src="GarlandCurvePt11-15.png" width="220"><br>
      <em>(c)</em>
    </td>
    </tr>
    </table>

    <em><strong>Figure 2.</strong> Compression buckling Garland curves for $\xi_1=-0.5$ (solid lines) and $\xi_1=0.5$ (broken lines). The corresponding lamination parameter coordinates $(\xi_1,\xi_2)$ are shown alongside each curve.</em>

    </div>



    As coupling is introduced, the design space expands. The design space becomes a 3D design space when one type of coupling is involved (e.g Bending-Twistiing) and 4D if 2 types (bending-Twisting-Extenson-Shearing). 

    <div id="CompressionContour+ModeShape.PNG">

    <img src="CompressionContour+ModeShape.PNG">

    <em><strong>Figure 1.</strong> Compression buckling contours $k_x(=N_xb^2/\pi^2D_{Iso})$ for $\xi_{11}$ = 0.0, with: $a/b$ = 1.0 (left); $a/b$ = 1.5 (middle) and; $a/b$ = 2.0 (right).</em>

    </div>

    [Figure 2](CompressionContour+ModeShape.PNG) illustrates contour maps with different aspect ratios ($a/b$ = 1, 1.5 and 2), where distinct different styles of parallel-line in-fill patterns, represent different buckling mode regions (indicated by the inset images above [Figure 2](CompressionContour+ModeShape.PNG).  The value of the buckling load for the contours is indicated by the numbers in the figure. Boundaries between these regions correspond to the cusps in Fig. \ref{figure:compressioncurve}. The 'mode change line’ (highlighted in one instance in Fig. \ref{figure:compressioncurve} and also in Fig. \ref{figure:CompressionContour+ModeShape} by a green line) separates two regions representing modes with one and two longitudinal half-waves, i.e. wavelength parameters m = 1 (red lines) and m = 2 (blue lines). Such boundary lines are readily determined whenever the closed-form buckling solution is applicable, by fixing one lamination parameter coordinate and solving for the other by simply equating $N_{x,m=1}$ and $N_{x,m=2}$.  The locations of the mode change at the boundaries correspond to ($\xi_{9}$, $\xi_{10}$) = (-0.567, 0.134) and (-0.691, 1), with buckling factor $k_x$ = 3.86 and 2.95, respectively.  The same procedure can be used to confirm the shape of the mode change line. 
