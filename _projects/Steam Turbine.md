---
layout: project
title: steam turbine efficiency analysis
description: study of a steam turbine with design change (increasing inlet temperature)
technologies: [thermodynamics concepts]
image: /assets/images/img_machinery_A3_01.jpg
math: true
---

## I- INTRODUCTION

Steam turbines are one of the most versatile and oldest prime mover technologies still in general production, used to drive a generator or mechanical machinery. A steam turbine is a heat engine that converts the thermal energy of high-pressure and high-temperature steam into mechanical shaft work.
The turbine derives most of its improvement in thermodynamic efficiency from the use of multiple stages in the expansion of the steam.


This project analyzes the thermodynamic operation of a steam turbine and evaluates how turbine performance changes when the turbine inlet temperature is increased.
Increasing the temperature is a common and realistic design change in modern power plants to improve efficiency and extract more useful work.


## II- QUALITATIVE DESCRIPTION OF THE DEVICE

A steam turbine operates by allowing superheated steam to expand through a series of blades. As the steam expands, its enthalpy decreases, and its steam exits at a lower pressure and temperature.
We often study this system assuming that it is at steady state and operates at constant volume with one inlet and one outlet. To simplify the study, we also assume that the change in kinetic and potential energy is negligible and that the system is adiabatic.


Here is a simplified diagram of a turbine 


![simplified diagram of a turbine]({{ "/assets/images/turbine_diagram.jpg.png" | relative_url }})


## III- GOVERNING EQUATIONS 

---

### a- Mass balance

For a steady flow system with one inlet and outlet:


<p><strong>Mass balance:</strong>
&nbsp; ṁ<sub>in</sub> = ṁ<sub>out</sub> = ṁ
</p>

---

### b- Energy balance (General first law for control volume)


The general steady-flow energy equation for a control volume is:

<p><strong>General form:</strong><br>
Q̇ − Ẇ = ṁ &nbsp;[ (h<sub>2</sub> − h<sub>1</sub>)
+ (V<sub>2</sub><sup>2</sup> − V<sub>1</sub><sup>2</sup>)/2
+ g (z<sub>2</sub> − z<sub>1</sub>) ]
</p>


For a turbine, we usually assume that:

<ul>
  <li>Q̇ ≈ 0 (approximately adiabatic)</li>
  <li>Change in kinetic energy ≈ 0</li>
  <li>Change in potential energy ≈ 0</li>
</ul>

So this simplifies to:

<p><strong>Turbine energy equation:</strong><br>
Ẇ<sub>out</sub> = ṁ (h<sub>1</sub> − h<sub>2</sub>)
</p>

where:
Ẇ<sub>out</sub> is the turbine power output
h<sub>1</sub> is the inlet enthalpy
h<sub>2</sub> is the outlet enthalpy

---

### c- Entropy balance (Second law for a cotrol volume)

<p><strong>Entropy balance:</strong><br>
ṁ (s<sub>2</sub> − s<sub>1</sub>) = Ṡ<sub>gen</sub> − Q̇ / T<sub>boundary</sub>
</p>

where:
s<sub>1</sub> is the specific entropy at the turbine inlet
s<sub>2</sub> is the specific entropy at the turbine outlet 
Ṡ<sub>gen</sub> ≥ 0 represents the entropy generation due to irreversibilities like friction, tubulence or non ideal expansion.

If the turbine was perfectly isentropic we would have s<sub>1</sub> = s<sub>2</sub> and Ṡ<sub>gen</sub> = 0. But for this example we will assume that it is a real turbine and therefore: s<sub>2</sub> > s<sub>1</sub> and Ṡ<sub>gen</sub> ≥ 0.

---

## IV- DESIGN CHANGE: INCREASING INLET TEMPERATURE

The chosen design modification is to increase the inlet temperature in the turbine.
We expect the pressure to remain constant, and we will analyze the changes in enthalpy and in the turbine’s performance.

