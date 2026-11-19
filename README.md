# Virtual EEE Laboratory

An interactive browser-based Electrical and Electronics Engineering workbench built in a single HTML file (`eee-virtual-lab.html`). It brings together 22 real-time simulations across 8 core EEE subjects, allowing students to adjust circuit parameters, inspect live waveforms, and log experimental readings without needing physical bench hardware or external software installations.

## Why I Built This

Most online circuit tools either require paid licenses, heavy downloads, or limit you to basic DC networks. I wanted a fast, self-contained laboratory that covers the actual undergraduate EEE syllabus—from RLC transients and CRO Lissajous figures to single-phase transformer OC/SC tests, DC machine speed control, induction motor torque-slip curves, PID tuning, and controlled SCR rectifiers—running purely on HTML5 Canvas and vanilla JavaScript.

## What's Inside

### 1. Basic Circuits & Network Theorems
* **RLC Step Transient:** Observe underdamped, critically damped, and overdamped responses while adjusting $R$, $L$, and $C$.
* **AC Resonance:** Compare series and parallel resonance curves, resonant frequency ($f_0$), bandwidth, and quality factor ($Q$).
* **Thevenin & Maximum Power Transfer:** Vary load resistance ($R_L$) to verify peak power delivery when $R_L = R_{th}$.

### 2. Electronic Measurements & CRO
* **Dual-Trace Oscilloscope:** Two-channel function generator (Sine, Square, Triangle, Sawtooth) with Volts/Div, Time/Div, phase shift, and trigger controls.
* **X-Y Lissajous Mode:** Measure phase difference and frequency ratios between Channel A and Channel B.
* **AC Bridges:** Null-balance simulations for Maxwell's inductance bridge and the Wien frequency bridge.

### 3. Analog Electronics & Devices
* **Diodes:** Forward and reverse V-I characteristics for Silicon ($0.7\text{ V}$), Germanium ($0.3\text{ V}$), and Zener breakdown regulators.
* **BJT Common-Emitter:** Output collector curves ($I_C$ vs. $V_{CE}$) overlaid with a live DC load line and Q-point tracker.
* **Operational Amplifiers:** Inverting, non-inverting, and integrator configurations demonstrating $\pm 15\text{ V}$ supply saturation.

### 4. Digital Logic & Sequential Systems
* **Karnaugh Map Solver:** 2, 3, and 4-variable Gray-code K-Map with Don't Care (`X`) cells, SOP minimization, and live gate rendering.
* **Combinational Circuits:** Interactive 4:1 Multiplexer and 1-Bit Full Adder with truth-table verification.
* **Sequential Counters:** JK Flip-Flop and Mod-8 asynchronous ripple counter timing diagrams.

### 5. Transformers & DC Machines
* **Single-Phase Transformer:** Open-Circuit and Short-Circuit parameter estimation ($R_0, X_0, R_{eq}, X_{eq}$), voltage regulation, and efficiency vs. load curves.
* **DC Motors:** Armature voltage and field flux speed control for DC Shunt and Series motors.
* **DC Generator:** Open-Circuit Characteristic (OCC) magnetization curve and external load drop.

### 6. AC & Synchronous Machines
* **3-Phase Induction Motor:** Full torque-slip characteristic showing starting torque ($s=1$), pull-out torque ($T_{max}$), and rotor resistance effects.
* **Synchronous Motor:** V-curves ($I_a$ vs. $I_f$) illustrating lagging, unity, and leading power factor operation.

### 7. Control Systems
* **PID Controller:** Closed-loop step response with real-time $K_p$, $K_i$, and $K_d$ sliders and live overshoot, rise time, and settling time readouts.
* **Bode Plot Analyzer:** Magnitude ($\text{dB}$) and phase angle plots with gain and phase margin indicators.

### 8. Power Electronics & Drives
* **Controlled SCR Rectifier:** Single-phase half-wave and full-wave bridge with firing angle ($\alpha$) control, $R$-$L$ load waveforms, and a freewheeling diode toggle.
* **DC-DC Converters:** Buck and Boost converter inductor current ripple across CCM and DCM boundaries.
* **SPWM Inverter:** Single-phase sinusoidal pulse-width modulation switching pulses and filtered output.

### Additional Utilities
* **Touch-to-Probe Crosshairs:** Tap or drag on any graph to read exact coordinates on both desktop and mobile screens.
* **Observation Logbook:** Save readings during a simulation run and export them directly to a `.csv` file.
* **Reference Section:** Searchable formula sheet and viva-voce review questions.
* **Light & Dark Themes:** Switch between paper-white and dark slate modes without reloading.

## Running Locally

No build tools, Node packages, or local servers are needed:

```bash
git clone [https://github.com/](https://github.com/)<your-username>/<repo-name>.git
cd <repo-name>
