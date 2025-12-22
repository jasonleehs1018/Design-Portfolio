# Project 06 — Off-axis alignment
The project aim to explore the effect of off-axis alignmennt on first ply failure (FPF) performance of composite laminates with double-angle configurations.

## Introducton

The final section of this chapter involves compression tests. The main objective of the tests is to characterise the compression behaviour of the material including compression stiffness, evaluate predictions made in this chapter and investigate the failure strength of the laminate designs discussed in this chapter. Due to COVID-19, I was not able to perform the manufacture and test process myself, but Prof. Christopher York and Dr Periyasamy Manikandan kindly helped carry out the processes at the Singapore Institution of Technology. Double angle-ply laminate design, \textcolor{blue}{\textbf{\textit{d}}} with $\beta$ = -46.1\textdegree, isotropic, \textit{E-S} coupled and balanced and symmetric (BS) laminates with $\beta$ = 37.3\textdegree were manufactured, with 3 specimens tested for each design. The stacking sequences are listed in Chapter \ref{sec:4.2}. SE 84LV low temperature cure carbon fibre epoxy prepreg was used [14], the designed length, width and thickness of the laminates were: 150 mm, 25 mm and 3.30 mm, and a cross sectional area, $A$, of 82.5 mm\textsuperscript{2}. 

The unidirectional (UD) prepreg tape was rolled out and cut manually to the required fibre orientations and the plies were manually stacked according to the specified stacking sequences. To remove any voids or air gaps between plies during the lay-up process, debulking was performed in every 6 plies of stacking. Stacked laminates were then cured using an autoclave programmed to the recommendations given by the material supplier, where pressure and temperature are 1 bar and 80 \textcelsius.

The laminates are then cut into the desired size as shown in Fig. \ref{figure:Samples-cutting}.

<div align="center" id="figure:Samples-cutting">

<img src="Samples-cutting.png" width="350"><br>

<em><strong>Figure 1.</strong> Cutting DD laminates</em>

</div>


[Figure 1](#figure:Samples-DD) shows a demonstration of the manufactured DD laminates.

<div align="center" id="figure:Samples-DD">

<img src="Samples-DD.png" width="350"><br>

<em><strong>Figure 2.</strong> Manufactured DD laminates</em>

</div>

All the specimens were held using a fully clamped end boundary condition for the tests. The compression test was carried out using the Z100 Universal Test machine at a displacement rate of 1 mm/min (meaning the crosshead of the UTM is allowed to move by 1 mm per minute). The fixture used was identical to the one described in the ASTM standard \cite{ASTM-D3410}. 

The compression test was conducted as follows:
	-  The manufactured specimen was placed and aligned at the centre of the wedges using an alignment bar.
	-  The specimen with wedges was placed into the wedge housing block assemblies.
	-  The housing assemblies were attached to the platens, with the upper wedge housing block assembly attached to the upper crosshead of the test machine and the lower housing block assembly fitted on a lower platen.
	-  To ensure that no small clearance or gap was present between the planar surface of the wedges and the housing block, an initial preload was applied to the specimen before recording the actual test data, in this case, the preload was 1 kN.
	-  The coupon was loaded to 1 kN and returned to 0 to monitor the strain readings, where the strains were usually about 100 to 200 micro-strain, which is negligible. 
	-  The compression test was started, and the samples were loaded until failure.

The measured values of the manufactured laminates are shown in Table \ref{Table:ExpSpecimenDimensions}, where DD, ES, BS and ISO represent the double angle-ply, \textit{Extension-Shear coupled}, balance and symmetric and fully isotropic designs. 

<div id="Table:ExpSpecimenDimensions">

| Specimen | <em>l</em> (mm) | <em>w</em> (mm) | <em>t</em> (mm) | <em>A</em> (mm<sup>2</sup>) |
|:--------:|:--------------:|:--------------:|:--------------:|:--------------------------:|
| DD-1 | 150 | 24.72 | 3.29 | 81.31 |
| DD-2 | 150 | 24.00 | 3.40 | 81.60 |
| DD-3 | 150 | 24.97 | 3.41 | 85.02 |
| **—** | **—** | **—** | **—** | **—** |
| ES-1 | 150 | 23.95 | 3.39 | 81.19 |
| ES-2 | 150 | 24.04 | 3.38 | 81.24 |
| ES-3 | 150 | 24.57 | 3.38 | 83.05 |
| **—** | **—** | **—** | **—** | **—** |
| BS-1 | 150 | 23.94 | 3.39 | 81.14 |
| BS-2 | 150 | 24.17 | 3.39 | 81.94 |
| BS-3 | 150 | 24.42 | 3.41 | 85.27 |
| **—** | **—** | **—** | **—** | **—** |
| ISO-1 | 150 | 24.64 | 3.27 | 80.48 |
| ISO-2 | 150 | 23.99 | 3.38 | 81.07 |
| ISO-3 | 150 | 24.02 | 3.35 | 80.45 |

<em><strong>Table 4.5.</strong> Measured dimensions of manufactured laminate designs.</em>

</div>
Examples of the laminates after failure are shown in Fig. \ref{figure:failedSample}.

\begin{figure}[H]
	\begin{subfigure}{.75\linewidth}
		\includegraphics[width=\linewidth]{Ch4-DD/Failure-After.jpg}
		\captionsetup{justification=centering,singlelinecheck=false}
		\caption{\label{figure:Failure-After}}
	\end{subfigure}
	\end{figure}
	\begin{figure}[ht]\ContinuedFloat
	\begin{subfigure}{.5\linewidth}
		\includegraphics[width=\linewidth]{Ch4-DD/Failure-Sample.jpg}
		\captionsetup{justification=centering,singlelinecheck=false}
		\caption{\label{figure:Failure-Sample}}
	\end{subfigure}
	\captionsetup{justification=raggedright,singlelinecheck=false}
	\caption{\label{figure:failedSample}Samples after failure for (a) all \textit{E-S} laminates and (b) a zoomed in capture of one of the laminates after failure.} 
\end{figure}

The resulting compressive stress is given as:
\begin{equation}
	\sigma_i = \frac{P_i}{A}			
\end{equation}
where P\textsubscript{i}} represents the compressive load at a particular point. 
Finally, the chord modulus of elasticity, E\textsubscript{chord}, is given as:
\begin{equation}
	E = \frac{\delta\sigma}{\delta\epsilon}			
