# Project 01 — Linear Buckling of a Composite Plate

This project studies the linear (eigenvalue) buckling behaviour of composite laminates with FEA and closed-form buckling solution.

## Contents
1. FEA
- Geometry setup
  - Plate dimensions: 300 mm × 300 mm
  - Shell modelling (S8R5 elements)
- Material properties
  - Graphite/epoxy T300/5208
- Layup
  - [-45/90/0/45/0/45/90/45/-45/0/-45/90/-45/90/45/90/0/-45/0/45/0/45/-45/90]<sub>T</sub>
- Mesh strategy
  - ![Mesh](https://github.com/jasonleehs1018/Design-Portfolio/blob/main/project-01-linear-buckling/mesh.JPG?raw=true)
- Boundary conditions
  - Simply supported on both ends
  - Compressive load applied in the x-direction
- Buckling load results
  - Eigenvalue from Abaqus: 10453
  - Converted buckling load: $N_x$ = 104.972 N/mm
- Mode shape visualisation
  - ![Buckling-mode](https://github.com/jasonleehs1018/Design-Portfolio/blob/main/project-01-linear-buckling/Buckling%20Plot.JPG?raw=true)
 
2. Closed-form buckling solution
- Equation: $N_x = \pi^2 [D_{11} (\frac{m}{a})^2 + 2(D_{11} + 2D_{66})(\frac{n^2}{b^2}) +D_{22}(\frac{n^4}{b^4})(\frac{a}{m})^2]$
  - a: length of the laminate
  - b: width of the laminate
  - m and n: the number of buckle half waves in the x and y axes
  - $D_{11}$ and $D_{22}$ are the elements from the ABD matrix 
- Buckling load results
  - $N_x$ = 105.214 N/mm
