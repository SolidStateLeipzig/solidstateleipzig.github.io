(sec-symmetry)=
# Content of lecture

## Symmetry operations

Long-range order of a crystal reflects its underlying symmetry. Most generally, **symmetry** of an object is a set of transformations that leave this object invariant. We will consider geometrical transformations that can be represented as

$$
    \rm{symmetry\ operation} = \mathbb{R} \oplus \mathbf{t} = \begin{pmatrix} R_{xx} & R_{xy} & R_{xz} \\ R_{yx} & R_{yy} & R_{yz} \\ R_{zx} & R_{zy} & R_{zz}\end{pmatrix} \oplus \begin{pmatrix}  t_x \\ t_y \\ t_z \end{pmatrix}

$$ (eq-symmetryop)

where $\mathbb{R}$ is a unitary transformation, such as rotation, and $\mathbf{t}$ is a translation in space by a given vector.

(sec-centering)=
## Translational symmetry: lattice centering


The simplest translational symmetry of a crystal is its periodicity. From Eq. {eq}`eq-Bravais` we know that $\mathbf{a},\mathbf{b},\mathbf{c}$ and their linear combinations are allowed translations, so all of them are symmetry operations of a crystal, as long as this crystal is periodic. Some other translations may be allowed too, leading to a classification of lattices by **lattice centering** into:

* **Primitive lattice** ($P$) has only $\mathbf{a},\mathbf{b},\mathbf{c}$ and their linear combinations as allowed translations
* **Face-centered lattice** ($F$) features additional translations $\mathbf{t}=\frac{1}{2}(\mathbf{a} \pm \mathbf{b}),\frac{1}{2}(\pm\mathbf{c}),\frac12(\mathbf{b}\pm\mathbf{c})$ (half of the face diagonal for each face)

* **Body-centered lattice** ($I$) features additional translations $\mathbf{t}=\frac12(\mathbf{a}\pm\mathbf{b}\pm\mathbf{c})$ (half of the body diagonals)

* **Base-centered lattice** ($A,B,C$) features additional translations by half of the face diagonal, but only for two faces out of six. For example, the $C$-centered lattice allows $\mathbf{t}=\frac12(\mathbf{a}\pm\mathbf{b})$

* **Rhombohedral lattice** ($R$) features an additional translation by $\mathbf{t}=\frac13(\mathbf{a}+\mathbf{b}+\mathbf{c})$ (one third of the body diagonal)

One could then ask why these additional vectors $\mathbf{t}$ are needed. Should they exist, lattice vectors can be re-defined as the shortest repetition vectors of the crystal, and every lattice will be primitive. True indeed, but some rotational symmetry may be lost on the way, as shown in {numref}`fig-cell`. Therefore, in a centered lattice one distinguishes:

* **Primitive cell** , which is the repetition unit with the smallest volume defined by the shortest translations $\mathbf{a}_p$, $\mathbf{b}_p$, $\mathbf{c}_p$

* **Conventional cell**, which is the smallest repetition unit of the highest symmetry defined by the lattice vectors $\mathbf{a},\mathbf{b},\mathbf{c}$

 ```{figure} /figures/ch2-unit-cell.svg
:name: fig-cell

Conventional and primitive unit cells of the body-centered cubic lattice. The lattice angles of the primitive cell deviate from $90^{\circ}$, so it has a lower symmetry than the conventional cell. Note that $\mathbf{a}_p,\mathbf{b}_p,\mathbf{c}_p$ are also shorter than $\mathbf{a},\mathbf{b},\mathbf{c}$, hence the primitive cell has the twice smaller volume than the conventional one.
```

In a primitive lattice, both unit cells coincide. In a centered lattice, the volume of the primitive cell is twice ($A,B,C,I$), three times ($R$), or four times ($F$) smaller than the volume of the conventional unit cell. 

