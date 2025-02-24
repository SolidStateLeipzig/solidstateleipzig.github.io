# Content of lecture

Starting from this chapter, we will go through different crystal properties and discuss the main parameters that describe them. We will also see how these properties are related to microscopic aspects of the crystals, especially the atoms and their chemical bonding that constitute lattice degrees of freedom.

## Hydrostatic pressure, Equation of state

**Hydrostatic pressure** implies that the same force acts on the sample from all directions. It is the type of pressure experienced by a sample immersed into water or another liquid. However, even liquids develop some pressure gradients. The most uniform pressure can be achieved by placing the crystal into helium gas. Helium solidifies at 11.5\,GPa at room temperature, but it is a van der Waals solid with a very low bulk modulus, so it ensures almost hydrostatic (so-called **quasi-hydrostatic**) pressure conditions up to at least $20-25$ GPa.


 
```{figure} /figures/ch9-EoS.svg
:name: fig-EoS

Pressure dependence of volume upon hydrostatic compression, according to the equations of state, \eqref{eq:murnaghan-2} and~\eqref{eq:bm-eos}.
```

Pressure renders chemical bonds more stiff, because atoms become closer to each other. Therefore, the bulk modulus increases on compression. One empirical (but very reasonable) approximation is linear pressure dependence of the bulk modulus,

$$
 B(p)=B_0+B_0'\,p
$$ (eq-murnaghan-1)

where $B_0$ is the bulk modulus at ambient pressure and $B_0'={\rm const}$ is pressure derivative of the bulk modulus. Using this pressure dependence in Eq.~\eqref{eq:bulkmod} gives rise to a differential equation,

$$
 -V\frac{dp}{dV}=B_0+B_0'\,p \Ra
 \frac{dp}{B_0+B_0'p}=-\frac{dV}{V}
$$

that can be integrated to obtain the relation between $p$ and $V$,

$$
 p(V)=\frac{B_0}{B_0'}\left[\left(\frac{V_0}{V}\right)^{B_0'}-1\right].
$$ (eq-murnaghan-2)

It is the **Murnaghan equation of state** that describes hydrostatic compression of crystals at low pressures $V/V_0\geq 0.9$ where Eq.~\eqref{eq:murnaghan-1} holds. This equation of state describes the crystal at a constant temperature.

