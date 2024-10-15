# Content of lecture

## Symmetry operations

Long-range order of a crystal reflects its underlying symmetry. Most generally, **symmetry** of an object is a set of transformations that leave this object invariant. We will consider geometrical transformations that can be represented as

$$
    \rm{symmetry\ operation} = \mathbb{R} \oplus \mathbf{t} = \begin{pmatrix} R_{xx} & R_{xy} & R_{xz} \\ R_{yx} & R_{yy} & R_{yz} \\ R_{zx} & R_{zy} & R_{zz}\end{pmatrix} \oplus \begin{pmatrix}  t_x \\ t_y \\ t_z \end{pmatrix}

$$

where $\mathbb{R}$ is a unitary transformation, such as rotation, and $\mathbf{t}$ is a translation in space by a given vector.

## Translational symmetry: lattice centering

The simplest translational symmetry of a crystal is its periodicity. From Eq. {eq}`eq-Bravais` we know that $\mathbf{a},\mathbf{b},\mathbf{c}$ and their linear combinations are allowed translations, so all of them are symmetry operations of a crystal, as long as this crystal is periodic. Some other translations may be allowed too, leading to a classification of lattices by **lattice centering** into:

* **Primitive lattice** ($P$) has only $\mathbf{a},\mathbf{b},\mathbf{c}$ and their linear combinations as allowed translations
* **Face-centered lattice** ($F$)

* **Body-centered lattice** ($I$)

* **Base-centered lattice** ($A,B,C$)

* **Rhombohedral lattice** ($R$)

One could then ask why these additional vectors $\mathbf{t}$ are needed. Should they exist, lattice vectors can be re-defined as the shortest repetition vectors of the crystal, and every lattice will be primitive. True indeed, but some rotational symmetry may be lost on the way, as shown in Fig.~\ref{fig:cell}. Therefore, in a centered lattice one distinguishes:

* **Primitive cell** , which is the repetition unit with the smallest volume defined by the shortest translations $\mathbf{a}_p$, $\mathbf{b}_p$, $\mathbf{c}_p$

* **Conventional cell**, which is the smallest repetition unit of the highest symmetry defined by the lattice vectors $\mathbf{a},\mathbf{b},\mathbf{c}$

Figure

In a primitive lattice, both unit cells coincide. In a centered lattice, the volume of the primitive cell is twice ($A,B,C,I$), three times ($R$), or four times ($F$) smaller than the volume of the conventional unit cell. 

From this point on, we will distinguish **lattice vectors** $\mathbf{a},\mathbf{b},\mathbf{c}$ that define the conventional unit cell, from **lattice translations** $\mathbf{t}$ that include $\mathbf{a},\mathbf{b},\mathbf{c}$ along with other vectors allowed by the lattice centering.

Lattice centering is an important part of describing crystal symmetry, but it may not have any immediate implications. We do not expect crystals with face-centered lattices to be distinct from the body-centered ones. However, in special cases, such as simple metals from {numref}`fig-metals`, lattice centering determines the packing fraction and directly affects density of the crystal.


## Rotational symmetry and birefringence

The $p$-fold \emph{rotation axis} is defined as the rotation by $\varphi = 360^{\circ}/p$. Here, $p$ must be integer because applying the same operation several times should end up in the full $360^{\circ}$ rotation. Rotation axes are labeled with numbers: two-fold rotation axis is 2, four-rold rotation axis is 4, etc. For a clockwise rotation, the corresponding transformation matrix is 
$$
    \mathbb{R} = \begin{pmatrix} \cos \varphi & \sin \varphi & 0 \\ -\sin \varphi & \cos \varphi & 0 \\ 0 & 0 & 1 \end{pmatrix}
$$
for a $p$-fold rotation axis parallel to $z$.

Rotation axes have some immediate ramifications. First, they impose constraints on lattice parameters. Consider a four-fold rotation axis along $c$. This symmetry operation transforms $\mathbf{a}$ into $\mathbf{b}$ and thus requires not only $a=b$, but also $\gamma=90^{\circ}$. Three of such axes render a crystal cubic!

Another ramification concerns crystal properties. A crystal with one 4-fold rotation axis shows distinct properties along this direction and in the plane perpendicular to it. This disparity is pretty obvious if we turn the crystal and measure its property along different directions. In fact, it can be seen even in a single experiment! Crystals refract light, and refractive index depends on the light polarization. Light polarized along the symmetry axis (i.e., the light with the electric field vector parallel to the symmetry axis of the crystal) and light polarized perpendicular to the symmetry axis feature different refractive indices, $n_{\|}$ and $n_{\perp}$, respectively. A non-polarized light is split by such a crystal into two distinct beams. This effect is known as **birefringence** ($\Delta n=n_{\|}-n_{\perp}$). 

Historically, birefringence has been the very first tool used to identify crystal symmetries. It is still employed by geologists during field trips where advanced instruments are not available. It is also used technologically for a quick monitoring of product quality. Amorphous solids are normally isotropic and should not exhibit birefringence (for example, it's not seen in ordinary glass). However, strains lead to anisotropy and can be mapped out by shining a suitably polarized light on the sample. You can read more about it [here](https://en.wikipedia.org/wiki/Photoelasticity).

