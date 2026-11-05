# AcousticPay Protocol: Zero-Infrastructure Offline Acoustic Payment & Multi-Lane Arbitration

[![USPTO Patent Pending](https://img.shields.io/badge/USPTO-Patent%20Pending%20(Dual%20Portfolio)-amber.svg)](https://patentcenter.uspto.gov)
[![Status](https://img.shields.io/badge/Status-Active%20Prototype-success.svg)](https://ranjith130384-droid.github.io/acousticpay/)
[![Location](https://img.shields.io/badge/HQ-Dubai%2C%20UAE-blue.svg)](#)

AcousticPay is a peer-to-peer, zero-infrastructure offline payment protocol that settles transactions securely using encrypted acoustic soundwaves between existing commodity smartphones and POS speakers/microphones—without cellular data, WiFi, Bluetooth pairing, NFC chips, or dedicated terminal hardware.

---

## 🏛️ Official USPTO Patent Portfolio

Both applications are formally filed and verified under **Preexam Processing** at the United States Patent and Trademark Office (USPTO):

| Patent Ref | USPTO Application # | Confirmation # | Title & Core Protected Claims | Legal Status |
| :--- | :--- | :--- | :--- | :--- |
| **Patent #1** | **`64/189,672`** | `3752` | **Systems and Methods for Secure Offline Contactless Transaction Settlement via Acoustic Data Transfer**<br>• Monotonic offline nonce sequence<br>• Signed cryptographic payment vouchers<br>• Instant receiver auto-disarm (zero echo double-charges) | **USPTO Patent Pending**<br>(Preexam Processing) |
| **Patent #2** | **`64/191,956`** | `2884` | **Systems and Methods for Channel Arbitration, Collision Mitigation, and Doppler Tracking in High-Density Acoustic Environments**<br>• A-OFDMA multi-channel turnstile arbitration (Channels α, β, γ)<br>• A-CSMA 15ms listen-before-talk carrier sniff<br>• Real-time Doppler shift tracking ($\kappa = 1 \pm v/c$)<br>• Acoustic Time-of-Flight (ToF) proximity bounding (< 1.0m) | **USPTO Patent Pending**<br>(Preexam Processing) |

**Inventor:** Ranjith Radhakrishnan (Dubai, United Arab Emirates)

---

## 🌐 Live Interactive Sandbox

Experience the dual-patent acoustic transmission and multi-lane arbitration directly in your browser:

🔗 **[https://ranjith130384-droid.github.io/acousticpay/](https://ranjith130384-droid.github.io/acousticpay/)**

### Interactive Features in the Live App:
1. **A-OFDMA Multi-Lane Selector:** Switch between Turnstile Gate A (1.8 - 3.1 kHz), Gate B (3.4 - 4.7 kHz), and Express Gate C (5.0 - 6.3 kHz).
2. **A-CSMA Carrier Sniff Indicator:** Demonstrates real-time 15ms listen-before-talk collision avoidance.
3. **Doppler Shift Velocity Tracker:** Displays real-time pedestrian walking speed compensation ($\pm\Delta f$).
4. **Time-of-Flight (ToF) Proximity Gate:** Validates near-field acoustic boundary (< 1.0m) to reject adjacent lane cross-talk.

---

## 💻 Running the Test Suites Locally

### 1. Test Core Offline Cryptographic Settlement (Patent #1):
```powershell
node test_engine.js
```
*Validates voucher signature generation, monotonic nonce enforcement, offline ledger balance transitions, and double-spend rejection.*

### 2. Test Multi-Lane Arbitration & Doppler Compensation (Patent #2):
```powershell
node test_collision_engine.js
```
*Validates 4-channel parallel decoding (100% throughput), A-CSMA backoff arbitration, Doppler shift frequency tracking at 2.0 m/s walking speeds, and acoustic Time-of-Flight distance bounding.*

---

## 🔒 Security Architecture

1. **Monotonic Offline Counter:** Prevents transaction rollback and state replays even if the payer's device clock is manipulated.
2. **Zero-Echo Auto-Disarm:** The merchant terminal receiver immediately closes its acoustic listening loop upon decoding a packet, eliminating room-echo re-reads.
3. **Multi-Channel Frequency Guard Bands:** 400 Hz zero-energy acoustic guard intervals prevent inter-channel cross-talk between adjacent transit gates.
4. **Physical Acoustic Bounding:** Ultrasonic / high-frequency acoustic attenuation ensures transactions cannot be intercepted or executed from beyond 1.0 meter.

---

## 📄 License & Intellectual Property Notice
Confidential Intellectual Property. All systems, protocols, algorithms, state machines, and mathematical formulations are protected under US Provisional Patent Applications `64/189,672` and `64/191,956`. All rights reserved.
