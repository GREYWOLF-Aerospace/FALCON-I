<h1 align="center">﷽</h1>

<h1 align="center">
<font size="6"><b>🛦 X-26 GREYWOLF PT-1</b></font>
</h1><br>

<h4 align="center">
  <b>The First High-Performance Experimental 12S EDF Prototype of the YF-26 GREYWOLF Program</b>
</h4>
<p align="center">
  <a href="#technical-specifications">Technical Specifications</a> •
  <a href="#visual-looks">Visual Looks</a> •
  <a href="#airframe-materials-list">Materials</a> •
  <a href="#electronics--propulsion-system">Electronics Strategy</a> •
  <a href="#system-wiring-diagram">Wiring Diagram</a> •
  <a href="#success-criteria--flight-goals">Flight Goals</a> •
  <a href="#assembly-guide">Assembly</a> •
  <a href="#credits">Credits</a> •
  <a href="#license">License</a>
</p>
<br>

> **Project Status:**Aerodynamic Simulation & CAD Phase Complete  
> **CAD Platform:** Autodesk Fusion 360  
> **Design Time Investment:** 50+ Hours  
---

## Technical Specifications

The **X-26 GREYWOLF PT-1** is a high-speed, scratch-built experimental scale RC jet aircraft. It is engineered around an advanced integrated propulsion duct system and a multi-axis high-lift control surface layout to study level transonic airflow behaviors, intake fluid dynamics, and low-altitude flight stability.

* **Total Length of Aircraft:** 1.3 - 1.5 meters
* **Total Height of Aircraft (without landing Gear):** 0.3m (~30cm)
* **Fuselage Hull Height:** 0.1m (~11cm) *(Optimized to wrap tightly around the internal engine bay)*
* **Wingspan:** ~1.0 meter
* **Wing Area:** ~0.1 m²
* **Total Control Channels:** 6 Channels (2x Flaps, 2x Ailerons, 2x Stabilators)
* **Aerodynamic Design & Fluid Optimization:** Validated via rigorous computational fluid dynamics (CFD) steady-state solver testing run at a 20 m/s airspeed vector, establishing a baseline cruise lift coefficient ($C_L$) of 0.0141 and an ultra-low geometric shape drag coefficient ($C_D$) of 0.0018.
* **Special Intake Engineering:** Features a custom-modeled internal S-Duct intake routing system designed to stabilize incoming air turbulence and manage static pressure gradients under high mass flows.
* **Performance Profile:** Estimated empty airframe weight ranges from 2.0 to 3.0 kg. Powered by a high-output 12S electric ducted fan producing between 4.0 - 5.0 kg of static thrust, yielding a >1:1 thrust-to-weight ratio for a flight envelope targeting 100 - 110 mph.
* **Short-Runway (STOL) Takeoff Speeds:**
  * *Unladen / Light Test Rig (3.5 kg):* 21.3 m/s - 23.0 m/s (~76 km/h)
  * *Maximum Operational Testing Payload (4.5 kg):* 24.6 m/s - 26.1 m/s (~94 km/h)
* **Control Surface Mixing:** Implements symmetrical **Flaperon** mixing, deflecting both flaps and main ailerons together at takeoff. This transforms **41.5% of the total wing area ($372.68\text{ cm}^2$)** into an active camber-shifting high-lift surface, rocketing the maximum takeoff lift coefficient ($C_{L_{\text{max}}}$) to approximately 0.165.

*Note: The structural frames, nose cone mechanics, and intake paths are modeled as completely independent components within the source assembly to allow for modular fabrication and fast battery bay accessibility.*

---

## Visual Looks

<h3 align="center"><b>CAD Model Overview</b></h3>
<p align="center">
  <img width="1366" alt="CAD Side Perspective" src="https://github.com/user-attachments/assets/79038fe9-667d-4d73-b458-954ee69030db" />
  <img width="1366" alt="CAD Front-Side Perspective" src="https://github.com/user-attachments/assets/3ff2fcdd-5998-4d4d-89cd-29c2dfe3bb96" />
  <img width="1332" alt="CAD Front Perspective" src="https://github.com/user-attachments/assets/44b34efe-ddbe-4e03-9ad8-37d1d54cd98a" />
  
  
  <a href="https://youtu.be/b9qI-MGt7ME"><b>A demonstration of the actuation of Control Surfaces</b></a>




