# Project 01 — Linear Buckling of a Composite Plate

This project studies the lamination parameter design space of standard quad finite length plates.

## Contents
- DESIGN SPACE INTERROGATION

    The database for Bend-Twist coupled designs with up to 21 plies is presented graphically in Figs. \ref{figure:PlyPercent&LPDesignSpace} and \ref{figure:21PlyPointClouds}.  Figure \ref{figure:PlypercentageExplanation} represents the lamination parameter design space for extensional stiffness ($\xi_{1}$,$\xi_{2}$) with ply percentage mapping of straight fibre ply orientation. As mentioned in Chapter \ref{Ch5-Intro}, $\xi_{1-4}$ represent the extensional stiffness, $\xi_{5-8}$ represent the coupling (in \& out of plane) stiffness and $\xi_{9-12}$ represent the bending stiffness, each set has its own feasible design region. The lamination parameter point cloud for extensional stiffness is illustrated by 112 points (grey circles) in Fig. \ref{figure:PlypercentageExplanation}. Here $\xi_{3}$ = $\xi_{4}$ = 0, the coupling stiffness $\xi_{5-8}$ = 0, and the bending stiffness $\xi_{12}$ = 0, while $\xi_{9}$, $\xi_{10}$ and $\xi_{11}$ are all non-zero. Each of the 112 unique points represents many individual laminate designs sharing the same proportion of standard ply orientations, i.e. 0\textdegree, 90\textdegree and \textpm45\textdegree plies, but with different stacking sequences that result in different bending stiffnesses (i.e. different values of $\xi_{9}$, $\xi_{10}$ and $\xi_{11}$). The contents of the database are also summarized in Table \ref{Table:PlyContiguity}. The larger black triangle in Fig. \ref{figure:PlypercentageExplanation} represents the feasible region of the design space when the extensional stiffness is uncoupled (i.e. $A_{16}$ and $A_{26}$ are zero). Note that the 10\% rule has been applied, which means that each design consists of at least 10\% of each of the standard ply orientations, this defines a smaller triangle (a sub-region) within the uncoupled design space corresponding to this constraint. Ply contiguity further constrains the available design space, which is set to a maximum of 3 adjacent plies with the same orientation, as is now common design practice. Ply contiguity is used to prevent ‘ply blocking’, which refers to a large numbers of consecutive repeating plies with the same fibre angle, that would increase the likelihood of delamination occurring \cite{Bailie1997}. This condition further shrinks the available design space. The smaller black triangle in Fig 1a is defined by the application of both these two types of constraint. The green grid lines represent constant ply percentage values for 0°, 90° and ±45° plies, ranging from 0 to 100\% in intervals of 10\%, where the top, left and right lines of the triangular design space represent purely 0\textdegree, 90\textdegree and \textpm45\textdegree plies respectively. To give an example of how to read this graph, the blue point in Fig. \ref{figure:PlypercentageExplanation} at ($\xi_{1}$, $\xi_{2}$) = (-0.7, 0.8) contains (0/$\pm$45/90) ply percentages of (10/10/80), as indicated by the green grid lines. Typical locations of aircraft wing skins, spars and stiffeners in this design space are indicated by the red points in Fig 1a. The results in Table 1 reveal that applying the contiguity constraint alone creates results that closely match predictions when applying the 10\% rule constraint alone, across all ply number groupings. Figure \ref{figure:3DDesignSpaceExplaination} shows 20 points in a three-dimensional design space for bending stiffness defined by $\xi_{9}$, $\xi_{10}$ and $\xi_{11}$. The points are randomly selected from all available designs correspond to the points shown in Fig. \ref{figure:PlypercentageExplanation}. 

    <div id="fig-composite">

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

    <em><strong>Figure X.</strong> Lamination design space and corresponding geometric mappings.</em>

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

    As coupling is introduced, the design space expands. The design space becomes a 3D design space when one type of coupling is involved (e.g Bending-Twistiing) and 4D if 2 types (bending-Twisting-Extenson-Shearing). 

    <div id="CompressionContour+ModeShape.PNG">

    <img src="CompressionContour+ModeShape.PNG">

    <em><strong>Figure 1.</strong> Compression buckling contours $k_x(=N_xb^2/\pi^2D_{Iso})$ for $\xi_{11}$ = 0.0, with: $a/b$ = 1.0 (left); $a/b$ = 1.5 (middle) and; $a/b$ = 2.0 (right).</em>

    </div>

    [Figure 1](CompressionContour+ModeShape.PNG) illustrates contour maps with different aspect ratios ($a/b$ = 1, 1.5 and 2), where distinct different styles of parallel-line in-fill patterns, represent different buckling mode regions (indicated by the inset images above [Figure 1](CompressionContour+ModeShape.PNG).  The value of the buckling load for the contours is indicated by the numbers in the figure. Boundaries between these regions correspond to the cusps in Fig. \ref{figure:compressioncurve}. The 'mode change line’ (highlighted in one instance in Fig. \ref{figure:compressioncurve} and also in Fig. \ref{figure:CompressionContour+ModeShape} by a green line) separates two regions representing modes with one and two longitudinal half-waves, i.e. wavelength parameters m = 1 (red lines) and m = 2 (blue lines).  This mode change is also apparent in Fig. \ref{figure:CompressiveCurvePt1-5}, between curves 2 and 3 at aspect ratio $a/b$ = 1.0.  Such boundary lines are readily determined whenever Eq. \ref{eq:bucklingCFS} is applicable, by fixing one lamination parameter coordinate and solving for the other by simply equating $N_{x,m=1}$ and $N_{x,m=2}$.  The locations of the mode change at the boundaries in Fig. \ref{figure:CompressiveCurvePt1-5} correspond to ($\xi_{9}$, $\xi_{10}$) = (-0.567, 0.134) and (-0.691, 1), with buckling factor $k_x$ = 3.86 and 2.95, respectively.  The same procedure can be used to confirm the shape of the mode change line. 
