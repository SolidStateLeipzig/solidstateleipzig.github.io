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