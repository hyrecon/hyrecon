# 📡 Backscatter Multimedia Data Communication System

> End-to-end monostatic backscatter system for wireless image transmission in low-power IoT environments.

## 📌 About

Traditional wireless systems rely on active RF transmission, which demands significant power and complex hardware — not ideal for battery-operated or energy-harvesting IoT devices. Backscatter communication offers a fundamentally different approach: instead of generating its own signal, the tag simply reflects and modulates an incoming carrier wave, drastically reducing power consumption.

This project implements a monostatic backscatter communication system that goes beyond simple sensor data (temperature, humidity, etc.) and demonstrates over-the-air transmission and reconstruction of complex image data — including full-color images — using custom hardware and signal processing algorithms.

## 🎯 Key Results

- Data rate: 80 kbps with OOK modulation
- SNR: ~30 dB at 30 cm (with microwave absorbers)
- BER: < 10⁻⁷ (error-free image reconstruction)
- Antenna gain: 7 dBi
- Antenna isolation: below −30 dB (with SRRs)
- Operating band: ISM 2.4–2.5 GHz

## 🔧 System Architecture

**Tag:** Arduino UNO (ATmega328P) + SPDT switch for OOK modulation

**Reader:** USRP N200 (Software-Defined Radio) for carrier generation and signal reception

**Antenna:** Planar 2×1 Yagi-Uda array with Split-Ring Resonators (SRRs) for high isolation

**Post-processing:** MATLAB-based demodulation, peak detection, K-means clustering, and image reconstruction

## 🛠️ Built With

`MATLAB` · `GNU Radio` · `Arduino IDE`

Arduino UNO · USRP N200 · SPDT switch · planar Yagi-Uda antenna array · Split-Ring Resonators · microwave absorber (VHP NRL)

## 📄 Publication

**H. Ryu** and S. Kim, "High-Isolation Yagi-Uda Antenna Array using Split-Ring Resonators for Practical Backscatter System," *Proc. IEEE AP-S/URSI*, 2025, pp. 2877–2879.
