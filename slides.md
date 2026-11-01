---
# try also 'default' to start simple
routerMode: hash
theme: scholarly
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://cover.sli.dev
# some information about your slides (markdown enabled)
title: Welcome to Slidev
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# apply UnoCSS classes to the current slide
class: text-center
# https://sli.dev/features/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: slide-left
# enable Comark Syntax: https://comark.dev/syntax/markdown
comark: true
# duration of the presentation
duration: 35min
authors:
  - name: Arjun Varma R
    institution: Université de Lorraine
  - name: Ahmed Dimokrati
    institution: Mohammed VI Polytechnic University, Morocco
  - name: Maeva Cottura
    institution: Université de Lorraine
  - name: Benoît Appolaire
    institution: Université de Lorraine
footerMiddle: Matériaux 2026
themeConfig:
  colorTheme: classic-blue
  fontTheme: modern
  chromeMode: dark
  sectionMode: dark
aspectRatio: 4/3
fontsize:
  body: 16px
  h1: 46px
  h2: 34px
  h3: 26px
---

# Discontinuous Precipitation

A elasticity-coupled multi-phase field investigation

<!--
<div @click="$slidev.nav.next" class="mt-12 py-1" hover:bg="white op-10">
  Press Space for next page <carbon:arrow-right />
</div>
-->

<div class="abs-br m-6 text-xl">
  <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="slidev-icon-btn">
    <carbon:edit />
  </button>
  <a href="https://github.com/slidevjs/slidev" target="_blank" class="slidev-icon-btn">
    <carbon:logo-github />
  </a>
</div>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---
transition: slide-left
layout:center
---

# Analyzing discontinuous precipitation


<div class="slide-content">
There are three types of simulations now:

 - Straight grain boundary (600 x 150) $c_0 = 0.2$   
 - Straight grain boundary (600 x 300) $c_0 = 0.2$ 
 - Curved grain boundary (600 x 600)   $c_0 = 0.2$ 
</div>

<style>
.slide-content {
  position: absolute;
  top: 35%;
  bottom: 3%;
  left: 5%;
  right: 2%;
  display: flex;
  flex-direction: column;
  gap: 0.4rem;
  min-height: 0;
}

.bullet-center {
  flex: 3;
  min-height: 0;
  display: flex;
  align-items: center;
  justify-content: center;
}

.bullet-center ul {
  width: 100%;
  margin: 0;
  padding-left: 1.4em;
}

.bullet-center li {
  margin-bottom: 0.25em;
}
</style>

<!--
You can have `style` tag in markdown to override the style for the current page.
Learn more: https://sli.dev/features/slide-scope-style
-->

<!--
<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>
-->

<!--
Here is another comment.
-->

---
transition: slide-left
layout:center
---
 
# Summary of the results

<div class="slide-content">

- Coherent-Coherent (CC) leads to flat precipitates growing equally in both directions but with no grain boundary migration.
- Incoherent-Incoherent (II) also leads to equal growth in both grains although with a more rounded shape of the tips.
- Coherent-Incoherent (CI) cases have a GB migration even for initially straight GBs, in the direction of growth of incoherent boundary.
- For a smaller eigenstrain, the flattening of precipitates along the horizontal direction is not pronounced.
- The key questions to be answered are: 
    - what makes the grain boundary migrate for the coherent-incoherent (CI) case?
    - what is the effect of particle spacing on the grain boundary bending?
    - what is the effect of the curved grain boundary?

</div>

<style>
.slide-content {
  position: absolute;
  top: 25%;
  bottom: 3%;
  left: 5%;
  right: 2%;
  display: flex;
  flex-direction: column;
  gap: 0.4rem;
  min-height: 0;
}
</style>
---
transition: slide-left
layout: default
---
# Precipitate evolution: CC and II cases

