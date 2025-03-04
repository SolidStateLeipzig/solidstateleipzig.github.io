# <img src="static_/logo.png" width="20" height="20"> Content


## Underlying approximations

This is an inline image: <img src="/content/_static/logo.png" width="40" height="20"> in a sentence. ![A pictogram](/content/_static/logo.png){width = 20 height = 20}

Atomic motion determines many, if not all, properties of a crystal. Molecules show characteristic vibrations (normal modes) that occur at special frequencies. Crystals feature collective atomic vibrations too, but their nature is somewhat more involved than in the case of molecules. To understand these vibrations in the simplest possible way, we will take advantage of several approximations:
* **classical**, namely, we will treat atomic motion using classical mechanics and obtain **displacement waves** that describe collective atomic motion in the crystal. Quantum mechanics requires this motion to be quantized. The corresponding quantum is called **phonon**, but we usually do not need to solve the respective problem on the quantum level. It is sufficient to quantize the waves obtained classically, as we will consciously do in Ch.~\ref{sec:heat}.
* **harmonic**, namely, elastic energy is quadratic in the displacement, or in other words any displacement creates a restoring force, which is proportional to the displacement. Harmonic approximation works well most of the time, although in Ch.~\ref{sec:expansion} we will see the need to go beyond it.
* **adiabatic**, namely, atomic (nuclear) and electronic degrees of freedom are separated from each other. This is possible because nuclei are much heavier than electrons, so electrons move a lot faster. One can then think of electrons as creating a potential energy landscape for the nuclear motion. The typical time scale of electronic and nuclear motion is $10^{-15}$\,s and $10^{-12}$\,s, respectively. This approximation is also known as the **Born-Oppenheimer approximation**, especially in the context of molecules. It goes back to the very general [adiabatic theorem](https://en.wikipedia.org/wiki/Adiabatic_theorem) of quantum mechanics. The adiabatic approximation fails when two different electronic states have similar energies, and nuclei no longer know in which potential energy landscape to move. Such cases are fairly rare in the ground state, (But by all means not impossible, see the [Jahn-Teller effect](http://doi.org/10.1119/1.17197).) yet they become more common when excited electronic states are considered, for example, when crystal is hit by a laser that drives an electronic excitation of some sort.


## Monoatomic chain

Let's consider the simplest possible case, a chain of atoms with equal spacings $a$. We will use the index $p$ to label atoms along this chain, and introduce the atomic displacements $u_p$ (Fig.~\ref{fig:chain}). Any displacement changes the interatomic distance, and we will assume that chemical bonds behave as springs with the stiffness $\mathcal {K}$. The overall elastic energy is then

$$
 \mathcal{E}_{\rm elastic}=\frac12\sum_p \mathcal{K}(u_{p+1}-u_p)^2.
$$

\begin{figure}
\centerline{\includegraphics{ch11-chain}}
\caption{\label{fig:chain}
Atomic displacements $u_p$ in the monoatomic chain. The right panel shows the dispersion relations for the displacement wave (orange) and elastic wave (blue). The light-blue arrows indicate the atomic displacements at $q=\pi/a$.
}
\end{figure}

Atomic displacements can be determined from the equations of motion,

$$
 m\,\frac{d^2u_p}{dt^2}=-\frac{\partial\mathcal{E}_{\rm elastic}}{\partial u_p}=-\mathcal{K}\,(2u_p-u_{p+1}-u_{p-1}).
$$ (eq-ph-motion)

where $m$ is the atomic mass. Instead of trying a brute force solution of these coupled differential equations, we will choose an ansatz,

$$
 u_p(t)=e^{i(qpa-\omega t)}
$$ (eq-ph-wave)

that essentially describes oscillations with the frequency $\omega$ that propagate along the chain with the propagation vector $q$ (we consider the 1D situation, so the scalar suffices). The first part, $e^{iqpa}$, is basically a phase shift between the oscillations of different atoms. 

Using Eq.~\eqref{eq:ph-wave} in Eq.~\eqref{eq:ph-motion}, one finds $-m\omega^2=-\mathcal{K}(2-e^{iqa}-e^{-iqa})$ and

$$
 \omega^2(q)=2\,\frac{\mathcal{K}}{m}\,[1-\cos(qa)]\Rightarrow
 \omega(q)=2\,\sqrt{\frac{\mathcal{K}}{m}}\times\left|\sin\frac{qa}{2}\right|
$$

where we used the absolute value because frequency must be positive. This is a **dispersion relation** for the displacement wave (phonon) in a monoatomic chain. One immediately notices that $\omega(q)$ is symmetric with respect to $q=0$ and shows periodicity of $2\pi/a$ (Fig.~\ref{fig:chain}) that intriguingly matches periodicity of the reciprocal lattice (Ch.~\ref{sec:reciprocal-detail}). Full implications of this fact will become clear in Ch.~\ref{sec:ph-reciprocal}. For now we will stay away from it and analyze the dispersion relation. By definition, the value of $q$ shows the phase shift between the displacements of neighboring atoms. When this phase shift is small, springs stretch very little, and the wave energy (hence frequency) is low. It increases with increasing $q$. At $q=\pi/a$, the phase shift becomes $\pi$, so adjacent atoms move opposite to each other, thus forming a standing wave (Fig.~\ref{fig:chain}). 

At low $q$, one can use $\sin(qa/2)\simeq qa/2$ and write the linear dispersion relation

$$
 \omega(q)=a\,\sqrt{\frac{\mathcal{K}}{m}}\times q
$$

that corresponds to the group velocity of

$$
 v_{\rm ph}=\frac{d\omega}{dq}=a\,\sqrt{\frac{\mathcal{K}}{m}}
$$ (eq-v-acoustic)

This is the speed of sound, as we will see shortly.

## Elastic waves and sound

Sound is an elastic wave that propagates in any compressible medium. Consider a bar with the cross-section $A$ subject to a deformation that leads to the displacement $u_x(x)$ of the volume element $A\,dx$ parallel to the bar (Fig.~\ref{fig:elastic}). Time dependence of the displacement is described by the usual equation of motion,

$$
 m\,\frac{\partial^2u_x}{\partial t^2}=\sum F=F(x+dx)-F(x)
$$

where forces act on both sides of the volume element. By introducing volume density $\rho=m/V$, one can write

$$
 (\rho A\,dx)\,\frac{\partial^2u_x}{\partial t^2}=F(x+dx)-F(x)\Rightarrow
 \rho\,\frac{\partial^2u_x}{\partial t^2}=\frac{1}{A}\frac{\partial F}{\partial x}=\frac{\partial\varsigma_{xx}}{\partial x}
$$

Hooke's law relates stress and strain, $\varsigma_{xx}=Y\epsilon_{xx}$ via the Young's modulus $Y$, whereas strain can be represented as $\epsilon_{xx}=\partial u_x/\partial x$, so overall

$$
 \frac{\partial^2 u_x}{\partial t^2}=\frac{Y}{\rho}\times\frac{\partial^2 u_x}{\partial x^2}.
$$

This is the standard wave equation solved by our earlier ansatz, Eq.~\eqref{eq:ph-wave}, but with the dispersion relation

$$
 \omega^2=v_s^2\,q^2\quad{\rm where}\quad v_s=\sqrt{\frac{Y}{\rho}}.
$$

The speed $v_s$ resembles our earlier result, Eq.~\eqref{eq:v-acoustic} obtained in the $q\rightarrow 0$ limit, and serves as the **speed of sound**. 

\begin{figure}
\begin{minipage}{9.2cm}
 \includegraphics{ch11-elastic}
\end{minipage}
\begin{minipage}{7.3cm}
\caption{\label{fig:elastic}
Compressional and shear elastic waves. The forces $F(x)$ and $F(x+dx)$ cause the displacements $u_x$ and $u_y$ along the bar and perpendicular to the bar, respectively.
}
\vspace{0.5cm}
\end{minipage}
\end{figure}

An important difference between the compressional elastic wave in a continuous medium, as we considered here, and the displacement wave in a crystal (Ch.~\ref{sec:ph-chain}) is that linear dispersion relation, $\omega=v_s\,q$, breaks down in the latter at higher $q$'s (Fig.~\ref{fig:chain}). This happens because crystal is discrete, so it can't be treated as a continuous medium when period of the displacement wave becomes comparable to the interatomic distance or, in other words, $q$ approaches $\pi/a$. However, the continuum approximation is perfectly justified at low $q$'s where period of the displacement wave is large compared to the interatomic distance. Continuum approximations are widely used in solid-state physics for describing mesoscopic phenomena, for example long-period spin textures and [magnetic skyrmions](https://en.wikipedia.org/wiki/Magnetic_skyrmion).

We can also envisage a wave of displacements $u_y$, which are perpendicular to the bar (Fig.~\ref{fig:elastic}). The solution is similar to the previous case and involves the shear stress, $\tau_{xy}=F/A$, as well as the shear strain, $\epsilon_{xy}=\partial u_y/\partial x$, related by $\tau_{xy}=G\,\epsilon_{xy}$ with the shear modulus $G$. The resulting wave equation,

$$
  \frac{\partial^2 u_y}{\partial t^2}=\frac{G}{\rho}\times\frac{\partial^2 u_y}{\partial x^2},
$$

describes a **shear wave** propagating with the velocity of $\sqrt{G/\rho}$. 

Compressional wave propagates in any elastic medium, whereas shear waves only propagate in solids because gases and liquids feature $G=0$ (their shape can be changed at no energy cost). This is the main reason why sound is a compressional wave. Shear wave can be thought as sound too, but it's not audible because our hearing mechanism involves sound transmission through air. 

## Longitudinal and transverse phonons

The phonon described in Ch.~\ref{sec:ph-chain} is called **acoustic* because $q\rightarrow 0$ part of its dispersion relation describes sound propagation in crystals. A similar acoustic phonon with displacements perpendicular to the propagation direction exists too. Different names can be used to describe these two types of motion depending on the context,



\centerline{%
\renewcommand{\arraystretch}{1.2}
\begin{tabular}{c@{\hspace{2cm}}c@{\hspace{2cm}}c}
 \textit{acoustic phonon} & longitudinal & transverse \\
 \textit{elastic wave} & compressional & shear \\
 \textit{seismic wave} & $p$-wave & $s$-wave
\end{tabular}
}
\medskip

Speeds of the corresponding waves are given by

$$
 v_{\rm LA}=\sqrt{\frac{B+\frac43G}{\rho}},\qquad\qquad v_{\rm TA}=\sqrt{\frac{G}{\rho}}

$$ (eq-acoustic-v)

This is an example of a footnote and tooltip[<sup id="fn1-back">1</sup>](#fn1 "footnote and tooltip 1").
Just a footnote[<sup id="fn2-back">2</sup>](#fn2).
Just a tooltip[<sup>3</sup>](#_blank "tooltip 3").

which are, for example, velocities of the primary ($p$) and secondary ($s$) seismic waves. Since $v_{\rm LA}>v_{\rm TA}$, $p$-wave always arrives earlier than $s$-wave. This time delay measured by a [seismometer](https://en.wikipedia.org/wiki/Seismometer) gauges the distance to the epicentre of an earthquake. Likewise, the data on the propagation of $p$-waves and $s$-waves provides information on the [internal structure of Earth](https://en.wikipedia.org/wiki/Internal_structure_of_Earth). The existence of the liquid outer core and inner solid core is inferred from the refraction of $p$-waves and from the fact that $s$-waves do not reach points on the opposite side of Earth, because shear waves do not propagate through liquid.

In Eq.~\eqref{eq:acoustic-v}, $v_{\rm TA}$ is equal to the velocity of the shear wave as determined in Ch.~\ref{sec:elastic-wave}. However, $v_{\rm LA}$ is different from the velocity of the compressional wave in a thin bar, because Poisson's ratio should be taken into account in a 3D solid. 

In liquid and gas, $G=0$ and speed of sound is described by the **Newton-Laplace equation**,

$$
 v=\sqrt{\frac{B}{\rho}}
$$


## Diatomic chain

Let us now extend this analysis to a diatomic chain with alternating atoms and equal separations, such that all bonds have the same stiffness $\mathcal{K}$. We will proceed similar to the previous case and consider atomic displacements propagating along the chain, but now the two atoms have different mass and should thus show different displacement amplitudes,

$$
 u_p(t)=A_1\,e^{i(qpa-\omega t)},\qquad v_p(t)=A_2\,e^{i(qpa-\omega t)}.
$$ (eq-ph-diatans)

\begin{figure}
\centerline{\includegraphics{ch11-diatomic}}
\caption{\label{fig:diatomic}
Left: atomic displacements in the diatomic chain comprising atoms with the masses $m_1$ and $m_2$ connected by the springs with the same stiffness $\mathcal{K}$. Right: dispersion relation for the two phonon modes, acoustic and optical.
}
\end{figure}

The equations of motion become
$$
\begin{align*}
 m_1\,\frac{d^2u_p}{dt^2}& =-\mathcal{K}(u_p-v_p)-\mathcal{K}(u_p-v_{p-1}), \\[0.3em]
 m_2\,\frac{d^2v_p}{dt^2}& =-\mathcal{K}(v_p-u_p)-\mathcal{K}(v_p-u_{p+1}).
\end{align*}
$$
Our ansatz for $u_p$ and $v_p$ returns a system of two linear equations for the amplitudes $A_1$ and $A_2$,

$$

\left\{ \begin{array}{l}
 -m_1\omega^2A_1=-\mathcal{K} A_1+\mathcal{K} A_2-\mathcal{K} A_1+\mathcal{K} A_2\,e^{-iqa} \\
 -m_2\omega^2A_2=-\mathcal{K} A_2+\mathcal{K} A_1-\mathcal{K} A_2+\mathcal{K} A_1\,e^{iqa}
\end{array}\right.
$$

or


$$
\left\{ \begin{array}{l}
 (m_1\omega^2-2\mathcal{K})A_1+\mathcal{K}(1+e^{-iqa})A_2=0 \\
 \mathcal{K}(1+e^{iqa})A_1+(m_2\omega^2-2\mathcal{K})A_2=0
\end{array}\right.
$$ (eq-phamplitude)

The solution for $A_1$ and A$_2$ exists when the determinant is zero, namely,

$$

\left| \begin{array}{cc}
 m_1\omega^2-2\mathcal{K} & \mathcal{K}(1+e^{-iqa}) \\
 \mathcal{K}(1+e^{iqa}) & m_2\omega^2-2\mathcal{K} \\
\end{array}\right|=0
$$

This condition returns a quadratic equation for $\omega^2$,

$$
 m_1m_2\,\omega^4-2\mathcal{K} (m_1+m_2)\,\omega^2+2\mathcal{K}^2[1-\cos(qa)]=0,
$$

and 

$$
 \omega^2(q)=\frac{\mathcal{K}}{\mathcal{m}}\pm \mathcal{K}\sqrt{\frac{1}{\mathcal{m}^2}-\frac{4}{m_1m_2}\sin^2\frac{qa}{2}}
$$

where we introduced the **reduced mass**,

$$
 \frac{1}{\mathcal{m}}=\frac{1}{m_1}+\frac{1}{m_2}
$$


## Acoustic and optical phonons

There are now two dispersion relations that define two **phonon branches**. The $\omega_-(q)$ branch has zero frequency at $q=0$. It is called \emph{acoustic} because it reduces to an elastic wave in the low-$q$ limit and describes sound propagation. The $\omega_+(q)$ branch is \emph{optical}, because it can interact with light, as we will see in Ch.~\ref{sec:optical}. Optical phonon has the finite frequency of $\sqrt{2\mathcal{K}/\mathcal{m}}$ at $q=0$. 

The main intrinsic difference between the acoustic and optical phonons lies in the amplitudes $A_1$ and $A_2$.  For an optical branch at $q=0$, Eqs.~\eqref{ph-eqamplitude} yield $A_1/A_2=-m_2/m_1$. The atoms of different type oscillate out-of-phase. On the other hand, $\omega_-=0$ of the acoustic mode yields $A_1/A_2=1$, such that atoms of different type oscillate in-phase near $q=0$. 

At $q=\pi/a$, one finds $\omega_+=\sqrt{2\mathcal{K}/m_2}$ and $\omega_-=\sqrt{2\mathcal{K}/m_1}$ when $m_1>m_2$. Then,

$$
 \left(\frac{A_1}{A_2}\right)_+=-\frac{\mathcal{K}(1+e^{-iqa})}{m_1\omega_+^2-2\mathcal{K}}\rightarrow 0,\qquad
 \left(\frac{A_1}{A_2}\right)_-=-\frac{m_2\omega_-^2-\mathcal{K}}{\mathcal{K}(1+e^{iqa})}\rightarrow\infty.
$$
It means that only the light atoms ($m_2$) oscillate in the optical mode, whereas only the heavy atoms ($m_1$) oscillate in the acoustic mode. A nice visualization of the modes at arbitrary $q$-values and for different $m_2/m_1$ ratios can be found [here](http://lampx.tugraz.at/~hadley/ss1/phonons/1d/1d2m.php).







[<sup id="fn1">1</sup>](#fn1-back) footnote and tooltip 1
[<sup id="fn2">2</sup>](#fn2-back) footnote 2