\end{equation}

A range of strain from 1000 to 3000 $\mu$ strain  is used for modulus calculations, which is recommended by ASTM standards \cite{ASTM-D3410}. Strain gauges were attached to the front and back surfaces of the test specimens, one on each surface. A compression load was applied until the specimens failed. The resulting failure strength, maximum stress, strain and modulus obtained using both the measured dimension and design dimensions are summarised in Tables \ref{Table:ExpCal-Measured} and \ref{Table:ExpCal-Designed}. The resulting stress-strain graphs of the specimens are presented in Fig. \ref{figure:StressStrainExp}. 
While FPF predictions are made using Tsai-Wu failure criteria for comparisons, which are given in Table \ref{Table:FPFPredictionForComText}, since the engineering properties of the SE 84LV material is not given by the material supplier, T300/5208 is used for the prediction and the predictions are used to compare to the test results.

\begin{table}[H]
	\centering
	\captionsetup{justification=raggedright,singlelinecheck=false}
	\caption{\label{Table:ExpCal-Measured}Resulted failure strength, maximum stress, strain and modulus obtained from using measured dimensions.}
	\begin{tabular}{ccccccccccc}
		\cline{1-1} \cline{3-6} \cline{8-11} 
		Property & & \multicolumn{4}{c}{P\textsubscript{max} (kN)} & & \multicolumn{4}{c}{$\sigma$\textsubscript{max} (kN)} \\
		\cline{1-1} \cline{3-6} \cline{8-11} 
		Sample & & Iso & DD & ES & BS & & ISO & DD & ES & BS \\
		\cline{1-1} \cline{3-6} \cline{8-11} 
		1 &  & 22.70 & 28.56 & 22.83 & 30.72 & & & 351.30 & 281.15 & 378.66 \\
		2 &  & 29.32 & 29.73 & 24.58 & 23.32 &  & 361.68 & 364.36 & 302.56 & 284.62 \\
		3 &  & 31.06 & 21.95 & 22.42 & 26.22 &  & 386.08 & 258.17 & 269.99 & 314.85 \\
		Average &  & 30.19 & 26.75 & 23.28 & 26.75 &  & 373.88 & 324.61 & 284.57 & 326.04 \\
		\cline{1-1} \cline{3-6} \cline{8-11} 
		Property &  & \multicolumn{4}{c}{$\epsilon$\textsuperscript{u}\textsubscript{av} (\%)} &  & \multicolumn{4}{c}{E (GPa)} \\
		\cline{1-1} \cline{3-6} \cline{8-11}  
		Sample &  & ISO & DD & ES & BS &  & ISO & DD & ES & BS \\
		1 &  &  & 0.86 & 0.62 & 1.05 &  &  & 42.99 & 38.66 & 40.13 \\
		2 &  & 0.74 & 1.01 & 0.81 & 0.87 &  & 51.19 & 39.07 & 38.72 & 39.67 \\
		3 &  & 0.70 & 0.68 & 0.75 & 0.87 &  & 48.88 & 40.78 & 37.85 & 36.40 \\
		Average &  & 0.72 & 0.85 & 0.73 & 0.93 &  & 50.03 & 40.95 & 38.41 & 38.74 \\
		\cline{1-1} \cline{3-6} \cline{8-11} 
	\end{tabular}
