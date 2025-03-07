(sec-vdw)=
# Content of lecture

## Covalent crystals

The formation of covalent bonds can be probed using the **covalent radius**.
```{note} 
The term *atomic radius* is somewhat more loosely defined, but most often it implies the covalent radius.

```
When $r_{AB}\leq r_A+r_B$, a covalent bond occurs between the atoms A and B. Shorter distances indicate stronger covalent bonds. This is well known from carbon in organic molecules where single (1.54 $\mathring{A}$), double (1.34 $\mathring{A}$), and triple (1.20 $\mathring{A}$) C--C bonds can be distinguished by their typical length and chemical environment. Covalent bonds in solids are not always identifiable as single, double, or triple, but the same trend holds.

Complex nature of the covalent bonds does not allow a generic description in the same vein as Eq.~\eqref{eq:enionic}. We can only say that shorter covalent bonds should lead to the increased lattice energy and higher bulk modulus. The typical lattice energies of covalent crystals are on the order of 10 eV/atom and the bulk moduli are in the range of $50-200$ GPa.

## Metallic crystals

There is not much to say about metallic crystals at this stage. We will address them in more detail in Ch.~\ref{sec:drude-sommerfeld}. For now let's mention without any explicit derivation that lattice energy of a metallic crystal is given by a rather non-intuitive expression

$$
 \mathcal{E}_{\rm lat}=\frac{3\,\hbar^2}{10\,m_e}(3\pi^2n_e)^{\frac23},
$$
so it depends on the electron concentration $n_e$ and decreases with increasing the lattice parameter. 

Metals can have lattice energies as low as 1 eV/atom and feature bulk moduli of several GPa only. Some of the elemental metals have melting points close to room temperature (cesium, gallium), whereas mercury is even a liquid. Nevertheless, other metals like tungsten are characterized by very high melting points and low compressibilities, exceeding those of the typical ionic crystals. It all depends on the electron concentration.

## Polymorphism

In elemental solids, the type of the crystal structure will be usually determined by chemical bonding. Metals tend to adopt simple and dense structures (see Ch.~\ref{sec:close-packing}), non-metals will often develop similar structures but with the packing of weakly bonded atoms (noble gases) or diatomic molecules (hydrogen, oxygen). Elements spanning the boundary between metals and non-metals show the most diverse behavior, as they can form different types of covalently-bonded structures and simultaneously appear in the metallic form. Tin is a celebrated example. It forms metallic crystals of white tin (body-centered tetragonal structure) that abruptly transform into non-metallic gray tin (diamond structure) on cooling. These two forms of tin are called **allotropes**. Allotropes are also known for carbon, sulphur, phosphorous.

Binary and more complex compounds will usually stick to one type of bonding and differ only in their structural details, although these details are by no means unimportant. They can have major implications for observed properties. One usually distinguishes:

* **polymorphs** as different structural forms of the same chemical compounds. They are labeled with Greek letters: $\alpha$-Sn, $\beta$-Sn, etc. Strictly speaking, allotropes can be also considered as polymorphs, as we just did for tin, and so all researchers do, especially when they deal with high-pressure structures of elemental solids. The somewhat old-fashioned word ``allotrope'' is basically reserved for different forms of elemental solids observed at ambient pressure.
* **enantiomorphs** as left and right forms of a chiral structure (see Ch.~\ref{sec:chirality})
*  **polytypes** as different structures arising from different stacking sequences. Polytypes are common in layered structures like graphite, but they could also occur in structures derived from close-packed layers, as in Ch.~\ref{sec:ionic-cp}. Labels of polytypes include the number of layers per unit cell and the indication of symmetry (cubic, hexagonal, rhombohedral). For example, zinc blende and wurtzite are the 3C- and 2H- polytypes of ZnS. Such polytypes are often observed in binary semiconductors.

## van der Waals radius and Lennard-Jones potential

Coming to van der Waals crystals, one usually defines the **van der Waals radius** as an effective radius of an atom or molecule. Such radii appeared due to van der Waals who proposed an equation of state for non-ideal gas,

$$
 \left(p+\frac{a}{V^2}\right)(V-b)=RT
$$

with the volume correction $b$ that subtracts volumes of individual molecules from the total volume of the system.
```{note}
The constant $a$ defines additional pressure caused by interactions between the molecules.
```
Ironically, van der Waals never worked on the problem of chemical bonding (let alone on solids), but his concept of an effective radius proved very useful to identify main interactions between weakly bonded atoms or molecules. An appreciable van der Waals bonding occurs when the distance between atoms is less than the sum of the corresponding van der Waals radii. Any further contacts will of course lead to some minute bonding too, but it is even weaker than the aforementioned one and, to a first approximation, negligible.

The interactions in van der Waals crystals are usually described by an effective potential,

$$
 \mathcal V(r_{ij})=-\frac{\mathcal A}{r_{ij}^6}+\frac{\mathcal B}{r_{ij}^{12}}