<div class="slide-content">

  <div class="gif-grid">
    <div class="gif-cell">
      <Mathlabel expr="\mathrm{II}:\ \epsilon^0_{11}=0.04,\ \sigma_{in}=0.75\;\mathrm{mJ}/\mathrm{m}^2" />
      <img src="/horizontal_new_higher_sup/II/straight_GB/eps_11_0.04/incoh_0.75/frames/plotsum_first_quadrant.gif" />
    </div>
    <div class="gif-cell">
      <Mathlabel expr="\mathrm{II}:\ \epsilon^0_{11}=0.04,\ \sigma_{in}=1.0\;\mathrm{mJ}/\mathrm{m}^2" />
      <img src="/horizontal_new_higher_sup/II/straight_GB/eps_11_0.04/incoh_1.0/frames/plotsum_first_quadrant.gif" />
    </div>
    <div class="gif-cell">
      <Mathlabel expr="\mathrm{CC}:\ \epsilon^0_{11}=0.04,\ \sigma_{coh}=0.3\;\mathrm{mJ}/\mathrm{m}^2" />
      <img src="/horizontal_new_higher_sup/CC/straight_GB/eps_11_0.04/r_2.5/frames/plotsum_first_quadrant.gif" />
    </div>
    <div class="gif-cell">
      <Mathlabel expr="\mathrm{CC}:\ \epsilon^0_{11}=0.04,\ \sigma_{coh}=0.6\;\mathrm{mJ}/\mathrm{m}^2" />
      <img src="/horizontal_new_higher_sup/CC/straight_GB/eps_11_0.04/r_1.25/frames/plotsum_first_quadrant.gif" />
    </div>
  </div>

  <div class="bullet-center">
    <ul>
      <li>PB energies are identical between the top and bottom rows.</li>
      <li>Elastic energy differences arise from the coherent versus incoherent precipitate boundaries.</li>
    </ul>
  </div>

</div>

<style>
/* =========================
   Common slide layout
   ========================= */

.slide-content {
  position: absolute;
  top: 20%;
  bottom: 3%;
  left: 5%;
  right: 2%;

  display: flex;
  flex-direction: column;
  gap: 0.4rem;
  min-height: 0;
}


/* =========================
   Four-GIF grid
   ========================= */

.gif-grid {
  flex: 7;
  min-height: 0;

  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  grid-template-rows: repeat(2, minmax(0, 1fr));
  gap: 8px;
}

.gif-cell {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;

  min-width: 0;
  min-height: 0;
  overflow: hidden;
}

.gif-cell img {
  display: block;

  width: 100%;
  height: 0;
  flex: 1;

  min-height: 0;
  object-fit: contain;
}




/* =========================
   Bullet section
   ========================= */

.bullet-center {
  flex: 3;
  min-height: 0;

  display: flex;
  align-items: center;
  justify-content: center;
}

.bullet-center ul {
  width: 100%;
  margin: 0;
  padding-left: 1.4em;
}

.bullet-center li {
  margin-bottom: 0.25em;
}
</style>

---
transition: slide-left
---

# What about the supersaturation?

<div class="slide-content">

  <div class="gif-grid">
    <div class="gif-cell">
      <Mathlabel expr="\mathrm{II}:\ \epsilon^0_{11}=0.04,\ \sigma_{in}=0.75\;\mathrm{mJ}/\mathrm{m}^2" />
      <img src="/horizontal_new_higher_sup/II/straight_GB/eps_11_0.04/incoh_0.75/c_profile_animation.gif" />
    </div>
    <div class="gif-cell">
      <Mathlabel expr="\mathrm{II}:\ \epsilon^0_{11}=0.04,\ \sigma_{in}=1.0\;\mathrm{mJ}/\mathrm{m}^2" />
      <img src="/horizontal_new_higher_sup/II/straight_GB/eps_11_0.04/incoh_1.0/c_profile_animation.gif" />
    </div>
    <div class="gif-cell">
      <Mathlabel expr="\mathrm{CC}:\ \epsilon^0_{11}=0.04,\ \sigma_{coh}=0.3\;\mathrm{mJ}/\mathrm{m}^2" />
      <img src="/horizontal_new_higher_sup/CC/straight_GB/eps_11_0.04/r_2.5/c_profile_animation.gif" />
    </div>
    <div class="gif-cell">
      <Mathlabel expr="\mathrm{CC}:\ \epsilon^0_{11}=0.04,\ \sigma_{coh}=0.6\;\mathrm{mJ}/\mathrm{m}^2" />
      <img src="/horizontal_new_higher_sup/CC/straight_GB/eps_11_0.04/r_1.25/c_profile_animation.gif" />
    </div>

  </div>

</div>

<style>
.slide-content {
  position: absolute;
  top: 20%;
  bottom: 3%;
  left: 5%;
  right: 2%;

  display: flex;
  flex-direction: column;
  gap: 0.4rem;
  min-height: 0;
}


/* =========================
   Gif Grid 2x2
   ========================= */

.gif-grid {
  flex: 7;
  min-height: 0;
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  grid-template-rows: repeat(2, minmax(0, 1fr));
  gap: 8px;
}

.gif-cell {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  min-width: 0;
  min-height: 0;
  overflow: hidden;
}

