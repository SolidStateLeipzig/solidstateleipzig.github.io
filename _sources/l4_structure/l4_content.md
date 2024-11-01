# Content

## Atomic coordinates and Wyckoff positions

Atomic positions in a crystal are defined as fractions of lattice translations,

$$
    \mathbf{r}=x\mathbf{a}+y\mathbf{b}+z\mathbf{c},
$$
where $x,y,z$ are **fractional (crystallographic) coordinates**. Their convenience in solid-state physics context will become clear soon (Ch.~\ref{sec:reciprocal}). On the other hand, evaluation of interatomic distances using $x,y,z$ does become problematic when lattice angles deviate from $90^{\circ}$. Whereas distances can be still calculated by hand, it is usually more practical to use dedicated software like [VESTA(https://jp-minerals.org/vesta/en/) that not only draws crystal structures but also gauges distances between the atoms and even measures bond angles. For atoms within the unit cell, $0\leq x,y,z<1$. Any other atom can be obtained via lattice translations.

Let an atom be placed at a position $(x,y,z)$. Without symmetry, this atom may feel rather lonely, but a symmetry element will typically generate counterparts of an atom. For example, inversion center at $(0,0,0)$ creates a counterpart at $(\bar x,\bar y,\bar z)$.
```{note}Crystallographers use bars to indicate minus sign in front of the coordinate.
```
A two-fold rotation axis, $2\parallel\mathbf{a}$, creates a counterpart at $(x,\bar y,\bar z)$ and so on. In this way, symmetry elements generate a **Wyckoff position**.


Figure

These Wyckoff positions can be general or special. A **general** Wyckoff position does not lie on any point symmetry element and shows the highest multiplicity allowed by the given space group. A **special** Wyckoff position lies on at least one point symmetry element, which then does not act on this atom, resulting in a lower multiplicity. For example, the general position in the space group $Pmm2$ has the multiplicity of 4; it is labeled $4i$. By contrast, the position $(0,0,z)$ on the two-fold rotation axis has the multiplicity of 1 (it is labeled $1a$) because it stays invariant under all symmetry operations (Fig.~\ref{fig:wyckoff}).


Wyckoff positions have two implications. First, they help us to make the description of crystal structures more systematic. Lists of possible Wyckoff positions are available for every space group (again, on the [Bilbao server](https://cryst.ehu.es/cryst/get_wp.html) or in the International Tables for Crystallography). Second, the distribution of atoms over different Wyckoff positions has ramifications for crystal properties, such as the type of phonon modes and their response in infrared and Raman experiments. We will briefly touch on this issue in Ch.~\ref{sec:optical}. You can also learn more by trying the [SAM utility](https://cryst.ehu.es/rep/sam.html) at the Bilbao server.


## Crystal structure

The structure of a given crystal is described by several elements:
* lattice parameters: $a,b,c$ and $\alpha,\beta,\gamma$
* symmetry (space group) symbol
* list of Wyckoff positions occupied by atoms, with the corresponding coordinates: $x_j,y_j,z_j$

You will almost never see the full list of atoms in the unit cell. Only the Wyckoff positions (i.e., positions unrelated by symmetry) will be given. Other atoms can be generated using symmetry elements. 

Let's address several beginners' questions about crystal structures:

**Where to find crystal structures?**
In databases that together contain over a million of crystal structures that have been determined experimentally. You can use [Crystallography Open Database](http://www.crystallography.net/cod/) (free), [Karlsruhe database or ICSD](https://icsd.products.fiz-karlsruhe.de/) (commercial, inorganic compounds), and [Cambridge Structural Database or CSD](https://www.ccdc.cam.ac.uk/structures/) (commercial, organic compounds). Each of these databases contains the so-called cif-files that summarize structural information in a common format.

**How to read crystal structures?**

Experts can learn a lot by reading the cif-file as plain text. However, most people will find it much easier to draw the crystal structure using software like [VESTA](https://jp-minerals.org/vesta/en/). Then you immediately see all atoms, their positions relative to the unit cell and lattice translations, etc.


**How to understand crystal structures?**

The answer to this question depends on the information that you seek to obtain. There are generally three ways of thinking about crystal structures, sometimes they are called structural models:

* **close packing**, works for relatively simple compounds, such as monoatomic crystals discussed in Ch.~\ref{sec:lattice}. We will see some further applications in the ionic crystals too (Ch.~\ref{sec:ionic}).

* **ball-and-stick** means that you connect atoms, which are sufficiently close to each other, and indicate chemical bonds. In this way, one finds connectivity of the crystal, whether it is built of molecules, chains, layers... This approach is most fruitful in covalent and van der Waals crystals (Ch.~\ref{sec:vdw}).

* **polyhedral** means that you connect an atom to its neighbors and treat the resulting unit as a rigid body. Then you analyze connectivity of such polyhedra. This approach is especially useful in more complex ionic crystals that can not be described as closed-packed structures.

## Bragg's law

At first glance, there is not much more in a crystal than what we already considered: the atoms and their exact positions in space that can be extracted from Wyckoff positions with the use of lattice parameters and symmetry. However, we can also see this in a different light when shining light (with a properly chosen photon energy) on a crystal. In fact, most of the information about the crystal structure comes from scattering experiments where radiation with the short wavelength ($\lambda\sim 1 \mathring{A}$) in order to match the typical interatomic distances) is used. The simplest model of this scattering is given by Bragg's law.