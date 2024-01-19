# Exercise 1: A general Hückel solver
A Python script to calculate the Huckel MO energies and their associated degeneracies for selected compounds, including:
- n-membered linear polyenes
- n-membered cyclic polyenes
- the following sp2 hybridised platonic solids:
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

## Physical interpretation of results

### Platonic solids
I find it improbable that most platonic solids possess a functional π system. In solids like the tetrahedron, cube, or octahedron, the orientation of the p orbitals may not facilitate effective bonding overlap between adjacent atoms. Note also that while Hückel theory assumes that only adjacent atoms can interact, here atoms that aren't directly adjacent might still interact with each other significantly due to their spatial proximity.

### Buckminsterfullerene
In this calculation, there appears to be a 9-fold degenerate level at energy α+1.000*β. Buckminsterfullerene belongs to the icosahedral point group, for which the largest degeneracy permitted is 5-fold. Therefore this level may arise through the accidental degeneracy of a 5-fold degenerate set and a 4-fold degenerate set.

### Linear and cyclic polyenes
The Hückel method tends to produce acceptable results for linear and cyclic polyenes. These structures adhere relatively well to the simplifying assumptions of the Hückel approach, allowing for reasonably accurate predictions.
