(sec-diffraction)=
# Content of lecture

(sec-strfactor)= 
## Structure factor

Reciprocal lattice serves as a connection between positions of Bragg peaks and lattice parameters of the crystal. Similarly, structure factor connects intensities of Bragg peaks to the atomic coordinates.

To calculate intensity of a Bragg peak, we go back to Laue's representation of the scattering process and take the scattering mechanism into account. Atoms are not point-like objects, and atoms are not scatterers *per se*. Instead, one should consider periodic scattering density $\rho(\mathbf{r})$ that satisfies $\rho(\mathbf{r}+\mathbf{r})=\rho(\mathbf{r})$ for every lattice vector $\mathbf{r}$. 

Every small volume element $\mathbf{dr}$ scatters the incident wave. The phase of the scattered wave depends on the position of $\mathbf{dr}$ inside the crystal. Indeed, from Laue's argument (Ch.~\ref{sec:laue}) the path difference for a given position $\mathbf{r}$ relative to the origin is

$$
 \frac{\lambda}{2\pi}\,\mathbf{r}(\mathbf{k}-\mathbf{k}')=\frac{\lambda}{2\pi}\,\mathbf{G}\,\mathbf{r}
$$

and the corresponding phase shift is $\Delta\varphi=\mathbf{G}\,\mathbf{r}$ where $\mathbf{G}$ is a reciprocal-lattice vector. The scattered wave is obtained by integrating such phase shifts over the unit cell, taking into account $\rho(\mathbf{r})$ as the concentration of scatterers in a given position $\mathbf{r}$,

$$
 e^{i(\mathbf{k}'\tilde{\mathbf{r}}-\omega t)}\cdot\int \rho(\mathbf{r})\,e^{i\mathbf{G}\mathbf{r}}\,\mathbf{dr}=e^{i(\mathbf{k}'\tilde{\mathbf{r}}-\omega t)}\,F(\mathbf{G})
$$

where the newly introduced \emph{structure factor} $F(\mathbf{G})$ is the amplitude of the scattered wave that travels away from the crystal into some arbitrary position $\tilde{\mathbf{r}}$. Intensity is proportional to the squared amplitude,

$$
 I(\mathbf{G})\sim |F(\mathbf{G})|^2,\qquad F(\mathbf{G})=\int\limits_{\rm UC} \rho(\mathbf{r})\,e^{i\mathbf{G}\mathbf{r}}\,\mathbf{dr}.
$$ (eq-strfactor)

```{note}
Experimentally, intensity depends on the exposure time and can be defined up to a scale factor, only.
```

Considering the periodicity of $\rho(\mathbf{r})$, it is sufficient to integrate over the unit cell (UC) when calculating $F(\mathbf{G})$, because other unit cells will simply lead to an additional pre-factor, which should be the same for every reflection.
```{note}
An adverse consequence of this multiplication is that $F(\mathbf{G})$ and $I(\mathbf{G})$ go to infinity in thermodynamic limit (for an infinite crystal). This is the drawback of the kinematic theory that neglects multiple scattering, although, as a matter of fact, a scattered wave should scatter again, and again, and again when the crystal is infinite. Such a multiple scattering is taken into account in the [dynamic theory of diffraction](http://doi.org/10.1107/S0108767311040219) that we will not consider here because for many practical purposes the kinematic theory suffices.}
```

It is instructive to compare the structure factor, Eq. {eq}`eq-strfactor`, with the Fourier decomposition of the scattering density,

$$
 \rho(\mathbf{r})=\sum_{\mathbf{G}}\rho_{\mathbf{G}}\,e^{i\mathbf{G}\mathbf{r}},\qquad \rho_{\mathbf{G}}=\frac{1}{V}\int \rho(\mathbf{r})\,e^{i\mathbf{G}\mathbf{r}}\,\mathbf{dr},
$$

where we restricted the summation to the reciprocal-lattice vectors $\mathbf{G}$ because $\rho(\mathbf{r})$ is periodic in direct space. In fact, structure factor is merely the Fourier component of the scattering density, up to a pre-factor.


## Atomic approximation

Strictly speaking, it is not necessary to think of atoms when we calculate $F(\mathbf{G})$, but life becomes easier when we do, namely, when the scattering density $\rho(\mathbf{r})$ is represented as a superposition of scattering densities $\rho_j(\mathbf{r}')$ from individual atoms. Consider $j=1,\ldots N$ atoms located at the positions $\mathbf{r}_1,\ldots \mathbf{r}_N$ within the unit cell. By introducing the volume element $\mathbf{dr}'$ within an atom, we represent $\mathbf{r}=\mathbf{r}_j+\mathbf{r}'$ (Fig.~\ref{fig:atoms}) and re-write the structure factor as a sum over individual atoms,

$$
 F(\mathbf{G})=\int \rho(\mathbf{r})\,e^{i\mathbf{G}\mathbf{r}}\,\mathbf{dr}=\sum_{j=1}^N\,\,e^{i\mathbf{G}\mathbf{r}_j}\int\limits_{\rm atom} \rho_j(\mathbf{r}')\,e^{i\mathbf{G}\mathbf{r}'}\mathbf{dr}'=\sum_{j=1}^N f_j(\mathbf{G})\,e^{i\mathbf{G}\mathbf{r}_j}.

$$ (eq-strfactor-2)

Here, we introduced the **atomic form factor** $f_j(\mathbf{G})$ that describes the scattering of the wave by a given atom $j$ in the direction of $\mathbf{G}$. 

```{figure} /figures/ch6-atoms.svg
:name: fig-atoms

Scattering density of the crystal, $\rho(\mathbf{r})$, is represented as a superposition of the scattering densities of individual atoms, $\rho_j(\mathbf{r}')$, with the vector $\mathbf{r}$ decomposed into $\mathbf{r}_1+\mathbf{r}'$.
```


To a first approximation, any given atom scatters waves in the same way regardless of the chemical environment of this atom. Then the same set of atomic form factors can be used for all crystals, and the variation of the Bragg peak intensity with $\mathbf{G}$ arises from two ingredients:

 *  *material-specific:* positions of atoms $\mathbf{r}_j$ within the unit cell 

 * *generic:* angular dependence of the scattering by a given atom, as defined by $f_j(\mathbf{G})$, regardless of the exact nature of the crystal 

(sec-extinction)=
## Extinction condition

The structure factor defined by Eq. {eq}`eq-strfactor` reflects the arrangement of atoms inside the crystal. Experimental structure factors can be used to determine atomic positions, as we will further discuss in Ch.~\ref{sec:structure-determination}. Interestingly, using only a simple maths one can draw some conclusions on the symmetry of the crystal when lattice centering (Ch.~\ref{sec:centering}) or open symmetry elements (Ch.~\ref{sec:open}) connect different atoms therein.

i) Lattice centering. Consider a body-centered crystal structure with the lattice translation of $\mathbf{t}=\frac12(\mathbf{a}+\mathbf{b}+\mathbf{c})$. Then an atom located at $(x,y,z)$ has a counterpart at $(x+\frac12,y+\frac12,z+\frac12)$. Using the standard representation $\mathbf{G}=h\mathbf{a}^*+k\mathbf{b}^*+l\mathbf{c}^*$, one finds

$$
 \mathbf{G}\,\mathbf{r}_j=(h\mathbf{a}^*+k\mathbf{b}^*+l\mathbf{c}^*)(x_j\mathbf{a}+y_j\mathbf{b}+z_j\mathbf{c})=2\pi(hx_j+ky_j+lz_j)
$$

(note an immediate advantage of fractional atomic coordinates in conjunction with the reciprocal lattice!) We can now write the structure factor as

$$
\begin{align}
 F(\mathbf{G})= \sum_{j=1}^N f_j(\mathbf{G})\,e^{i\mathbf{G}\mathbf{r}_j}= &\sum_{j=1}^{N/2} f_j(\mathbf{G})\left[ e^{2\pi i(hx_j+ky_j+lz_j)} + e^{2\pi i \left[ h(x_j+\frac12) + k(y_j+\frac12) + l(z_j+\frac12)\right]} \right] \notag\\
 = & \sum_{j=1}^{N/2} f_j(\mathbf{G})\,e^{2\pi i(hx_j+ky_j+lz_j)} \left[ 1+e^{\pi i(h+k+l)} \right]
\end{align}
$$

The expression in square brackets can be either 0 or 2 depending on whether $h+k+l$ is odd or even, respectively. We thus see that lattice centering defines a special rule for the reflection intensities. Only reflections with $h+k+l=2n$ (even) are observed. This is the **reflection condition** for a body-centered crystal. The systematic absence of reflections is known as an **extinction**, so we could also introduce an extinction condition $h+k+l=2n+1$ (odd).

ii) Open symmetry elements. Glide planes and screw axes cause their own extinctions. Consider the glide plane $a\perp\mathbf{c}$. It leads to the transformation $(x,y,z)\rightarrow (x+\frac12,y,\bar z)$. Then the structure factor becomes

