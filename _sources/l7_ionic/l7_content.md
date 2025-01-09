# Content of lecture

## Types of chemical bonding

Many of the crystal properties can be understood from the perspective of bonding between the atoms. Four main types of chemical bonding are usually distinguished:
* **ionic**, due to electrostatic forces between charged units (ions)
* **covalent**, due to an overlap of atomic orbitals
* **metallic**, due to shared (itinerant) electrons
* **van der Waals**, due to dipole-dipole and other weak interactions, such as London dispersion force (between induced dipoles)


One often identifies a separate group of **hydrogen bonds**, which occur between atoms with small, fractional charges, such as H and O in water and organic molecules. These bonds are somewhat stronger than the typical van der Waals bonds, yet for our purpose they fall into the same group of weak bonding. We will also discuss **molecular crystals** where finite units (molecules) formed by covalent bonds are held together by van der Waals bonds.

## Cohesive and lattice energies

Stability of the crystal is characterized by its energy. In this context, two closely related energies can be defined. **Cohesive energy** is the energy required to break the crystal into individual atoms. **Lattice energy** is the energy required to split the crystal into its constituents.

```{note}
Older textbooks, including the one by Ashcroft and Mermin define cohesion energy simply as lattice energy and describe the formation of crystal from its constituents as *cohesion*.
```

The cohesive and lattice energies are equal for metallic crystals and for simple covalent crystals like diamond. However, they are very different in molecular crystals where molecules formed by covalent bonds are held together by van der Waals bonds. In this case, only lattice energy is the relevant energy scale because it shows the energy cost of breaking the crystal into individual molecules (think of sublimation of iodine into a gas of $I_2$ molecules). A somewhat similar situation occurs in ionic crystals. Compare

$$
\begin{align*}
 {\rm AB}_{(s)}+\mathcal{E}_{\rm coh}\ & \longrightarrow\ \ {\rm A}_{(g)} + {\rm B}_{(g)},  \\
 {\rm AB}_{(s)}+\mathcal{E}_{\rm lat}\ & \longrightarrow\ \ {\rm A}^+_{(g)} + {\rm B}^-_{(g)} 

\end{align*}

$$
where the subscripts $(s)$ and $(g)$ denote the solid and gas states, respectively. 

Lattice energies are obtained from **calorimetry experiments** where the amount of heat released or absorbed in a given process is measured. Sublimation enthalpy of a metallic, covalent, or molecular crystal is a direct measure of its lattice energy.
```{note} 
In thermochemistry, enthalpies are commonly used instead of energies because measurements are performed at a constant pressure rather than constant volume. Then, strictly speaking, lattice *enthalpy* is obtained. This difference is usually unimportant, since solids show only a minor difference between energy and enthalpy owing to the small thermal expansion, see also Ch.~\ref{sec:expansion}.
``` 
More often, though, the quantity measured in the experiment is the formation enthalpy $\Delta_fH$, which is neither cohesive nor lattice energy of the crystal:
$$ {\rm Na}_{(s)}+\tfrac12{\rm Cl}_{2(g)}\ \longrightarrow \ \ {\rm NaCl}_{(s)}+\Delta_fH$$

