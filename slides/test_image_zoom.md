# Простая картинка

<br>
<figure>
  <img src="/ESL_figure_7.1.png" style="width: 530px !important;">
  <figcaption style="color:#b3b3b3ff; font-size: 11px; position: relative; top: 10px; left: 400px;">Image source:
    <a href="https://hastie.su.domains/ISLP/ISLP_website.pdf#page=262">ISLP Fig. 6.14</a>
  </figcaption>
</figure>
<br>

---

# Зуммируемая картинка

<div style="width:200px">
<vue-image-zoomer
	regular="ESL_figure_7.1_small.png" 
	zoom="ESL_figure_7.1.png"
	:click-zoom="true"
	:show-message="false"
	:zoom-amount="4"
	img-class="img-fluid"
	message-pos="top" />
</div>

---

# Зуммируемая картинка 2

<div style="width:300px">
<inner-image-zoom
	src="ESL_figure_7.1_small.png"
	zoomSrc="ESL_figure_7.1.png"
	zoomType="click" />
</div>

---

# Зуммируемая картинка 3

<div style="width:400px">
  <zoom-on-hover img-normal="ESL_figure_7.1.png"></zoom-on-hover>
</div>