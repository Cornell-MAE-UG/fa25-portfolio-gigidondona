---
layout: project
title: steam turbine efficiency analysis
description: study of a steam turbine with design change (increasing inlet temperature)
technologies: [thermodynamics concepts]
image: /assets/images/img_machinery_A3_01.jpg
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
h_1 is the inlet enthalpy 
h_2 is the outlet enthalpy 

c- Entropy balance (Second law for a cotrol volume)
$$
\dot{m}(s_2 - s_1) = \dot{S}_{gen} - \frac{\dot{Q}}{T_{boundary}}
$$
$$
\dot{S}_{gen} = \dot{m}(s_2 - s_1)
$$

where:
s_1 is the specefic entropy at the turbine inlet 
s_2 is the specefic entropy at the turbine outlet 
$$\dot{S}_{gen} \geq 0$$ represents the entropy generation due to irreversibilities like friction, tubulence or non ideal expansion.

If the turbine was perfectly isentropic we would have s_1 = s_2 and \dot{S}_{gen} = 0. But for this example we will assume that it is a real turbine and therefore: s_2 > s_1 and $$\dot{S}_{gen} > 0$$.


## IV- DESIGN CHANGE: INCREASING INLET TEMPERATURE

The chosen design modification is to increase the inlet temperature in the turbine.
We expect the pressure to remain constant, and we will analyze the changes in enthalpy and in the turbine’s performance.


Let's imagine two different inlet and study the difference.


### a-Thermodynamic States – Original Design

| State | Description             | p (MPa) | T (°C) | h (kJ/kg) | s (kJ/kg·K) | Region            | Notes                                |
|------:|--------------------------|--------:|-------:|----------:|------------:|-------------------|--------------------------------------|
| 1     | Turbine inlet            | 8       | 450    | 3273      | 6.59        | Superheated       | Superheated table @ 8 MPa, 450°C     |
| 2s    | Isentropic outlet        | 0.010   | —      | 2090      | 6.59        | Two-phase         | Using s₂s = s₁ at 10 kPa             |
| 2     | Real outlet (ηₜ = 0.85)  | 0.010   | —      | 2383      | ~7.1–7.5    | Two-phase         | Using efficiency relation            |



### b-Thermodynamic States – Modified Design

| State | Description             | p (MPa) | T (°C) | h (kJ/kg) | s (kJ/kg·K) | Region            | Notes                                |
|------:|--------------------------|--------:|-------:|----------:|------------:|-------------------|--------------------------------------|
| 1     | Turbine inlet            | 8       | 550    | 3583      | 6.66        | Superheated       | Superheated table @ 8 MPa, 550°C     |
| 2s    | Isentropic outlet        | 0.010   | —      | 2090      | 6.66        | Two-phase         | Using s₂s = s₁ at 10 kPa             |
| 2     | Real outlet (ηₜ = 0.85)  | 0.010   | —      | 2270      | 7.53        | Two-phase         | Using efficiency relation            |



### c- impact on device performance

1- work output 
$$
\dot{W}_{out} = \dot{m}(h_1 - h_2)
$$
According to the tbale we can see that as T increases, h_1 > h_2.
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

