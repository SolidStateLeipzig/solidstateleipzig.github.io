
# Content

## Atomic coordinates and Wyckoff positions

Atomic positions in a crystal are defined as fractions of lattice translations,

$$
    \mathbf{r}=x\mathbf{a}+y\mathbf{b}+z\mathbf{c},
$$
where $x,y,z$ are **fractional (crystallographic) coordinates**. Their convenience in solid-state physics context will become clear soon (Ch.~\ref{sec:reciprocal}). On the other hand, evaluation of interatomic distances using $x,y,z$ does become problematic when lattice angles deviate from $90^{\circ}$. Whereas distances can be still calculated by hand, it is usually more practical to use dedicated software like [VESTA](https://jp-minerals.org/vesta/en/) that not only draws crystal structures but also gauges distances between the atoms and even measures bond angles. For atoms within the unit cell, $0\leq x,y,z<1$. Any other atom can be obtained via lattice translations.

Let an atom be placed at a position $(x,y,z)$. Without symmetry, this atom may feel rather lonely, but a symmetry element will typically generate counterparts of an atom. For example, inversion center at $(0,0,0)$ creates a counterpart at $(\bar x,\bar y,\bar z)$.
```{note} Crystallographers use bars to indicate minus sign in front of the coordinate.
```
A two-fold rotation axis, $2\parallel\mathbf{a}$, creates a counterpart at $(x,\bar y,\bar z)$ and so on. In this way, symmetry elements generate a **Wyckoff position**.


```{figure} /figures/ch4-Wyckoff.svg
:name: fig-Wickoff

Selected Wyckoff positions of the space group $Pmm2$ (No.~25). $4i$ is the general position not lying on any symmetry element. $2f$ and $1a$ are special positions with the lower multiplicity. In this figure, we used some standard notation of the symmetry diagrams: solid lines show the mirror planes, whereas gray pointed ovals are the two-fold rotation axes. You can find more of the symbols [here](https://crystalsymmetry.wordpress.com/space-group-diagrams/).
```

These Wyckoff positions can be general or special. A **general** Wyckoff position does not lie on any point symmetry element and shows the highest multiplicity allowed by the given space group. A **special** Wyckoff position lies on at least one point symmetry element, which then does not act on this atom, resulting in a lower multiplicity. For example, the general position in the space group $Pmm2$ has the multiplicity of 4; it is labeled $4i$. By contrast, the position $(0,0,z)$ on the two-fold rotation axis has the multiplicity of 1 (it is labeled $1a$) because it stays invariant under all symmetry operations ({numref}`fig-Wyckoff`).


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

Consider atomic planes separated by a distance $d$ from each other ({numref}`fig-bragg`). The waves reflected by two adjacent planes accumulate the path difference of $2d\sin\theta$ where $\theta$ is the angle between the incident beam and the atomic plane. These waves interfere constructively when the path difference equals an integer number of wavelengths ($m$), leading to the simple condition

$$ 
 2d\sin\theta=m\lambda
$$ (eq-bragg)

known as **Bragg's law**. It is customary to choose $m=1$. Higher-order interference maxima may occur too, but we don't need to take them into account. In Ch.~\ref{sec:recbragg} we will see that these $m\neq 1$ maxima are in fact due to the $m=1$ scattering but from different planes.

```{figure} /figures/ch4-bragg.svg
:name: fig-bragg

Bragg's law. Reflection of waves from parallel atomic planes gives rise to a constructive interference when the path difference is equal to an integer number of wavelengths. Experimentally, the angle $2\theta$ between the incident and scattered waves is measured.
```

Bragg's law shows that by scattering waves such as x-rays on a crystal, one expects to see a series of intensity maxima known as **Bragg peaks** or simply **reflections**. Experimentally, the angle $\theta$ can not be measured, but the angle $2\theta$ between the incident and scattered wave is easy to monitor. The $2\theta$ positions of the Bragg peaks correspond to the distances $d$ that contain information on the periodicity of the crystal. It is the basics of crystal structure determination, although by no means a complete procedure yet, as we will see in the following.


## Scattering experiments and x-ray diffraction

The setup described by Bragg's law is an example of a scattering experiment. One generally distinguishes
* **elastic scattering** where the scattered beam has the same energy as the incident beam
* \emph{inelastic scattering} where some energy is exchanged between the incident beam and the crystal

Elastic scattering is resolved in the angle $2\theta$. When Bragg peaks in the sense of Eq. {eq}`eq-bragg` are observed, this experiment is called **diffraction**. Inelastic scattering can be resolved in both angle $\theta$ and energy transfer $\mathcal{E}$. This experiment is in fact similar to spectroscopy, although spectroscopy is a somewhat broader term that also includes experiments that are done at the fixed scattering angle and resolved in energy, only.

Scattering experiments can be done with any kind of waves. We will see such examples later in these lecture notes, but for now our favorite type will be x-rays because their wavelength is matched to the typical interatomic distances and lattice parameters. Other types of radiation can be neutrons and electrons, as we will see in Ch.~\ref{sec:diffraction}.

**X-ray diffraction**, better known as **XRD**, is one of the most common experimental tools in solid-state research. It is essentially the scattering of monochromatic x-rays (photons with the single wavelength $\lambda$) on a crystalline sample. The scattered radiation is collected by a detector, and the angle $2\theta$ between the incident and scattered beams is measured. A diffraction pattern with a series of Bragg peaks is recorded. The positions and intensities of the Bragg peaks can be used for:
* identifying the sample and identifying different chemical compounds in mixed, multi-phase samples; each crystal structure gives rise to a unique series of Bragg peaks that serves as a fingerprint of this structure and underlying chemical compound.
* determining orientation of a crystal surface or a thin film
* resolving the crystal structure (more on this in Ch.~\ref{sec:diffraction})

```{note} The role of the intensities will become clear in Ch.~\ref{sec:diffraction}
```

XRD is a much more versatile technique compared to electron microscopy (Ch.~\ref{sec:microscopy}). It does not destroy the sample and does not require high vacuum. It is compatible with different sample environments and can be performed in a broad range of temperatures, pressures, electric and magnetic fields.


## Lattice planes and Miller indices

The concept of atomic or \emph{lattice planes} used in Bragg's law requires their proper classification. Importantly, in the derivation of Bragg's law one uses not a single lattice plane, but a series of periodically spaced planes of the whole crystal. Consider now two of these planes, the one that goes through origin and the plane adjacent to it. The latter crosses lattice vectors $\mathbf{a},\mathbf{b},\mathbf{c}$ at the positions $d_a,d_b,d_c$ away from the origin ({numref}`fig-hkl`). Then **Miller indices** $h,k,l$ for this family of atomic planes are defined as

$$
 h=a/d_a,\qquad k=b/d_b,\qquad l=c/d_c.

$$ (eq-hkl)


```{figure} /figures/ch4-hkl.svg
:name: fig-hkl

Left: definition of Miller indices $h,k,l$. The leftmost plane goes through the origin. An adjacent plane crosses the lattice vectors $\mathbf{a},\mathbf{b},\mathbf{c}$ at $d_a=a/h$, $d_b=b/k$, and $d_c=c/l$. The distance between the planes is $d_{hkl}$. Middle and right: the (200) planes are similar to the (100) planes but show a twice smaller spacing.
```

The Miller index of zero means that the lattice plane never crosses the respective axis, i.e., it is parallel to this axis. Three faces of the unit cell will then have indices of $(100)$, $(010)$, and $(001)$. Increasing the Miller indices shortens the spacing between the planes. For example, $(200)$ are the same lattice planes as $(100)$, but with the twice shorter spacing ({numref}`fig-hkl`).

The Miller indices must be integer to comply with periodicity of the lattice. Later we will come to see that they also describe a position in the reciprocal space and can be arbitrary in this sense. However, only integer values of $h,k,l$ describe something that matches periodicity of the crystal. 

The Miller indices can be used to determine the $d$ value in Bragg's law. For a crystal with $\alpha=\beta=\gamma=90^{\circ}$, 

$$
 \frac{1}{d_{hkl}^{\,2}}=\frac{h^2}{a^2}+\frac{k^2}{b^2}+\frac{l^2}{c^2}.
$$ (eq-d-distance)

We will prove this relation shortly (Ch.~\ref{sec:recbragg}). For now let's explain how the actual experiment works. An XRD measurement returns a set of peak positions $\theta_i$ that can be re-calculated into $d_i$'s using Bragg's law. Then one has to find the values of $a,b,c,\alpha,\beta,\gamma$ such that every $d_i$ is described by some integer values of $h,k,l$. This procedure is known as **indexing** of the Bragg peaks. A successful indexing returns lattice parameters of the crystal.


## Crystal faces and crystal directions
It should be clear from the above that crystal faces (and, consequently, surfaces) are labeled with the same Miller indices $h,k,l$. Here, one considers a single plane only, so there will be no difference between $(100)$, $(200)$, $(300)$, and so on, hence the smallest indices are always used. 

The notation of lattice planes and crystal faces should not be confused with the notation of crystal directions, even though three integer numbers $u,v,w$ are also involved in this case,

$$
 \mathbf{R}_{[u\,v\,w]}=u\,\mathbf{a}+v\,\mathbf{b}+w\,\mathbf{c}.

$$ (eq-direction)

In simple cases, these vectors $\mathbf{R}$ are perpendicular to the lattice planes with the same indices. For example, viewing a cubic crystal along the $[100]$ direction means that you look at the $(100)$ face of the cube. However, this is not true in general. We will see very soon that the $h,k,l$ values define a vector in the reciprocal space, whereas Eq. {eq}`eq-direction` corresponds to a real-space direction. Note also the different type of brackets used for the (lattice planes) vs. [crystal directions].


