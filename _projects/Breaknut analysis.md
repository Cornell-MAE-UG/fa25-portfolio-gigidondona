---
layout: project
title: nuts breaker 
description: Statics additionnal exercise
technologies: [statics]
image: /assets/images/Breaknutoriginal.png
math: true
---
## Additional exercise of homework 4 
Design problem: Imageine you have a macadamia nut that you want to crack open by hand
using a simple lever nut cracker

### a- Come up with a design to make this task feasible 

Given: 
    load to crack a nut: 222.18kg 
    nut size: 20mm = 2.0cm 
    grip strenght: 40Kg

Find: 
    dimensions od the design of the nut cracker

Plan: 
    draw a free body diagram of the nut breaker 
    find the moment at the joints to calculate the ratio of lenghts and heights

Solution:

<div style="display:flex; align-items:center; gap:40px;">

<div style="flex:1;">

$$
\begin{aligned}
\sum M_A &= \ell_{\text{tot}}F_e - \ell_{\text{nut}}F_{\text{nut}} = 0 \\
\Rightarrow \frac{\ell_{\text{tot}}}{\ell_{\text{nut}}}
&= \frac{F_{\text{nut}}}{F_e}
= \frac{222.18}{40}
\approx 5.56 \\
\Rightarrow h_{\text{tot}} &= 5.56\,h_{\text{nut}} \\
&= 5.56(2\,\text{cm}) \\
&\approx 11.12\,\text{cm}
\end{aligned}
$$

<img src="/fa25-portfolio-gigidondona/assets/images/breaknut.png" style="width:260px; border-radius:8px;">

Therefore: 

<div style="text-align:center; margin:40px 0;">

<img
src="/fa25-portfolio-gigidondona/assets/images/breaknutresult.png"
alt="Final break-nut geometry result"
style="width:520px; max-width:90%; border-radius:8px; box-shadow:0 8px 20px rgba(0,0,0,0.12);">

<div style="margin-top:10px; font-size:0.95em; color:#555;">
Final break-nut geometry obtained from the moment equilibrium analysis.
</div>

</div>

### b- Discuss the usability of the nutcracker that you designed

The nutbreaker is approximately 22cm long and 11cm large, which makes it difficult to use when a nut is inserted. As the height is pretty large, it would make the obejct difficult to use, and therefore not ideal to break the nut. 


### c- Modify your design to use a linear actuator.

Using the datas of a linear actuator found online:

Given: Linear motion actuator:
    force = 200lbs 
    stroke lenght = 4in
    closed lenght = 10.88 in 

Find: 
    dimensions of the updtaed nutbreaker 

Plan:
    Draw a free body diagram with missing values 
    Use the sum of the moments at joint A to find the new heights and lenghts 

Solution: 

<div style="display:flex; align-items:center; gap:40px;">

<div style="flex:1;">

$$
\begin{aligned}
\sum M_A &= \ell_{\text{tot}}F_e - \ell_{\text{nut}}F_{\text{nut}} = 0 \\
\Rightarrow
\frac{\ell_{\text{tot}}}{\ell_{\text{nut}}}
&=
\frac{F_{\text{nut}}}{F_e}
=
\frac{222.18}{200}
\approx 2.49 \\
\frac{\ell_{\text{tot}}}{\ell_{\text{nut}}}
&=
\frac{h_{\text{tot}}}{h_{\text{nut}}} \\
\Rightarrow
h_{\text{nut}}
&=
\frac{\ell_{\text{nut}}h_{\text{tot}}}{\ell_{\text{tot}}} \\
h_{\text{nut}}
&=
\frac{10.88 \times 2.54}{2.49} \\
&\approx 11.32\,\text{cm}
\end{aligned}
$$


<img src="/fa25-portfolio-gigidondona/assets/images/breaknut.png" style="width:260px; border-radius:8px;">

The design must first contact the nut before continuing to rise.

<div style="text-align:center; margin:40px 0;">

<img
src="/fa25-portfolio-gigidondona/assets/images/breaknutupdated.png"
alt="Updated break-nut geometry solution"
style="width:520px; max-width:90%; border-radius:8px; box-shadow:0 8px 20px rgba(0,0,0,0.12);">

<div style="margin-top:10px; font-size:0.95em; color:#555;">
Updated break-nut geometry satisfying the moment equilibrium constraint.
</div>

</div>



