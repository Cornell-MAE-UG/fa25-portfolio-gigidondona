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

a- Mass balance
For a steady flow system with one inlet and outlet:
$$
\dot{m}_{in} = \dot{m}_{out} = \dot{m}
$$

b- Energy balance (General first law for control volume)
The general steady-flow energy equation for a control volume is:
$$
\dot{Q} - \dot{W} =
\dot{m} \left[(h_2 - h_1)
+ \frac{V_2^2 - V_1^2}{2}
+ g(z_2 - z_1)\right]
$$

For a turbine, we usually assume that:
$$
\dot{Q} = 0
\deltaKE = \deltaPE = 0 
$$

So this simplifies to:

$$
\dot{W}_{out} = \dot{m}(h_1 - h_2)
$$

where:
$$\dot{W}_{out}$$ is the turbine power output 
$h_1$ is the inlet enthalpy 
$h_2$ is the outlet enthalpy 

c- Entropy balance (Second law for a cotrol volume)
$$
\dot{m}(s_2 - s_1) = \dot{S}_{gen} - \frac{\dot{Q}}{T_{boundary}}
$$
$$
\dot{S}_{gen} = \dot{m}(s_2 - s_1)
$$

where:
$$s_1$$ is the specefic entropy at the turbine inlet 
$$s_2$$ is the specefic entropy at the turbine outlet 
$$\dot{S}_{gen} \geq 0$$ represents the entropy generation due to irreversibilities like friction, tubulence or non ideal expansion.

If the turbine was perfectly isentropic we would have $s_1 = s_2$ and $$\dot{S}_{gen} = 0$$. But for this example we will assume that it is a real turbine and therefore: $s_2 > s_1$ and $$\dot{S}_{gen} > 0$$.


## IV- DESIGN CHANGE: INCREASING INLET TEMPERATURE

The chosen design modification is to increase the inlet temperature in the turbine.
We expect the pressure to remain constant, and we will analyze the changes in enthalpy and in the turbine’s performance.

Let's imagine two different inlet and study the difference.




### a-Thermodynamic States – Original Design

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




### b-Thermodynamic States – Modified Design

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

1- work output 
$$
\dot{W}_{out} = \dot{m}(h_1 - h_2)
$$
According to the tbale we can see that as T increases, $$h_1 > h_2$$.
Therefore $$\dot{W}_{out}$$ increases: the turbine delivers more power for a same flow rate. 

2- Thermal efficiency, Carnot efficiency 
Carnot efficiency is the maximum theoretical efficiency of a heat engine operating between two thermal reservoirs, defined by the temperatures of the hot and cold reservoirs
The relation of carnot efficiency is:
$$
\eta \approx 1 - \frac{T_{cold}}{T_{hot}}
$$
Where $$T_{hot}$$ is related to the turbine inlet temperature and T_{cold} is related to the turbine outlet temperature. In this case it $$T_{hot}$$ increases, the efficiency would increases.
With this new design higher efficiencies are achieved, and more useful work can be drawn from the turbine.




## V- CONCLUSION 

This project explains the main principles of a turbine and discusses how its performance would change with an increase in inlet temperature.
This project has linked theory with real-world engineering decisions.
In a future study, we could analyze the system itself and understand the material limitations of the turbine.

