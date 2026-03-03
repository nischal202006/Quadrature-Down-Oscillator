# Quadrature Down Converter Design & Simulation

An end-to-end design and simulation of a Direct-Conversion Quadrature Down Converter. This project involves the implementation of a high-precision Quadrature Oscillator and a Dual-Mixer architecture to perform frequency translation and I/Q signal separation.

##  Project Overview
Direct-conversion (Zero-IF) receivers are essential in modern digital communications for their high integration and low power consumption. This project focuses on the hardware-level design of the down-conversion stage, ensuring phase accuracy and minimal signal distortion.

### Key Components
* **Quadrature Sine Wave Oscillator:** A wide-band op-amp based oscillator designed to provide two carrier signals (Sine and Cosine) with a precise 90° phase shift.
* **Dual-Mixer Architecture:** Implemented two balanced mixers to multiply the RF input with the quadrature Local Oscillator (LO) signals.
* **I/Q Signal Path:** Separates the input into In-phase (I) and Quadrature (Q) components, essential for modern modulation schemes like QAM and PSK.
* **Filtering Stage:** Integrated Low-Pass Filters (LPF) to suppress high-frequency mixing products and isolate the baseband signal.

## 🛠️ Technical Stack
* **Simulation Tool:** LTspice (Advanced Transient and AC Analysis).
* **Circuit Design:** Operational Amplifier-based oscillators and active/passive mixer topologies.
* **Theory:** RF System Design, Direct-Conversion architectures, and Quadrature Signal Processing.

## 📈 System Architecture
The system follows a classic direct-conversion topology:
1. **RF Input:** Receives the high-frequency modulated signal.
2. **LO Generation:** The Quadrature Oscillator generates the $sin(\omega t)$ and $cos(\omega t)$ signals.
3. **Mixing:** The RF signal is split and mixed with the LO signals in two parallel paths.
4. **Baseband Output:** The resulting signals are filtered to provide the I and Q baseband components.



##  Simulation & Results
The design was validated through extensive LTspice simulations:
* **Quadrature Accuracy:** Verified the 90-degree phase difference between the LO outputs.
* **Frequency Conversion:** Confirmed successful down-conversion of a test RF carrier to baseband.
* **Signal Integrity:** Analyzed Total Harmonic Distortion (THD) and Mixer conversion loss.

### Sample Circuit Implementation (LTspice)
The repository includes several `.asc` files representing the modular stages of the design:
* `QuadureOscillator.asc`: The primary 90° phase-shift source.
* `Mixer.asc`: Individual mixer stage testing.
* `Quadrature Down Convertor.asc`: The full integrated system.

##  Project Structure
* `/Simulations`: LTspice circuit files (.asc).
* `/Documentation`: Technical reports and reference papers on direct-conversion transceivers.
* `/Presentation`: Project overview and summary of results.

## 👥 Contributors
* **Nischal Ganipisetty**
* **Project Team ID: 39**

---
*Developed as part of a formal study on RF transceiver architectures and hardware-software integration.*