$$
  F(\mathbf{G})=\sum_{j=1}^{N/2} f_j(\mathbf{G})\left[ e^{2\pi i(hx_j+ky_j+lz_j)} + e^{2\pi i \left[ h(x_j+\frac12) + ky_j-lz_j\right]} \right].
$$

This expression does not look very spectacular, but it becomes simpler in the special case of $l=0$. Then,

$$
 F_{hk0}= \sum_{j=1}^{N/2} f_j(hk0)\,e^{2\pi i(hx_j+ky_j)} \left[ 1+e^{\pi ih} \right]
$$

and we expect the reflection condition $hk0, h=2n$ for the $a$-glide plane perpendicular to $\mathbf{c}$. 

Reflection conditions for a given space group can be obtained from the [HKLCOND](https://cryst.ehu.es/cryst/get_hkl.html) utility at the Bilbao Server. By analyzing extinctions, crystal symmetry can be determined or, more precisely, narrowed down to a list of possible space groups.

More generally, one can see the reflection (extinction) conditions as a manifestation of the periodicity. The reciprocal lattice defined using three lattice vectors, Eq. {eq}`eq-recdef`, corresponds to the situation when no additional translations are allowed. Crystals with lattice centering have a shorter periodicity indicated by the primitive cell, so their reciprocal lattices should be more sparse. This effect is achieved by removing some of the reciprocal-lattice points via extinctions. For example, reciprocal lattice of a bcc lattice is an fcc lattice with the periodicity of $4\pi/a$. 

(sec-structure-determination)=
## Crystal strucutre determination

Crystal structures are determined from diffraction experiments that involve an accurate measurement of both position and intensity for every Bragg peak. The structure solution includes three consecutive steps:

* *indexing* of the Bragg peaks, finding lattice parameters from the peak positions
* *analyzing* extinctions in order to determine the crystal symmetry
```{note}
More precisely, lattice centering can be determined, and a subset of possible space groups defined. Space groups that contain neither lattice centering nor open symmetry elements do not have any reflection conditions and can not be distinguished in this way.
```
* *finding* a structural model that gives the best fit to the experimental Bragg peak intensities


The principal advantage of the diffraction methods is that many Bragg peaks can be measured in order to determine atomic positions with a very high accuracy. A typical diffraction experiment covers thousands of Bragg peaks, and interatomic distances are determined with an uncertainty of less than 0.01\,\r A. Such a high spatial resolution is only possible with the reciprocal-space technique (measurement of Bragg peaks in the reciprocal space) and can not be matched by the direct-space imaging with electron microscopy (Ch.~\ref{sec:microscopy}). 

## Atomic form factors
From Eq. {eq}`eq-strfactor-2`, atomic form factor is defined as the Fourier-transformed scattering density $\rho(\mathbf{r})$ of a single atom,

$$
 f(\mathbf{q})=\int\rho(\mathbf{r})\,e^{i\mathbf{q}\mathbf{r}}\,\mathbf{dr}
$$ (eq-formfactor)

where $\mathbf{q}$ is a vector in the reciprocal space (the vectors $\mathbf{q}$ are no longer restricted to the reciprocal-lattice vectors $\mathbf{G}$, because atom is not periodic). Spherical symmetry of an atom implies that $f$ depends only on $|\mathbf{q}|$ and not on the direction of $\mathbf{q}$. It is then customary to represent $|\mathbf{q}|$ as $2\pi/d$ similar to Ch.~\ref{sec:recbragg} and consider $1/d\sim \sin\theta/\lambda$ from Bragg's law. Therefore, atomic form factors are tabulated as a function of $\sin\theta/\lambda$, measured in \r A$^{-1}$. They can be found in the International Tables for Crystallography and [on the web](http://lampx.tugraz.at/~hadley/ss1/crystaldiffraction/atomicformfactors/formfactors.php).


```{figure} /figures/ch6-formfactor.svg
:name: fig-formfactor

Scattering densities (left) and the resulting atomic form factors (right) for the x-ray and neutron scattering. Different densities are not drawn to the scale. Spin density is typically associated with the $d$- and $f$-atomic orbitals that have nodes at $r=0$.
```


The scattering density in Eq. {eq}`eq-formfactor` depends on the nature of the wave being scattered. Several cases are of special importance ({numref}`fig-formfactor`):

* *x-rays* are scattered by electrons, so $\rho(\mathbf{r})$ is electron density that gradually decreases away from the atom. Then $f(\mathbf{q})$ is also a slowly decreasing function. Larger values of $|\mathbf{q}|$ correspond to smaller values of $d_{hkl}$ that, in turn, correspond to the higher angles $\theta$. Therefore, one sees lower intensities in XRD patterns at high angles

 * *neutrons* are scattered by the atomic nuclei, which are very small. Then, $\rho(\mathbf{r})$ looks more like a $\delta$-function, while its Fourier transform is a constant. In a neutron diffraction experiment, reflection intensities only weakly depend on the angle $\theta$. 

* *neutrons* are also scattered by the spin density, namely, by valence electrons with an unpaired spin. This is the primary experimental tool for studying magnetic order in crystals. The corresponding magnetic form factor decreases even faster than the x-ray one because only valence electrons are involved, so magnetic Bragg peaks are observed at low angles only

* *electrons* are scattered by other electrons, so their $f(\mathbf{q})$ is similar to that of x-rays. The intensities decrease with the angle. However, electrons are impatient and will usually scatter several times as they travel through the crystal. Intensities of Bragg peaks in electron diffraction are, therefore, strongly affected by multiple scattering.

