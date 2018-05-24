---
layout: default
title:  A bit of theory...
permalink: /a_bit_of_theory/
---
<h1> A bit of theory... </h1>

<h2> Dielectrophoresis principle </h2>

<p class="retrait">
The term "dielectrophoresis" was first introduced by Pohl in 1951 to describe the motion of dielectric particles due to interaction with a non uniform electric field. </p>
<p class="retrait">Depending on the frequency of the applied field and on the dielectric properties of the particle and its immersion medium, different polarization mechanisms come into play, the main mechanisms being related to the formation of a double electric layer at the particle/liquid interface and to charge accumulation at interfaces between media of different electrical properties (Maxwell-Wagner interfacial polarization effect).
</p>

<p> The force resulting from the interaction between the induced dipole moment $\mathbf{m}$ and the field gradient is expressed by: $$\begin{equation} \mathbf{F_{DEP}}=-\mathbf \nabla U_{El}=(\mathbf m.\mathbf \nabla)\mathbf E \tag{1}\label{equ1}\end{equation}$$ where $U_{El}$ refers to the electric potential energy and $\mathbf E$ to the electric field.</p>

<p>For a spherical particle of radius $r_{ext}$, the induced dipolar moment is given by:
$$\mathbf{m}=4\pi \epsilon_{m} f_{CM}(\omega)r_{ext}^3 \mathbf {E} $$</p>

<p>where $f_{CM}$ is the Clausius-Mossotti factor:
  $$\begin{equation}f_{CM}(\omega)=\frac{\epsilon_{p}^{\ast}-\epsilon_{m}^{\ast}}{\epsilon_{p}^{\ast}+2\epsilon_{m}^{\ast}}\tag{2}\label{fCM}\end{equation}$$
$\epsilon_{p}^{\ast}$ and $\epsilon_{m}^{\ast}$ refer to the complex permittivities of particle and medium, which depend on their respective conductivities and permittivities and on the field frequency $\omega$ :

$$\epsilon^{\ast}= \epsilon-j\frac{\sigma}{\omega}$$</p>

<p> Development of equation \eqref{equ1} leads to the expression of the generalized DEP force:
$$\begin{equation} \mathbf{F_{DEP}}=2\pi \epsilon_m r_{ext}^3 \left\{ Re[f_{CM}(\omega)]\mathbf \nabla E_{RMS}^2+Im[f_{CM}(\omega)] (E_x^2\mathbf \nabla \phi_x+E_y^2\mathbf \nabla \phi_y+E_z^2\mathbf \nabla \phi_z) \right\} \tag{3}\label{FDEPg}\end{equation}$$ </p>

<h3> Conventional dielectrophoresis </h3>

<p class="retrait">When a stationary field is applied, the expression of the time-averaged DEP force \eqref{FDEPg} simplifies to :
$$\mathbf{F_{cDEP}}=2\pi \epsilon_m r^3 Re[f_{CM}(\omega)]\mathbf \nabla E_{RMS}^2$$
This phenomenon is sometimes referred to as "conventional dielectrophoresis" (cDEP). The force depends on the gradient of the squared electric field intensity and exists only in the presence of a non uniform electric field. It is proportional to the volume of the particle, as well as to the real part of the Clausius-Mossotti factor, $ Re[f_ {CM}(\omega)] $. This term reflecting the polarizability contrast between the particle and its immersion medium also determines the direction of the force:
<ul>
<li>When the particle is more polarizable than its immersion medium ($Re[f_{CM}(\omega)]>0$), the force acts in the gradient direction and therefore drives the particle towards areas of maximum field intensity. This corresponds to <i>positive dielectrophoresis</i> (pDEP).</li>
<li>On the contrary, in the case where the particle is less polarizable than its immersion medium ($Re[f_{CM}(\omega)]<0$), the force moves the particle against the gradient, towards the regions of minimum field intensity, which is referred to as <i>negative dielectrophoresis</i> (nDEP).</li>
</ul>
</p>

<div class="DIVimage">

    <img class="im" src='/assets/img/PositiveDEP.png' />
    <figcaption class="figcap"><b>Illustration of pDEP principle. A. </b>The particle and its immersion medium get polarized under the effect of the electric field. Here the particle is more polarizable than its immersion medium. <b>B.</b> The net dipole moment $\mathbf m$ is directed in the same direction as the field. Due to the field non uniformity <span class="saut">($E_B>E_A$), coulomb </span>forces exerted on opposed induced charges are unbalanced&nbsp;($F_B>F_A$), which induces a net displacement of the particle towards the region of maximum field intensity.
    </figcaption>
</div>
