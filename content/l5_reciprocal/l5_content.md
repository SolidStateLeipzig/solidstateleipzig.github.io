# Content of lecture
## Laue condition

Bragg's law is so simple that it does not describe all features of the scattering process. It does not account for the presence of different atoms, nor for the different reflection intensities, and it treats atomic planes as simple mirrors that reflect the incident beam in one direction. A more realistic description has been proposed by Laue who considered interference of wmathbf{a}es scattered on two different atoms inside the crystals. 

```{figure} /figures/ch5-laue.svg
:name: fig-laue

Laue condition of the constructive interference. The wmathbf{a}es scattered by two atoms, which are separated by the lattice vector $\mathbf{R}$, acquire a path difference that should be a multiple of the wmathbf{a}elength $\lambda$. The unitary vectors $\mathbf{n}$ and $\mathbf{n}'$ show the directions of $\mathbf{k}$ and $\mathbf{k}'$, the propagation vectors of the incident and scattered wmathbf{a}es, respectively.
```

Without loss of generality, we consider $\mathbf{k}$ and $\mathbf{k}'$, the propagation vectors of the incident and scattered wmathbf{a}es, respectively. If two atoms are separated by a vector $\mathbf{R}$, the path difference between the two scattered wmathbf{a}es becomes ({numref}`fig-laue`)

$$
 R\cos\theta+R\cos\theta'=\mathbf{r}\,(\mathbf{n}'-\mathbf{n})
$$

where $\mathbf{n}$ and $\mathbf{n}'$ are unitary vectors along $\mathbf{k}$ and $\mathbf{k}'$, respectively. Using the definition of the propagation vector, $\mathbf{k}=(2\pi/\lambda)\,\mathbf{n}$ and $\mathbf{k}'=(2\pi/\lambda)\,\mathbf{n}'$, the interference condition can be written as