This formation enthalpy can be related to the lattice energy by considering all intermediate processes (Fig.~\ref{fig:born-haber}) and adding up relevant energies: sublimation energy of the Na metal, ionization potential of the Na atom, bond dissociation energy of the Cl$_2$ molecule, and electron affinity of the Cl atom. All these quantities can be measured in separate experiments, and eventually lattice energy of NaCl can be obtained from $\Delta_fH$ of NaCl. This method is known as the **Born-Haber cycle**. Thermochemistry data can be found in multiple sources, such as [NIST Chemistry WebBook](https://webbook.nist.gov/chemistry/) and [CRC Handbook of Chemistry and Physics](https://hbcp.chemnetbase.com).

\begin{figure}
\hspace{0.2cm}
\begin{minipage}{8cm}
 \includegraphics[scale=1.15]{ch7-energy}
\mathcal{E}d{minipage}
\hfill
\begin{minipage}{7cm}
\caption{\label{fig:energy-r}
Crystal energy $\mathcal{E}_{\rm tot}$ as a function of the interatomic distance $r$. Lattice parameters define the equilibrium value $r_0$, while the depth of the energy minimum is the lattice energy $\mathcal{E}_{\rm lat}$.
}
\vspace{0.5cm}
\mathcal{E}d{minipage}
\mathcal{E}d{figure}

It is also helpful to represent crystal energy as a function of an effective interatomic distance, $\mathcal{E}(r)$, as shown in Fig.~\ref{fig:energy-r}. Then the position of the energy minimum yields the equilibrium distance $r_0$ and, consequently, the lattice parameter of the crystal. The depth of the minimum is the lattice energy $\mathcal{E}_{\rm lat}$.


## Madelung constant

We will now concentrate on the ionic crystals and try to calculate $\mathcal{E}(r)$. To this end, we assume that the interatomic forces are Coulomb in nature and determine the electrostatic potential at a given site $i$,

$$
 \mathcal V_i=\frac{e}{4\pi\varepsilon_0}\sum_j\frac{z_j}{r_{ij}}
$$ `eq-ionic-potential`

where $z_j$ is the ionic charge and $r_{ij}$ is the distance between ions. This summation can be replaced with

$$
 \mathcal V_i=\frac{e}{4\pi\varepsilon_0}\frac{\alpha_i}{r}
$$

where $r$ stands for the nearest-neighbor distance and $\alpha_i$ is the **Madelung constant** for the site~$i$. This Madelung constant is defined for a given structure type and ionic charge and does not depend on the exact lattice parameter. Getting the actual values of $\alpha_i$ is far from trivial because Coulomb interactions are long-range, and the series defined by Eq.~\eqref{eq:ionic-potential} is [conditionally convergent](https://en.wikipedia.org/wiki/Conditional_convergence).

```{note}
Some instructive examples of the conditional convergence of electrostatic energy in ionic crystals can be found [here](https://doi.org/10.1021/ed078p1198) and [here](https://doi.org/10.1021/ed052p58).
```

 One practical approach to this problem is the [Ewald summation](https://en.wikipedia.org/wiki/Ewald_summation).

Coulomb energy of the crystal can be then written as

$$
 \mathcal{E}_{\rm Coul}=\tfrac12\sum_i ez_i\mathcal V_i= \tfrac12\sum_i\frac{e^2z_i\alpha_i}{4\pi\varepsilon_0r}
$$

with the pre-factor $\frac12$ to avoid double-counting. This summation will include several terms according to the number of different atomic positions in the crystal. In a simple AB crystal, symmetry requires that $\alpha_+=\alpha_-=\alpha$. Using $z_+=-z_-=z$, one finds

$$
 \mathcal{E}_{\rm Coul}=-\frac{\alpha z^2e^2}{4\pi\varepsilon_0r}
$$

This energy does not have a minimum, and indeed an ionic crystal with only Coulomb forces should collapse. An energy minimum in the vein of Fig.~\ref{fig:energy-r} appears when Coulomb energy is augmented by a repulsive energy,

$$
 \mathcal{E}_{\rm tot}(r)=-\frac{\alpha z^2e^2}{4\pi\varepsilon_0r}+\frac{C_{\rm rep}}{r^m}

$$ `eq-enionic`

where $C_{\rm rep}={\rm const}$ and $m$ is also a constant that takes values between 6 and 10 depending on the ions. This repulsive potential is empirical in nature and mimics the intuitive understanding that different atoms cannot penetrate into each other. Beyond this common intuition, the repulsion goes back to the Pauli exclusion principle, as explained [here](https://doi.org/10.1063/1.5081060).


## Born-Landé equation

Equilibrium distance $r_0$ corresponds to the energy minimum of $\mathcal{E}_{\rm tot}(r)$ from Eq.~\eqref{eq:enionic},

$$
 \frac{d\mathcal{E}_{\rm tot}}{dr}=0\Rightarrow
 \frac{\alpha z^2e^2}{4\pi\varepsilon_0r_0^2}-m\frac{C_{\rm rep}}{r_0^{m+1}}=0 \Rightarrow
 r_0^{m-1}=4\pi\varepsilon_0\frac{mC_{\rm rep}}{\alpha z^2e^2}\Rightarrow
 C_{\rm rep}=\frac{\alpha z^2e^2}{4\pi\varepsilon_0m}r_0^{m-1}
$$ `eq-crep`

It can be used to calculate lattice energy,

$$
 \mathcal{E}_{\rm lat}=-\mathcal{E}_{\rm tot}(r_0)=\frac{\alpha z^2e^2}{4\pi\varepsilon_0r_0}-\frac{\alpha z^2e^2}{4\pi\varepsilon_0r_0}\frac{1}{m}=\frac{\alpha z^2e^2}{4\pi\varepsilon_0r_0}\left(1-\frac{1}{m}\right),
$$ `eq-born-Landé`


resulting in the **Born-Landé equation** for ionic crystals.

This equation has some immediate implications:

* lattice energy of an ionic crystal increases with the ionic charge; therefore, oxides ($z=2$) usually have much higher melting points than halides ($z=1$)
* lattice energy of an ionic crystal decreases with the interatomic distance ($r_0$); therefore, melting points decrease from NaF to NaI and from NaF to CsF and correlate with the lattice parameter

Typical lattice energies of ionic crystals are in the range of $5-10$ eV/f.u. Born-Landé equation can also be used to calculate lattice energy for the known interatomic distance, which is usually determined by XRD. The unknown parameter $m$ enters the energy as $1/m$ and changes the result only marginally. This parameter can be determined when another experimental observable, such as bulk modulus, is available. 

## Bulk modulus

The isothermal **bulk modulus** is defined as

$$
 B=-V\left(\frac{\partial p}{\partial V}\right)_T
$$ `eq-bulkmod`

It shows the change in the crystal volume under pressure (more on this in Ch.~\ref{sec:eos}). The bulk modulus can be obtained from $\mathcal{E}_{\rm tot}$ if one considers thermodynamic definition of pressure, $p=-(\partial \mathcal{E}/\partial V)_T$. The bulk modulus is essentially the second derivative of $\mathcal{E}_{\rm tot}$ with respect to $V$. In contrast to lattice energy, Eq.~\eqref{eq:born-Landé}, the exact expression for the bulk modulus depends on the structure type, which defines the relation between $V$ and $r$ in the crystal. 

Let's choose rocksalt-type structure (Ch.~\ref{sec:ionic-radius}) as an example. The distance $r$ is the separation between the cation and anion, $r=a/2$. Then, $V=a^3/4=2r^3$ (volume per formula unit) and 

$$
 \frac{d}{dV}=\frac{1}{6r^2}\frac{d}{dr}\Rightarrow 
 B=V\frac{d}{dV}\frac{d\mathcal{E}_{\rm tot}}{dV}=\frac{r}{18}\frac{d}{dr}\left(\frac{1}{r^2}\frac{d\mathcal{E}_{\rm tot}}{dr}\right).
$$

This value should be taken at $r=r_0$ where $d\mathcal{E}_{\rm tot}/dr=0$. Then, the equation simplifies to

$$
 B=\frac{1}{18\,r_0}\left.\frac{d^2\mathcal{E}_{\rm tot}}{dr^2}\right|_{r=r_0}=\frac{m-1}{18}\frac{\alpha z^2e^2}{4\pi\varepsilon_0r_0^4}
$$

where we used Eq.~\eqref{eq:crep} to express $C_{\rm rep}$ via $r_0$.

Clearly, bulk modulus shows the same trends as lattice energy. Oxides are less compressible than halides, that is, they feature higher bulk moduli. Compressibility of an ionic crystal increases upon increasing its lattice parameter. By measuring both $B$ and $r_0$, the value of $m$ and, eventually, the exact lattice energy can be determined. Typical bulk moduli of ionic crystals are in the range of $10-200$ GPa.

## Ionic radius and Pauling's rule

Whereas the Born-Landé equation, Eq.~\eqref{eq:born-Landé}, offers a simple explanation for changes in lattice energy, melting points, and bulk moduli across different ionic crystals, it fails to answer one fundamental question: which structure type is chosen by a given ionic material? The Madelung constants for different structure types can be compared, but how to deal with the distance $r_0$? 

Typical values of $r_0$ can be obtained from the so-called **ionic radii** that have been estimated for every possible ion of every chemical element by analyzing the statistics of interatomic distances in thousands of crystal structures determined experimentally. One assumes $r_0\simeq r_+ + r_-$ and finds the optimal values of $r_+$ and $r_-$ that fit the experimental $r_0$ in different materials. Different sets of ionic radii exist, the most common one being the system by Shannon and Prewitt quoted in multiple handbooks, for example [here](http://abulafia.mt.ic.ac.uk/shannon/). Because the ionic radii are determined from the experimental data, they take different values depending not only on the ionic charge but also on the coordination number. Increasing the charge and/or the coordination number reduces ionic radius of a cation. The opposite is true for anions, which are generally larger than cations because adding an electron requires extra space. 

Ionic radii are often sufficient to analyze structure types of different ionic crystals. **Pauling's first rule** postulates that the coordination number of a cation in an ionic crystal is determined by the ratio $r_+/r_-$.
 ```{note}
Four other Pauling's rules are even more empirical and can be found [here](https://en.wikipedia.org/wiki/Pauling's_rules).
```
This rule goes back to a simple geometrical argument that anions should not come too close to each other. Therefore, smaller cations require lower coordination numbers. The threshold values of $r_+/r_-$ have been derived as follows:


\begin{center}
\renewcommand{\arraystretch}{1.2}
\begin{tabular}{c@{\hspace{1.5cm}}c@{\hspace{1.5cm}}c}
 \textit{CN} & \textit{polyhedron} & \textit{$r_+/r_-$ larger than} \\
  3 & triangle & 0.155 \\
	4 & tetrahedron & 0.225 \\
	6 & octahedron & 0.414 \\
%	8 & anticube & 0.645 \\
	8 & cube & 0.732 
\mathcal{E}d{tabular}
\mathcal{E}d{center}
\medskip

The most common coordination numbers are 4 and 6. Representative structure types are **zinc blende** and **rocksalt** shown in Fig.~\ref{fig:structure-types}. Very large cations like Cs $^+$ may form **CsCl-type** structures with the cubic coordination.

\begin{figure}
\includegraphics{ch7-structure-types}
\caption{\label{fig:structure-types}
Common structure types of ionic crystals: zinc blende (fcc lattice), rocksalt (fcc lattice), and CsCl-type (primitive cubic lattice).
}
\mathcal{E}d{figure}

Pauling's consideration of the ionic radii inspires polyhedral description of ionic crystals. Anions form the polyhedron around a cation. By defining these polyhedra, the connectivity of the structure can be analyzed. 

## Ionic crystals as close-packed structures

Structures of ionic crystals can be also analyzed from the perspective of close packing. Anions form close-packed layers because they are usually bigger than cations. Then cations fill octahedral and tetrahedral voids between these close-packed layers. There is one octahedral and two tetrahedral voids per anion.

Let anions form the cubic close packing:
* filling octahedral voids yields the \href{https://en.wikipedia.org/wiki/Cubic_crystal_system#Rock-salt_structure}{rocksalt structure} (NaCl)
* filling $\frac12$ of the tetrahedral voids yields the \href{https://en.wikipedia.org/wiki/Cubic_crystal_system#Zincblende_structure}{zinc blende structure} (ZnS, CdTe)
* filling all tetrahedral voids yields the \href{https://en.wikipedia.org/wiki/Fluorite_structure}{fluorite structure} (CaF$_2$). Note that in fluorite cations form the close-packed structure, whereas anions occupy the tetrahedral voids. The situation is reversed in antifluorite (Na$_2$O) where anions form the close-packed structure and anions are in the voids.
* filling octahedral and $\frac12$ of the tetrahedral voids yields the \href{https://en.wikipedia.org/wiki/Spinel_group}{spinel structure} (MgAl$_2$O$_4$)

A similar construction is possible for the hexagonal close packing of anions too:
 * filling octahedral voids yields the \href{https://en.wikipedia.org/wiki/Hexagonal_crystal_family#Nickel_arsenide_structure}{NiAs structure} (MnS)
* filling $\frac12$ of the tetrahedral voids yields the \href{https://en.wikipedia.org/wiki/Hexagonal_crystal_family#Wurtzite_structure}{wurtzite structure} (ZnS, AgI)

This simple principle describes many of the common structure types of ionic compounds and also elucidates their hexagonal or fcc symmetries. However, it is not always easy to understand which structure type is preferred by a given compound. One compound may form different structures as in the case of ZnS. This is an example of **polymorphism**.