\end{table}

\begin{table}[H]
	\centering
	\captionsetup{justification=raggedright,singlelinecheck=false}
	\caption{\label{Table:ExpCal-Designed}Resulted failure strength, maximum stress, strain and modulus obtained from using designed dimensions.}
	\begin{tabular}{ccccccccccc}
		\cline{1-1} \cline{3-6} \cline{8-11} 
		Property & & \multicolumn{4}{c}{P\textsubscript{max} (kN)} & & \multicolumn{4}{c}{$\sigma$\textsubscript{max} (kN)} \\
		\cline{1-1} \cline{3-6} \cline{8-11} 
		Sample & & Iso & DD & ES & BS & & ISO & DD & ES & BS \\
		\cline{1-1} \cline{3-6} \cline{8-11} 
		1 &  & 22.70 & 28.56 & 22.83 & 30.72 & &  & 346.24 & 276.69 & 372.41 \\
		2 &  & 29.32 & 29.73 & 24.58 & 23.32 & & 355.41 & 360.38 & 297.93 & 282.67 \\
		3 &  & 31.06 & 21.95 & 22.42 & 26.22 & & 376.48 & 266.07 & 271.78 & 317.79 \\
		Average &  & 330.19 & 26.75 & 23.28 & 26.75 & & 365.95 & 324.23 & 282.13 & 324.29 \\
		\cline{1-1} \cline{3-6} \cline{8-11} 
		Property &  & \multicolumn{4}{c}{$\epsilon$\textsuperscript{u}\textsubscript{av} (\%)} &  & \multicolumn{4}{c}{E (GPa)} \\
		\cline{1-1} \cline{3-6} \cline{8-11}  
		Sample &  & ISO & DD & ES & BS &  & ISO & DD & ES & BS \\
		1 &  &  & 0.86 & 0.62 & 1.05 & & & 42.99 & 38.66 & 40.13 \\
		2 &  & 0.74 & 1.01 & 0.81 & 0.87 & & 51.19 & 39.07 & 38.72 & 39.67 \\
		3 &  & 0.70 & 0.68 & 0.75 & 0.87 & & 48.88 & 40.78 & 37.85 & 36.40 \\
		Average &  & 0.72 & 0.85 & 0.73 & 0.93 & & 50.04 & 40.95 & 38.41 & 38.74 \\
		\cline{1-1} \cline{3-6} \cline{8-11} 
	\end{tabular}
\end{table}

\begin{table}[H]
	\centering
	\captionsetup{justification=raggedright,singlelinecheck=false}
	\caption{\label{Table:FPFPredictionForComText}First ply Failure load predictions of the fully isotropic, DD design \textcolor{blue}{\textbf{\textit{d}}} with $\beta$=-46.1\textdegree, \textit{E-S} coupled and balanced and symmetric designs $\beta$=37.3\textdegree under compressive load.}
	\begin{tabular}{cccc}
		\hline 
		\multicolumn{4}{c}{FPF Strength Prediction (N)}\\
		\hline 
		ISO & DD laminate design \textcolor{blue}{\textbf{\textit{d}}} ($\beta$ = -46.1) & \textit{ES} & BS ($\beta$=37.3\textdegree) \\
		\hline
		22,780 & 19,977 & 18,059 & 19,279 \\ 
		\hline
	\end{tabular}
