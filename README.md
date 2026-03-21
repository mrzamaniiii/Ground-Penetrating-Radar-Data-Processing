![2](https://github.com/user-attachments/assets/a8d89660-fdab-4bad-a6de-baf34634f21e)

# GPR Concrete Wall Analysis

## Overview
The primary objective was to process 15 parallel vertical profiles to detect and visualize the reinforcement rebars structure. The project moves from raw data analysis to a full 3D cube representation, enabling a clear view of the rebar layout within the wall.

## Parameters
The dataset consists of 15 parallel vertical profiles collected with the following specifications:

| Parameter | Value |
| :--- | :--- |
| **Nominal Frequency** | 3 GHz |
| **Polarization** | HH |
| **TX-RX Distance** | 6 cm |
| **Profile Inter-distance** | 10 cm |
| **Trace Increment** | 4 mm |
| **Total Traces** | 6752 |

---

## Processing Workflow
The data was processed using Reflexw software through the following pipeline:

### 1. Static Correction & Alignment
* **Phase Correction:** We applied the "correct max. phase" operation two times to align all profiles effectively.
* **Time Calibration:** The start time was moved by -0.9 ns to calibrate the zero-time surface reflection.

### 2. Signal Filtering
To improve the signal-to-noise ratio:
* **Bandpass Butterworth Filter:** Applied to isolate the most energetic region of the spectrum.
* **Background Subtraction:** A subtracting average procedure (window: 250 traces) was used to remove background noise and horizontal ringing.

### 3. Velocity Analysis & Migration
* **Velocity Analysis:** By fitting diffraction hyperbolas, the propagation velocity was estimated at 0.135 m/ns.
* **Migration (Diffraction Stack):** This step collapsed the diffraction hyperbolas to correctly position the targets.

### 4. Visualization
* **Envelope Extraction:** Calculated to visualize signal energy strength.
* **3D Modeling:** A 3D cube was generated to view the rebar grid in volumetric space.


## Results
* **Rebar Spacing:** The analysis revealed a clear grid with rebars spaced approximately 0.2 m (20 cm) apart.
* **Target Depth:** The reinforcement bars are located at a depth of approximatel 5 cm.
* **Structure:** The 3D view highlighted that the rebars are not perfectly straight, indicating variations during the construction phase.
