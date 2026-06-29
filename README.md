# Enhanced-Inverse-Model-Predictive-Control-EIMPC-for-EV-Chargers-DC-DC-Side

##  Overview

This project presents the design and simulation of an **Enhanced Inverse Model Predictive Control (EIMPC)** strategy for the **DC-DC stage of an Electric Vehicle (EV) charger** using **MATLAB/Simulink**. The controller regulates battery charging by predicting future converter behavior and selecting the optimal switching state based on an enhanced cost function.

The implemented EIMPC improves charging performance by providing accurate current tracking, reducing current ripple, minimizing switching losses, and maintaining stable converter operation.

---

##  Objectives

* Design a bidirectional DC-DC converter for EV battery charging.
* Implement an Enhanced Inverse Model Predictive Controller (EIMPC).
* Regulate battery charging voltage and current.
* Reduce inductor current ripple.
* Minimize switching losses.
* Validate controller performance through simulation.

---

##  Features

* Bidirectional DC-DC converter model
* Enhanced Inverse Model Predictive Control (EIMPC)
* Predictive inductor current estimation
* Voltage-error-based current reference generation
* Current tracking
* Current limiting for converter protection
* Ripple reduction
* Switching loss minimization
* Complementary MOSFET gate control
* MATLAB Function-based controller implementation

---

##  Control Strategy

The controller continuously measures:

* **DC Bus Voltage (Vdc)**
* **Battery Voltage (Vbat)**
* **Inductor Current (iL)**

The battery voltage error is converted into a reference charging current:

```math
i_ref = K(V_ref - V_bat)
```

The controller predicts the future inductor current for both possible switching states and minimizes the following enhanced cost function:

```math
J = w_1(i_ref-i_pred)^2+w_2(i_pred-i_L)^2+w_3(u-u_prev)^2
```

where:

* **w₁** – Current tracking weight
* **w₂** – Ripple reduction weight
* **w₃** – Switching penalty weight

The switching state with the minimum cost is applied to the converter MOSFETs.

---

##  Software Used

* MATLAB
* Simulink
* MATLAB Function Block
* Simscape Electrical

---

##  Future Improvements

* Adaptive weight tuning
* State of Charge (SOC) estimation
* Multi-step predictive control
* Hardware implementation using DSP or FPGA
* Experimental validation on a real-time EV charger

---

##  Author

**Satvika Gobi**