From this point on, we will distinguish **lattice vectors** $\mathbf{a},\mathbf{b},\mathbf{c}$ that define the conventional unit cell, from **lattice translations** $\mathbf{t}$ that include $\mathbf{a},\mathbf{b},\mathbf{c}$ along with other vectors allowed by the lattice centering. [](#sec-rotational).

Lattice centering is an important part of describing crystal symmetry, but it may not have any immediate implications. We do not expect crystals with face-centered lattices to be distinct from the body-centered ones. However, in special cases, such as simple metals from {numref}`fig-metals`, lattice centering determines the packing fraction and directly affects density of the crystal.

(sec-rotational)=
## Rotational symmetry and birefringence

The $p$-fold \emph{rotation axis} is defined as the rotation by $\varphi = 360^{\circ}/p$. Here, $p$ must be integer because applying the same operation several times should end up in the full $360^{\circ}$ rotation. Rotation axes are labeled with numbers: two-fold rotation axis is 2, four-rold rotation axis is 4, etc. For a clockwise rotation, the corresponding transformation matrix is 

$$
    \mathbb{R} = \begin{pmatrix} \cos \varphi & \sin \varphi & 0 \\ -\sin \varphi & \cos \varphi & 0 \\ 0 & 0 & 1 \end{pmatrix}
$$ (eq-rotation)

for a $p$-fold rotation axis parallel to $z$.

Rotation axes have some immediate ramifications. First, they impose constraints on lattice parameters. Consider a four-fold rotation axis along $c$. This symmetry operation transforms $\mathbf{a}$ into $\mathbf{b}$ and thus requires not only $a=b$, but also $\gamma=90^{\circ}$. Three of such axes render a crystal cubic!

Another ramification concerns crystal properties. A crystal with one 4-fold rotation axis shows distinct properties along this direction and in the plane perpendicular to it. This disparity is pretty obvious if we turn the crystal and measure its property along different directions. In fact, it can be seen even in a single experiment! Crystals refract light, and refractive index depends on the light polarization. Light polarized along the symmetry axis (i.e., the light with the electric field vector parallel to the symmetry axis of the crystal) and light polarized perpendicular to the symmetry axis feature different refractive indices, $n_{\|}$ and $n_{\perp}$, respectively. A non-polarized light is split by such a crystal into two distinct beams. This effect is known as **birefringence** ($\Delta n=n_{\|}-n_{\perp}$). 

Historically, birefringence has been the very first tool used to identify crystal symmetries. It is still employed by geologists during field trips where advanced instruments are not available. It is also used technologically for a quick monitoring of product quality. Amorphous solids are normally isotropic and should not exhibit birefringence (for example, it's not seen in ordinary glass). However, strains lead to anisotropy and can be mapped out by shining a suitably polarized light on the sample. You can read more about it [here](https://en.wikipedia.org/wiki/Photoelasticity).

## Reflection and inversion symmetry

Eq. {eq}`eq-rotation` covers only some of the unitary transformations. Two further important operations are **inversion center** (labeled $\bar 1$ or $-1$) and **mirror plane** ($m$),

$$
 \mathbb{R}_{\rm inversion}=\begin{pmatrix} -1 & 0  & 0 \\ 0 & -1 & 0 \\ 0 & 0 & -1 \end{pmatrix}, \qquad\qquad
 \mathbb{R}_{\rm reflection}=\begin{pmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & -1 \end{pmatrix},
$$ (eq-inversion-reflection)
where the latter describes a mirror plane perpendicular to $z$ ($m \perp \mathbb{c}$). These symmetry elements can be combined with the rotation axes, namely, both can be present in the crystal at the same time. 

The reflection and inversion symmetries also have important implications. They determine polarity and chirality of the crystal. We will get back to this in Ch.~\ref{sec:symgroups} after we learn how individual symmetry elements build up a symmetry group.


## Neumann's principle

A general and very intuitive principle commonly attributed to Neumann is that **properties of a crystal should be invariant under its symmetry operations**. Neumann's principle is usually invoked in its mathematical form, which states that any tensor property $\mathbf{\sigma}$ should follow

$$
    \mathbf{\sigma} = \mathbb{R}^{-1} \mathbf{\sigma} \mathbb{R}
$$ (eq-neumann)

Consider linear-response properties, such as conductivity $\mathbf{\sigma}$ defined by Ohm's law $\mathbf{j}=\mathbf{\sigma}\,\mathbf{E}$ ($\mathbb{j}$ is electric current density and $\mathbf{E}$ is electric field) or permittivity $\mathbf{\varepsilon}$ defined by $\mathbf{P}=(\mathbf{\varepsilon}-1)\varepsilon_0\mathbf{E}$ ($\mathbf{P}$ is electric polarization). Both $\mathbf{\sigma}$ and $\\mathbf{\varepsilon}$ are second-rank tensors because electric field applied along one direction causes a response, polarization or current, along all three directions of the crystal. We express this idea by writing

$$
 j_{\alpha}=\sigma_{\alpha\beta}E_{\beta}
$$

and implying that conductivity has the general form of 

$$
    \mathbf{\sigma}=\begin{pmatrix}{\sigma_{xx}} &{\sigma_{xy}} & {\sigma_{xz}} \\ {\sigma_{yx}} & {\sigma_{yy}}&{\sigma_{yz}}\\{\sigma_{zx}}&{\sigma_{zy}}&{\sigma_{zz}} \end{pmatrix}
$$

with up to 9 independent components. 

Such tensors are usually symmetric, $\sigma_{\alpha\beta}=\sigma_{\beta\alpha}$. Their symmetry is rooted in some fundamental physical principles. For thermodynamic (equilibrium) properties it follows simply from their definition via change of free energy in the applied field,

$$
dG=-S\,dT+V\,dp-\mathbf{P}\,d\mathbf{E} \Rightarrow \mathbf{P}=-\left(\frac{\partial G}{\partial \mathbf{E}}\right)_{T,p}.
$$

Permittivity is then related to the second derivative of $G$ with respect to $\mathbf{E}$, and mixed derivatives must be equal,

$$
    \frac{\partial^2 G}{\partial E_{\alpha}\partial E_{\beta}}=\frac{\partial^2 G}{\partial E_{\beta}\partial E_{\alpha}} \Rightarrow \varepsilon_{\alpha\beta}=\varepsilon_{\beta\alpha}.
$$

A similar statement for transport properties is known as [Onsager reciprocal relations](https://journals.flvc.org/cee/article/download/122425/121384/). Without going into details we only mention here that these relations need to be amended in the presence of a magnetic field where conductivity tensor becomes antisymmetric (more on this in Ch.~\ref{sec:drude}).

Symmetry of the tensor reduces the number of independent components from 9 to 6. Additional constraints can be derived from crystal symmetry using Eq {eq}`eq-neumann`. For example, consider the 4-fold rotation axis parallel to $z$. According to Eq. {eq}`eq-rotation`, it leads to the transformation $(x,y,z)\rightarrow (y,-x,z)$ that converts $\mathbf{\sigma}$ into an equivalent tensor $\mathbf{\sigma}'$,

$$
    \mathbf{\sigma}'=\begin{pmatrix}{\sigma_{yy}}&{-\sigma_{yx}}&{\sigma_{yz}}\\{-\sigma_{xy}}&{\sigma_{xx}}&{-\sigma_{xz}}\\{\sigma_{zy}}&{-\sigma_{zx}}&{\sigma_{zz}}\end{pmatrix}\qquad{\rm vs.}\qquad\mathbf{\sigma}=
 \begin{pmatrix}{\sigma_{xx}}&{\sigma_{xy}}&{\sigma_{xz}}\\{\sigma_{yx}}&{\sigma_{yy}}&{\sigma_{yz}}\\{\sigma_{zx}}&{\sigma_{zy}}&{\sigma_{zz}}\end{pmatrix}.
$$

The tensor components should be pairwise equal, so $\sigma_{yy}=\sigma_{xx}$, whereas $-\sigma_{yx}=\sigma_{xy}$. For a symmetric tensor it means that all off-diagonal components vanish, leading to the final form of

$$
    \mathbf{\sigma} = \begin{pmatrix} \sigma_{xx} & 0 & 0\\ 0& \sigma_{xx} & 0 \\ 0 & 0 & \sigma_{zz} \end{pmatrix}
$$

for a crystal with the 4-fold symmetry axis.

Tensor form for a given crystal symmetry can be checked on the [Bilbao server](https://cryst.ehu.es/cgi-bin/cryst/programs/tensor.pl).

## Rotation vs. periodicity
Different symmetry operations have been friends until now, but they can be foes too. Specifically, not every kind of rotational symmetry is compatible with periodicity of the lattice. One can show that only 2-fold, 3-fold, 4-fold, and 6-fold rotations do not forbid periodicity in two and three dimensions and can be thus present in periodic crystals. This statement is known as [crystallographic restriction theorem](https://en.wikipedia.org/wiki/Crystallographic_restriction_theorem}). Its mathematical proof can be found [here](http://doi.org/10.2307/3647934).

Forbidden symmetries are not entirely impossible. For example, one may consider a crystal with the 5-fold symmetry and, therefore, without periodicity. Such crystals have been discovered in 1980's and dubbed **quasicrystals**. They are typically metallic and combine several chemical elements in rather weird proportions like Al $_{65}$ Cu $_{20}$ Fe $_{15}$. They serve as examples of aperiodic crystals. 
