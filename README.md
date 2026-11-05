# AcousticPay Protocol: Global Zero-Infrastructure Offline Acoustic Settlement & High-Density Transit

[![USPTO Patent Pending](https://img.shields.io/badge/USPTO-Patent%20Pending%20(Dual%20Portfolio)-amber.svg)](https://patentcenter.uspto.gov)
[![Status](https://img.shields.io/badge/Status-Production%20Prototype-success.svg)](https://acousticpay.tech)
[![Priority](https://img.shields.io/badge/Priority-Paris%20Convention%20(179%2B%20States)-blue.svg)](#)

AcousticPay is a universal, software-only settlement protocol that transforms any commodity smartphone speaker and microphone into a secure cryptographic payment transceiver. Zero cellular data. Zero WiFi. Zero NFC chips. Zero specialized terminal hardware.

Compatible across **5.4+ billion audio-equipped mobile devices worldwide**, bridging offline retail, mass transit networks, mobile money operators, and remote commerce globally.

---

## 🏛️ Official USPTO Patent Portfolio

Both foundational specifications are formally filed and verified under **Preexam Processing** at the United States Patent and Trademark Office (USPTO), securing global priority across 179+ member states under the Paris Convention:

| Patent Ref | USPTO Application # | Confirmation # | Title & Core Protected Claims | Legal Status |
| :--- | :--- | :--- | :--- | :--- |
| **Patent #1** | **`64/189,672`** | `3752` | **Systems and Methods for Secure Offline Contactless Transaction Settlement via Acoustic Data Transfer**<br>• Hardware-enclave backed monotonic nonce sequence<br>• Signed cryptographic payment micro-vouchers<br>• Instant receiver auto-disarm (zero echo double-charges) | **USPTO Patent Pending**<br>(Preexam Processing) |
| **Patent #2** | **`64/191,956`** | `2884` | **Systems and Methods for Channel Arbitration, Collision Mitigation, and Doppler Tracking in High-Density Acoustic Environments**<br>• A-OFDMA multi-channel transit turnstile arbitration (Channels α, β, γ)<br>• A-CSMA 15ms listen-before-talk carrier sniff<br>• Real-time Doppler shift tracking ($\kappa = 1 \pm v/c$)<br>• Acoustic Time-of-Flight (ToF) proximity bounding (< 1.0m) | **USPTO Patent Pending**<br>(Preexam Processing) |

**Inventor:** Ranjith Radhakrishnan

---

## 🌐 Live Interactive Flagship Sandbox

Experience the dual-patent acoustic transmission and multi-lane arbitration directly in your browser:

🔗 **[https://acousticpay.tech](https://acousticpay.tech)**

### Interactive Capabilities in the Live App:
1. **A-OFDMA Multi-Lane Selector:** Dynamically switch between Turnstile Gate A (1.8 - 3.1 kHz), Gate B (3.4 - 4.7 kHz), and Express Gate C (5.0 - 6.3 kHz).
2. **A-CSMA Carrier Sniff Indicator:** Demonstrates real-time 15ms listen-before-talk collision avoidance.
3. **Doppler Shift Velocity Tracker:** Displays real-time pedestrian walking speed compensation ($\pm\Delta f$ up to 2.5 m/s).
4. **Time-of-Flight (ToF) Proximity Gate:** Validates near-field acoustic boundary (< 1.0m) to reject adjacent lane cross-talk.

---

## 🌍 Strategic Global Use Cases

* **Global Mass Transit & Rail Turnstiles:** Sub-second passenger throughput across international transit networks (London Underground, New York MTA, Tokyo Metro, Paris RATP, Singapore SMRT) directly via phone speakers with zero physical smartcards, tokens, or NFC hardware.
* **Universal Point-of-Sale & Soundboxes:** Firmware-level upgrade converting tens of millions of deployed merchant soundboxes and point-of-sale terminals into bidirectional acoustic payment receivers.
* **Financial Inclusion (1.4B+ Devices):** Enabling instant digital transactions across 1.4+ billion low-cost smartphones and 2G/3G/4G feature phones lacking NFC chips across emerging markets worldwide.
* **In-Flight & Maritime Commerce:** 100% offline contactless settlement on commercial airlines at 35,000 feet, maritime cruise lines, underground mines, and remote emergency disaster relief zones.

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

1. **Hardware Enclave Nonces:** Enforces monotonic counter state transitions inside the device's secure processor, preventing offline replay or cloning.
2. **Zero-Echo Auto-Disarm:** The merchant terminal receiver immediately closes its acoustic listening loop upon decoding a packet, eliminating room-echo re-reads.
3. **Multi-Channel Frequency Guard Bands:** Non-harmonic, prime-ratio frequency spacing prevents adjacent transit turnstile cross-talk.
4. **Physical Acoustic Bounding:** Ultrasonic and high-frequency acoustic attenuation ensures transactions cannot be intercepted or executed from beyond 1.0 meter.

---

## 📄 License & Intellectual Property Notice
Confidential Intellectual Property. All systems, protocols, algorithms, state machines, and mathematical formulations are protected under US Provisional Patent Applications `64/189,672` and `64/191,956` with worldwide priority under the Paris Convention. Inquiries: `inquiries@acousticpay.tech`.
