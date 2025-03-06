# Content of lecture

Whereas acoustic phonons are responsible for propagation of sound, optical phonons interact with light. To understand this interaction, we will first review the meaning of optical constants and then derive optical reflectivity of an ionic crystal due to phonons.


## Refractive index and reflectivity

Optical response of a material (solid, liquid, or gas) is determined by its **refractive index**. The refractive index $n$ appears in the dispersion relation of an electromagnetic wave (Ch.~\ref{app:wave}),

$$
 \varepsilon\,\omega^2=c^2k^2\quad{\rm with}\quad \varepsilon=n^2
$$ (eq-dispersion-relation)
where $\varepsilon$ is permittivity, $k$ is the length of the propagation vector, and $c=3\times 10^8$\,m/s is speed of light in vacuum. Since $\varepsilon$ is generally a complex number, $n$ is a complex number too, $n=n'+in''$.

%\footnote{We use primes in these lecture notes, but it %is also customary to write $n=n_1+in_2$ and %$\varepsilon=\varepsilon_1+i\varepsilon_2$.}

Using $\mathbf{k}=(n/c)\,\omega=n\,\mathbf{k}_0$, one writes the oscillating electric field as

$$
 \mathbf{E}=\mathbf{E}_0\,e^{i(\mathbf{k}\mathbf{r}-\omega t)}=\mathbf{E}_0\,e^{i(n\mathbf{k}_0\mathbf{r}-\omega t)}=\mathbf{E}_0\,e^{-n''\mathbf{k}_0\mathbf{r}}\,e^{i(n'\mathbf{k}_0\mathbf{r}-\omega t)}
$$

where $\mathbf{k}_0$ is the propagation vector in vacuum ($\varepsilon=1$). It is then clear that $n'$, real part of the refractive index, describes **refraction**, namely, the change in speed of light inside the material. In contrast, the imaginary part $n''$ describes **absorption**, the attenuation of the wave amplitude inside the material. 

\begin{figure}[!h]
\hspace{0cm}
\begin{minipage}{9cm}
 \includegraphics[scale=1.0]{ch12-reflectivity}
\end{minipage}
\hfill
\begin{minipage}{6.5cm}
\caption{\label{fig:reflectivity}
Propagation of light at the crystal surface. The incident beam splits into the reflected and transmitted beams. Their intensities are determined by the complex refractive index of the crystal, $n=n'+in''$.
}
\end{minipage}
\hfill
\end{figure}

Absorption measurements require a suitably chosen sample thickness, such that the fraction of the absorbed intensity is neither too large nor too small. It is often more convenient to measure **reflectivity**, which is defined as the intensity ratio of the incident and reflected light. In the case of normal incidence, all of the incident, reflected, and transmitted waves travel along the $z$ direction perpendicular to the surface (Fig.~\ref{fig:reflectivity}),

$$
\begin{align*}
 {\rm incident}\!:&\qquad E_i=E_{i0}\,e^{i(k_0z-\omega t)} \\
 {\rm transmitted}\!:&\qquad E_t=E_{t0}\,e^{i(nk_0z-\omega t)} \\
 {\rm reflected}\!:&\qquad E_r=E_{r0}\,e^{i(-k_0z-\omega t)}
\end{align*}
$$

At the interface, which we choose as $z=0$, electric field should change continuously, so the amplitudes fulfill the condition $E_{t0}=E_{i0}+E_{r0}$. A similar condition should hold for the magnetic field too, $\omega\mathbf{B}=\mathbf{k}\times\mathbf{E}$ according to Eq.~\eqref{eq:wave-2}. Therefore, 

$$
 nE_{t0}=E_{i0}-E_{r0}.
$$

It is then easy to eliminate $E_{t0}$ and calculate reflectivity,\footnote{This expression is derived for the case of normal incidence. More complex [Fresnel equations](https://en.wikipedia.org/wiki/Fresnel_equations) are required for an arbitrary incidence angle. In particular, polarization of light changes upon the non-$90^{\circ}$ reflection, which is the cornerstone of the optical method called [ellipsometry](https://doi.org/10.1146/annurev.ms.11.080181.000525).}

$$
 R=\frac{|E_{r0}|^2}{|E_{i0}|^2}=\frac{|1-n|^2}{|1+n|^2}.
$$

In Ch.~\ref{sec:phonon-light}, we will see that $R$ values close to 1 are obtained when $n''$ is large, whereas $n'$ vanishes. Then any light transmitted through the interface is immediately absorbed, so the sample is non-transparent: no light can go through. In a more general situation, part of the transmitted amplitude, $E_{t0}$, is then lost due to absorption ($A$), whereas transmittance of the whole sample is $T=1-R-A$.

## Fluctuating dipoles

We now return to the phonons and consider the diatomic chain (Ch.~\ref{sec:ph-diatomic}) where the two atoms not only have different masses but also carry the charges of $+q_e$ and $-q_e$, respectively. At $q=0$, the optical mode involves opposite displacements of these atoms, such that a fluctuating dipole moment $\mu_d(t)$ is induced by the phonon. Our strategy now will be calculating this dipole moment and the corresponding permittivity $\varepsilon$ to obtain the refractive index $n$ and analyze optical response of the crystal. We will do this using a very simple -- and, in all honesty, oversimplified -- model before drawing an argument why the predictions of this model remain valid in the more general case.

Light features an oscillating electric field, $E\sim e^{-i\omega t}$, that interacts with the charges. Then the force acting on the atoms should be augmented by the Columb force, and the equations of motion from Ch.~\ref{sec:ph-diatomic} should be revised as

$$
\left\{ \begin{array}{l}
 m_1\,\frac{d^2u_p}{dt^2}=-2\mathcal{K}(u_p-v_p)+q_eE_{\rm local} \\[0.5em]
 m_2\,\frac{d^2v_p}{dt^2}=-2\mathcal{K}(v_p-u_p)-q_eE_{\rm local} \\
\end{array} \right.
$$
The phonon is considered at $q\rightarrow 0$, so all atoms of a given type undergo the same displacement, and we end up with only one differential equation for $l=u_p-v_p$, the dipole length. Indeed, dividing the first equation by $m_1$ and the second equation by $m_2$ returns the single equation for $l$,

$$
 \frac{d^2l}{dt^2}=-\mathcal{K}\left(\frac{1}{m_1}+\frac{1}{m_2}\right)l+\left(\frac{1}{m_1}+\frac{1}{m_2}\right)q_e E_{\rm local}\Rightarrow
\mathcal{m}\,\frac{d^2l}{dt^2}+\mathcal{m}\,\omega_0^2\,l=q_eE_{\rm local}.
$$
This is a standard equation for a driven harmonic oscillator with $\omega_0=\sqrt{2\mathcal{K}/\mathcal{m}}$, the frequency of the optical phonon at $q=0$ in the absence of any electric charges (as in Ch.~\ref{sec:optical}). 

Electric field is local in the sense of Ch.~\ref{sec:dielectic-local}. It includes the internal field due to light, as well as Lorenz and depolarizing fields, which are proportional to polarization. The polarization oscillates too, following oscillations of the dipole moment $\mu_d=q_e\,l$. Therefore, it makes sense to choose the oscillating form of $E_{\rm local}=E_0\,e^{-i\omega t}$ and search for the oscillating solution, $l(t)=A\,e^{-i\omega t}$. The result is,

$$
 A(\omega)=\frac{q_e/\mathcal{m}}{\omega_0^2-\omega^2}\,E_0\Rightarrow
\mu_d(t)=q_e\,l(t)=\frac{q_e^2/\mathcal{m}}{\omega_0^2-\omega^2}\,E_{\rm local}(t),
$$

and polarizability of the crystal due to an optical phonon becomes

$$
 \alpha(\omega)=\frac{q_e^2/\mathcal{m}}{\omega_0^2-\omega^2}.
$$ (eq-polarizability-ionic)
Electric field drives oscillations and creates resonance when its frequency matches the frequency of the system, which is the frequency of the optical phonon at $q\rightarrow 0$.


## LO vs. TO

We should now use this polarizability $\alpha$ to calculate optical parameters from Ch.~\ref{sec:reflectivity}. Before doing that, let's compare electric polarizations created by the TO and LO phonons. These two types of phonons differ by the direction of their displacements relative to the propagation direction $\mathbf{q}$. The displacements take the form $\mathbf{u}=\mathbf{u}_0\,e^{i(\mathbf{q}\mathbf{r}-\omega t)}$ where $\mathbf{q}$ is the chain direction, so we expect $\mathbf{P}=\mathbf{P}_0\,e^{i(\mathbf{q}\mathbf{r}-\omega t)}$ with $\mathbf{P}\parallel\mathbf{q}$ (LO) and $\mathbf{P}\perp\mathbf{q}$ (TO). 

In the absence of an external electric field, Eq.~\eqref{eq:basic-d} becomes

$$
 \mathbf{D}=\varepsilon_0\mathbf{E}_{\rm depol}+\mathbf{P},
$$

and we expect the same wave-like form of $\mathbf{D}=\mathbf{D}_0\,e^{i(\mathbf{q}\mathbf{r}-\omega t)}$ and $\mathbf{E}_{\rm depol}=\mathbf{E}_0\,e^{i(\mathbf{q}\mathbf{r}-\omega t)}$ because both of them arise from the same atomic displacements. Additionally, one of Maxwell's equations requires ${\rm div}\mathbf{D}=0\Rightarrow \mathbf{D}\cdot\mathbf{q}=0$. For the LO phonon, this condition holds with $\mathbf{D}=0$ only, hence $\mathbf{E}_{\rm depol}=-\mathbf{P}/\varepsilon_0$ corresponding to the depolarization factor $f=1$. On the other hand, the TO phonon entails $\mathbf{D}\perp\mathbf{q}$ for an arbitrary $\mathbf{D}$ and satisfies the above condition, but another Maxwell's equation, $\rm rot\,\mathbf{E}=0$, requires $\mathbf{q}\times\mathbf{E}=0$, which is possible with $\mathbf{E}_{\rm depol}=0$ only because $\mathbf{E}_{\rm depol}\perp\mathbf{q}$ in this case. Therefore, the TO phonon corresponds to the depolarization factor $f=0$. Altogether,

$$
 {\rm LO}\!:\quad E_{\rm local}=\frac{P}{3\,\varepsilon_0}-\frac{P}{\varepsilon_0}=-\frac{2P}{3\,\varepsilon_0},\qquad\qquad
 {\rm TO}\!:\quad E_{\rm local}=\frac{P}{3\,\varepsilon_0}
$$
where $P(t)$ is electric polarization created by the fluctuating dipoles $\mu_d(t)$. 

Using these expressions in the definition of the electric polarization, $P=n_d\mu_d=n_d\alpha E_{\rm local}$, one finds simple relations for the LO and TO phonon frequencies
$$

 P=\frac{n_dq_e^2}{3\mathcal{m}\,\varepsilon_0}\,\frac{-2P}{\omega_0^2-\omega_{\rm LO \,}^2}\quad \Rightarrow \quad
 \omega_{\rm TO \,} ^2=\omega_0^2-\frac{n_d\,q_e^2}{3\mathcal{m}\,\varepsilon_0}

 $$ (eq-omegaTO)

$$
 P=\frac{n_dq_e^2}{3\mathcal{m}\,\varepsilon_0}\,\frac{P}{\omega_0^2-\omega_{\rm TO \,}^2}\quad \Rightarrow \quad
 \omega_{\rm LO \,}^2=\omega_0^2+\frac{2n_d\,q_e^2}{3\mathcal{m}\,\varepsilon_0}

$$ (eq-omegaLO)

We thus conclude that $\omega_{\rm LO \,}\geq\omega_{\rm TO}$. The difference between these frequencies gauges ionicity of the crystal. We basically see that atomic charges modify the phonon frequency $\omega_0=\sqrt{2\mathcal{K}/\mathcal{m}}$ that has been obtained for neutral atoms. The LO and TO phonons shift charges in different ways and create different local polarizations. The LO phonon separates the charges and creates internal electric fields that counteract the atomic displacements. Therefore, higher energy is required for the LO-type atomic motion. 

The oversimplified nature of this model is not to be overlooked, though. We assumed the same stiffness $\mathcal{K}$ for the longitudinal and transverse atomic motion, which is of course far from realistic in the light of the differences between the compressional and shear waves (Ch.~\ref{sec:ph-LT}). Nevertheless, we will see that even this primitive model does lead to a qualitatively correct physical picture, which justifies the exaggerated approximations involved.

## Interaction with light, polaritons

Expressions~\eqref{eq:omegaTO} and~\eqref{eq:omegaLO} for the phonon frequencies lead to a convenient simplification of the permittivity, which is obtained via the Clausius-Mosotti relation, Eq.~\eqref{eq:clausius},
\be
 \varepsilon(\omega)=\frac{1+2n_d\alpha/(3\varepsilon_0)}{1-n_d\alpha/(3\varepsilon_0)}=\frac{\omega_{\LO}^2-\omega^2}{\omega_{\rm TO}^2-\omega^2}
\label{eq:permittivity-ionic}
\ee
The conjectured frequency $\omega_0$ disappears, and only the tangible frequencies, $\omega_{\rm TO}$ and $\omega_{\rm LO}$, remain. Permittivity diverges at $\omega=\omega_{\rm TO}$ and shows a zero crossing at $\omega=\omega_{\rm LO}$ (Fig.~\ref{fig:phonon-epsilon}, left). 

This form of the permittivity modifies an electromagnetic wave at frequencies near $\omega_{\TO}$ and $\omega_{\LO}$. Indeed, by using Eq.~\eqref{eq:permittivity-ionic} in the dispersion relation, Eq.~\eqref{eq:dispersion-relation}, one finds that the standard linear dispersion $\omega\sim k$ does not hold in the vicinity of the phonon frequency, and no real solution exists for $\omega(k)$ at $\omega_{\TO}\leq \omega<\omega_{\LO}$. It means that photons can not propagate in the crystal within this frequency range. The characteristic dispersion shown in Fig.~\ref{fig:phonon-epsilon} (middle) is often ascribed to a \emph{polariton}, an electromagnetic wave strongly coupled to an intrinsic and dipole-carrying excitation of the crystal.

\begin{figure}
\centerline{\includegraphics{ch12-epsilon}}
\caption{\label{fig:phonon-epsilon}
Interaction of optical phonon with light. Left: frequency dependence of the permittivity. Middle: polariton dispersion caused by the interaction of light with the phonon. Right: frequency dependence of the reflectivity with the \textit{Reststrahlen} band at $\omega_{\TO}<\omega<\omega_{\LO}$. 
}
\end{figure}

The polariton formation causes the crystal to reflect electromagnetic waves. Indeed, at $\omega<\omega_{\TO}$ and at $\omega>\omega_{\LO}$, one finds $\varepsilon>0$, such that $n=n'+in''$ is a real number with $n'\neq 0$ and $n''=0$. Crystal refracts light, as we know from NaCl, quartz, and many other ionic crystals. On the other hand, at $\omega_{\TO}<\omega<\omega_{\LO}$, negative $\varepsilon$ renders $n$ a purely imaginary number with $n'=0$ and $n''\neq 0$.\footnote{This distinction between the purely real and purely imaginary $n$ is, of course, a drawback of our naive approximation. The purely real $\varepsilon(\omega)$ arises from the purely real $\alpha(\omega)$ obtained in Ch.~\ref{sec:dipoles} from the equations of motion that did not include any damping term. Realistically, damping creates a phase shift between $\mu_d(t)$ and $E_{\rm local}(t)$, thus rendering all optical parameters complex numbers.} The resulting reflectivity is 
\be
 R=\frac{|1-in''|^2}{|1+in''|^2}=1,
\ee
so ionic crystals reflect light in the frequency range between $\omega_{\TO}$ and $\omega_{\LO}$ (Fig.~\ref{fig:phonon-epsilon}, right). These so-called \emph{Reststrahlen bands} are observed, for example, in ionic crystals in the infrared range ($\omega=0.3-400$\,THz) typical for optical phonons. A similar mechanism underlies the response of polar molecules that absorb infrared radiation at frequencies of their vibrational modes.

## Lydanne-Sachs-Teller relation

Eq.~\eqref{eq:permittivity-ionic} returns the low-frequency (static) limit of $\varepsilon_{\rm st}=\omega_{\LO}^2/\omega_{\TO}^2$ and the high-frequency limit of 1. Practically, however, more than one optical phonon is usually present in the crystal, so this high-frequency limit of one phonon mode will be the low-frequency limit of another one with a higher energy. Moreover, beyond all phonon frequencies one still expects electronic excitations at energies of $E=10^0-10^4$\,eV. Therefore, it is customary to introduce $\varepsilon_{\infty}\neq 1$ and write permittivity as\footnote{This equation can be obtained rigorously by augmenting the ionic polarizability in Eq.~\eqref{eq:polarizability-ionic} with the atomic polarizability $\alpha_0$ as the origin of $\varepsilon_{\infty}\neq 1$. Unfortunately, this small amendment leads to a far more tedious algebra than what we did here, so this exercise is recommended for nerds only.} 
\be
 \varepsilon(\omega)=\varepsilon_{\infty}\,\frac{\omega_{\LO}^2-\omega^2}{\omega_{\rm TO}^2-\omega^2},
\ee
resulting in
\be
 \frac{\varepsilon_{\rm st}}{\varepsilon_{\infty}}=\frac{\omega_{\LO}^2}{\omega_{\TO}^2},
\ee
the \emph{Lyddane-Sachs-Teller relation}.

\begin{figure}[!h]
\hspace{0cm}
\begin{minipage}{9cm}
 \includegraphics[scale=0.9]{ch12-epsilon-ranges}
\end{minipage}
\hfill
\begin{minipage}{6.5cm}
\caption{\label{fig:epsilon}
Schematic representation of different contributions to the permittivity. Re-orientation of permanent dipoles at low frequencies (Fig.~\ref{fig:debye-relaxation}, right) is followed by the ionic polarization due to phonons and eventually by the electronic polarization due to induced dipoles within individual atoms. Electronic and ionic relaxations give rise to wiggles, which are broadened versions of the divergence of $\varepsilon(\omega)$ shown in Fig.~\ref{fig:phonon-epsilon} (left). 
}
\end{minipage}
\hfill
\end{figure}

An interesting outcome of this analysis is that static permittivity of a crystal is determined by its phonon frequencies. Even a nonpolar crystal without any permanent dipoles may show $\varepsilon_{\rm st}$ well above 1.0 because charges inside the crystal move as a result of the atomic motion. A crystal with permanent dipoles shows an additional contribution to $\varepsilon_{\rm st}$ due to these pre-existing dipoles. Then, $\varepsilon_{\rm st}$ of the Lyddane-Sachs-Teller relation is $\varepsilon_{\infty}$ of the Debye relaxation (Ch.~\ref{sec:debye-relaxation}). Different contributions to the permittivity are sketched in Fig.~\ref{fig:epsilon}.

## Infra-red active phonon modes

While the appealing form of the permittivity, Eq.~\eqref{eq:permittivity-ionic}, is the result of several simplifications introduced in our model (linear chain, same spring constant for the longitudinal and transverse displacements), the qualitative behavior displayed in Fig.~\ref{fig:phonon-epsilon} is quite general. We can see this by re-iterating the arguments from Ch.~\ref{sec:LO-TO} but now considering a displacement wave in the crystal triggered by the oscillating electric field of light. Assume that the electric field $\mathbf{E}=\mathbf{E}_0\,e^{i(\mathbf{k}\mathbf{r}-\omega t)}$ generates the polarization $\mathbf{P}=\mathbf{P}_0\,e^{i(\mathbf{k}\mathbf{r}-\omega t)}$ and the displacement field $\mathbf{D}=\mathbf{D}_0\,e^{i(\mathbf{k}\mathbf{r}-\omega t)}$. According to Maxwell's equations, 
\be
 \div\mathbf{D}=0\quad{\rm and}\quad\rot\mathbf{E}=0 \quad\Ra\quad
 \mathbf{k}\cdot\mathbf{D}=0\quad{\rm and}\quad\mathbf{k}\times\mathbf{E}=0.
\ee
The former condition requires $\mathbf{D}=0$ or $\mathbf{k}\perp\mathbf{D}$ (hence $\mathbf{k}\perp\mathbf{E}$), while the latter requires $\mathbf{E}=0$ or $\mathbf{k}\prl\mathbf{E}$ (hence $\mathbf{k}\prl\mathbf{D}$). 

Consider the TO phonon. In this case, $\mathbf{D}\perp\mathbf{k}$, so $\mathbf{E}$ must be zero for the second condition to be fulfilled. Then, $\varepsilon\rightarrow\infty$ because $\mathbf{D}=\varepsilon\varepsilon_0\mathbf{E}$, so $\varepsilon(\omega)$ diverges at $\omega_{\TO}$. On the other hand, the LO phonon implies $\mathbf{E}\|\mathbf{k}$, so $\mathbf{D}$ must be zero, which is only possible at $\varepsilon=0$. Therefore, a zero crossing of $\varepsilon(\omega)$ should occur at $\omega_{\LO}$. The pre-condition for these arguments is our assumption that $\mathbf{D}\prl\mathbf{E}$ or, basically, the diagonal form of the permittivity tensor expected in crystals with the sufficiently high symmetry (Ch.~\ref{sec:neumann}). 

The situation becomes more complex in crystals with lower symmetry. Indeed, even distinguishing between longitudinal and transverse phonons is not possible in this case, because atomic displacements are not constrained to be parallel or perpendicular to the propagation vector of the phonon (see also Ch.~\ref{sec:ph-reciprocal}). However, what matters for our analysis is not $\mathbf{q}$ but $\mathbf{k}$, the propagation direction of light. One can think of splitting atomic displacements of an arbitrary phonon mode into two components. The component perpendicular to $\mathbf{k}$ leads to a divergence of $\varepsilon(\omega)$ at $\omega=\omega_{\rm TO}$, whereas the component parallel to $\mathbf{k}$ results in the zero crossing at some effective frequency $\omega=\omega_{\rm LO}$. 

It may seem that almost every phonon mode of a non-cubic crystal should show up in $\varepsilon(\omega)$ and in the optical (infrared) spectrum. Not quite. No coupling to light occurs when phonon mode does not generate any dipole moment. This may happen in a covalent crystal or when the phonon preserves inversion symmetry.\footnote{Such modes are called \textit{even} (\textit{gerade}), in contrast to \textit{odd} (\textit{ungerade}) modes that break the inversion symmetry. For a given crystal, the distribution of modes into odd and even can be analyzed on the basis of crystal symmetry and occupied Wyckoff positions, for example using the SAM utility at the Bilbao server.} What ultimately matters is the formation of a dipole moment (i.e., atomic displacements) parallel to $\mathbf{E}$ of light. The coupling between this dipole moment and oscillating electric field renders phonon-mode \emph{IR-active}. Polarized light is often used to single out modes with a given direction of the atomic displacements.