.gif-cell img {
  display: block;
  width: 100%;
  height: 0;
  flex: 1;
  min-height: 0;
  object-fit: contain;
}

</style>

---
transition: slide-left
---
# Interfacial curvature and concentration

#### $\mathrm{II}:\ \epsilon^0_{11}=0.04,\ \sigma_{in}=0.75\;\mathrm{mJ}/\mathrm{m}^2 (\mathrm{above}),\; \sigma_{in}=1.0\;\mathrm{mJ}/\mathrm{m}^2 (\mathrm{below})$
<div class="grid grid-rows-2 gap-2">
  <img src="/horizontal_new_higher_sup/II/straight_GB/eps_11_0.04/incoh_0.75/results_tips/tips_vs_time.png" style="width: 20cm; height: auto;" />
  <img src="/horizontal_new_higher_sup/II/straight_GB/eps_11_0.04/incoh_1.0/results_tips/tips_vs_time.png" style="width: 20cm; height: auto;"/>
</div>

---
transition: slide-left
---
# Interfacial curvature and concentration

#### $\mathrm{CC}:\ \epsilon^0_{11}=0.04,\ \sigma_{in}=0.3\;\mathrm{mJ}/\mathrm{m}^2 (\mathrm{above}),\; \sigma_{in}=0.6\;\mathrm{mJ}/\mathrm{m}^2 (\mathrm{below})$
<div class="grid grid-rows-2 gap-2">
  <img src="/horizontal_new_higher_sup/CC/straight_GB/eps_11_0.04/r_2.5/results_tips/tips_vs_time.png" style="width: 20cm; height: auto;" />
  <img src="/horizontal_new_higher_sup/CC/straight_GB/eps_11_0.04/r_1.25/results_tips/tips_vs_time.png" style="width: 20cm; height: auto;"/>
</div>


---
transition: slide-left
---


# And von Mises stress?

<div class="slide-content">

  <div class="gif-grid">
    <div class="gif-cell">
      <Mathlabel expr="\mathrm{II}:\ \epsilon^0_{11}=0.04,\ \sigma_{in}=0.75\;\mathrm{mJ}/\mathrm{m}^2" />
      <img src="/horizontal_new_higher_sup/II/straight_GB/eps_11_0.04/incoh_0.75/vonmises_map.gif" />
    </div>
    <div class="gif-cell">
      <Mathlabel expr="\mathrm{II}:\ \epsilon^0_{11}=0.04,\ \sigma_{in}=1.0\;\mathrm{mJ}/\mathrm{m}^2" />
      <img src="/horizontal_new_higher_sup/II/straight_GB/eps_11_0.04/incoh_1.0/vonmises_map.gif" />
    </div>
    <div class="gif-cell">
      <Mathlabel expr="\mathrm{CC}:\ \epsilon^0_{11}=0.04,\ \sigma_{coh}=0.3\;\mathrm{mJ}/\mathrm{m}^2" />
      <img src="/horizontal_new_higher_sup/CC/straight_GB/eps_11_0.04/r_2.5/vonmises_map.gif" />
    </div>
    <div class="gif-cell">
      <Mathlabel expr="\mathrm{CC}:\ \epsilon^0_{11}=0.04,\ \sigma_{coh}=0.6\;\mathrm{mJ}/\mathrm{m}^2" />
      <img src="/horizontal_new_higher_sup/CC/straight_GB/eps_11_0.04/r_1.25/vonmises_map.gif" />
    </div>

  </div>

</div>

<style>
.slide-content {
  position: absolute;
  top: 20%;
  bottom: 3%;
  left: 5%;
  right: 2%;

  display: flex;
  flex-direction: column;
  gap: 0.4rem;
  min-height: 0;
}


/* =========================
   Gif Grid 2x2
   ========================= */

.gif-grid {
  flex: 7;
  min-height: 0;
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  grid-template-rows: repeat(2, minmax(0, 1fr));
  gap: 8px;
}

.gif-cell {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  min-width: 0;
  min-height: 0;
  overflow: hidden;
}

.gif-cell img {
  display: block;
  width: 100%;
  height: 0;
  flex: 1;
  min-height: 0;
  object-fit: contain;
}

</style>

---
transition: slide-left
---
# And von Mises stress?

