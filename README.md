# Enhanced-Inverse-Model-Predictive-Control-EIMPC-for-EV-Chargers-DC-DC-Side

Project Description

The rapid adoption of Electric Vehicles (EVs) has increased the demand for efficient, reliable, and intelligent battery charging systems. The DC-DC converter is one of the most critical stages in an EV charger, as it is responsible for regulating the charging voltage and current delivered to the battery. Traditional control methods such as Proportional-Integral (PI) controllers are widely used due to their simplicity; however, they often exhibit slower dynamic response, require extensive parameter tuning, and may struggle to maintain optimal performance under varying operating conditions.

To address these limitations, this project implements an Enhanced Inverse Model Predictive Control (EIMPC) strategy for the DC-DC side of an Electric Vehicle charger using MATLAB/Simulink. The controller employs predictive decision-making to determine the optimal switching state of a bidirectional DC-DC converter, enabling efficient battery charging with improved dynamic performance.

The developed system consists of a high-voltage DC bus, a bidirectional DC-DC converter, an energy storage inductor, complementary MOSFET switches, voltage and current measurement blocks, and an Enhanced Inverse Model Predictive Controller implemented using a MATLAB Function block. The DC bus acts as the charging source, while the converter transfers energy to the EV battery in buck mode during charging.

The control strategy begins by continuously measuring the DC bus voltage (Vdc), battery voltage (Vbat), and inductor current (iL). The measured battery voltage is compared with a predefined reference charging voltage to calculate the voltage error. Instead of directly controlling the battery voltage, an inverse model converts this voltage error into a reference charging current (iref), allowing the predictive controller to regulate the battery indirectly through current control.

The EIMPC algorithm predicts the future inductor current for every possible switching state of the converter using a discrete mathematical model of the inductor. For each prediction, an enhanced cost function is evaluated to determine the most suitable switching action. Unlike conventional predictive controllers that primarily focus on tracking the reference current, the implemented enhanced controller simultaneously considers multiple performance objectives, including Accurate tracking of the reference charging current, Reduction of inductor current ripple, Minimization of unnecessary switching transitions to reduce switching losses, Current limiting to protect the converter and battery from excessive charging current

The controller evaluates all possible switching states during every sampling interval and selects the one that minimizes the overall cost function. The selected switching signal drives the upper MOSFET, while a complementary gate signal controls the lower MOSFET, ensuring proper converter operation and efficient energy transfer.

The entire controller was developed using a MATLAB Function block within Simulink, enabling real-time evaluation of the predictive control algorithm during simulation. The model integrates power electronic components with the control algorithm to emulate the charging process and validate controller performance under different operating conditions.

Simulation results demonstrate that the implemented controller is capable of maintaining stable battery charging while regulating the charging current and voltage. The predictive nature of the controller enables rapid decision-making, while the enhanced cost function contributes to improved current regulation, reduced ripple, and lower switching activity compared to conventional control strategies.

This project provided practical experience in power electronics, predictive control techniques, converter modeling, MATLAB/Simulink simulation, and advanced control algorithm implementation. It also strengthened the understanding of bidirectional DC-DC converters, model predictive control principles, battery charging strategies, and controller integration for electric vehicle charging applications.
---

##  Author

**Satvika Gobi**

