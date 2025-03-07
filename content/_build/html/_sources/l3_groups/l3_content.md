(sec-symgroups)=
# Content of lecture

(sec-symelements)=
## Point symmetry operations

Only a few local (point) symmetry operations $\mathbb{R}$ are compatible with periodicity. Every periodic crystal can be then assigned to one or another symmetry group that comprises a subset of the following symmetry elements:

* Rotation axes: $2,3,4,6$ ($C_2,C_3,C_4,C_6$)
* Inversion centre: $\bar 1$ ($i$)
* Mirror plane: $m$ ($\sigma_v,\sigma_h$)
* Rotoinversion axes: $\bar 3$, $\bar 4$, $\bar 6$

Here, we use labels in the international (Hermann-Mauguin) notation, which is common in crystallography. The symbols in brackets are Sch\"onflies notation favored by spectroscopists.

The last element, **rotoinversion axes**, has not been discussed yet and requires a further comment. This symmetry element is a rotation followed by inversion,

$$
    \mathbb{R}_{\bar n} = \begin{pmatrix} -\cos \varphi & -\sin \varphi & 0 \\ \sin \varphi & -\cos \varphi & 0 \\ 0 & 0 & -1 \end{pmatrix}
$$

The inversion center $\bar 1$ is in fact the end member of this series, because it combines inversion with the 1-fold rotation. Using Eqs. {eq}`eq-rotation` and {eq}`eq-inversion-reflection`, one can verify that $\bar 2=m$. Three other rotoinversion axes are independent symmetry elements, which are needed to describe special situations, such as the symmetry of a tetrahedron ($\bar 4$). 

No Sch\"onflies symbols for rotoinversion axes exist, because a different symmetry element, **rotation-reflection axes** ($S_n$), is considered in this case. They are quite similar to $\bar n$, but rotation is followed by a mirror-plane reflection. This operation is also known as an **improper rotation**,

$$ 
    \mathbb{R}_{S_n} = \begin{pmatrix} \cos \varphi & \sin \varphi & 0 \\ -\sin \varphi & \cos \varphi & 0 \\ 0 & 0 & -1 \end{pmatrix}
$$

assuming $S_n\parallel z$. Simple algebra shows that $\bar 3=S_6$, $\bar 6=S_3$, and $\bar 4=S_4$, whereas $S_2=\bar 1$ and $S_1=m$, so we end up with exactly the same symmetry operations and an unnecessarily confusing notation.

