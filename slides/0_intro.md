---
zoom: 0.9
---

# Complexity$^3$ of Modern HEP Experiments

<div class="grid grid-cols-[6fr_7fr_5fr] gap-5">
<div>
<figure>
  <img src="/SherpaPP.png" style="width: 580px !important;">
  <figcaption style="font-size: 18px; position: relative; top: 10px; left: 45px;">Complex phenomena
  </figcaption>
</figure>
</div>
<div>
<figure>
  <img src="/CCC-v2022.png" style="width: 480px !important;">
  <figcaption style="font-size: 18px; position: relative; top: 10px; left: 60px;">Complex machines
  </figcaption>
</figure>
</div>
<div>
<figure>
  <img src="/D810_NEF_3483.jpg" style="width: 480px !important;">
  <figcaption style="font-size: 18px; position: relative; top: 10px; left: 50px;">Complex detectors<br> and reconstruction
  </figcaption>
</figure>
</div>
</div>
<br>

#### Stochastic processes → intractable likelihood (matrix element, parton shower, detector simulation... result in latent variables)
#### Costly MC simulators to generate $x \sim p(x | \theta)$ (for each event, thousands of randomized choices)

---

# Typical Analysis Pipeline

<br>
<figure>
  <img src="/analysis_pipeline.drawio.png" style="width: 880px !important;">
  <figcaption style="color:#b3b3b3ff; font-size: 16px; position: relative; top: 40px; left: 350px;">The diagram is from Pietro Vischia's <a href="https://indico.cern.ch/event/1291157/contributions/5892384/">slides from ICHEP2024</a>
  </figcaption>
</figure>

---

# Determining Multiple Parameters

* Determining multiple parameters ~ fitting a function
* The optimisation of a detector or a reconstruction chain is
conceptually the same thing
*  To perform this optimisation we need to know $\frac{\partial \epsilon}{\partial \theta}$:<br> how does our photon efficiency change w.r.t. the reconstruction parameters $\theta$?

<figure>
  <img src="/gradient.png" style="width: 400px !important;">
</figure>
<br>

* Gradients can be calculated
  * Numerically: unfeasible for many parameters
  * Algorithmically: requires unbroken gradients throughout the whole chain: every step needs to be differentiable
  * **Differentiable programming**

---
zoom: 0.8
---

# Differentiable Programming

<div class="grid grid-cols-[5fr_3fr] gap-10">
<div>

* Differentiable programming is used by, but is independent of ML
* At its core: in any operation, include a way to access its gradient w.r.t. all
parameters (if it exists): auto differentiation
* Auto-differentiation is neither pure numeric nor pure symbolic differentiation
  * Numerical differentiation is not feasible for large optimisation problems
  * Fully symbolic differentiation can easily become not feasible from computational point of view
</div>
<div>
<figure>
  <img src="/backprop.png" style="width: 450px !important; position: relative; top: 0px; left: 0px;">
</figure>
</div>
</div>

* In most cases, back propagation is used ($A \rightarrow X \rightarrow L$)
  * Calculate the numerical values of $b = dL/dx$ using the analytic gradient of the operation
  * Calculate the numerical values of $b \cdot dx/dA$ in the same way
* Each ‘atomic’ simple operation only needs to be equipped with a simple analytic
gradient, then evaluated numerically: best of both worlds.
* This is implemented in one way or another in all modern ML frameworks (TF, torch, JAX)
* Even expressing non-ML algorithms in differentiable frameworks comes with huge advantages w.r.t. the capability of optimising their parameters, and using state-of-the-art libraries to do so

<div style="position: relative; top: 0px; left: 650px;">

##### See also MadJAX approach [arXiv:2203.00057v1 [hep-ph]](https://arxiv.org/abs/2203.00057) 
</div>

---
layout: center
---

# What is MODE about?

---
layout: center
---

# Use differentiable programming to optimise particle physics detectors given a quantification of the physics target(s) and the detector cost

---
layout: image

# the image source
image: /mode/MODE_logos.svg
---

---
zoom: 1.1
--- 

# The MODE Goals

* "We aim to create a versatile, scalable, customizable infrastructure, where a generic detector design task can be encoded, along with all the players (pattern reco, nuisances, cost constraints, a well constructed objective function)"
  * Then **automatic scanning** of the space of design solutions becomes possible!

* This doesn't replace the work of the physicist! We aim at **extending the physicist's abilities** by producing **design assistance tools**, focusing on diagnostic tools and visualizations for **interpretability**

* We don't propose the one *optimal solution* to a given problem, we aim at proposing a **distribution of solutions** in a region of optimality, to assist design choices!

* Optimization targets are not only strictly physics-related (e.g. significances): we consider also **financial cost** and other constraints in the optimization

---
zoom: 1.2
--- 

# The MODE Goals

* We identified and started studying some **relatively simple use cases**: muon tomography detector optimization, calorimeter optimization

* Plan to proceed to other simple use cases (e.g. small detectors for HL-LHC), providing **proofs of concept of increasing complexity**
  * "*Every problem is difficult if you want to solve it well and make an impact*"