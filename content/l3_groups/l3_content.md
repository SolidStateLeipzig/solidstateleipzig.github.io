# Content of lecture

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

The inversion center $\bar 1$ is in fact the end member of this series, because it combines inversion with the 1-fold rotation. Using Eqs. {eq}(eq-rotation) and {eq}(eq-rotation-inversion), one can verify that $\bar 2=m$. Three other rotoinversion axes are independent symmetry elements, which are needed to describe special situations, such as the symmetry of a tetrahedron ($\bar 4$). 

No Sch\"onflies symbols for rotoinversion axes exist, because a different symmetry element, **rotation-reflection axes** ($S_n$), is considered in this case. They are quite similar to $\bar n$, but rotation is followed by a mirror-plane reflection. This operation is also known as an **improper rotation**,

$$ 
    \mathbb{R}_{S_n} = \begin{pmatrix} \cos \varphi & \sin \varphi & 0 \\ -\sin \varphi & \cos \varphi & 0 \\ 0 & 0 & -1 \end{pmatrix}
$$

assuming $S_n\parallel z$. Simple algebra shows that $\bar 3=S_6$, $\bar 6=S_3$, and $\bar 4=S_4$, whereas $S_2=\bar 1$ and $S_1=m$, so we end up with exactly the same symmetry operations and an unnecessarily confusing notation.