$$
 \frac{\lambda}{2\pi}\,\mathbf{R}(\mathbf{k}'-\mathbf{k})=m\lambda\quad \Rightarrow \quad
 \mathbf{R}\,(\mathbf{k}'-\mathbf{k})=2\pi m
$$ (eq-laue)

with integer $m$. This equation is known as the \emph{Laue condition}. It should hold for every lattice vector $\mathbf{R}$ defined by Eq. {eq}`eq-Bravais`, because a pair of atoms can be found for every such vector.


## Reciprocal lattice

The vectors $\mathbf{k}'-\mathbf{k}$ satisfying the Laue condition form a \emph{reciprocal lattice} of the crystal. One defines the reciprocal lattice as a family of vectors $\mathbf{G}$ that fulfill

$$
 e^{i\mathbf{G}\mathbf{R}}=1

$$ (eq-reclat)

for every lattice vector $\mathbf{R}$. It is common to say that $\mathbf{R}$'s belong to the direct lattice of the crystal in real space, whereas $\mathbf{G}$'s occur in the **reciprocal space**. 

Reciprocal lattice can be constructed explicitly by choosing the vectors 

$$
 \mathbf{a}^*=2\pi\,\frac{[\mathbf{b}\times\mathbf{c}]}{\mathbf{a}\cdot[\mathbf{b}\times\mathbf{c}]},\quad
 \mathbf{b}^*=2\pi\,\frac{[\mathbf{c}\times\mathbf{a}]}{\mathbf{a}\cdot[\mathbf{b}\times\mathbf{c}]},\quad
 \mathbf{c}^*=2\pi\,\frac{[\mathbf{a}\times\mathbf{b}]}{\mathbf{a}\cdot[\mathbf{b}\times\mathbf{c}]}.

$$ eq-recdef

Then it is easy to verify that

$$
 \mathbf{a}^*\mathbf{a}=2\pi,\quad \mathbf{a}^*\mathbf{b}=0,\quad \mathbf{a}^*\mathbf{c}=0
$$

and so on, such that any vector

$$
 \mathbf{G}=h\mathbf{a}^*+k\mathbf{b}^*+l\mathbf{c}^*
\label{eq:recvector}
$$

with integer $h,k,l$ satisfies the Laue condition, Eq. {eq}`eq-laue`.

It is almost trivial to construct the reciprocal lattice when lattice vectors $\mathbf{a},\mathbf{b},\mathbf{c}$ are mutually orthogonal. In this case, $\mathbf{a}\cdot[\mathbf{b}\times\mathbf{c}]=abc$ and $[\mathbf{b}\times\mathbf{c}]\parallel\mathbf{a}$. Then $\mathbf{a}^*\parallel\mathbf{a}$ and $|\mathbf{a}^*|=2\pi/a$, hence the name \textit{reciprocal lattice}. Its directions are parallel to those of the direct lattice ({numref}`fig-reciprocal`), whereas reciprocal-lattice parameters are inverse of the lattice parameters in real space, times the pre-factor of $2\pi$. This holds true for the orthorhombic, tetragonal, and cubic symmetries.

Other symmetries are more involved. Consider a monoclinic lattice with $\beta\neq 90^{\circ}$. Then, $\mathbf{a}\cdot[\mathbf{b}\times\mathbf{c}]=abc\sin\beta$, and one finds

$$
 |\mathbf{a}^*|=\frac{2\pi}{a\sin\beta},\quad |\mathbf{b}^*|=\frac{2\pi}{b},\quad |\mathbf{c}^*|=\frac{2\pi}{c\sin\beta}.
$$

Now, $\mathbf{a}^*$ and $\mathbf{c}^*$ are no longer parallel to $\mathbf{a}$ and $\mathbf{c}$ ({numref}`fig-reciprocal`). Instead, they form an angle of $\beta^*=180^{\circ}-\beta$. 


```{figure} /figures/ch5-reciprocal.svg
:name: fig-reciprocal

Direct-lattice and reciprocal-lattice vectors for the orthogonal (right) and non-orthogonal (left) lattice vectors. Note that the reciprocal-lattice vectors are not always parallel to those of the direct lattice, yet they are perpendicular to the corresponding lattice planes: for example, $\mathbf{a}^*$ is perpendicular to the (100) planes. 
```


We should also note that $\mathbf{a}\cdot[\mathbf{b}\times\mathbf{c}]=V$, the unit-cell volume in real space according to the standard definition of the [triple product](https://mathinsight.org/scalar_triple_product). To obtain unit-cell volume in the reciprocal space, one needs vector identities,

$$
 \mathbf{a}_1\cdot[\mathbf{a}_2\times\mathbf{a}_3]=\mathbf{a}_2\cdot[\mathbf{a}_3\times\mathbf{a}_1]\quad\text{and}\quad
 [\mathbf{a}_1\times[\mathbf{a}_2\times\mathbf{a}_3]]=\mathbf{a}_2(\mathbf{a}_3\cdot\mathbf{a}_1)-\mathbf{a}_3(\mathbf{a}_1\cdot\mathbf{a}_2),
$$

that return

$$
 V^*=\mathbf{a}^*\cdot[\mathbf{b}^*\times\mathbf{c}^*]=\frac{2\pi}{V}\,[\mathbf{b}\times\mathbf{c}]\cdot[\mathbf{b}^*\times\mathbf{c}^*]=\frac{2\pi}{V}\,\mathbf{b}^*\cdot[\mathbf{c}^*\times[\mathbf{b}\times\mathbf{c}]]=\frac{(2\pi)^3}{V}.
$$
This result will be needed in the future when we do summations over the reciprocal space. 

At this point, reciprocal lattice may still look like a rather arbitrary mathematical construction, but it is in fact undeniably real because it is observed in every scattering experiment: intensity maxima appear at every or almost every (see Ch.~\ref{sec:extinction}) reciprocal-lattice site. We can also say that each crystal lives two parallel lives. One is in real space and constitutes tangible crystal properties. Another one is in the reciprocal space and incorporates intrinsic effects such as atomic vibrations and electronic transitions. Only by grasping reciprocal-space phenomena can one understand real-space properties of the crystal!

## Relation to Bragg's law

The Laue condition and reciprocal lattice have a direct connection to Bragg's law. In fact, every reciprocal-lattice vector defined by Eq.~\eqref{eq:recvector} corresponds to the lattice planes with the Miller indices $h,k,l$. To verify this statement, choose the lattice planes $(hkl)$ and define $\mathbf{n}$ as the unitary vector perpendicular to these planes. Now choose $\mathbf{G}=2\pi\mathbf{n}/d_{hkl}$ and consider it as a propagation vector of a wmathbf{a}e with the wmathbf{a}elength of $d_{hkl}$. This wmathbf{a}e has the form $e^{i\mathbf{G}\mathbf{R}}$. One expects $e^{i\mathbf{G}\mathbf{R}}=1$ at $\mathbf{R}=0$. Since $\mathbf{R}=0$ corresponds to one of the lattice planes, the condition $e^{i\mathbf{G}\mathbf{R}}=1$ should also hold on any other lattice plane because they are separated by an integer number of wmathbf{a}elengths (Fig.~\ref{fig:recbragg}). Each point $\mathbf{R}$ of the direct lattice belongs to one or another lattice plane. Therefore, $e^{i\mathbf{G}\mathbf{R}}=1$ for every $\mathbf{R}$, and the condition~\eqref{eq:reclat} is fulfilled. Then $\mathbf{G}$ must be a reciprocal-lattice vector. 

```{figure} /figures/ch5-bragg.svg
:name: fig-recbragg

Relation between the reciprocal lattice and Bragg's law. The vector $\mathbf{G}$ chosen perpendicular to the lattice planes is a reciprocal-lattice vector. The Miller indices $h,k,l$ define the representation of $\mathbf{G}$ in terms of $\mathbf{a}^*$, $\mathbf{b}^*$, $\mathbf{c}^*$.
```



Now we have to prove that the reciprocal-lattice vector $\mathbf{G}=h\mathbf{a}^*+k\mathbf{b}^*+l\mathbf{c}^*$ corresponds to the planes with the Miller indices $h,k,l$. Let this vector define some lattice planes, which are perpendicular to it. We know that the corresponding interplane distance is given by $|\mathbf{G}|=2\pi/d$. The distance between the origin and the nearest plane is a vector of the length $d$ in the direction of $\mathbf{G}$ (Fig.~\ref{fig:recbragg}), namely, $\mathbf{d}=d\,\mathbf{G}/|\mathbf{G}|=d^2\,\mathbf{G}/(2\pi)$. To determine the distance $d_a$ that this plane intersects on the $\mathbf{a}$-axis, one has to compute

$$
 d_a=\frac{d}{\cos\varphi}=\frac{d}{\mathbf{d}\cdot\mathbf{a}/(da)}=\frac{2\pi a}{\mathbf{G}\cdot\mathbf{a}}=\frac{2\pi a}{h\,\mathbf{a}^*\cdot\mathbf{a}}=\frac{a}{h},
$$

which is equivalent to Eq. {eq}`eq-hkl` that served as the definition of the Miller indices $h,k,l$.

We now realize that the lattice planes used in Bragg's law are real-space manifestations of the reciprocal lattice. Incident light sees crystal as an optical grating, with different gratings identified by different families of the lattice planes. There need not be atoms on a given lattice plane to produce a Bragg peak. The positions of these Bragg peaks define the reciprocal lattice and directly convey lattice parameters of the crystal. 

This statement also sheds light on Eq. {eq}`eq-d-distance` for $d_{hkl}$ that immediately follows from $|\mathbf{G}|^2=h^2|\mathbf{a}^*|^2+k^2|\mathbf{b}^*|^2+l^2|\mathbf{c}^*|^2$ as the vector length in the reciprocal space (assuming $\mathbf{a},\mathbf{b},\mathbf{c}$ are mutually orthogonal). The calculation of $d_{hkl}$ for an arbitrary lattice also becomes straight-forward, albeit tedious when non-$90^{\circ}$ angles have to be taken into account.


## Aperiodic crystals

We can also see reciprocal lattice as a Fourier transform of the direct lattice. Bragg peaks at the reciprocal-lattice points indicate periodicity of the crystal in real space. This statement is in fact much more general, because aperiodic crystals also show characteristic diffraction patterns with a series of Bragg peaks. Such peaks manifest the underlying long-range order of the aperiodic crystal. The difference from periodic crystals is that the reciprocal lattice spun by $\mathbf{a}^*$, $\mathbf{b}^*$, and $\mathbf{c}^*$ is no longer sufficient to describe the Bragg peaks. 

Many of the aperiodic crystals can be seen as \emph{modulated structures}. Their diffraction patterns are described by a 3D reciprocal lattice plus one or more additional vectors $\mathbf{t}_i$ known as modulation vectors. Mathematically, these $\mathbf{t}_i$'s can be still decomposed into reciprocal-lattice vectors,
$$
 \mathbf{t}_i=p_1\mathbf{a}^*+p_2\mathbf{b}^*+p_3\mathbf{c}^*.
$$
When $p_1,p_2,p_3$ are simple fractions like $\frac12$ or $\frac15$, the structure is called \emph{commensurately modulated}. It is nothing but a periodic crystal with the larger unit cell. For example, $p_1=\frac12$ would mean that $\mathbf{a}^*$ should be twice shorter, hence the lattice parameter $a$ should be twice longer: some element of the structure develops a twice longer periodicity than the rest of the crystal and requires a two-fold expansion of the unit cell. By contrast, a structure with random values of $p_1,p_2,p_3$ is **incommensurately modulated**. 

Special mathematical formalism has been developed for modulated structures. It is based on a proper (periodic) lattice defined in a $3+n$-dimensional space known as \emph{superspace} where modulation vectors $\mathbf{t}_i$ are accommodated along additional, artificial dimensions, in order to restore periodicity of the system. For example, quasicrystals can be described as periodic structures in the 5D or 6D reciprocal space. This space is, of course, unphysical, but its 3D projection forms the physical reciprocal space where diffraction pattern is observed. The introduction of additional dimensions may seem bizarre at first glance, but it becomes more palatable if one considers that crystallographic restriction theorem forbids 5-fold symmetry only in 3D space. In higher dimensions, five-fold rotations may be compatible with periodicity. 

Incommensurate modulations may have different origin depending on the chemical nature of the crystal. Sometimes it is related to deformations or rotations of structural units that occupy a certain position in space, but vary with a different periodicity compared to the rest of the lattice. Other examples of aperiodic crystals are framework structures with channels where atoms in channels have their own periodicity compared to the framework. Aperiodic crystals are inconspicuous but abundant. They may occur in elemental solids, including Bi and Te under pressure, or in such a common material as Na$_2$CO$_3$, better known as washing soda. A short [memorial article](http://doi.org/10.1107/S2053273318016765) can serve as a good introduction into aperiodic crystals. 