</p>

<h3 align="center"><b>High-Fidelity Rendered Visuals</b></h3>
<p align="center">
  <img width="1366" alt="Render 1" src="https://github.com/user-attachments/assets/2d3e70eb-05b6-482c-999b-a1dfd2cca9a0" />
  <img width="1366" alt="Render 2" src="https://github.com/user-attachments/assets/05801154-7e74-43a8-a288-93ab383051e0" />
  <img width="1366" alt="Render 3" src="https://github.com/user-attachments/assets/a454421b-2992-45c8-9742-f32c235d7944" />
  <img width="1366" alt="Render 4" src="https://github.com/user-attachments/assets/90b29206-22b7-4296-b81f-d5549d2630e6" />
</p>

> **Design Note on Airframe Influence:** > The X-26 Greywolf airframe merges generation-defining design aspects. It utilizes high-efficiency forward intakes inspired by the F-22 Raptor, twin vertical stabilizing surfaces and an exhaust layout optimized similarly to the F-35 Lightning II, and an internal structural distribution derived from the F-16 Fighting Falcon. 

---

## Airframe Materials List

The structural framework utilizes a lightweight, high-strength composite prototyping approach to handle structural stress thresholds while maximizing the power-to-weight ratio:

1. **Depron Foam / High-Speed LW-PLA:** Used for the aerodynamic outer skin contours, wing surfacing, and lightweight internal fuselage formers.
2. **Carbon Fiber Spars & Rods (3mm):** Integrated directly into high-stress structural joints, serving as the main wing load spars, tail pivot shafts, and longitudinal fuselage stiffeners.
3. **Aircraft-Grade Plywood:** Selected for high-vibration structural hardpoints, specifically the main 12S EDF engine mount and landing gear mounting plates.

---

## Electronics & Propulsion Strategy

The PT-1's avionics bay is engineered to safely sustain high continuous current loads. Comprehensive component sourcing, unit prices, and specific funding breakdowns are tracked in the dedicated [Bill of Materials Guide](BOM.md).

### Power Architecture Summary:
1. **High-Voltage Power Loop:** Two independent 6S LiPo battery packs (5200mAh - 5900mAh) are linked in **series** using a heavy-duty **QS-8 Anti-Spark Series Harness** to deliver a unified 12S nominal voltage supply (44.4V nominal / 50.4V peak) directly to the ESC.
2. **Propulsion Drive Loop:** High-gauge phase leads feed directly from the Hobbywing 100A V2 ESC to the brushless motor inside the 80mm fan shroud.
3. **Low-Voltage Signal Loop:** Signal power to the 10-channel FlySky receiver steps down cleanly via the ESC's integrated Battery Eliminator Circuit (BEC) lines.
4. **Control Surface Actuation:** Symmetrical servos are linked across the receiver layout using heavy-duty Y-harness extensions to maintain precise dual-aileron, dual-flap, and stabilator mechanical sync.

---

## System Wiring Diagram

The PT-1 utilizes a clean point-to-point wiring schematic optimized for minimal line resistance and spatial balance within the narrow fuselage ribbing. 

<p align="center">
  <img width="1366" alt="Point to Point Wiring Schematic" src="https://github.com/user-attachments/assets/5e5e0da4-2eb1-411f-bb1d-6472232fde2c" />
  <img width="1366" alt="Internal Fuselage Electronics Layout" src="https://github.com/user-attachments/assets/3f0233a8-e0d2-44fd-b3ad-49cb08857d07" />
</p>

---

## Success Criteria & Flight Goals

To rigorously evaluate the airframe engineering and telemetry code, the testing program focuses on three definitive goals:
1. **Aerodynamic Validation:** Confirm stable, level cruise tracking at a 20 m/s airspeed vector to ground-truth our baseline steady-state CFD dataset.
2. **STOL Performance:** Verify short-runway rotation and lift-off performance using the 41.5% trailing-edge flaperon configuration under incremental payload loads.
