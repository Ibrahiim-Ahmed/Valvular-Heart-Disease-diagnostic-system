# 💓 VHD: Valvular Heart Disease Diagnostic System

A portable, embedded system for the **automatic detection and classification of valvular heart disease (VHD)** using heart sound signals (phonocardiograms) and **on-device machine learning** — designed specifically for use in remote or low-resource settings.

## 🧠 Project Overview

This project leverages **digital auscultation**, **signal processing**, and **Edge AI** to build a diagnostic tool that:

- **Captures heart sounds** using a high-fidelity I2S microphone.
- **Filters and conditions the signal** using analog front-end circuits.
- **Extracts relevant features** (e.g., MFCC, spectrograms) from audio in real-time.
- **Classifies heart murmurs** using an on-device deep learning model.
- **Identifies which heart valve is affected** (Aortic, Mitral, Pulmonary, Tricuspid).
- **Displays diagnostic results** via a local OLED or GUI — no internet required.

## 🔬 Motivation

In South Asia and other developing regions, VHD remains a major cause of morbidity and mortality — yet many communities lack access to trained cardiologists or echocardiography. By building an **affordable and offline diagnostic system**, this project aims to bridge that gap using embedded intelligence.

## ⚙️ Core Components

| Module              | Description |
|---------------------|-------------|
| `INMP441` I2S Mic   | Captures heart sounds in digital format |
| `TL072 Op-Amp`      | Analog signal amplification |
| `Band-Pass Filter`  | Removes unwanted frequencies (low & high) |
| `Google Coral Dev Board` | Performs real-time inference using its Edge TPU |
| `OLED Display`      | Shows valve location, classification result, and heart rate |

## 🧩 Methodology

1. **Signal Acquisition** – PCG signal is collected via chest-placed stethoscope.
2. **Signal Conditioning** – Amplified and filtered through analog circuitry.
3. **Feature Extraction** – MFCC or spectrograms are computed from the audio.
4. **Model Inference** – A trained neural network predicts the murmur class and associated valve.
5. **Result Output** – OLED display shows result + confidence level.

## 📊 Target Features

- Heart murmur detection (Normal vs Abnormal)
- Valve identification
- Disease classification (e.g., stenosis, regurgitation)
- On-device inference (no cloud needed)
- Local result display (OLED or GUI)
- Dataset training + evaluation tools

## 🧾 Dataset(s)

- [PhysioNet 2022 Heart Sound Challenge Dataset](https://physionet.org/content/challenge-2022/1.0.0/)
- Custom heart sound recordings (to be collected)

## 🚀 Planned Improvements

- Bluetooth or WiFi-based remote diagnosis
- Mobile app integration for visualization
- Adaptive noise filtering using AI denoising

## 📚 Research-Backed Approach

This project is backed by insights from 20+ recent research papers (2020–2025) covering:
- Deep learning for auscultation
- Edge computing with TPUs
- Feature extraction techniques
- Heart valve-specific detection methods


---

> This project is part of a Final Year Design Project (FYDP) aimed at solving real-world medical accessibility challenges using embedded systems and machine learning.

