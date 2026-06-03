# LECTOR-Based Current-Starved VCO in 90 nm CMOS for Wireless IoT Networks

**Authors:** Raisul Islam Ratul, Anindya Chanda Tirtha  
**Institution:** Department of Electrical, Electronic and Communication Engineering, Military Institute of Science and Technology (MIST), Dhaka, Bangladesh  
**Technology:** 90 nm CMOS (Cadence Virtuoso)  
**Supply Voltage:** V<sub>DD</sub> = 1.2 V  

---

## Abstract

This project presents a novel **LECTOR-based Current-Starved Voltage-Controlled Oscillator (CS-VCO)** designed for ultra-low-power IoT wireless applications. The LECTOR (LEakage ConTrol TransistOR) technique integrates additional leakage control transistors into each inverter stage of a three-stage ring oscillator to suppress subthreshold leakage currents — achieving over **90% reduction in static power consumption** compared to conventional CS-VCOs, while preserving full voltage swing and stable oscillation.

---

## Table of Contents

- [Background & Motivation](#background--motivation)
- [Circuit Architecture](#circuit-architecture)
  - [LECTOR-Based Inverter](#lector-based-inverter)
  - [Three-Stage CS-VCO](#three-stage-cs-vco)
- [Simulation Results](#simulation-results)
  - [Oscillation Characteristics](#oscillation-characteristics)
  - [Frequency Tuning Curve](#frequency-tuning-curve)
  - [Phase Noise Performance](#phase-noise-performance)
  - [Layout](#layout)
- [Performance Summary](#performance-summary)
- [Comparative Evaluation](#comparative-evaluation)
- [IoT Suitability](#iot-suitability)
- [Files in This Repository](#files-in-this-repository)
- [References](#references)

---

## Background & Motivation

The rapid expansion of Internet of Things (IoT) ecosystems has intensified demand for ultra-low-power, high-performance oscillators. VCOs are indispensable building blocks in:

- Frequency synthesizers and PLLs
- Clock generation units
- RF transceivers for Wi-Fi, Bluetooth, and 5G

At deep submicron (90 nm and below), conventional CMOS and current-starved VCOs suffer from:

- **High subthreshold leakage currents** — dominant at low supply voltages
- **Limited tuning range** — constraining multi-standard compatibility
- **Degraded phase noise** — due to leakage-induced current fluctuations

The **LECTOR technique** addresses these issues by inserting cross-coupled leakage control transistors (LCTs) into the inverter pull-up/pull-down networks. This project is — to the best of the authors' knowledge — **the first implementation of a LECTOR-based CS-VCO** architecture evaluated in the context of IoT wireless networks.

---

## Circuit Architecture

### LECTOR-Based Inverter

The LECTOR inverter e