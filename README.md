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

By setting α to 0 and β to 1, the Hückel Hamiltonian can be reduced to the adjacency matrix. The energy eigenvalues are related to the eigenvalues of the adjacency matrix by: 

$$
E_i = \alpha + \lambda_i \beta
$$

Where

$$
\begin{equation*}
\begin{aligned}
E_i & : \text{Energy eigenvalue of the Hückel Hamiltonian} \\
\alpha & : \text{the Coulomb integral} \\
\lambda_i & : \text{Eigenvalue of the adjacency matrix} \\
\beta & : \text{the resonance integral}
\end{aligned}
\end{equation*}
$$

For linear and cyclic systems, the program automatically generates the adjacency matrix based on the number of atoms. For the sp2-hybridized Platonic solids and Buckminsterfullerene, predefined adjacency matrices are included due to their complexity.

## Usage

To launch the program, run huckel_solver.py. The program requires user input for the type of molecule to be analysed.

### Available input modes:
- linear polyene (prompt for n)
- cyclic polyene (prompt for n)
- a set of preset molecules:
  - tetrahedron
  - octahedron
  - cube
  - icosahedron
  - dodecahedron
  - Buckminsterfullerene