$$
where $\mathcal A$ and $\mathcal B$ are constants, and $r_{ij}$ is the distance between atoms. The first (attractive) term is due to [London dispersion force](https://en.wikipedia.org/wiki/London_dispersion_force) between dipoles. The second (repulsive) term is an empirical potential akin to the one we used in Eq.~\eqref{eq:enionic}. The power of 12 is chosen for reasons of mathematical convenience because this effective potential can be recast into the form

$$
 \mathcal V(r_{ij})=4\epsilon\left[-\left(\frac{\sigma}{r_{ij}}\right)^6 +\left(\frac{\sigma}{r_{ij}}\right)^{12} \right]
$$ (eq-lennard)

known as **Lennard-Jones potential** with $\sigma=(\mathcal B/\mathcal A)^{\frac16}$ and $\epsilon=\mathcal A^2/4\mathcal B$.
```{note}
We use $\sigma$ and $\epsilon$ following the standard notation of the Lennard-Jones potential. They should not be confused with the stress and strain appearing in Ch.~\ref{sec:mechanical}.
```



## Lattice energy

We will now repeat the same steps as in Ch.~\ref{sec:ionic} to determine the equilibrium distance $r_0$ and the corresponding lattice energy. Total energy of a van der Waals crystal is determined by the summation of Eq.~\eqref{eq:lennard},

$$
 \mathcal{E}_{\rm tot}(r)=\tfrac12\sum_{i,j}\mathcal V(r_{ij})=2\epsilon\left[-A_6\left(\frac{\sigma}{r}\right)^6 + A_{12}\left(\frac{\sigma}{r}\right)^{12} \right]
$$

where $r$ is the nearest-neighbor interatomic distance and we introduced lattice sums $A_6$ and $A_{12}$. They are similar in their meaning to the Madelung constant (Ch.~\ref{sec:madelung}), yet much easier to calculate because the series converge very fast. For an fcc crystal, $A_6=14.45$ and $A_{12}=12.13$.

Setting the derivative of $\mathcal{E}_{\rm tot}$ to zero yields the equilibrium distance,

$$
 \frac{d\mathcal{E}_{\rm tot}}{dr}=0 \Rightarrow
 2\epsilon\left[\frac{6A_6}{r_0}\left(\frac{\sigma}{r_0}\right)^6-\frac{12A_{12}}{r_0}\left(\frac{\sigma}{r_0}\right)^{12}\right]=0 \Rightarrow
 r_0=\sigma\left(\frac{2A_{12}}{A_6}\right)^{\frac16}
$$

that solely depends on the $\sigma$ parameter of the potential. Then, 

$$
 \mathcal{E}_{\rm lat}=-\mathcal{E}_{\rm tot}(r_0)=-2\epsilon\left[-A_6\left(\frac{\sigma}{r_0}\right)^6 + A_{12}\left(\frac{\sigma}{r_0}\right)^{12} \right]=\epsilon\,\frac{A_6^2}{2A_{12}},
$$
so lattice energy solely depends on $\epsilon$. This is certainly more elegant than the ionic case. 

An interesting feature of van der Waals crystals is that they become more stable on increasing the lattice parameter. This is because $\mathcal A$ increases with the atomic radius, as the atoms become more polarizable. The $\mathcal B$ value should increase too to ensure the increase in $\sigma=(\mathcal B/\mathcal A)^{\frac16}$ and the lattice parameter, but $\epsilon=\mathcal A^2/4\mathcal B$ increases concurrently, because it contains $\mathcal A^2$. Larger atoms and molecules develop stronger van der Waals bonds. For example, melting points increase across the family of noble gases from neon to xenon, and likewise increase across halogens from $F_2$ to $I_2$. On the absolute scale, lattice energies of van der Waals crystal remain quite low, though, typically in the range of $10-200$ meV/atom. 

## Bulk modulus

To calculate the bulk modulus, we repeat the procedure from Ch.~\ref{sec:bm-ionic}. We will assume the fcc structure again, but now the atoms are at the lattice sites, so $r=a/\sqrt 2$. Then volume per atom is $V=r^3/\sqrt 2$ and

$$
 \frac{d}{dV}=\frac{\sqrt 2}{3r^2}\frac{d}{dr},
$$

hence

$$
 B=V\,\frac{d^2\mathcal{E}_{\rm tot}}{dV^2}=\frac{\sqrt 2}{9\,r_0}\left.\frac{d^2\mathcal{E}_{\rm tot}}{dr^2}\right|_{r=r_0}=\frac{4\epsilon}{\sigma^3}\,A_{12}\left(\frac{A_6}{A_{12}}\right)^{\frac52}.
$$

There is now the ratio of $\epsilon$ and $\sigma^3$, so the trend may be less intuitive than in the case of energy, but nevertheless bulk modulus of van der Waals crystals will typically increase with increasing the lattice parameter. Iodine is less compressible than solid bromine. The absolute values of the bulk modulus are typically below 10 GPa and even below 1 GPa for some of the lighter atoms and molecules.