# 🛡️ DROBITOS Defense Systems
**Decentralized Passive Multi-Modal Counter-UAS Detection, 3D Localization & Lab-Safe Interdiction Mesh**

---

### 1. System Architecture Overview
DROBITOS is a 100% passive, decentralized perimeter defense network engineered to detect, classify, and track low-RCS rogue drones and loitering munitions in complex urban and high-altitude mountain environments—without emitting detectable active radar signatures.

* **🔊 Stage 1 — Acoustic Array Triangulation:** ReSpeaker 4-Mic arrays with ePTFE wind filtering and BME280 thermal calibration compute real-time Angle-of-Arrival (AoA) and Time-Difference-of-Arrival (TDOA) on BLDC motor harmonics (150–2,000 Hz).
* **📡 Stage 2 — Passive RF Spectrum Sniffing:** Sub-GHz RTL-SDR V4 receivers (433/868/915 MHz) and 2.4 GHz ESP32 promiscuous packet sniffers detect FHSS telemetry bursts and Wi-Fi beacon frames.
* **🌡️ Stage 3 — Edge-AI EO/IR Verification:** Slew-to-cue Sony IMX708 optical and MLX90640 thermal arrays powered by a 26-TOPS Hailo-8 NPU verify motor thermal signatures (+15°C above ambient) to eliminate biological false alarms (bird flocks).
* **⚡ Stage 4 — WPC-Compliant Soft-Kill Validation:** Autonomous C2 trigger routing a HackRF One SDR interdiction waveform directly into a shielded **50-Ω SMA RF Dummy Load** (0 mW radiated) for safe laboratory verification.

---

### 2. Repository Index

| Repository | Subsystem | Status |
| :--- | :--- | :--- |
| **[drobitos-c2-sim](https://github.com/DROBITOS/drobitos-c2-sim)** | 3D WebGL Digital Twin & 4-Quadrant Physics Telemetry Console | 🟢 Active (TRL 3) |
| **drobitos-dsp-lab** *(Private)* | GCC-PHAT Acoustic DSP, Nonlinear Least-Squares TDOA & 6-State EKF | 🔒 Internal R&D |
| **drobitos-edge-node** *(Private)* | Raspberry Pi 5 + Hailo-8 Embedded Sensor Drivers & 5 GHz Mesh | 🔒 Internal R&D |
| **drobitos-hardware** *(Private)* | BOM, IP66 Enclosure CAD, Power Budget & Wiring Schematics | 🔒 Internal R&D |