Let's imagine two different inlet and study the difference.





<h3>a. Thermodynamic States – Original Design</h3>

<table class="steam-table">
  <thead>
    <tr>
      <th>State</th>
      <th>Description</th>
      <th>p (MPa)</th>
      <th>T (°C)</th>
      <th>h (kJ/kg)</th>
      <th>s (kJ/kg·K)</th>
      <th>Region</th>
      <th>Notes</th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>1</td>
      <td>Turbine inlet</td>
      <td>8</td>
      <td>450</td>
      <td>3273</td>
      <td>6.59</td>
      <td>Superheated</td>
      <td>Table @ 8 MPa, 450°C</td>
    </tr>

    <tr>
      <td>2s</td>
      <td>Isentropic outlet</td>
      <td>0.010</td>
      <td>—</td>
      <td>2090</td>
      <td>6.59</td>
      <td>Two-phase</td>
      <td>s₂ = s₁ at 10 kPa</td>
    </tr>

    <tr>
      <td>2</td>
      <td>Real outlet (ηₜ = 0.85)</td>
      <td>0.010</td>
      <td>—</td>
      <td>2383</td>
      <td>~7.1–7.5</td>
      <td>Two-phase</td>
      <td>Efficiency relation</td>
    </tr>
  </tbody>
</table>






<h3>b. Thermodynamic States – Modified Design</h3>

<table class="steam-table">
  <thead>
    <tr>
      <th>State</th>
      <th>Description</th>
      <th>p (MPa)</th>
      <th>T (°C)</th>
      <th>h (kJ/kg)</th>
      <th>s (kJ/kg·K)</th>
      <th>Region</th>
      <th>Notes</th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>1</td>
      <td>Turbine inlet</td>
      <td>8</td>
      <td>550</td>
      <td>3583</td>
      <td>6.66</td>
      <td>Superheated</td>
      <td>Table @ 8 MPa, 550°C</td>
    </tr>

    <tr>
      <td>2s</td>
      <td>Isentropic outlet</td>
      <td>0.010</td>
      <td>—</td>
      <td>2090</td>
      <td>6.66</td>
      <td>Two-phase</td>
      <td>s₂ = s₁ at 10 kPa</td>
    </tr>

    <tr>
      <td>2</td>
      <td>Real outlet (ηₜ = 0.85)</td>
      <td>0.010</td>
      <td>—</td>
      <td>2270</td>
      <td>7.53</td>
      <td>Two-phase</td>
      <td>Efficiency relation</td>
    </tr>
  </tbody>
</table>




### c- impact on device performance
---
**1- work output**

<p><strong>Turbine work equation:</strong><br>
Ẇ<sub>out</sub> = ṁ (h<sub>1</sub> − h<sub>2</sub>)
</p>

According to the table we can see that as T increases, 
<p>
h<sub>1</sub> &gt; h<sub>2</sub>
</p>
Therefore: 
Ẇ<sub>out</sub> increases which means that the turbine delivers more power for a same flow rate. 

---

**2- Thermal efficiency, Carnot efficiency** 

Carnot efficiency is the maximum theoretical efficiency of a heat engine operating between two thermal reservoirs, defined by the temperatures of the hot and cold reservoirs
The relation of carnot efficiency is:

<p><strong>Carnot efficiency:</strong><br>
η ≈ 1 − (T<sub>cold</sub> / T<sub>hot</sub>)
</p>

Where T<sub>hot</sub> is related to the turbine inlet temperature and T<sub>cold</sub> is related to the turbine outlet temperature. In this case if T<sub>hot</sub> increases, the efficiency would increases.
With this new design higher efficiencies are achieved, and more useful work can be drawn from the turbine.


---

## V- CONCLUSION 

This project explains the main principles of a turbine and discusses how its performance would change with an increase in inlet temperature.
This project has linked theory with real-world engineering decisions.
In a future study, we could analyze the system itself and understand the material limitations of the turbine.

