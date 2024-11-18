---
zoom: 0.72
---

# TomOpt: Muon Scattering Tomography Optimization


<figure>
  <img src="/TomOpt_9.png" style="width: 1200px !important;">
</figure>

<br>

<div class="grid grid-cols-[5fr_5fr] gap-5">
<div>

* Differential optimization = <br> minimisation of loss function $\mathcal{L}(a_n)$
	* where $a_n$ are detector parameters
* $\mathcal{L}(a_n) =$ inference error + constraints
* Gradient descent : $\color{red}a_{n+1}\color{#006} = a_n − \gamma \color{red}\nabla\mathcal{L}(a_n)$
</div>
<div>
<figure>
  <img src="/TomOpt_8.png" style="width: 500px !important;">
</figure>
</div>
</div>

<div class="grid grid-cols-[7fr_4fr_5fr] gap-5">
<div>
<br>
<br>
<br>

##### [1]: [arXiv:2309.14027v3 [physics.ins-det]](https://arxiv.org/pdf/2309.14027)
</div>
<div>

* Initial detector parameters:<br>
position, area
* Passive volume (red) with<br> true assigned voxel-wise $X_0$
</div>
<div>

* Muons generation
* Hits recorded in detector panels
* Scattering model used to propagate muons in passive volume in short steps of $\mathcal{O}$(1 cm)
</div>
</div>