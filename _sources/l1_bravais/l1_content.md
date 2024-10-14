# Content of lecture

## Bravais lattice and unit cell

Periodic pattern of the crystal can be described by a **Bravais lattice** defined as a set of points

$$ 
    \mathbf{R} = n_1 \mathbf{a} + n_2 \mathbf{b} + n_3 \mathbf{c}
$$ (eq-Bravais)

where $n_1$, $n_2$, $n_3$ are integers and $\mathbf{a}$, $\mathbf{b}$, $\mathbf{c}$ are three vectors that do not lie in the same plane. They are known as **lattice translations** or **lattice vectors**. The parallelepiped spun by these three vectors is the repetition unit of the lattice or its **unit cell** with the **lattice parameters** ($a,b,c$) and **lattice angles** ($\alpha,\beta,\gamma$). It is customary to define the angle between $\mathbf{b}$ and $\mathbf{c}$ as $\alpha$, the angle between $\mathbf{a}$ and $\mathbf{c}$ as $\beta$, and the angle between $\mathbf{a}$ and $\mathbf{b}$ as $\gamma$.

Not every lattice is a Bravais lattice. Consider for example hexagonal (honeycomb) lattice, one of the popular geometries in modern solid-state physics. This lattice is clearly periodic, but it is not a Bravais lattice _per se_, because its lattice sites can not be described with Eq. {eq}`eq-Bravais`. Bravais lattice of the honeycomb lattice is constructed by connecting second neighbors, as shown in {numref}`fig-Bravais`. The unit cell then contains two sites of the parent honeycomb lattice, one at the corner and one in the interior. This situation is known as a Bravais lattice **with basis**. Here, basis is the group of atoms contained by the unit cell. Of course, it is also possible to choose hexagon as the repetition unit of the honeycomb lattice. However, such a choice would introduce a disparity with other lattices, such as square lattice where the repetition unit is obviously a square. The advantage of Eq.{eq}`eq-Bravais` lies in the unified description of all periodic structures, so it is not surprising that Bravais lattice became the cornerstone of solid-state physics.

```{figure} /figures/ch1-lattice.svg
:name: fig-Bravais

Left: Bravais lattice, lattice vectors, and unit cell. Right: honeycomb lattice is not a Bravais lattice per se; its Bravais lattice is indicated by the red lines, with two atoms per unit cell.
```

## Close packing and structures of metals

A naive way of seeing crystals is arrays of atoms placed in the positions defined by Eq. {eq}`eq-Bravais`. The most dense packing is achieved when atoms touch each other. Consider atom as a sphere and put such atoms onto a simple cubic lattice. Its lattice parameter should be twice the radius of the sphere, $a=2r$. With one sphere per unit cell, the volume occupied by the sphere is $V_{sphere}=\frac{4}{3}\pi r^3=\pi a^3/6$. On the other hand, the unit-cell volume is $V_{cell}=a^3$. The ratio of these two volumes is the **packing fraction**, $p=V_{sphere}/V_{cell}$, and amounts to only 52 % for the simple cubic lattice. We can also introduce the **coordination number**, i.e., the number of neighboring atoms, which is as low as 6 in this case. Simple cubic lattice does not allow dense structures.

Finding a dense packing of spheres (better known as **close packing** in solid-state physics) is in fact a common [mathematical problem](https://arxiv.org/abs/math/9811071v2). By solving it, or by using general intuition of putting together spherical objects like billiard balls, we know that each sphere can be surrounded by six other spheres, resulting in a close-packed honeycomb layer. The next layer should follow the dips formed by the first one. Different possible stackings give rise to a series of close-packed structures, including:
 * ...ABABAB... (_hcp_ or hexagonal close packing)

 * ...ABCABC... (_ccp_ or cubic close packing, or \textit{fcc} = face-centered cubic structure)


 ```{figure} /figures/ch1-metals.svg
:name: fig-metals

Structures of simple metals. \textit{dhcp} is the double-hexagonal close-packing, ...ABACABAC...
```

 These two structures are much denser than the simple cubic lattice, thanks to the coordination number of 12 (six neighbors in each layer, plus three neighbors in each of the two adjacent layers). They are in fact common for simple metals, which are well described by this packing concept because only one type of atoms is present in the crystal and because denser packing allows higher electron concentration, which is favorable for the metallic bonding. Fig. {numref}`fig-metals` shows that more than half of simple metals adopt either hcp or fcc structures. Most of the remaining metals form a bcc (body-centered cubic) structure, which is only slightly less dense than the close-packed ones. 



| lattice type | packing fraction | coordination number|
| :--: | :--: | :--: |
| simple cubic | 0.52 | 6 |
| body-centered cubic (bcc) | 0.68 | 8 |
| hexagonal close-packed (hcp) | 0.74 | 12 |
| face-centered cubic (fcc) | 0.74 | 12 |


The choice between the bcc, fcc, and hcp structures for a given metal is far from trivial and depends on details of its band structure (Ch.~\ref{sec:bands}). Nevertheless, already at this point we can make a general prediction that bcc metals should transform into hcp or fcc structures on compression. This happens indeed in alkaline metals and also in iron that looses its magnetism upon transforming from bcc to hcp polymorph around 15 GPa (why denser structures are less likely to be magnetic is a separate and rather non-trivial question that will only be covered in the Advanced Solid-State Physics module). 




 

