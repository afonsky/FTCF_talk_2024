---
theme: seriph
addons:
  - "@twitwi/slidev-addon-ultracharger"
addonsConfig:
  ultracharger:
    inlineSvg:
      markersWorkaround: false
    disable:
      - metaFooter
      - tocFooter
NObackground: >-
  https://images.unsplash.com/photo-1511149755252-35875b273fd6?ixlib=rb-4.0.3&dl=leon-contreras-qpdfU6vehgs-unsplash.jpg&w=1920&q=80&fm=jpg&crop=entropy&cs=tinysrgb
background: /logo/tmp_cover.jpg
highlighter: shiki
routerMode: hash
lineNumbers: false

css: unocss
title: Design of Experiments Using Machine Learning
subtitle: FTCF Workshop Guangzhou
date: 21 November 2024
venue: on behalf the MODE collaboration
author: Alexey Boldyrev
---

<br>
<br>
<br>
<br>

# <span style="font-size:30.0pt" v-html="$slidev.configs.title?.replaceAll(' ', '<br/>')"></span>
## FTCF Workshop Guangzhou (17-21 November 2024)
<br>
<br>

## Alexey Boldyrev <span style="font-size:18.0pt">(HSE University)</span>
### on behalf the MODE collaboration
<br>

<span style="font-size:18.0pt" v-html="$slidev.configs.date?.replaceAll(' ', '<br/>')"></span>

<div class="abs-tl mx-5 my-1">
  <img src="/logo/mode_logo.svg" class="h-36">
</div>

<div>
<br>
<br>
<!-- <span style="color:#b3b3b3ff; font-size: 11px; float: right;">Изображение: Midjourney 6.0. Запрос "Visual perception and data visualization"
</span> -->
</div>


<style>
  :deep(footer) { padding-bottom: 3em !important; }
</style>

<!--
NB: This demo uses a custom syntax (using preparser extensions), with all the @@@@.
-->

---
src: ./slides/0_outline.md
---

---
src: ./slides/0_intro.md
---

---
src: ./slides/1_TomOpt.md
---

---
src: ./slides/2_NeutronTom.md
---

---
src: ./slides/3_SWGO.md
---

---
src: ./slides/4_ECALs.md
---

---
src: ./slides/4_GranularCalo.md
---

---
src: ./slides/5_Neuromorphic.md
---

---
src: ./slides/0_end.md
---