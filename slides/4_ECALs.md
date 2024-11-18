---
zoom: 0.8
---

# Calorimeters Optimization

<div class="grid grid-cols-[10fr_3fr] gap-10">
<div>
<figure>
  <img src="/ECAL_2.png" style="width: 630px !important; position: relative; top: 0px; left: 0px;">
</figure>
</div>
<div>
<figure>
  <img src="/ECAL_1.png" style="width: 250px !important; position: relative; top: 0px; left: 0px;">
</figure>
</div>
</div>

<br>
<br>

<div class="grid grid-cols-[7fr_5fr_5fr] gap-5">
<div>

#### Calorimeters:
* Complex showers
* So far designs relatively simple
* Good place to invest in systematic gradient-based optimization
* Requirements:
	* Length < 180 cm
	* Cost < 50 kCHF
* Simple diffusion model (DNN):
	* One input (noise) and one final output ($E$)
	* Conditioned on $\theta$, $E_t$
</div>
<div>
<figure>
  <img src="/ECAL_3.png" style="width: 350px !important; position: relative; top: -30px; left: 0px;">
</figure>
</div>
<figure>
  <img src="/ECAL_4.png" style="width: 280px !important; position: relative; top: -30px; left: 0px;">
</figure>
<div>
</div>
</div>
<figure>
  <img src="/ECAL_5.png" style="width: 720px !important; position: relative; top: -110px; left: 440px;">
</figure>

---
zoom: 0.95
---

# Robust Reconstruction Models for ECal Optimization

<div class="grid grid-cols-[5fr_10fr] gap-10">
<div>

#### Module granularity from<br> $15\times15$ to $255\times255$ cells$^2$
<figure>
  <img src="/LHCb_ECAL_1.png" style="width: 290px !important; position: relative; top: 0px; left: 0px;">
</figure>
</div>
<div>
<figure>
  <img src="/LHCb_ECAL_5.png" style="width: 580px !important; position: relative; top: 0px; left: 0px;">
</figure>
</div>
</div>
<br>

<div class="grid grid-cols-[5fr_9fr] gap-5">
<div>

#### **Flexible** DNN architectures
* ResNet-like blocks
* 2..6 convolution layers
* 2..3 linear layers
<figure>
  <img src="/LHCb_ECAL_4.png" style="width: 290px !important; position: relative; top: 0px; left: 0px;">
</figure>
</div>
<div>
<br>

##### Joint network architecture and hyperparameter search provides robust estimations of cluster energy and position for different cell granularities
<br>
<div class="grid grid-cols-[5fr_6fr] gap-10">
<div>
<figure>
  <img src="/LHCb_ECAL_2.png" style="width: 380px !important; position: relative; top: 0px; left: 0px;">
</figure>
</div>
<div>
<figure>
  <img src="/LHCb_ECAL_3.png" style="width: 340px !important; position: relative; top: 0px; left: 0px;">
</figure>
<br>

</div>
</div>

##### Submitted to IEEE Access. See also [[1]](https://doi.org/10.1088/1748-0221/15/05/C05032), [[2]](https://iopscience.iop.org/article/10.1088/1748-0221/15/09/C09030/pdf), [[3]](https://doi.org/10.1088/1742-6596/1740/1/012047)
</div>
</div>

---
zoom: 0.9
---

# Future Muon Collider Calorimeter Optimization

<div class="grid grid-cols-[10fr_3fr] gap-10">
<div>

#### Beam Induced Background (BIB) problem for TeV-scale muon collider
* BIB simulation at 1.5 TeV center-of-mass energy
	* Energy deposits in ECal
* Reference design is CRILIN for ECal
	* Array of $1 \times 1 \times 4.5 \mathrm{cm}^3 ~\mathrm{PbF}_2$ voxels arranged in a dodecahedron
	* 5 layers per wedge
	* Modular design
* Optimizing photon reconstruction efficiency and material cost
</div>
<div>
<figure>
  <img src="/BIB_1.png" style="width: 230px !important; position: relative; top: -85px; left: 50px;">
</figure>
</div>
</div>
<figure>
  <img src="/BIB_2.png" style="width: 830px !important; position: relative; top: -70px; left: 0px;">
</figure>