# Enhanced-Inverse-Model-Predictive-Control-EIMPC-for-EV-Chargers-DC-DC-Side

Electric Vehicle (EV) charging systems require efficient and intelligent control strategies to ensure safe, fast, and reliable battery charging. This project implements an Enhanced Inverse Model Predictive Control (EIMPC) algorithm for the DC-DC stage of an EV charger using MATLAB/Simulink. The objective is to improve charging performance by accurately regulating battery current and voltage while reducing current ripple and switching losses.

The system consists of a bidirectional DC-DC converter connecting a high-voltage DC bus to an EV battery. The converter is controlled using an Enhanced Inverse Model Predictive Controller implemented through a MATLAB Function block. The controller continuously monitors the DC bus voltage (Vdc), battery voltage (Vbat), and inductor current (iL) to determine the optimal switching state of the converter.

An inverse model first converts the battery voltage error into a reference charging current. The predictive controller then estimates the future inductor current for all possible switching states using the converter's mathematical model. An enhanced cost function evaluates each predicted state by considering multiple objectives, including current tracking accuracy, ripple reduction, and switching loss minimization. The switching state with the lowest cost is selected and applied to the converter through complementary MOSFET gate signals.

To improve system reliability, the controller also incorporates current limiting, preventing excessive charging current and protecting both the converter and the battery. The complete control strategy was developed and validated through simulation in MATLAB/Simulink.

This project demonstrates the practical implementation of Model Predictive Control (MPC) techniques in power electronics and highlights their advantages over conventional control methods for EV charging applications. It provides hands-on experience in predictive control, bidirectional DC-DC converter operation, controller implementation using MATLAB Function blocks, and simulation-based validation of advanced control algorithms.

---

## Key Features
Enhanced Inverse Model Predictive Control (EIMPC)
Bidirectional DC-DC converter for EV charging
Predictive inductor current estimation
Voltage-error-based current reference generation
Multi-objective cost function for optimal switching
Current tracking and voltage regulation
Current limiting for converter protection
Reduced current ripple and switching losses
Complementary MOSFET gate control
MATLAB/Simulink implementation and validation

---

##  Author

**Satvika Gobi**