(sec-pointgroup)
## Point groups and crystal classes. Polarity
A combination of symmetry elements constitutes a **symmetry group**. Here, group is used in [mathematical sense](https://en.wikipedia.org/wiki/Group_(mathematics)), as a closed set of elements with an operation that transforms them into each other. For example, a two-fold rotation axis and a mirror plane perpendicular to it generate the symmetry group (Fig.{numref}`fig-point`):

$$
 2/m = \left\{\,1,2,m,\bar 1\,\right\}.
$$

Repeated application of the two-fold rotation leads to the unitary operation, $2\otimes 2=1$. The same is true for the mirror plane, $m\otimes m=1$. Finally, 2 followed by $m$ results in the inversion center $\bar 1$. 

Another example: a point group composed of three mutually orthogonal mirror planes perpendicular to $\mathbf{a}$, $\mathbf{b}$, and $\mathbf{c}$ (Fig. {numref}`fig-point`). A consecutive application of $m_a$ and $m_b$ leads to the coordinate transformation $x,y,z\longrightarrow \bar x,\bar y,z$, so it is equivalent to a two-fold rotation axis along~$\mathbf{c}$. Each pair of planes generates a rotation axis, but we don't need to list them all, and the point group is labeled simply as $mmm$. It features eight symmetry elements,

$$
 mmm= \left\{\,1, 2_a, 2_b, 2_c, m_a, m_b, m_c, \bar 1\,\right\}.
$$

 ```{figure} /figures/ch3-point-groups.svg
:name: fig-point

Examples of point groups of symmetry.
```


Since one symmetry element can be obtained from a few others, it is customary to label the symmetry group by its main generators, similar to the examples above. One usually chooses rotation axis of the highest order and then symmetry elements perpendicular to it. Consider the following examples:

* $4/m$ is the four-fold rotation along $\mathbf{c}$ and the mirror plane perpendicular to $\mathbf{c}$.
* $4mm$ is the four-fold rotation along $\mathbf{c}$, the mirror planes perpendicular to $\mathbf{a}$ and $\mathbf{b}$, and the mirror planes perpendicular to $\mathbf{a}\pm\mathbf{b}$. The absence of / means that no mirror plane perpendicular to $\mathbf{c}$ occurs. Moreover, the $\mathbf{a}$ and $\mathbf{b}$ directions are equivalent (orange planes in Fig. {numref}`fig-point`, so they are mentioned only once, while the second $m$ stands for the mirror planes, which are perpendicular to the $ab$-diagonals (green).

There are altogether 32 **point groups** formed by the symmetry operations from Ch.~\ref{sec:symelements}. The full list can be found [on Wikipedia](https://en.wikipedia.org/wiki/Crystallographic_point_group) along with an explanation of the Sch\"onflies symbols of point groups that we will not consider here. Every point group defines its own **crystal class**, a family of crystals with the similar shape that reflects the underlying symmetry of the crystal structure. 

The relation between the crystal class and crystal shape is most useful in mineralogy. Synthetic crystals can be grown in different shapes, and they are often cut to a custom shape as required by the experiments. The point symmetry remains important, though, because it determines whether or not the crystal is polar. **Polar direction** is defined as the direction that stays invariant under all symmetry operations of the system. Crystal or molecule with at least one polar direction are capable of having dipole moment and electric polarization, which is important for ferroelectric and pyroelectric properties. Inversion centers and rotoinversion axes obviously forbid polarity. Examples of \emph{polar} symmetries are $4mm$ and $3m$, examples of \emph{non-polar} symmetries are $4/m$ and $3\,2$. 

## Crystal systems

32 points groups are hard to remember, and only crystallographers know them all (simply from experience and not from hard learning), but it is useful to be familiar with seven **crystal systems** that are distinguished by symmetry constraints imposed on the lattice parameters:

|   |   | |
| :--: | :--: | :--: |
| **Cubic** | $\alpha=\beta=\gamma=90^{\circ}$  |  $m\bar 3m$, $\bar 43m$, 432, $m\bar 3$, 23 |
| **Tetragonal** | $a=b\neq c$, $\alpha=\beta=\gamma=90^{\circ}$ |$4$, $4mm$, $4/m$, $4/mmm$, $\bar 4$, 422, $\bar 42m$ |
| **Orthorombic** | $a\neq b\neq c$, $\alpha=\beta=\gamma=90^{\circ}$ | $222$, $mm2$, $mmm$ |
| **Hexagonal**| $a=b\neq c$, $\alpha=\beta=90^{\circ}$, $\gamma=120^{\circ}$ | $6$, $6/m$, $6mm$, $6/mmm$, $\bar 6$, $622$, $\bar 6m2$ |
|**Trigonal** | $a=b\neq c$, $\alpha=\beta=90^{\circ}$, $\gamma=120^{\circ}$ | $3$, $3m$, $\bar 3$, $\bar 3m$, 32 |
|**Monoclinic** | $a\neq b\neq c$, $\alpha\neq\gamma\neq 90^{\circ}$, $\beta=90^{\circ}$| $2$, $m$, $2/m$ |
| **Triclinic** | $a\neq b\neq c$, $\alpha\neq\beta\neq\gamma\neq 90^{\circ}$| $1, \bar 1$|

Crystal system defines the form of tensor properties according to Neumann's principle, as explained in Ch.~\ref{sec:neumann}. The knowledge of the crystal system is also important for constructing reciprocal lattice and analyzing diffraction experiments, as we will see in Ch.~\ref{sec:structure} and~\ref{sec:reciprocal}.

Crystal system can be combined with the lattice centering from Ch.~\ref{sec:centering}. Back then, we mentioned that centering only makes sense when the conventional unit cell has a higher symmetry than the primitive cell. Otherwise, lattice vectors could be re-defined without loss of symmetry. Indeed, a centered triclinic lattice is redundant, because its unit cell can always be reduced. On the other hand, both face and body-centering occur for cubic and some other crystal systems where symmetry elements would be lost otherwise. Combining crystal systems and lattice centering gives rise to **14 Bravais lattices** that can be encountered in periodic crystals.

(sec-open)=
## Open symmetry elements

Only point symmetry operations have been considered so far. Crystals also feature translational symmetry, and they are allowed to have combined symmetry elements that contain both local transformations and translations within one operation in the sense of Eq.~\eqref{eq:symoperation}. Such symmetry elements are called **open** because they generate an infinite array out of a single atom. 

Importantly, open symmetry elements can only occur in crystals, so they are always accompanied by pure translations (Ch.~\ref{sec:centering}) and should be compatible with periodicity. Repeated application of an open symmetry element leads to a simple shift of an atom without any reflection or rotation. This shift should match one of the lattice translations that have been defined in Ch.~\ref{sec:centering}.

Two types of open symmetry elements should be introduced: glide plane and screw axis. **Glide plane** is a mirror reflection followed by a shift $\mathbf{t}'$. The label of the glide plane indicates the shift direction:

* $a,b,c$ involve the shift by half of the corresponding lattice vector; for example, $\mathbf{t}'=\mathbf{a}/2$ in the case $a$
* $n$ involves the shift by half of the face diagonal; for example, $\mathbf{t}'=(\mathbf{a}\pm\mathbf{b})/2$
*  $d$ involves the shift by one quarter of the face or body diagonal; for example, $\mathbf{t}'=(\mathbf{a}\pm\mathbf{b})/4$; it only occurs in the presence of lattice centering, because the shift by $2\,\mathbf{t}'$ should be an allowed lattice translation

The shift direction is always parallel to the plane. For example, an $a$ glide plane can't be perpendicular to the lattice vector $\mathbf{a}$.

```{note} Note that we have to distinguish italicized symbols ($a$), which are used for the glide planes, from bold symbols ($\mathbf{a}$) used for vectors. 
```
Otherwise, repeated application of the glide plane would generate a new translational symmetry along $a$, which is incompatible with the lattice translations.

**Screw axis** is a rotation followed by a shift of $\mathbf{t}'$ along this axis. Here, the shift direction is fixed, but the length of $\mathbf{t}'$ should match the order of rotation. The screw axis $n_p\parallel\mathbf{c}$ involves the rotation by $360^{\circ}/n$ followed by the shift of $\mathbf{t}'=\frac{p}{n}\,\mathbf{c}$. For example:

* $3_1$ is the $120^{\circ}$ rotation followed by a shift of $\mathbf{c}/3$
* $4_2$ is the $90^{\circ}$ rotation followed by a shift of $\mathbf{c}/2$

(sec-chirality)=
## Chirality

Screw axes impart their sense of rotation to the atomic arrangement and, therefore, to the crystal as a whole. For example $3_1$ and $3_2$ produce similar helical chains with the counter-clockwise and clockwise rotations, respectively ({numref}`fig-chirality`). It is an example of chirality.

```{figure} /figures/ch3-chirality.svg
:name: fig-chirality

Helical chains formed by the $3_1$ and $3_2$ screw axes in elemental tellurium. The numbers **1-2-3-4** show the consecutive action of the symmetry operator. In the case of $3_2$, the missing atoms are added through the regular lattice translation by $\mathbf{c}$.
```




More generally, **chirality** is defined as the property of an object not to match its mirror image. Mirror-plane symmetry renders an object non-chiral because the object does not change under this operation at all. On the other hand, any symmetry group that does not contain mirror operations (nor it contains inversion centers and rotoinversion axes, which are equivalent to the rotation-reflection axes) is chiral. Examples of chiral point groups are $2\,2\,2$ and $3\,2$. Note that some symmetry groups are polar and non-chiral or chiral and non-polar. Both polarity and chirality are rooted in the crystal symmetry, but different aspects of the symmetry are relevant in each case.

Chiral objects are interesting because they exist in (at least) two forms, known as left and right **enantiomers** (for molecules) and **enantiomorphs** (for crystals). These forms are almost indistinguishable, yet they may show drastically different properties. For example, many of the aminoacids, carbohydrates, and other biologically relevant molecules are chiral. Only one enantiomer is usually present in nature, and this choice of chirality has tremendous repercussions for biological systems.

## Space groups

Full symmetry of the crystal is defined by its:
* lattice centering that contains all translations allowed in this crystal (Ch.~\ref{sec:centering})
* point symmetry elements (Ch.~\ref{sec:symelements})
* open symmetry elements (Ch.~\ref{sec:open})

The combination of the three makes a **space group**. Space groups are labeled by four symbols: the first one indicates lattice centering, while the three others stand for symmetry elements along three nonequivalent directions. For example, $Pnma$ means:

* primitive lattice
* $n$ glide plane perpendicular to $\mathbf{a}$
* mirror plane ($m$) perpendicular to $\mathbf{b}$
* $a$ glide plane perpendicular to $\mathbf{c}$

Absent symmetry elements are usually not written. For example, $P2/m=P\,1\,2/m\,1$. On the other hand, $P\,4_2/m\,b\,c$ means 
* $4_2$ screw axis along $\mathbf{c}$ and a mirror plane ($m$) perpendicular to $\mathbf{c}$
* $b$ glide plane perpendicular to $\mathbf{a}$ (and, respectively, $a$ glide plane perpendicular to $\mathbf{b}$)
* $c$ glide planes perpendicular to $\mathbf{a}\pm\mathbf{b}$ 

(check again Ch.~\ref{sec:pointgroup} for the choice of directions in the 4-fold symmetric case).

An exhaustive list of \emph{230 space groups} can be found on the [Bilbao Crystallographic Server](https://cryst.ehu.es/cgi-bin/cryst/programs/nph-table?from=getwp) and in[International Tables for Crystallography](https://it.iucr.org/).
```{note} Many of the universities, including Leipzig, do not have access to this book. Fortunately, symmetry diagrams for many of the space groups can be also obtained free of charge from the [The Fascination of Crystals and Symmetry](https://crystalsymmetry.wordpress.com/space-group-diagrams/) website by Frank Hoffmann.

```



While 230 may look like a huge number, it still means that the number of possible symmetries is finite, so it is possible to go through each of them when necessary. Many of the interesting crystal properties become possible for selected symmetries only. Then the classification of crystals by their space groups helps one to identify those specific materials where the property of interest is likely to appear. This approach has been common in many recent studies, for example [here](https://doi.org/10.1038/s41467-017-00133-2).

```{note} Beware that you will need a quite advanced knowledge to understand the content of this paper.
```

The crystal class is determined by both point and open symmetry elements of the space group, because open symmetry elements have the same effect on lattice symmetry as the point ones. For example, $Pnma$ belongs to the $mmm$ crystal class and orthorhombic crystal system. $P4_2/mbc$ belongs to the $4/mmm$ crystal class and tetragonal crystal system. Both space groups are non-polar and non-chiral.

One tricky thing about space groups is that their different settings are usually possible. For example, $Pmmn$, $Pnmm$, and $Pmnm$ are all the same space group with the different choices of $\mathbf{a},\mathbf{b},\mathbf{c}$. Likewise, $P2/a$ and $P2/c$ are the same space group, with the $\mathbf{a}$ and $\mathbf{c}$ axes swapped. Such an ambiguity is unavoidable, but it has been mitigated by creating a catalog of space groups in their standard settings, again at the Bilbao server and in related sources. Each space group has got a unique number, which is often supplied in publications along with the space group symbol. Crystalloghers have also done a great job in enforcing standard settings and standard notations for the crystal symmetry. You can take a peek into their very systematic and perfectly organized world by visiting the website of International Union of Crystallography with its own [dictionary](https://dictionary.iucr.org), [teaching pamphlets](https://www.iucr.org/education/pamphlets), and a lot more.
