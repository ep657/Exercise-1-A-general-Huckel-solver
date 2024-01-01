# Exercise 1: A general Hückel solver
A Python script to calculate the Huckel MO energies and their associated energies for selected compounds, including:
- n-membered linear polyenes
- n-membered cyclic polyenes
- sp2 hybridised platonic solids, including:
  - tetrahedron
  - octahedron
  - cube
  - icosahedron
  - dodecahedron
- Buckminsterfullerene

  ## Theory
The Hückel method simplifies molecular orbital theory for conjugated hydrocarbon systems.
The Hückel matrix is formed from the assumptions:

$$
H_{ij} = \begin{cases}
    \alpha & \text{if } i = j \\
    \beta & \text{if } i \text{ is adjacent to } j \\
    0 & \text{otherwise}
\end{cases}
$$