\end{table}
Note that one of the strain gauges for ES-1 specimens malfunctioned during the test and no strain gauges were installed for ISO-1. Therefore, the results for these 2 test samples are simply discarded. 

\begin{figure}[H]
	\begin{subfigure}{.4\linewidth}
		\includegraphics[width=\linewidth]{Ch4-DD/StressStrain-Iso.PNG}
		\captionsetup{justification=centering,singlelinecheck=false}
		\caption{\label{figure:StressStrain-Iso}}
	\end{subfigure}
	\begin{subfigure}{.4\linewidth}
		\includegraphics[width=\linewidth]{Ch4-DD/StressStrain-DD.PNG}
		\captionsetup{justification=centering,singlelinecheck=false}
		\caption{\label{figure:StressStrain-DD}}
	\end{subfigure}
	
	\begin{subfigure}{.4\linewidth}
		\includegraphics[width=\linewidth]{Ch4-DD/StressStrain-ES.PNG}
		\captionsetup{justification=centering,singlelinecheck=false}
		\caption{\label{StressStrain-ES}}
	\end{subfigure}
	\begin{subfigure}{.4\linewidth}
	\includegraphics[width=\linewidth]{Ch4-DD/StressStrain-BS.PNG}
	\captionsetup{justification=centering,singlelinecheck=false}
	\caption{\label{StressStrain-BS}}
	\end{subfigure}
		\captionsetup{justification=raggedright,singlelinecheck=false}
		\caption{\label{figure:StressStrainExp}Stress-strain curves of specimens for (a): Isotropic; (b): DD design \textcolor{blue}{\textbf{\textit{d}}}; (c): \textit{Extension-Shear} and; (d): Balanced and Symmetric laminates.} 
\end{figure}

Table \ref{Table:FPFPredictionForComText} shows the numerical predictions of FPF for the 4 different designs. It can be seen that the isotropic design has the highest predicted FPF load, the \textit{E-S} coupled design has the lowest failure strength and the DD design has a similar performance as the balanced and symmetric design. The compression test results for the 4 designs in Tables \ref{Table:ExpCal-Measured} and \ref{Table:ExpCal-Designed} show a similar relationship but with higher values. The isotropic design has the highest failure load, while the \textit{E-S} design is the first to fail and the DD and balanced and symmetric designs lie in the middle with very similar failure strengths. Figure \ref{figure:StressStrainExp} presents the stress and strain relationships of the samples for the 4 different designs. The results show that \textit{E-S} coupled laminates have the most consistent results, but only 2 samples were available for comparison. The \textit{E-S} coupled design does not show any favourable improvement compared to the other designs, while DD laminate with off-axis alignment gives a similar failure strength as the balanced and symmetric design with standard fibre orientation. Laminate design \textcolor{blue}{\textbf{\textit{d}}} was chosen as the weakest without off-axis alignment, other DD designs (which have stronger FPF strength without off-axis alignment) with their beta that gives their responding maximum \textit{E-S} can be manufactured and tested. 

This is a preliminary experiment, only 3 specimens were manufactured and tested for each design, which cannot conclude the findings reliably, therefore more specimens should be manufactured and tested with 155 mm length that provides more accurate results. The failure load of the predictions is on average 3,000 N lower than the test results, the difference between the prediction and test results is due to the difference in material used for the predictions and actual test. For future experiment, the engineering properties should be characterised for better predictions and direct comparisons with the test. The difference in failure load can also be associated with the prediction tool, predictions were made with the Tsai-Wu failure criterion, but failure is predicted slightly differently according to the failure criteria, as discussed in Chapter \ref{Chapter:Introduction}. Therefore, predictions should be done with other failure criteria and compared to the experimental results to find out the criterion that has the closest fit to the test results. 

Moreover, the recommended length of the specimen is 140 to 155 mm, and the actual size of the specimen is 150 mm, which is within the suggested range. However, the sample is subjected to shear deformation soon after the load is not pure axial compression load. After 50 tests, it was concluded that specimens with 155 mm length provided more accurate modulus and strength values compared to the data provided by the supplier, than 150 mm samples. Moreover, specimens of 155 mm were able to be slotted within the wedges more firmly, reducing the chance of in-plane shear motion occurring under axial compression loads.

In terms of potential future work, buckling and first ply failure tests can also be performed, which would act as validations for all the numerical and analytical work performed in the past 4 years.  
