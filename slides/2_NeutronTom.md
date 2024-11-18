# Automatic Optimization of O-PPAC

<div class="grid grid-cols-[5fr_5fr] gap-15">
<div>

##### (Parallel-Plate Avalanche Counter with Optical Readout)<br> 33 SiPMs per array
<br>

#### 1. Define parameters of interest:
* Collimator Length ($L$)
* Pressure of the scintillating gas ($p$)
</div>
<div>
<figure>
  <img src="/NeutronOpt_1.png" style="width: 500px !important;">
</figure>
</div>
</div>

<div class="grid grid-cols-[6fr_5fr] gap-5">
<div>

#### 2. Set loss function:
$\mathcal{L}(p, L, x, y) =$<br>
$\frac{1}{2} \big[ \big(x - \hat{x}(p, L, x, y)\big)^2 + \big(y - \hat{y}(p, L, x, y)\big)^2\big]$
<br>

#### 3. Use AD to find the minimum of $\mathcal{L}$ w.r.t. $p$ and $L$:
* Fully-Connected NN with 3 layers
* 64 neurons per layer
</div>
<div>
<br>
<br>
<div class="grid grid-cols-[5fr_5fr] gap-5">
<div>
<figure>
  <img src="/NeutronOpt_2.png" style="width: 600px !important;">
</figure>
</div>
<div>
<figure>
  <img src="/NeutronOpt_3.png" style="width: 600px !important;">
</figure>
</div>
</div>
</div>
  <div style="color:#b3b3b3ff; font-size: 14px; position: relative; top: 0px; left: 500px;">L matches the <a href="https://iopscience.iop.org/article/10.1088/1748-0221/13/10/P10006">traditional approach</a> (superimposed)
  </div>
</div>

<figure>
  <img src="/NeutronOpt_4.png" style="width: 120px !important; position: relative; top: -220px; left: 540px;">
</figure>