<div class="slide-content">

  <div class="gif-grid">
    <div class="gif-cell">
      <Mathlabel expr="\mathrm{II}:\ \epsilon^0_{11}=0.04,\ \sigma_{in}=0.75\;\mathrm{mJ}/\mathrm{m}^2" />
      <img src="/horizontal_new_higher_sup/II/straight_GB/eps_11_0.04/incoh_0.75/vonmises_profile.gif" />
    </div>
    <div class="gif-cell">
      <Mathlabel expr="\mathrm{II}:\ \epsilon^0_{11}=0.04,\ \sigma_{in}=1.0\;\mathrm{mJ}/\mathrm{m}^2" />
      <img src="/horizontal_new_higher_sup/II/straight_GB/eps_11_0.04/incoh_1.0/vonmises_profile.gif" />
    </div>
    <div class="gif-cell">
      <Mathlabel expr="\mathrm{CC}:\ \epsilon^0_{11}=0.04,\ \sigma_{coh}=0.3\;\mathrm{mJ}/\mathrm{m}^2" />
      <img src="/horizontal_new_higher_sup/CC/straight_GB/eps_11_0.04/r_2.5/vonmises_profile.gif" />
    </div>
    <div class="gif-cell">
      <Mathlabel expr="\mathrm{CC}:\ \epsilon^0_{11}=0.04,\ \sigma_{coh}=0.6\;\mathrm{mJ}/\mathrm{m}^2" />
      <img src="/horizontal_new_higher_sup/CC/straight_GB/eps_11_0.04/r_1.25/vonmises_profile.gif" />
    </div>

  </div>

</div>

<style>
.slide-content {
  position: absolute;
  top: 20%;
  bottom: 3%;
  left: 5%;
  right: 2%;

  display: flex;
  flex-direction: column;
  gap: 0.4rem;
  min-height: 0;
}


/* =========================
   Gif Grid 2x2
   ========================= */

.gif-grid {
  flex: 7;
  min-height: 0;
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  grid-template-rows: repeat(2, minmax(0, 1fr));
  gap: 8px;
}

.gif-cell {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  min-width: 0;
  min-height: 0;
  overflow: hidden;
}

.gif-cell img {
  display: block;
  width: 100%;
  height: 0;
  flex: 1;
  min-height: 0;
  object-fit: contain;
}

</style>

--



---
transition: slide-left
---

# Coherent - Incoherent (CI)


<div class="slide-content">

  <div class="gif-grid">
    <div class="gif-cell">
      <Mathlabel expr="\mathrm{CI}:\ \epsilon^0_{11}=0.04,\ \sigma_{in}=0.3\;\mathrm{mJ}/\mathrm{m}^2,\ \sigma_{coh}=0.3\;\mathrm{mJ}/\mathrm{m}^2" />
      <img src="/horizontal_new_higher_sup/CI/straight_GB/eps_11_0.04/sigma_CI_equal/r_2.5/frames/plotsum_first_quadrant.gif" />
    </div>
 <div class="gif-cell">
      <Mathlabel expr="\mathrm{CI}:\ \epsilon^0_{11}=0.04,\ \sigma_{in}=0.6\;\mathrm{mJ}/\mathrm{m}^2,\ \sigma_{coh}=0.6\;\mathrm{mJ}/\mathrm{m}^2" />
      <img src="/horizontal_new_higher_sup/CI/straight_GB/eps_11_0.04/sigma_CI_equal/r_1.25/frames/plotsum_first_quadrant.gif" />
    </div>
 <div class="gif-cell">
      <Mathlabel expr="\mathrm{Concentration\;Profile}" />
      <img src="/horizontal_new_higher_sup/CI/straight_GB/eps_11_0.04/sigma_CI_equal/r_2.5/c_profile_animation.gif" />
    </div>
 <div class="gif-cell">
      <Mathlabel expr="\mathrm{Concentration\;Profile}" />
      <img src="/horizontal_new_higher_sup/CI/straight_GB/eps_11_0.04/sigma_CI_equal/r_1.25/c_profile_animation.gif" />
    </div>
    </div>
  </div>


<style>
.slide-content {
  position: absolute;
  top: 15%;
  bottom: 3%;
  left: 5%;
  right: 2%;

  display: flex;
  flex-direction: column;
  gap: 0.6rem;
  min-height: 0;
}


/* =========================
   Gif Grid 2x2
   ========================= */

.gif-grid {
  flex: 7;
  min-height: 0;
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  grid-template-rows: repeat(2, minmax(0, 1fr));
  gap: 4px;
}

.gif-cell {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  min-width: 0;
  min-height: 0;
  overflow: hidden;
}

.gif-cell img {
  display: block;
  width: 100%;
  height: 0;
  flex: 1;
  min-height: 0;
  object-fit: contain;
}