At higher pressures, a quadratic term should be added to Eq.~\eqref{eq:murnaghan-1}, leading to the second-order Murnaghan equation of state. However, it is more common to use the so-called Birch-Murnaghan equations of state obtained by expanding free energy in powers of the strain (the step-by-step derivation can be found [here](https://doi.org/10.3390/min9120745)). This equation can be second-, third-, or even higher order depending on how many terms in the expansion are retained. For the reference, we quote here the third-order **Birch-Murnaghan equation of state**, which is commonly used in geoscience,

$$
 p(V)=\frac{3B_0}{2} \left[\left(\frac{V_0}{V}\right)^{\frac73}-\left(\frac{V_0}{V}\right)^{\frac53}\right] \left[ 1+\frac34\,(B_0'-4)\left(\left(\frac{V_0}{V}\right)^{\frac23}-1\right) \right].

$$ (eq-bm-eos)
This equation contains the same three parameters as Eq.~\eqref{eq:murnaghan-2}, but entails a different underlying approximation because no linear pressure dependence of $B$ is assumed.

All equations of state show that volume decreases with pressure and develops a positive curvature, as shown in Fig.~\ref{fig:EoS}, because crystals harden on compression. Direct measurement of this $V(p)$ curve using **high-pressure XRD** (i.e., x-ray diffraction on a crystal placed into a pressure cell) is the main experimental tool for studying compressibility of solids and determining their bulk moduli. 

## Uniaxial pressure
In the absence of **pressure medium** like liquid or gas that could transmit the applied pressure into all directions and make it hydrostatic, one deals with **uniaxial pressure**. Such pressure is often called **stress**, $\sigma_x=F_x/A_x$ where $F_x$ is the applied force and $A_x$ is the area of the sample surface perpendicular to which this force is applied (Fig.~\ref{fig:strain}, middle). Uniaxial stress creates **strain**, $\epsilon_x=\Delta L_x/L_x$, defined as the relative length change of the sample. Stress has units of pressure, whereas strain is a dimensionless quantity.

While it is difficult to expand the crystal hydrostatically, uniaxial pressure could either compress or stretch the crystal along a certain direction. One thus distinguishes between the **compressive** ($\epsilon>0$) and **tensile** ($\epsilon<0$) strains. Practically, uniaxial pressure can be created simply by squeezing the crystal between the two plates. However, more and more often [piezo-devices](http://doi.org/10.1063/1.5075485) are used instead. A suitably shaped crystal is attached to a piezoelectric stage that can create strains up to $1.5-2$\%, both compressive and tensile.

Stress and strain are related by the familiar **Hooke's law**,

$$
 \sigma_x=Y\epsilon_x
$$

where $Y$ is **Young's modulus**.



```{figure} /figures/ch9-strain.svg
:name: fig-strain

Hydrostatic compression (left), uniaxial pressure (middle), and shear deformation (right). Uniaxial strain is defined as $\epsilon_x=\Delta L_x/L_x$, whereas shear strain is defined as $\epsilon_{xy}=\tg\ph\simeq\ph$.
```





Uniaxial pressure changes not only the sample length, but also its aspect ratio. Squeezing the crystal along one direction will typically force it to expand along the perpendicular direction, and the other way around. This effect is gauged by the **Poisson's ratio**, $\nu=-\epsilon_y/\epsilon_x$. Most of the solid-state materials are characterized by $\nu>0$. However, it is also possible to design materials with $\nu<0$ known as \emph{auxetic}. They play an important role in engineering, as explained [here](https://doi.org/10.1038/natrevmats.2017.78).

## Shear deformation

Force can be applied not only perpendicular to the sample surface, but also parallel to it, leading to a so-called shear deformation that changes sample shape without changing its volume. Such shear stress $\tau_{xy}=F_y/A_x$ is defined in the same way as the uniaxial stress, whereas shear strain $\epsilon_{xy}=\Delta L_y/L_x={\rm tan}\varphi$ is the relative displacement of the sample surface caused by $F_y$. For low displacements, ${\rm tan}\varphi\simeq\varphi$, and shear strain is measured simply as angle (Fig.~\ref{fig:strain}, right).

The same linear relation between stress and strain holds in this case,

$$
 \tau_{xy}=G\,\epsilon_{xy},
$$

with the **shear modulus** $G$ that complements $B$ and $E_Y$ in describing elastic properties of materials.

Up to this point we never referred to periodicity of the crystals. In fact, all of the above applies to any solid, be it crystalline or amorphous. In engineering, one often considers an isotropic medium, namely, a medium that shows the same behavior along all the directions. Such an isotropic medium is characterized by

$$
 E_Y=3B(1-2\nu)=2G(1+\nu).
$$ (eq-elastic-isotropic)


Its elastic properties are then fully described by only two parameters. This is the case for a typical amorphous material like glass. Note however that Eq.~\eqref{eq:elastic-isotropic} does not hold for crystals, because even cubic crystals are not isotropic. Their $[100]$, $[110]$, and $[111]$ directions are distinct, as they are not related by any symmetry.

## Stress and strain tensors

## Elastic constants


General relation between stress and strain is set by the \emph{elastic constants} $C_{ijkl}$,

$$
 \sigma_{ij}=C_{ijkl}\,\epsilon_{kl}.
$$

They have the same units of pressure (Pa) as all the elastic moduli. Elastic constants describe mechanical response of anisotropic media, including crystals. Technically, $C_{ijkl}$ is a fourth-rank tensor (**elasticity tensor**) with 81 components, but symmetries of the stress and strain tensors allow several simplifications. Indeed, with only six independent components in $\sigma$ and $\epsilon$, respectively, it becomes convenient to introduce the aliases, 
\begin{center}
\begin{tabular}{c@{\hspace{0.8cm}}c@{\hspace{0.8cm}}c@{\hspace{0.8cm}}c@{\hspace{0.8cm}}c@{\hspace{0.8cm}}c}
 $xx$ & $yy$ & $zz$ & $xy$ & $xz$ & $yz$ \\
   1  &   2  &   3  &   4  &   5  &   6  \\
\end{tabular}
\end{center}\smallskip
and consider 36 elastic constants from $C_{11}$ to $C_{66}$. 

Elastic constants can be also defined in a thermodynamic fashion as second derivatives of the elastic energy (energy acquired by the crystal due to its deformation),

$$
 \mathcal{E}=\mathcal{E}_0+\frac12\sum_{ij,kl}C_{ijkl}\,\epsilon_{ij}\,\epsilon_{kl}.
$$

Mixed second derivatives are equal, so $C_{ijkl}=C_{klij}$ (see also Ch.~\ref{sec:neumann}), thus reducing the number of independent elastic constants to 21. Symmetry constrains them further. For example, elasticity tensor of a cubic crystal takes the form
$$
 \mathbb C=\left(
\begin{array}{cccccc}
 C_{11} & C_{12} & C_{12} & 0 & 0 & 0 \\
 C_{12} & C_{11} & C_{12} & 0 & 0 & 0 \\
 C_{12} & C_{12} & C_{11} & 0 & 0 & 0 \\
 0 & 0 & 0 & C_{44} & 0 & 0 \\
 0 & 0 & 0 & 0 & C_{44} & 0 \\ 
 0 & 0 & 0 & 0 & 0 & C_{44} \\
\end{array}
\right)
$$

with only three independent parameters.

Inversion of the elasticity tensor yields the **compliance tensor**,

$$
 \epsilon_{ij}=S_{ijkl}\,\sigma_{kl}.
$$

In Ch.~\ref{sec:ionic} and~\ref{sec:vdw}, we saw that bulk modulus depends on the chemical bonding in crystals. Stronger bonds give rise to less compressible crystals. The same would be true for all the elastic constants. They are determined by the type of the crystal structure and the nature of chemical bonds. 

Experimentally, elastic constants are determined from **resonant ultrasound spectroscopy**. Single crystal of the material is placed between two plates. Mechanical vibration is induced in one of these plates and transmitted to the opposite plate that shows vibrations at those frequencies where external modulation resonates with own frequencies of the crystal. These frequencies depend on the elastic constants of the material, but also on the shape and dimensions of the crystal. With the sufficient number of the resonant frequencies, all the 21 elastic constants can be determined and further measured as a function of temperature or other external parameters.

## Plastic deformation

Instead of the ultrasound spectroscopy, engineers use **mechanical tests** where stress is applied to the sample and strain is measured, so that a **stress-strain curve** is obtained (Fig.~\ref{fig:stress-strain}). The initial, linear part of this curve yields one or another elastic modulus from Ch.~\ref{ch:uniaxial} and~\ref{ch:shear}. Such measurements will typically extend beyond the linear part of the curve until the regime of plastic deformation is reached. Whereas **elastic deformation** is reversible, **plastic deformation** remains in the sample after the stress is removed. 



```{figure} /figures/ch9-stress-strain.svg
:name: fig-stress-strain

Stress-strain curve with the regions of elastic (reversible) and plastic (irreversible) deformation. Point $a$ is the \textit{yield point}, the onset of the plastic deformation. Point $b$ shows the \textit{ultimate strength} of the material. Point $c$ indicates the \textit{fracture} (breaking point).
```



Plastic deformation is characterized by a nonlinear regime of the stress-strain curve that starts at the so-called **yield point** and usually reaches a plateau where sample length keeps increasing without any additional stress applied. The material starts to ``flow'', similar to the heavily loaded plastic bag carried from the supermarket. This stretching region is followed by another increase (strain hardening) until the material reaches its point of **ultimate strength**. When this point is reached, a neck forms spontaneously even if no additional stress is applied, and eventually the sample breaks apart. 

Materials characterized by a broad region of the plastic deformation are called **ductile**, in contrast to **brittle** materials that break close to the yield point. Ductility is usually defined with respect to tensile strain. The robustness of a material toward plastic deformation upon compressive or shear strain is called **malleability**. It is of crucial importance for metals and shows whether they can be rolled and bent. Finally, **hardness** is defined as the robustness of a material against indentation.

Microscopically, plastic deformations are related to the propagation of **dislocations**, linear defects that hinder periodicity of the crystal. The motion of dislocations shifts parts of the crystal relative to each other and increases the crystal length. Dislocations are especially abundant in metallic crystals where itinerant electrons are responsible for the chemical bonding, and relative positions of the atoms are less important. Therefore, metals, in contrast to the covalent and ionic crystals, are amenable to plastic deformations. On the other hand, alloys like steel where iron atoms are interspersed with carbon atoms, are less ductile because impurity atoms block the motion of dislocations.

Importantly, only elastic properties are intrinsic properties of the crystal, i.e., they are fully determined by the structure of the crystal, its constituent atoms and chemical bonds. On the other hand, ductility and other properties related to the plastic deformation are rooted in the microstructure, a combination of impurities and defects that affect the motion of dislocations. 