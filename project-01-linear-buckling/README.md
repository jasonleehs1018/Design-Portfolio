# Project 01 — Linear Buckling of a Composite Plate

This project studies the linear (eigenvalue) buckling behaviour of composite laminates with different layups using Abaqus shell modelling.

## Contents
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
  - Converted buckling load: 1049.72 N/mm
- Mode shape visualisation
  - ![Buckling-mode](https://github.com/jasonleehs1018/Design-Portfolio/blob/main/project-01-linear-buckling/Buckling%20Plot.JPG?raw=true)