</style>


---
transition: slide-left
---

# Coherent - Incoherent (CI) cntd...

<div class="grid grid-rows-2 gap-2">
  <img src="/horizontal_new_higher_sup/CI/straight_GB/eps_11_0.04/sigma_CI_equal/r_2.5/results_tips/tips_vs_time.png" style="width: 20cm; height: auto;" />
  <img src="/horizontal_new_higher_sup/CI/straight_GB/eps_11_0.04/sigma_CI_equal/r_1.25/results_tips/tips_vs_time.png" style="width: 20cm; height: auto;"/>
</div>


---
transition: slide-left
---

# Coherent - Incoherent (CI) cntd...

<div class="slide-content">

  <div class="gif-grid">
    <div class="gif-cell">
      <Mathlabel expr="\mathrm{CI}:\ \epsilon^0_{11}=0.04,\ \sigma_{in}=0.3\;\mathrm{mJ}/\mathrm{m}^2,\ \sigma_{coh}=0.3\;\mathrm{mJ}/\mathrm{m}^2" />
      <img src="/horizontal_new_higher_sup/CI/straight_GB/eps_11_0.04/sigma_CI_equal/r_2.5/vonmises_map.gif" />
    </div>
 <div class="gif-cell">
      <Mathlabel expr="\mathrm{CI}:\ \epsilon^0_{11}=0.04,\ \sigma_{in}=0.6\;\mathrm{mJ}/\mathrm{m}^2,\ \sigma_{coh}=0.6\;\mathrm{mJ}/\mathrm{m}^2" />
      <img src="/horizontal_new_higher_sup/CI/straight_GB/eps_11_0.04/sigma_CI_equal/r_1.25/vonmises_map.gif" />
    </div>
 <div class="gif-cell">
      <Mathlabel expr="\mathrm{von\;Mises\;stress\;Profile}" />
      <img src="/horizontal_new_higher_sup/CI/straight_GB/eps_11_0.04/sigma_CI_equal/r_2.5/vonmises_profile.gif" />
    </div>
 <div class="gif-cell">
      <Mathlabel expr="\mathrm{von\;Mises\;stress\;Profile}" />
      <img src="/horizontal_new_higher_sup/CI/straight_GB/eps_11_0.04/sigma_CI_equal/r_1.25/vonmises_profile.gif" />
    </div>
    </div>
  </div>


<style>
.slide-content {
  position: absolute;
  top: 15%;
  bottom: 3%;
  left: 5%;
  right: 2%;

  display: flex;
  flex-direction: column;
  gap: 0.6rem;
  min-height: 0;
}


/* =========================
   Gif Grid 2x2
   ========================= */

.gif-grid {
  flex: 7;
  min-height: 0;
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  grid-template-rows: repeat(2, minmax(0, 1fr));
  gap: 4px;
}

.gif-cell {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  min-width: 0;
  min-height: 0;
  overflow: hidden;
}

.gif-cell img {
  display: block;
  width: 100%;
  height: 0;
  flex: 1;
  min-height: 0;
  object-fit: contain;
}

</style>

---
transition: slide-left
---

# When the difference is only coherency

#### Ahmed's simulation: $\epsilon^0_{11} = 0.04, \sigma = 0.267 \mathrm{J}/\mathrm{m}^2$

<div class="grid grid-rows-1 gap-0">
  <img src="/Ahmed/pnpm-lock.gif" class="w-full" />
</div>

---
transition: slide-left
---

# When the difference is only coherency.

#### Ahmed's simulation: $\epsilon^0_{11} = 0.04, \sigma = 0.267 \mathrm{J}/\mathrm{m}^2$

<div class="grid grid-rows-1 gap-0">
  <img src="/Ahmed/results_tips/tips_vs_time.png" class="w-full" />
</div>


---
transition: slide-left
---
# Curved Grain Boundary
#### CC: $\epsilon^0_{11} = 0.02,\;\sigma=0.3\mathrm{J}/\mathrm{m}^2$  (above), CI:  $\epsilon^0_{11} = 0.04,\;\sigma=0.6\mathrm{J}/\mathrm{m}^2$  (below)
<div class="grid grid-rows-2 gap-4">
  <img src="/Curved_GB/job.2581766.gkh74/plotsum_animation.gif" class="w-full" />
  <img src="/Curved_GB/job.2581781.gkh74/plotsum_animation.gif" class="w-full" />
</div>

<PoweredBySlidev mt-10 />
